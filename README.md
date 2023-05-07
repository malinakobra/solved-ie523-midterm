Download Link: https://assignmentchef.com/product/solved-ie523-midterm
<br>
I want you to write a comprehensive, readable (i.e. put a lot of comments; have meaningful variable names; etc. etc.) <em>Portfolio Optimization Software Package </em>in C++ assuming you have parallel shifts in the term structure.

<strong>Input Specification</strong>: The input file to your software will have the following format:

<em>1st-line:                      </em>#CFs

<em>2nd-line:                    </em>CF-1’s PV                Maturity

<em>3rd-line:                     </em>CF-2’s PV                Maturity

<em>4th-line:                     </em>CF-3’s PV                Maturity

<ul>

 <li>·· ··· ···         ···        ···        ···        ···          ···          ···          ···</li>

</ul>

<em>kth-line:                      </em>CF-<em>k</em>’s PV                Maturity

<table width="254">

 <tbody>

  <tr>

   <td width="98">(<em>k </em>+ 1)<em>th-line:</em></td>

   <td width="104">FV of user’s</td>

   <td width="52">due</td>

  </tr>

  <tr>

   <td width="98"> </td>

   <td width="104">debt obligation</td>

   <td width="52">date</td>

  </tr>

 </tbody>

</table>

(i.e. <em>k</em>-many Bonds; the 1st number in each row is the PV of the bond, followed by the bond’s cash-flows; not all of them have the same maturity; followed by the FV of user’s debt obligation and the time when its is due).

<strong>Output Specification 1</strong>: We do not assume a flat term structure, but we assume the term structure changes are <em>parallel </em>(i.e. the yield changes by the same %-age amount for all maturities).

<ol>

 <li>Compute the <em>YTM </em>for each cash flow.</li>

 <li>Compute the <em>duration </em>for each cash flow.</li>

 <li>Compute the <em>convexity </em>for each cash flow.</li>

</ol>

<strong>Output Specification 2 </strong>Assuming no changes in term structure, compute the %-age of the face value of each cash flow you would have to purchase to meet the future debt obligation.

<strong>Output Specification 3</strong>: Pick the bond-portfolio that will meet this obligation when it is due, and has the largest convexity among all possible portfolio choices. You should pose this as a Linear Programming Problem and use lp solve to find the optimal answer. Your final answer will say that we need to buy <em>λ</em><sub>1</sub>% of first cash flow, <em>λ</em><sub>2</sub>% of second cash flow, <em>λ</em><sub>3</sub>% of third cash flow, etc. No short-selling is permitted (i.e. all your <em>λ</em>’s have to be non-negative).

<ol>

 <li>In your write-up, present an explanation of the strategy/method that you used in picking the best portfolio.</li>

 <li>Make sure your program will handle the case when there is no portfolio that will meet the debt obligation if we are worried about (parallel) movements in the term structure (cf. figure 2).</li>

</ol>

I also want to see a couple of sample runs (cook-up your own data; or use lesson 4 of my notes).

<em>Partial Credit Information: </em>This should help you decide how your efforts should be spent in the next two weeks.

<ol>

 <li>(<em>20 points</em>) Making sure you catch every possible error/infeasibility that might occur in the general setting.</li>

 <li>(<em>20 points</em>) Soundness of your theoretical arguments for the design-methodology that you adopt for the portfolio design.</li>

 <li>(<em>60 points</em>) The correct functioning of your code.</li>

</ol>

A sample screen shot is shown in figure 1.

Figure 1: A sample screen shot.

Figure 2: A sample screen shot of an infeasible set of cashflows.

Figure 3: A sample screen shot for the example that is done in lesson 4. You can compare these results with those in the Brute-Force Excel Spreadsheets provided on Compass with Lesson 4.