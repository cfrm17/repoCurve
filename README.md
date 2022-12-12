# Repo Curve

A repo curve calibration methodology is presented to bring it more consistent with market quotation. Instead of a fixed term structure for an issuer, the repo curve in essence becomes a “repo factor collection” in which a constant repo factor is stored with respect to each outstanding bond of the issuer.  

A repo curve is defined as an adjustment to the discount curve in the pricing of a bond/FRN, when the credit default swaps (CDS) market implied default probability of the issuer is used in the pricing. We have changed the repo curve generation methodology. 

Instead of a fixed term structure, the repo curve for each issuer in essence becomes “repo collections” in which a constant repo factor is stored with respect to each outstanding bond with same issuer. The computation of the repo factor for each bond remains unchanged. 

The repo curve of an issuer is defined as a collection of N repo factors,  , associated with each outstanding Bonds/FRNs of the issuer.  The ith bond is described by a principal  and coupon payment dates  (maturity) with coupon payment  . 

The default probability of the issuer is described by the hazard rate curve  , which is calibrated by market information of CDS trades with the issuer being the reference entity.  With this definition the default probability functions built upon the hazard rate curve are

(1)	 = Survival probability.

(2)	  = Default probability density function seen at time zero

With certain probability the bond won’t default before maturity. In this case the bondholder receives coupons at coupon payment dates and principal at maturity. However, there is a possibility that the bond will default before maturity thus the bondholder will only receive a recovered value based on principal plus accrued coupon. The present value (PV) of the ith  bond can be calculated by

(3)  .

  is the day count fraction; R is the recovery rate; D(t) is the discount factor.   is defined as

(4)	 ,

where   is Repo Factor of  the ith bond in  .    is calculated by  letting PV in Eq.(3)  equal to the market price of the bond. We do such calibration for all the outstanding bonds/FRNs with same issuer to get the repo curve or “repo factor collection” for the issuer.

Repo factor actually defines the relationship between CDS spreads and bond yield spreads. Theoretically there is a relationship between bond yield spread and CDS spread, which has been verified by empirical analysis.  The repo factor looks at risky bonds in a different way, with the assumption that the default probability of the issuer is same as that implied by the CDS trades. All other information implied in the bond yield spread, such as liquidity and funding cost difference between bonds and CDS trades, still remains the adjustment to the discount factor. 

The computation of PV of risky bond, as shown in Eq.(3), appears to have same definitions and assumptions on payoff, interest rate, default, and recovery rate, no matter what information one believes implied by the bond yield spread. The calculation of repo factor by current definition is straightforward. 

References:
https://finpricing.com/lib/IrCurveIntroduction.html




