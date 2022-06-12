
**Inflow Computation in Reservoirs**

Efficient water management strategies and resource planning are required to maximize the value of water resources; knowledge of historical inflow data is very relevant.There are no direct methods to measure water inflows as it typically comprises of stream runoffs and surrounding tributaries. 

Reservoir inflow is estimated using water balance method involving reservoir release and change in storage during the period considered. Water discharge data of the mainstream is readily available available, however observations from the tributaries are not easily quantifiable. The water balance equation is

<p align="center">

<img width="568" alt="Screen Shot 2022-06-11 at 8 28 07 PM" src="https://user-images.githubusercontent.com/107319637/173209262-cf43e84f-1e59-4d93-a587-d7b657c343f1.png">
</p>

The reservoir storage is estimated by the reservoir stage-elevation relationship
<p align="center">
<img width="107" alt="Screen Shot 2022-06-11 at 8 31 01 PM" src="https://user-images.githubusercontent.com/107319637/173209314-16e866a9-ce47-4f3b-bcb0-9962ff3c7646.png">
</p>
Here, HW is the observed water level. It should be noted that the water losses are not usually quantified so for this calculation, it is assumed to be negligible.


The data for computing the relationship between the reservoir storage and elevation were provided by the TVA through direct correspondence, which is plotted to obtain the function as shown in Fig 10. A second-degree polynomial relationship is identified between the elevation level and reservoir volume, expressed as:
<p align="center">
<img width="481" alt="Screen Shot 2022-06-11 at 8 38 15 PM" src="https://user-images.githubusercontent.com/107319637/173209488-2c97a832-43da-49bd-be9a-de68a81d5e13.png">
</p>
The initial inflow estimation produced inflow values with significant negative terms as shown in the figure below:
<p align="center">
<img width="604" alt="Screen Shot 2022-06-11 at 8 49 48 PM" src="https://user-images.githubusercontent.com/107319637/173209645-64f377a3-670f-4c24-8455-abaac7b54f86.png">
</p>

When computing the reservoir volume, each term the water balance equation has associated errors, and the following reasons can cause estimated negative inflows.

a)	A small inaccuracy in the reservoir elevation observations might cause a considerable variation in the reservoir volume estimation.

b)	Due to the lack of recent data for computing the reservoir volume- elevation curve, the reservoir capacity at specific elevations can be miscalculated.

c)	The estimated uncertainties in computed outflows for lakes having continuous-record gaging stations at or near their outlets range from 5 to 10%

**Replacing computed negative inflow**
1. *Smoothing headwater curve*

A reservoir level hydrograph smoothing technique was adopted to deal with the changes in elevation. Interpolation was used to replace null values and smoothened using an analog based low-pass Butterworth filter

<p align="center">
<img width="679" alt="Screen Shot 2022-06-11 at 8 47 56 PM" src="https://user-images.githubusercontent.com/107319637/173209625-0383df64-0580-437e-8dd2-5da33480d172.png">
</p>
