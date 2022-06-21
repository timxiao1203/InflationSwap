# Inflation Swap

An inflation linked asset swap is a security in which a stream of inflation linked cash flows, that match the payments of an inflation linked bond, are swapped for a stream of cash flows that pay LIBOR plus a spread, or a fixed rate.

The valuation of inflation linked asset swap considers only the case where the cash flows matching the bond coupon and principal repayments are linked to inflation by a scaling factor. When the indexation lag for the inflation swap is not the same as that for the zero coupon swaps there is an additional convexity correction.

The valuation of a floating LIBOR stream is standard and this report discusses only the valuation of inflation linked leg. The coupon cash flows of the inflation linked leg are given and the principal repayment at time Tn is provided.

The present value of each expected cash flow is obtained by discount it from the payment date to the value date, i.e., and the present value of the principal repayment is given. 

where df (t,TP )is the discount factor between i-th payment date and the value date, and the expectation is calculated under the T-forward measure. The value of the inflation linked leg, V is the sum of present values of all cash flows:

Zero coupon inflation swaps are usually defined with an indexation lag of two months and the expected RPI value is obtained from the forward RPI curve constructed from zero coupon (ZC) inflation swaps, i.e.,

for the payment at time T. If the indexation lag m in the equations for the ILAS is the same as that for ZC swaps, then the expected value of the index is replaced by its forward value interpolated from a ZC implied RPI forward curve.

When the indexation lags do not match there is an additional convexity correction that arises from a timing mismatch between the natural payment time of the forward RPI index (2 months after the index reset) and the actual payment time. For example, if m = 8 months, getting expected RPI value from the forward RPI curve constructed from zero coupon (ZC) inflation swaps provides and the expectation is calculated under the (T months) i − 6 -forward measure rather than T, i.e., there is 6 months time mismatch.

The close out reserve represents the cost of flattening out (i.e. closing out) the exposure to RPI index. The formula used to calculate the close-out reserve, R(Close −Out), on a per bucket basis is given where ΔS is the ZC inflation swap bid/offer spread

The seasonality reserve, , is based on the results of scenario testing with 39 scenarios. Once portfolio MtM’s are obtained under various seasonality adjustment scenarios, the Mark-to-Market of the worst case, , is determined in the following way

where MtM(0) is the current MtM, MtM(W1 ) is the worst (lowest) MtM and MtM(W2 ) is the second worst MtM. The reserve is calculated as

R(SI ) = MtM(0)− MtM(W)

For ILAS, current MtM is calculated without convexity adjustment. This adjustment is added to reserve as convexity reserve, R(Convx), and it is given by

R(Convx) = max(0, MtM(0)− MtM(Convx))

where MtM(Convx) is portfolio MtM with convexity adjustment.



Reference:

https://finpricing.com/lib/EqVariance.html

https://zenodo.org/record/6607394#.YpjM_KgpBD8

https://zenodo.org/record/6607394/files/inflationSwap.pdf

