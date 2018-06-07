[Back to index](https://pedroysb.github.io/Privacy-by-Evidence)

# Case Study I: Smart Metering

<p>In this section, we present the first case study, a smart metering application which uses information regarding energy consumption. Although the main objective is to validate the <em>PbE</em>, we believe that the results presented in this section are of importance for the smart metering area. These results were to be applied in the LiteMe<a href="#fn1" class="footnoteRef" id="fnref1"><sup>1</sup></a> application, a project developed by the Smartiks<a href="#fn2" class="footnoteRef" id="fnref2"><sup>2</sup></a> company in partnership with the <em>Federal University of Campina Grande</em> (<em>UFCG</em>).</p>
<h2 id="context-and-data-formats">Context and Data Formats</h2>
<p>Smart Grids are systems that combine the traditional power grid with modern information technologies to enable a more efficient and robust grid. With these systems, power providers can monitor, analyze and control the network and communicate with the consumers to improve the energy quality, reduce energy consumption and cost, and maximize the transparency and reliability of the energy supply chain. In this scenario, a key component on the consumers’ side is the use of smart meters.</p>

<p>Smart meters are devices that measure electricity consumption in real time and transmit this data to remote servers. These devices may represent a turning point in the energy industry and foster the development of new services and improvement of existing ones. In a typical smart metering architecture, the analysis of the collected data can help power providers to learn how to better manage the areas within their networks. Thus, helping to understand the business benefits of investing in Smart Grids. Figure 6 presents a smart metering system architecture.</p>

<div class="figure">
<center>
<img src="figs/architecture.png" />
<p class="caption">Figure 6: Smart metering system architecture and data usage applications <span class="citation">(Waters 2006)</span>.</p>
</center>
</div>

<p>Despite the benefits, smart meters raise concerns about the privacy of consumers. Electricity data may contain private sensitive information, such as which appliances are being used, if the house is empty, when people take a shower or shut down the television. The privacy issues are some of the main reasons why smart meters were still not deployed in many countries <span class="citation">(Koehle 2012)</span>. Clearly, there is a trade-off between utility and privacy.</p>
<p>As an example of the data format, Figure 7 shows a daily profile of a residential consumer.<a href="#fn3" class="footnoteRef" id="fnref3"><sup>3</sup></a> Using advanced power signature analysis tools, such as the <em>Non-Intrusive Appliance Load Monitoring</em> (<em>NIALM</em>), it is possible to find out private information about the consumer’s lifestyle. Batra <em>et al.</em> <span class="citation">(Batra et al. 2014)</span> designed some methodologies to identify the use of appliances from load profiles. In Figure 7, the appliance with highest wattage and easier to identify is the laundry dryer. If the load monitoring algorithm is running remotely, the consumers may not know that their behaviors are being monitored.</p>

<div class="figure">
<center>
<img src="figs/dailyProfile.png" />
<p class="caption">Figure 7: Residential (black solid) and Laundry Dryer (red dashed) daily profiles with measurements at each 1 minute.</p>
</center>
</div>

<p>In a traditional industrial setting, such behavior information is not in principle useful for a power provider. However, currently this type of information is of interest to many businesses that want to identify the profile of a potential consumer of their products and services. Therefore, disclosing such profiles and habits of consumers evokes issues about privacy. Clear rules are needed to protect consumers from misuse of their behavioral data and to avoid that Smart Grids become a new type of Big Brother <span class="citation">(Boccuzzi 2010)</span>. Unfortunately, protection laws may take decades to be applied whereas smart meters are already operational.</p>
<h2 id="sec:normssmartmetering">Norms and Legislation</h2>
<p>Regarding the activity of checking compliance with norms and legislations for the energy data, the <em>Brazilian National Agency of Electrical Energy</em> (<em>ANEEL</em>) establishes a normative resolution<a href="#fn4" class="footnoteRef" id="fnref4"><sup>4</sup></a> with the following rule of privacy for smart metering: “<em>In the hypothesis of a metering system with a remote communication, the power provider has to adopt procedures and technologies to ensure the security of the data traffic and, specially, of the collected personal information</em>”. In other words, this rule determines that security mechanisms such as encryption and certification must be used.</p>
<p>In the same article, <em>ANEEL</em> establishes another rule: “<em>It is forbidden for the power provider to disclose to third parties the data collected from consumer units without authorization of the owners</em>”. These rules could help to provide some evidences of privacy, but unfortunately they were suspended by the agency since February 11, 2014. Moreover, even if they come back in the future, it is known that there are possibilities of external hackers to penetrate systems (including the Meter Data Management in the power provider), or internal malicious employees to export the data after a decryption.</p>
<p>Another rule<a href="#fn5" class="footnoteRef" id="fnref5"><sup>5</sup></a> established by <em>ANEEL</em> is: “<em>The meters must have mass storage capable of storing active and reactive energy data, demand and tension, considering the direct and reverse flow of energy according to the usage, at programmable intervals of 5 (five) to 60 (sixty) minutes</em>”. The granularity of 5 minutes is the important information here. This could help to provide evidences of privacy, however it is known that <em>NIALM</em> algorithms can still identify appliance usages with this granularity. Moreover, this rule is only applied to official and regulated meters. The energy meter used by the LiteMe application is just an additional device that does not have the goal to replace existing traditional meters. Therefore, for many purposes, this device has the ability to collect and send data with time intervals of 1 second.</p>
<p>Despite the lack of norms and legislation to be applied in this application, the study and the summary of possibilities suggest a concern for privacy in this project, generating this, an evidence of privacy. Table 4 describes a sheet for this evidence <span class="math inline"><em>E</em>1</span> and Figure 8 presents the first part of the <em>GSN</em> for the privacy case of a smart metering application. This representation is still to grow, according to the normal software evolution and our proposed methodology. In this application context, assuming that security assurances have been taken, there is an argument that the privacy is being preserved according to the provided evidences. For now, there is only one evidence provided (<span class="math inline"><em>E</em>1</span>).</p>

<table>
  <caption>Table 4: Sheet for the evidence <span class="math inline"><em>E</em>1</span>. Norms and legislations for smart metering.</caption>
  <tr>
    <td align="left">E1</td>
    <td align="left">Norms and legislations have been studied</td>
    <td align="left"><b>Status:</b><br>Done</td>
    <td align="left"><b>Review Date:</b><br>August 2015</td>
    <td align="left"><b>Weight:</b><br>1</td>
  </tr>
  <tr>
    <td colspan="5"><i>PbE Activity</i>: Check Compliance with Norms and Legislation</td>
  </tr>
  <tr>
    <td colspan="5"><i>Driven by</i>: G1 → G2; <i>In context of</i>: C1; <i>Assumptions</i>: As1</td>
  </tr>
  <tr>
    <td colspan="5"><u>Description</u>: Possible norms and legislations that could be applied for the smart metering application have been studied and summarized. In Brazil, it was not found any norm or law dealing with the collection, storage and processing of energy metering data that could affect the design of the LiteMe application. There are norms proposed by the <i>ANEEL</i>, but only applied to official and regulated meters.</td>
  </tr>
    <tr>
    <td colspan="5"><u>References</u>: <a href="https://pedroysb.github.io/Privacy-by-Evidence/case1#norms-and-legislation">Norms and Legislation</a> </td>
  </tr>
</table>

<div class="figure">
<center>
<img src="figs/gsn-smartmetering1.png" alt="First iteration of the construction of the GSN representation for the privacy case of a smart metering application." />
<p class="caption">Figure 8: First iteration of the construction of the <em>GSN</em> representation for the privacy case of a smart metering application.</p>
</center>
</div>

<h2 id="sec:smrisk">Utilities and Risk Assessment</h2>
<p>For the risk assessment, first we identified what is possible to do with the collected energy data. Since individual values (such as the consumption of a house in an instant of time) are more sensitive than aggregate values (such as the total consumption in a region with <span class="math inline"><em>N</em></span> consumers, or the total consumption of a house in the end of a billing period), the privacy techniques need to focus on hiding individual values.</p>
<p>Many utilities that use metering data were listed in Table 5. From this list, using a risk binary scale, “load forecasting for individual consumers”, “individual data analytics” and “demand-based rates” were considered as privacy threats that needed to be solved. This classification is based on the usage of individual values. The check if a utility uses individual values (and thus if it is a privacy risk) can be found in the references.</p>
<p>Unfortunately, “demand-based rates” may be a legitimate utility but regarded as a privacy risk. Power providers would charge based on the instantaneous power, but to do that, it is necessary to know the individual measurements.</p>

<table>
  <center>
  <caption>Table 5: List of metering data utilities.</caption>
  <tr>
    <td align="center" style='font-weight:bold;'>Feature / Benefit</td>
    <td align="center" style='font-weight:bold;'>Privacy Risk?</td>
  </tr>
  <tr>
    <td align="center" >Billing optimization <span class="citation">(Barbosa et al. 2014)</span></td>
    <td align="center" style="color:green">No</td>
  </tr>
  <tr>
    <td align="center" >Load monitoring and management for specific groups or regions <span class="citation">(Barbosa et al. 2014)</span></td>
    <td align="center" style="color:green">No</td>
  </tr>
  <tr>
    <td align="center" >Energy theft/losses detection <span class="citation">(Anas et al. 2012)</span></td>
    <td align="center" style="color:green">No</td>
  </tr>
  <tr>
    <td align="center" >Load forecasting for specific groups or regions <span class="citation">(Ilić et al. 2013)</span></td>
    <td align="center" style="color:green">No</td>
  </tr>
  <tr>
    <td align="center" >Load forecasting for individual consumers <span class="citation">(Ilić et al. 2013)</span></td>
    <td align="center" style="color:orange">Yes</td>
  </tr>
  <tr>
    <td align="center" >Time-based rates (<em>e.g.</em>, different prices based on time of day and season) <span class="citation">(Barbosa et al. 2014)</span></td>
    <td align="center" style="color:green">No</td>
  </tr>
  <tr>
    <td align="center" >Demand-based rates (<em>e.g.</em> different prices based on demand levels) <span class="citation">(Procel 2011)</span></td>
    <td align="center" style="color:orange">Yes</td>
  </tr>
  <tr>
    <td align="center" >Individual data analytics (<em>e.g.</em> <em>NIALM</em> and marketers) <span class="citation">(Barbosa, Brito, and Almeida 2015; NIST 2014)</span></td>
    <td align="center" style="color:orange">Yes</td>
  </tr>
  <tr>
    <td align="center" >In-home feedback tools: estimated bills, device profiles etc <span class="citation">(Ying-Xun et al. 2013)</span></td>
    <td align="center" style="color:green">No</td>
  </tr>
  </center>
</table>

<h3 id="adversary-model">Adversary Model</h3>

<p>In the smart metering privacy literature, it is common to consider the power provider as an adversary (honest, but curious) and, transitively, the data exposure to third parties becomes a threat to privacy too. Therefore, it is resonable to consider the power provider as an adversary and to apply the privacy techniques on the consumers’ side <span class="citation">(Busom et al. 2015; Erkin and Tsudik 2012; Garcia and Jacobs 2010; Backes and Meiser 2014; Kalogridis et al. 2010; McLaughlin, McDaniel, and Aiello 2011; Zhao et al. 2014; Backes and Meiser 2014; Kalogridis et al. 2010; McLaughlin, McDaniel, and Aiello 2011; Zhao et al. 2014)</span>. Figure 9 presents the second iteration of the construction of the <em>GSN</em> representation for this case study. The diagram now considers the adversary model, <em>i.e.</em>, the assumption that the sensor is not an adversary and the strategy to provide mitigations considering that the service is an adversary.</p>

<div class="figure">
<center>
<img src="figs/gsn-smartmetering2.png" alt="Second iteration of the construction of the GSN representation for the privacy case of a smart metering application." />
<p class="caption">Figure 9: Second iteration of the construction of the <em>GSN</em> representation for the privacy case of a smart metering application.</p>
</center>
</div>

<h2 id="sec:sm_priv_techniques">Privacy Techniques</h2>

<p>With the considerable amount of privacy-preserving techniques that can be adopted to ensure privacy in smart metering, the need to better understand and compare these solutions rise. In general, there are techniques based on homomorphic encryption <span class="citation">(Busom et al. 2015; Erkin and Tsudik 2012; Garcia and Jacobs 2010)</span>, the techniques that use rechargeable batteries <span class="citation">(Backes and Meiser 2014; Kalogridis et al. 2010; McLaughlin, McDaniel, and Aiello 2011; Zhao et al. 2014)</span>, and the ones that make use of noise addition <span class="citation">(S. Wang et al. 2012; Bohli, Sorge, and Ugus 2010; He, Zhang, and J. Kuo 2013; Barbosa, Brito, and Almeida 2016)</span>. Since the main privacy issues are derived from individual data, these privacy preserving approaches tend to reveal aggregate data and hide individual data.</p>
<p>To enable power providers to process smart meter measurements, while preventing them to access private data, cryptographic tools like homomorphic encryption may be used. With these approaches, before sending its measurement, each smart meter runs a cryptographic routine. The power provider receives encrypted measurements, but can still perform useful computations and output the correct aggregate values, like the total consumption of a consumer during a billing period or the total consumption in the region in an instant of time. Thus, some benefits of using smart metering are still provided, while the consumer privacy is maintained.</p>
<p>Techniques based on the usage of rechargeable batteries consist in using a battery between the smart meter and home appliances. Therefore, the disclosed information is the battery load profile, but not the daily activities and appliance usages of consumers.</p>
<p>Through noise addition techniques, individual measurements are masked by adding random numbers. This masking happens in a way that does not affect the outcome of the aggregating operations but hides the individual measurements.</p>
<p>The privacy techniques were evaluated <span class="citation">(Barbosa et al. 2016)</span>, and it was concluded that noise addition stands out from the others. Despite the disadvantage in accuracy, it has a low complexity, scalability, meters’ independence, low cost and low environmental impact (this one, when compared with rechargeable batteries approach).</p>

<h3 id="sec:noise">Noise Addition</h3>

<p>Noise addition is a privacy preserving technique to mask the data. Wang <em>et al</em>. <span class="citation">(S. Wang et al. 2012)</span> propose an approach to mask the data adding random numbers from a <em>Gaussian Mixture Models</em> (<em>GMM</em>), whereas Bohli <em>et al</em>. <span class="citation">(Bohli, Sorge, and Ugus 2010)</span> and He <em>et al</em>. <span class="citation">(He, Zhang, and J. Kuo 2013)</span> propose approaches to mask the data using Gaussian noise. Noise addition is a promising and efficient technique, however, these mentioned approaches do not have formal models to calculate the amount of noise that should be added to guarantee desired privacy and utility levels. In fact, He <em>et al</em>. <span class="citation">(He, Zhang, and J. Kuo 2013)</span> argue that for real world system design, a proper trade-off between privacy protection and accuracy should be considered.</p>
<p>We propose that for every measurement, the smart meter reads the consumption and adds a random number <span class="citation">(Barbosa et al. 2014)</span>. Thus, after an aggregating operation (such as the calculation of the total consumption in a region or the total consumption of a consumer in the end of a billing period), the result will be: <br />
  
  <span class="math display">&sum;<sub>i=1</sub><sup>N</sup> c<sub>i</sub> ~ &sum;<sub>i=1</sub><sup>N</sup> ( c<sub>i</sub> + x<sub>i</sub> )</span><br /> 
  
  where <span class="math inline"><em>N</em></span> is the total number of measurements, <span class="math inline"><em>x</em><sub><em>i</em></sub></span> is a random number generated from a probabilistic distribution and <span class="math inline"><em>c</em><sub><em>i</em></sub></span> is an individual consumption measurement.</p>
<p>The previous formalization can also be rewritten as follows: <br /><span class="math display">$$\sum_{i=1}^N c_i\ =\ \sum_{i=1}^N \left( c_i\ +\ x_i \right)\ -\ e_o$$</span><br /> where <span class="math inline"><em>e</em><sub><em>o</em></sub></span> is the obtained error by the addition of random numbers. Therefore, <span class="math inline"><em>e</em><sub><em>o</em></sub></span> is the sum of all added random values: <br /><span class="math display">$$e_o\ =\ \sum_{i=1}^N x_i \text{ .}$$</span><br /></p>
<p>We developed many analytical models using probability theory for different distributions <span class="citation">(Barbosa, Brito, and Almeida 2015)</span>. Here we consider the Laplace distribution. Let <span class="math inline"><em>x</em><sub><em>i</em></sub></span> be a random variable generated from this distribution. Its variance is <span class="math inline"><em>σ</em><sub><em>x</em></sub><sup>2</sup>  =  2<em>b</em><sup>2</sup></span>, where <span class="math inline"><em>b</em></span> is a scale parameter. Now, for a large <span class="math inline"><em>N</em></span>, the central limit theorem ensures that the obtained error for billing purpose follows a normal distribution with mean <span class="math inline"><em>μ</em><sub><em>e</em><sub><em>o</em></sub></sub> = 0</span> and variance: <br /><span class="math display"><em>σ</em><sub><em>e</em><sub><em>o</em></sub></sub><sup>2</sup>  =  <em>N</em><sup>2</sup>(<em>σ</em><sub><em>x</em></sub><sup>2</sup> / <em>N</em>)  =  <em>N</em><em>σ</em><sub><em>x</em></sub><sup>2</sup>  = 2<em>N</em><em>b</em><sup>2</sup> .</span><br /></p>
<p>In other words, to have an obtained error between two accepted values (with high probability), we can use the following normal distribution: <br /><span class="math display"><em>e</em><sub><em>o</em></sub>  ∼  <em>N</em>(0, 2<em>N</em><em>b</em><sup>2</sup>) .</span><br /></p>
<p>As an example, Figure 7 shows a daily profile of a residential consumer. There are 16 appliances in this consumption profile. However, the appliance with highest wattage and easier to identify is the laundry dryer. Assuming the billing period as one month, the total consumption of this consumer during the billing period (one month of 31 days) is 131.978 kWh. Considering a maximal allowed error of 5% for billing purpose, we have 6.5989 kWh. Thus, the variance for a high probability (<em>e.g.</em>, 0.98) of not exceeding this value is <span class="math inline"><em>σ</em><sub><em>e</em><sub><em>o</em></sub></sub><sup>2</sup> = 8.04626</span>. Isolating the scale parameter <span class="math inline"><em>b</em></span> from Equation [eq:lapVar], we have (for measurements at each 1 minute, <span class="math inline"><em>N</em> = 44, 640</span>): <br /><span class="math display">$$b\ =\ \sqrt{\sigma_{e_o}^2 / \left(2 N \right)} \ =\ 0.0094934 \text{ .}$$</span><br /></p>

<p>Figure 10 presents the daily profile of Figure 7 masked using this Laplacian noise. Considering that at the end of the month the power provider sums the informed masked values by the consumer, it obtains a value of 133.7977 kWh. The real value is 131.978 kWh. The difference between these values is an error of 1.3788%, less than the maximum allowed error (5%). This error may be less if the consumer does not mask the measurements all the time. Also, if the meter firmware accumulates the sum of the added random numbers and sends that with the last measurement of the month, the error is zero.</p>

<div class="figure">
<center>
<img src="figs/maskedDailyProfile.png" />
<p class="caption">Figure 10: Residential masked daily profile with measurements at each 1 minute.</p>
</center>
</div>

<p>The existence of errors in applications of electrical networks are often found nowadays (since these errors should be less than established limits). For example, in Brazil, the INMETRO (National Institute of Metrology, Standardization and Industrial Quality) establishes percentual error limits to measurements for billing purposes. For residential customers (defined as class B), the percentual relative error for active energy must stay between +/- 2%, while for industrial customers (defined as class A), this error must stay between +/-3%. For more information see the ordinance number 375 of September 27, 2011 <span class="citation">(INMETRO 2011)</span>.</p>
<p>A key feature of the approach is the possibility to allow the consumer and the power provider to negotiate the privacy and utility levels by just changing the allowed error/noise magnitude. Moreover, since this masking approach considers only the data that is disclosed to the power provider, it does not affect the customer’s ability of analyzing his own real consumption profile inside his home and identifying appliance usage <span class="citation">(Ying-Xun et al. 2013)</span>.</p>
<p>We claim that the proposed approach is lightweight <span class="citation">(Barbosa et al. 2014)</span> because in order to preserve privacy the approach just generates a random number. Also, it is possible to provide differential privacy <span class="citation">(Dwork 2006)</span> guarantees for appliance usages, making them indistinguishable in a consumption profile <span class="citation">(Barbosa, Brito, and Almeida 2016)</span>.</p>
<h4 id="differential-privacy-for-appliances">Differential Privacy for Appliances</h4>
<p>Dwork <span class="citation">(Dwork 2006)</span> proposed the notion of differential privacy for general datasets. A mechanism of obfuscation is differentially private if its outcome is not significantly affected by the removal or addition of a single dataset participant. Here, we instantiate this notion for datasets of energy consumption profiles.</p>
<p>Since the privacy is related with appliance usage (<em>i.e.</em>, the consumer behavior), we aim to achieve differential privacy for appliances in metering data without affecting the aggregate data. Thus, appliances are participants in consumption profiles and an adversary learns approximately the same information about any individual appliance, regardless of its presence or absence in the original profile.</p>
<p>Considering that a consumption profile is a set of appliances, we say profiles <span class="math inline"><em>P</em>1</span> and <span class="math inline"><em>P</em>2</span> differ in at most one appliance if one is a proper subset of the other and the larger dataset profile contains just one additional appliance.</p>
<p>An obfuscation mechanism <span class="math inline"><em>K</em></span> gives <span class="math inline"><em>ϵ</em></span>-differential privacy if for all profiles <span class="math inline"><em>P</em>1</span> and <span class="math inline"><em>P</em>2</span> differing in at most one appliance, and all <span class="math inline"><em>S</em> ⊆ <em>R</em><em>a</em><em>n</em><em>g</em><em>e</em>(<em>K</em>)</span>, <br /><span class="math display"><em>P</em><em>r</em>[<em>K</em>(<em>P</em>1)∈<em>S</em>]≤<em>e</em><em>x</em><em>p</em>(<em>ϵ</em>)×<em>P</em><em>r</em>[<em>K</em>(<em>P</em>2)∈<em>S</em>]</span><br /> where the probability is taken over the randomness of <span class="math inline"><em>K</em></span>.</p>
<p>The <span class="math inline"><em>ϵ</em></span> value is the privacy metric and for better privacy, a small value is desirable. A mechanism <span class="math inline"><em>K</em></span> satisfying this definition addresses concerns that any appliance might have about the leakage of its information: even if the appliance has been removed from the dataset, no outputs (and thus consequences of outputs) would become significantly more or less likely.</p>
<p>Differential privacy is achieved by the addition of noise whose magnitude is a function of the largest change a single appliance could have on the output profile; this quantity is referred as the sensitivity of the function.</p>
<p>For <span class="math inline"><em>f</em> : <em>P</em> → <em>R</em><sup><em>k</em></sup></span>, the sensitivity of <span class="math inline"><em>f</em></span> is <br /><span class="math display"><em>Δ</em><em>f</em> = max<sub><em>P</em>1, <em>P</em>2</sub> ∥ <em>f</em>(<em>P</em>1)−<em>f</em>(<em>P</em>2)∥<sub>1</sub></span><br /> for all <span class="math inline"><em>P</em>1</span>, <span class="math inline"><em>P</em>2</span> differing in at most one appliance.</p>
<p>In particular, when <span class="math inline"><em>k</em> = 1</span> the sensitivity of <span class="math inline"><em>f</em></span> is the maximum difference in the values that the function <span class="math inline"><em>f</em></span> may take on a pair of profiles that differ in only one appliance.</p>
<p>The privacy mechanism, denoted <span class="math inline"><em>K</em></span> for a query function <span class="math inline"><em>f</em></span>, computes <span class="math inline"><em>f</em>(<em>X</em>)</span> and adds noise with a Laplace distribution with mean <span class="math inline"><em>μ</em> = 0</span> and scale parameter <span class="math inline"><em>b</em></span>: <br /><span class="math display"><em>b</em> = <em>Δ</em><em>f</em>/<em>ϵ</em> ∴  <em>ϵ</em> = <em>Δ</em><em>f</em>/<em>b</em> .</span><br /></p>
<p>The variance of the noise distribution is <span class="math inline">2<em>b</em><sup>2</sup></span>. On query function <span class="math inline"><em>f</em></span> the privacy mechanism <span class="math inline"><em>K</em></span> responds with <br /><span class="math display"><em>f</em>(<em>X</em>)+(<em>L</em><em>a</em><em>p</em>(<em>Δ</em><em>f</em>/<em>ϵ</em>))<sup><em>k</em></sup></span><br /> adding noise with distribution <span class="math inline"><em>L</em><em>a</em><em>p</em>(<em>Δ</em><em>f</em>/<em>ϵ</em>)</span> independently to each of the <span class="math inline"><em>k</em></span> components of <span class="math inline"><em>f</em>(<em>X</em>)</span>. Note that decreasing <span class="math inline"><em>ϵ</em></span>, a publicly known parameter, flattens out the <span class="math inline"><em>L</em><em>a</em><em>p</em>(<em>Δ</em><em>f</em>/<em>ϵ</em>)</span> curve, yielding larger expected noise magnitude.</p>
<p>[theorem:diffPriv] For <span class="math inline"><em>f</em> : <em>P</em> → <em>R</em><sup><em>k</em></sup></span>, the mechanism <span class="math inline"><em>K</em></span> that adds independently noise with distribution <span class="math inline"><em>L</em><em>a</em><em>p</em>(<em>Δ</em><em>f</em>/<em>ϵ</em>)</span> gives <span class="math inline"><em>ϵ</em></span>-differential privacy.</p>
<p>The proof of Theorem [theorem:diffPriv] is straightforward and Dwork gives this proof for general datasets in <span class="citation">(Dwork 2008)</span>. This theorem describes a relationship between <span class="math inline"><em>Δ</em><em>f</em></span>, <span class="math inline"><em>b</em></span>, and the differential privacy. To achieve <span class="math inline"><em>ϵ</em></span>-differential privacy, one must choose <span class="math inline"><em>b</em> ≥ <em>Δ</em><em>f</em>/<em>ϵ</em></span>. Given a sufficiently small <span class="math inline"><em>ϵ</em></span>, differential privacy limits the ability of an adversary to identify an appliance in the consumption profile.</p>
<p>Note that it is not hard for a user (or an automated mechanism) to identify the wattage of an appliance purchased. That said, the global sensitivity of the profile from Figure 7 is the maximum variation of the appliance with highest wattage (laundry dryer):</p>
<p><br /><span class="math display"><em>Δ</em><em>f</em> = 0.01022 .</span><br /></p>
<p>We can conclude that, from Equation [eq:b], using an utility requirement of 5%, the achieved privacy level in this example is: <br /><span class="math display">$$\epsilon = \frac{\Delta f}{b} = 1.077 \text{ .}$$</span><br /></p>
<p>In the literature of differential privacy, some researchers argue that the value of <span class="math inline"><em>ϵ</em></span> may be relative because for the same value of <span class="math inline"><em>ϵ</em></span>, the probability of identifying a participant is dependent on the context. Lee et al. <span class="citation">(Lee and Clifton 2011)</span> propose a technique to, in accordance with a context, find a suitable value of <span class="math inline"><em>ϵ</em></span>: <br /><span class="math display">$$\epsilon = \frac{\Delta f}{\Delta v} \ln \frac{(n - 1)p}{1-p} 
  \label{eq:goodEpsilon}$$</span><br /> where <span class="math inline"><em>Δ</em><em>v</em></span> is the largest distance of possible values, <span class="math inline"><em>p</em></span> is the probability of identifying the presence of an individual and <span class="math inline"><em>n</em></span> is the number of individuals in the data set. In the previous example for the consumption profile, we have <span class="math inline"><em>Δ</em><em>v</em> = 0.0178</span> (highest value presented in the profile) and <span class="math inline"><em>n</em> = 16</span> (number of appliances). Thus, considering that the probability of identifying the usage of an appliance is <span class="math inline">1/3</span>, it is suggested to have: <br /><span class="math display">$$\epsilon \leq \frac{0.01022}{0.0178} \ln \frac{15 \cdot 3}{3 \cdot 2} = 1.1568 \text{ .}$$</span><br /></p>
<p>Since in our example the obtained value of <span class="math inline"><em>ϵ</em></span> is <span class="math inline">1.077</span>, we can conclude that an attacker has a probability of identifying the laundry dryer less than <span class="math inline">1/3</span>. In other words, on average, he/she has to try more than three moments to be able to guess one moment of usage of the laundry dryer (and maybe he/she does not know that).</p>
<p>Rearranging Equation [eq:goodEpsilon], we can determine the probability: <br /><span class="math display">$$p = \frac{1}{1 + (n - 1) \cdot exp(- \frac{\epsilon \Delta v}{\Delta f})} \text{ .} 
  \label{eq:prob}$$</span><br /></p>
<p>In Table [tab:appliances] we present the wattages and achieved privacy levels for some appliances of the profile from the previous example. The wattages were obtained from the Tracebase dataset <span class="citation">(Reinhardt et al. 2012)</span>, the <span class="math inline"><em>ϵ</em></span> values were obtained from Equation [eq:b], and the probability values of identifying appliances were obtained from Equation [eq:prob].</p>
<p><span>M<span>0.25</span>M<span>0.2</span>M<span>0.15</span>M<span>0.21</span></span> <strong>Appliance&amp; <strong>Max. Wattage &amp; <strong>Privacy (<span class="math inline"><em>ϵ</em></span>) &amp; <strong>Probability (<span class="math inline"><em>p</em></span>)<br />
Charger Smartphone &amp; <span class="math inline">∼</span>6 &amp; 0.001 &amp; 0.0626<br />
Router &amp; <span class="math inline">∼</span>9 &amp; 0.003 &amp; 0.0628<br />
Playstation 3 &amp; <span class="math inline">∼</span>130 &amp; 0.037 &amp; 0.0663<br />
TV LCD &amp; <span class="math inline">∼</span>140 &amp; 0.075 &amp; 0.0706<br />
PC Desktop &amp; <span class="math inline">∼</span>300 &amp; 0.077 &amp; 0.0708<br />
Refrigerator &amp; <span class="math inline">∼</span>1000 &amp; 0.099 &amp; 0.0733<br />
Printer &amp; <span class="math inline">∼</span>600 &amp; 0.127 &amp; 0.0767<br />
Water Fountain &amp; <span class="math inline">∼</span>260 &amp; 0.143 &amp; 0.0787<br />
Toaster &amp; <span class="math inline">∼</span>700 &amp; 0.257 &amp; 0.0944<br />
Cooking Stove &amp; <span class="math inline">∼</span>900 &amp; 0.276 &amp; 0.0973<br />
Vacuum Cleaner &amp; <span class="math inline">∼</span>1100 &amp; 0.336 &amp; 0.1068<br />
Iron &amp; <span class="math inline">∼</span>1500 &amp; 0.347 &amp; 0.1087<br />
Coffee Maker &amp; <span class="math inline">∼</span>1300 &amp; 0.353 &amp; 0.1097<br />
Microwave Oven &amp; <span class="math inline">∼</span>1400 &amp; 0.457 &amp; 0.1287<br />
Washing Machine &amp; <span class="math inline">∼</span>3000 &amp; 0.903 &amp; 0.2431<br />
Laundry Dryer &amp; <span class="math inline">∼</span>3500 &amp; 1.077 &amp; 0.3031<br />
</strong></strong></strong></strong></p>
<p>As discussed before, lower values of <span class="math inline"><em>ϵ</em></span> or <span class="math inline"><em>p</em></span> imply better privacy. Naturally, the consumer behavior and privacy are correlated with the appliance usage and some of these information may be more sensitive than others.</p>
<p>As we can see in Table [tab:appliances], the appliance wattage is very correlated with the privacy level. However, some appliances with higher wattage have better privacy than some appliances with lower wattage. This is because the accumulated consumption (kWh) is not only dependent on the wattage, but also on the time of use of the appliance.</p>
<p>It is known that less measurements implies higher privacy. Taking an extreme example, if a consumer sends to the power provider only one measurement with the total consumption at the end of the billing period, the achieved privacy is much better than sending measurements at each 1 minute. However, when the number of measurements in a time period is large, our approach generates noise to hide each individual measurement, and the achieved privacy could be as higher as sending only one measurement with the total consumption at the end of the billing period.</p>
<p>Using the proposed model, it is also possible to calculate the achieved utility level for a given privacy requirement. From Equation and we have: <br /><span class="math display">$$\sigma_{e_o}^2 = \frac{2 \cdot N \cdot \Delta f ^ 2}{\epsilon ^ 2} \text{ .}  
  \label{eq:utility}$$</span><br /></p>
<p>Therefore, with this variation, the maximum obtained error (utility level) is easily calculated using the inverse cumulative density function (quantiles) of the normal distribution.</p>
<h4 id="example-of-load-monitoring-in-a-region">Example of Load Monitoring in a Region</h4>
<p>If each consumer masks his data based on the billing period, the power provider may obtain accurate values for billing. However, to obtain accurate values for load monitoring in a region, the number of consumers should be as many as possible because it is desired that the added noise should be unnoticed in the aggregated data used for load monitoring.</p>
<p>The data used in the next example are measurements collected at each 30 minutes from real residential consumers (anonymised) from Ireland (<em>Commission for Energy Regulation – CER</em>) <span class="citation">(CER 2012)</span>. Suppose that the power provider wants to compute the total consumption in a region with many consumers through time for load monitoring (<em>e.g.</em>, find peak times, leak detection, load forecasting and many other applications). Using a billing period of 1 month and measurements at each 30 minutes, it has <span class="math inline"><em>N</em> = 1488</span> measurements for each consumer during a month with 31 days (March). So, in this experiment, we consider a region with 1488 consumers (thus, the data forms a square matrix). Figure 11 shows the regional profile during March obtained from original consumer profiles versus the regional profile obtained from masked profiles.</p>

<div class="figure">
<center>
<img src="figs/regionProfile.png" />
<p class="caption">Figure 11: Regional profile using original data (blue solid) versus using masked data (red dashed) with measurements of 30 min. The profiles are very similar.</p>
</center>
</div>

<p>As depicted in Figure 11, visually there is no difference between the two profiles. However, the obtained errors depend on the population behavior. For example, in a high consumption period the obtained error has a different proportion from the obtained error in a low consumption period. The large errors in Figure 11 were obtained in periods of low consumption (<em>e.g.</em>, during the night), because while consuming less, consumers are still masking their data using a noise level based on the billing period. The blue dashed line in Figure 12 presents the obtained errors through time for this scenario (Figure 11). These errors may be lower if not all consumers decide to mask their data all the time.</p>

<div class="figure">
<center>
<img src="figs/regionErrors.png" />
<p class="caption">Figure 12: Obtained errors for the regional profile using masked profiles versus using filtered profiles. Using filtered profiles implies in better accuracy for load monitoring.</p>
</center>
</div>

<p>The possibility of having consumers deciding when to send masked (vs. original) measurements is in accordance with the privacy definition mentioned by Stallings <em>et al</em>. <span class="citation">(Stallings and Brawn 2015)</span> and can be implemented through a privacy switch (<em>i.e.</em>, enable or disable the masking). As not all consumers are masking the measurements all the time (making the obtained error to be lower), this implies in a utility improvement.</p>

<h3 id="rechargeable-batteries">Rechargeable Batteries</h3>

<p>Rechargeable batteries between appliances and smart meters can help to reduce the privacy issues as the appliance signatures are no longer legible <span class="citation">(Backes and Meiser 2014; Kalogridis et al. 2010; McLaughlin, McDaniel, and Aiello 2011; Zhao et al. 2014)</span>.</p>
<p>Mclaughlin <em>et al</em>. <span class="citation">(McLaughlin, McDaniel, and Aiello 2011)</span> propose an approach called <em>Non-Intrusive Load Leveling</em> (<em>NILL</em>). The goal of a <em>NILL</em> system is to level the load profile to a constant <em>target load</em>, thus removing appliance signatures. When an appliance turns ON, it will exert a load beyond the target load. Thus, <em>NILL</em> will discharge the battery to partially supply the load created by the appliance, maintaining the target load. Similarly, if an appliance enters the OFF state, the load profile will decrease below the target load. These opportunities are used to charge the battery while restoring the target load.</p>
<p>The <em>NILL</em> system consists of two parts: a battery and a control system that regulates the battery’s charge and discharge based on the present load and battery state. The controller attempts to maintain a steady state target load <span class="math inline"><em>K</em><sub><em>S</em><em>S</em></sub></span>, but will go into one of two special states <span class="math inline"><em>K</em><sub><em>L</em></sub></span> or <span class="math inline"><em>K</em><sub><em>H</em></sub></span> if the battery needs to recover from a low or high state of charge.</p>
<p>The essence of <em>NILL</em> is described by the equation, <span class="math inline"><em>u</em>(<em>t</em>)=<em>d</em>(<em>t</em>)+<em>b</em>(<em>t</em>)</span>, where <span class="math inline"><em>b</em>(<em>t</em>)</span> is the battery’s rate of charge overtime, <span class="math inline"><em>d</em>(<em>t</em>)</span> is the actual load profile of the residence and <span class="math inline"><em>u</em>(<em>t</em>)</span> is the load under the influence of <em>NILL</em> as perceived by the smart meter and what is disclosed to the power provider. If <span class="math inline"><em>b</em>(<em>t</em>)&gt;0</span>, the battery is charging, otherwise <span class="math inline"><em>b</em>(<em>t</em>)&lt;0</span> and the battery is discharging. Finally, <span class="math inline"><em>c</em>(<em>t</em>)</span> is used to represent the battery’s state of charge, thus: <br /><span class="math display"><em>c</em>(<em>t</em>)=∫<sub><em>t</em><sub>0</sub></sub><sup><em>t</em></sup><em>b</em>(<em>t</em>)<em>d</em><em>t</em> + <em>c</em>(<em>t</em><sub>0</sub>) .</span><br /></p>
<p>Therefore, <span class="math inline"><em>c</em>(<em>t</em>)</span> is monitored. If <span class="math inline"><em>c</em>(<em>t</em>)&lt;<em>L</em></span>, where <span class="math inline"><em>L</em></span> is the lower safe limit on the battery’s state of charge, then the battery needs to be recharged and the system goes to the <span class="math inline"><em>K</em><sub><em>L</em></sub></span> state. Similarly, if <span class="math inline"><em>c</em>(<em>t</em>)&gt;<em>H</em></span>, the system goes to the <span class="math inline"><em>K</em><sub><em>H</em></sub></span> state and the battery is discharged.</p>

<h3 id="using-a-modified-elgamal-encryption">Using a Modified ElGamal Encryption</h3>

<p>The first homomorphic encryption solution that we consider is based on a modification in the ElGamal encryption, a cryptographic system that relies on the discrete logarithm problem. The ElGamal cryptosystem proceeds as follows:</p>
<ul>
<li><p><em>Set up</em>: a large prime <span class="math inline"><em>q</em></span> is chosen. Next, a generator <span class="math inline"><em>g</em></span> of the cyclic group <span class="math inline">ℤ<sub><em>q</em></sub><sup>*</sup></span> is selected.</p></li>
<li><p><em>Key generation</em>: a secret key <span class="math inline"><em>x</em></span> is generated by setting its value as a random number <span class="math inline"><em>x</em>∈<sub><em>R</em></sub>ℤ<sub><em>q</em></sub><sup>*</sup></span>. The corresponding public key is computed as <span class="math inline"><em>y</em> = <em>g</em><sup><em>x</em></sup></span>.</p></li>
<li><p><em>Encryption</em>: a message <span class="math inline"><em>m</em> ∈ <em>G</em></span> is encrypted under public key <span class="math inline"><em>y</em></span> by taking a random number <span class="math inline"><em>r</em>∈<sub><em>R</em></sub>ℤ<sub><em>q</em></sub><sup>*</sup></span> and computing <span class="math inline"><em>c</em> = <em>g</em><sup><em>r</em></sup></span> and <span class="math inline"><em>d</em> = <em>m</em> ⋅ <em>y</em><sup><em>r</em></sup></span>. The ElGamal encryption of <span class="math inline"><em>m</em></span> under public key <span class="math inline"><em>y</em></span>, <span class="math inline"><em>E</em><sub><em>y</em></sub>(<em>m</em>)</span>, is the tuple <span class="math inline">(<em>c</em>, <em>d</em>)</span>.</p></li>
<li><p><em>Decryption</em>: a ciphertext <span class="math inline"><em>E</em><sub><em>y</em></sub>(<em>m</em>)</span> is decrypted using the private key <span class="math inline"><em>x</em></span> by computing <span class="math inline"><em>m</em> = <em>d</em> ⋅ <em>c</em><sup>−<em>x</em></sup></span>.</p></li>
</ul>
<p>Given messages <span class="math inline"><em>m</em><sub>1</sub></span> and <span class="math inline"><em>m</em><sub>2</sub></span>, we can obtain an encryption of <span class="math inline"><em>m</em><sub>1</sub> ⋅ <em>m</em><sub>2</sub></span> by computing: <br /><span class="math display">$$\begin{aligned}
  E_y(m_1) \cdot E_y(m_2) &amp;= (c_1 \cdot c_2, d_1 \cdot d_2) \\
  &amp;= (g ^ {r_1 + r_2}, m_1 \cdot m_2 \cdot y ^ {r_1 + r_2}) \\
  &amp;= E_y(m_1 \cdot m_2) \text{ .}\end{aligned}$$</span><br /> Hence, ElGamal is a multiplicative homomorphic cryptosystem.</p>
<p>To calculate the total consumption in a region, Busom <em>et al</em>. <span class="citation">(Busom et al. 2015)</span> propose a protocol which uses an additive ElGamal cryptosystem. Given <span class="math inline"><em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub>1</sub></sup>)</span> and <span class="math inline"><em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub>2</sub></sup>)</span>, then, <span class="math inline"><em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub>1</sub></sup>)⋅<em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub>2</sub></sup>)=<em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub>1</sub></sup> ⋅ <em>g</em><sup><em>m</em><sub>2</sub></sup>)=<em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub>1</sub> + <em>m</em><sub>2</sub></sup>)</span>.</p>
<p>Initially, each smart meter possess the following values: a big prime number <span class="math inline"><em>q</em></span> and its generator <span class="math inline"><em>g</em></span>; a secret key <span class="math inline"><em>x</em><sub><em>i</em></sub></span>; a public key <span class="math inline"><em>y</em><sub><em>i</em></sub> = <em>g</em><sup><em>x</em><sub><em>i</em></sub></sup></span>. To encrypt the measurements, it is necessary a global public key <span class="math inline">$y = \prod\limits_{i=1}^{N} y_i$</span>.</p>
<p>Let <span class="math inline"><em>m</em><sub><em>i</em></sub></span> denote the measurement of a smart meter. To calculate the total consumption in the region, the following protocol is executed:</p>
<ol>
<li><p>Each meter generates a random noise value <span class="math inline"><em>z</em><sub><em>i</em></sub> ∈ ℤ<sub><em>q</em></sub><sup>*</sup></span> and computes a ciphertext as <span class="math inline"><em>C</em><sub><em>i</em></sub> = <em>E</em><sub><em>y</em></sub>(<em>g</em><sup><em>m</em><sub><em>i</em></sub> + <em>z</em><sub><em>i</em></sub></sup>)=(<em>c</em><sub><em>i</em></sub>, <em>d</em><sub><em>i</em></sub>)</span> which is sent to the aggregator (which can be the power provider).</p></li>
<li><p>The aggregator combines all the messages as <span class="math inline">$C = (\prod\limits_{i=1}^{N}c_i, 
    \prod\limits_{i=1}^{N}d_i) = (c,d)$</span> and sends <span class="math inline"><em>c</em></span> to each meter.</p></li>
<li><p>Each meter computes <span class="math inline"><em>T</em><sub><em>i</em></sub> = <em>c</em><sup><em>x</em><sub><em>i</em></sub></sup> ⋅ <em>g</em><sup><em>z</em><sub><em>i</em></sub></sup></span> and sends the result to the aggregator. After that, each meter removes <span class="math inline"><em>z</em><sub><em>i</em></sub></span> from its memory.</p></li>
<li><p>Finally, the aggregator computes <span class="math inline">$D = d \cdot (\prod\limits_{i=1}^{N}T_i)^{-1}$</span> and <span class="math inline">$log_gD = M = \sum\limits_{i=1}^{N}m_i$</span>, where <span class="math inline"><em>M</em></span> is the total consumption in the region.</p></li>
</ol>
<p>Notice that, since <span class="math inline"><em>M</em></span> is a relatively small number, the discrete logarithm problem in step 4 can be solved in a short time. In step 2, the aggregator computes: <br /><span class="math display">$$C = (\prod\limits_{i=1}^N g^{r_i}, \prod\limits_{i=1}^N g^{m_i + z_i} \cdot y^{r_i}) = 
  (g^r, g^{M + z} \cdot y^r) = (c , d) \text{ ,}$$</span><br /> and in step 3, each meter computes: <br /><span class="math display"><em>T</em><sub><em>i</em></sub> = <em>c</em><sup><em>x</em><sub><em>i</em></sub></sup> ⋅ <em>g</em><sup><em>z</em><sub><em>i</em></sub></sup> = <em>g</em><sup><em>r</em> ⋅ <em>x</em><sub><em>i</em></sub></sup> ⋅ <em>g</em><sup><em>z</em><sub><em>i</em></sub></sup> = <em>g</em><sup><em>x</em><sub><em>i</em></sub> ⋅ <em>r</em></sup> ⋅ <em>g</em><sup><em>z</em><sub><em>i</em></sub></sup> = <em>y</em><sub><em>i</em></sub><sup><em>r</em></sup> ⋅ <em>g</em><sup><em>z</em><sub><em>i</em></sub></sup> .</span><br /> Therefore, the protocol works because in step 4 the aggregator computes: <br /><span class="math display">$$D = d \cdot (\prod\limits_{i=1}^N T_i)^{-1} = \dfrac{g^{M + z} \cdot
y^r}{\prod\limits_{i=1}^N (y_i^r \cdot g^{z_i})} = \dfrac{g^{M + z} \cdot
y^r}{(\prod\limits_{i=1}^N y_i^r) \cdot g^z} = \dfrac{g^{M + z} \cdot
y^r}{g^z \cdot y^r} = g^M \text{ .}$$</span><br /></p>

<h3 id="using-paillier-encryption-and-secret-sharing">Using Paillier Encryption and Secret Sharing</h3>

<p>A protocol based on Paillier encryption and <em>secret sharing</em> was proposed by Garcia <em>et al</em>. <span class="citation">(Garcia and Jacobs 2010)</span>. The Paillier cryptosystem proceeds as follows:</p>
<ul>
<li><p><em>Set up</em>: two large primes <span class="math inline"><em>p</em></span> and <span class="math inline"><em>q</em></span> are chosen, <span class="math inline"><em>n</em> = <em>p</em> ⋅ <em>q</em></span>, and <span class="math inline"><em>λ</em> = <em>l</em><em>c</em><em>m</em>(<em>p</em> − 1, <em>q</em> − 1)</span>. A random number <span class="math inline"><em>g</em>∈<sub><em>R</em></sub>ℤ<sub><em>n</em><sup>2</sup></sub><sup>*</sup></span> is chosen in such a way that <span class="math inline"><em>g</em><em>c</em><em>d</em>(<em>b</em>, <em>n</em>)=1</span>, where <span class="math inline"><em>b</em> = <em>L</em>(<em>g</em><sup><em>λ</em></sup> <em>m</em><em>o</em><em>d</em> <em>n</em><sup>2</sup>)</span> and <span class="math inline">$L(u) = \frac{(u-1)}{n}$</span>.</p></li>
<li><p><em>Key generation</em>: let <span class="math inline"><em>μ</em></span> be the modular multiplicative inverse of <span class="math inline"><em>b</em></span> modulo <span class="math inline"><em>n</em></span>, <em>i.e.</em>, <span class="math inline"><em>μ</em> = <em>b</em><sup>−1</sup> <em>m</em><em>o</em><em>d</em> <em>n</em></span>. Thus, the public key is <span class="math inline"><em>P</em><sub><em>k</em></sub> = (<em>n</em>, <em>g</em>)</span> and the private key is <span class="math inline"><em>S</em><sub><em>k</em></sub> = (<em>n</em>, <em>λ</em>, <em>μ</em>)</span>.</p></li>
<li><p><em>Encryption</em>: a message <span class="math inline"><em>m</em></span> is encrypted under public key <span class="math inline"><em>P</em><sub><em>k</em></sub></span> by taking a random number <span class="math inline"><em>r</em>∈<sub><em>R</em></sub>ℤ<sub><em>n</em> − 1</sub><sup>*</sup></span> and computing <span class="math inline"><em>E</em><sub><em>P</em><sub><em>k</em></sub></sub>(<em>m</em>)=<em>g</em><sup><em>m</em></sup> ⋅ <em>r</em><sup><em>n</em></sup> <em>m</em><em>o</em><em>d</em> <em>n</em><sup>2</sup></span>.</p></li>
<li><p><em>Decryption</em>: a ciphertext <span class="math inline"><em>c</em> = <em>E</em><sub><em>P</em><sub><em>k</em></sub></sub>(<em>m</em>)</span> is decrypted using the private key <span class="math inline"><em>S</em><sub><em>k</em></sub></span> by computing <span class="math inline"><em>m</em> = <em>L</em>(<em>c</em><sup><em>λ</em></sup> <em>m</em><em>o</em><em>d</em> <em>n</em><sup>2</sup>)⋅<em>μ</em> <em>m</em><em>o</em><em>d</em> <em>n</em></span>.</p></li>
</ul>
<p>Given messages <span class="math inline"><em>m</em><sub>1</sub></span> and <span class="math inline"><em>m</em><sub>2</sub></span>, we can obtain an encryption of <span class="math inline"><em>m</em><sub>1</sub> + <em>m</em><sub>2</sub></span> by computing: <br /><span class="math display">$$\begin{aligned}
  E_{P_k}(m_1) \cdot E_{P_k}(m_2) &amp;= g^{m_1} \cdot r^n_1 \cdot g^{m_2} \cdot r^n_2\ mod\ n^2\\
  &amp;= g ^ {m_1 + m_2} \cdot (r_1 \cdot r_2)^n\ mod\ n^2\\
  &amp;= E_{P_k}(m_1 + m_2) \text{ .}\end{aligned}$$</span><br /> Hence, Paillier is an additive homomorphic cryptosystem.</p>
<p>Garcia <em>et al</em>. <span class="citation">(Garcia and Jacobs 2010)</span> propose that each smart meter possess a public key <span class="math inline"><em>P</em><sub><em>k</em><em>i</em></sub></span> and a private key <span class="math inline"><em>S</em><sub><em>k</em><em>i</em></sub></span>. Let <span class="math inline"><em>m</em><sub><em>i</em></sub></span> denote the measurement of the meter. To calculate the total consumption in the region, the following protocol is executed:</p>
<ol>
<li><p>Each meter sends its public key to the aggregator.</p></li>
<li><p>The aggregator receives all public keys and shares them with all meters. Thus, each meter stays with its private key <span class="math inline"><em>S</em><sub><em>k</em><em>i</em></sub></span> and all the public keys <span class="math inline">{<em>P</em><sub><em>k</em>1</sub>, <em>P</em><sub><em>k</em>2</sub>, …, <em>P</em><sub><em>k</em><em>n</em></sub>}</span>.</p></li>
<li><p>Each meter calculates <span class="math inline"><em>N</em></span> secret shares for its measurement <span class="math inline"><em>m</em><sub><em>i</em></sub></span>, in such a way that <span class="math inline">$m_i = \sum\limits_{j=1}^N s_{ij}$</span>. Then, the meter keeps <span class="math inline"><em>s</em><sub><em>i</em><em>i</em></sub></span> privately and sends to the aggregator all the other secret shares encrypted with the public keys of the other <span class="math inline"><em>N</em> − 1</span> meters, <em>i.e.</em>, it sends <span class="math inline"><em>E</em><sub><em>P</em><sub><em>k</em><em>j</em></sub></sub>(<em>s</em><sub><em>i</em><em>j</em></sub>)</span> for <span class="math inline"><em>j</em> = 1, …, <em>i</em> − 1, <em>i</em> + 1, …, <em>N</em></span>.</p></li>
<li><p>After receiving all the encrypted secret shares, the aggregator multiplies the ones encrypted with the same public key. Due to the Paillier homomorphic property, for each meter <span class="math inline"><em>i</em></span>, it has <span class="math inline">$E_{P_{ki}}(m_i') = \prod\limits_{j \neq i}^N E_{P_{ki}}(s_{ji}) =
    E_{P_{ki}}(\sum\limits_{j \neq i}^N s_{ji})$</span>. Then, the aggregator sends <span class="math inline"><em>E</em><sub><em>P</em><sub><em>k</em><em>i</em></sub></sub>(<em>m</em><sub><em>i</em></sub>′)</span> for each meter <span class="math inline"><em>i</em></span>.</p></li>
<li><p>Using its private key <span class="math inline"><em>S</em><sub><em>k</em><em>i</em></sub></span>, each meter decrypts <span class="math inline"><em>E</em><sub><em>P</em><sub><em>k</em><em>i</em></sub></sub>(<em>m</em><sub><em>i</em></sub>′)</span> and adds its <span class="math inline"><em>s</em><sub><em>i</em><em>i</em></sub></span>, obtaining <span class="math inline">$\sum\limits_{j=1}^N s_{ji}$</span>. The meter then sends this value to the aggregator.</p></li>
<li><p>Finally, the aggregator can sum all the received values, obtaining the total consumption in the region <span class="math inline">$M = \sum\limits_{i=1}^N\sum\limits_{j=1}^N s_{ji}$</span>.</p></li>
</ol>
<p>In this approach, the total consumption in the region is computed and at the same time, neither the aggregator nor any other consumer has access to any real measurement from a consumer, for they can only access random shares. Since in step 6 the aggregator simply sum all the secret shares, the proof that the protocol works is straightforward.</p>

<h3 id="using-a-modified-paillier-encryption">Using a Modified Paillier Encryption</h3>

<p>Erkin <em>et al</em>. <span class="citation">(Erkin and Tsudik 2012)</span> propose a protocol based on a modification in the Paillier encryption. Starting, there is a single pair of Paillier keys (<span class="math inline"><em>P</em><sub><em>k</em></sub></span> and <span class="math inline"><em>S</em><sub><em>k</em></sub></span>) shared with all <span class="math inline"><em>N</em></span> meters. Let <span class="math inline"><em>m</em><sub><em>i</em></sub></span> denote the measurement of the meter. To calculate the total consumption in the region, the following protocol is executed:</p>
<ol>
<li><p>Each meter generates <span class="math inline"><em>N</em> − 1</span> random numbers, one for every one of the other meters, and sends them using secure communication (<em>e.g.</em>, RSA encryption between meters). Thus, there is a total of <span class="math inline"><em>N</em> ⋅ (<em>N</em> − 1)</span> message exchanges in this step.</p></li>
<li><p>After receiving all the random numbers generated by the other meters, the meter computes <span class="math inline">$R_i = n + \sum\limits_{j \neq i}^N r_{(i \to j)} - \sum\limits_{j \neq i}^N r_{(j \to i)}$</span>, where <span class="math inline"><em>n</em></span> is the Paillier modulo and <span class="math inline"><em>r</em><sub>(<em>i</em> → <em>j</em>)</sub></span> is the random number generated by the meter <span class="math inline"><em>i</em></span> for the meter <span class="math inline"><em>j</em></span>.</p></li>
<li><p>Following, the meter computes a hash <span class="math inline"><em>h</em><sub><em>t</em></sub></span> using the timestamp of the current measurement <span class="math inline"><em>m</em><sub><em>i</em></sub></span>. This hash must be coprime with the Paillier modulo <span class="math inline"><em>n</em></span>, <em>i.e.</em>, <span class="math inline"><em>g</em><em>c</em><em>d</em>(<em>h</em><sub><em>t</em></sub>, <em>n</em>)=1</span>. Since the timestamp is synchronized, the obtained hash is the same for all meters.</p></li>
<li><p>After computing <span class="math inline"><em>R</em><sub><em>i</em></sub></span> and <span class="math inline"><em>h</em><sub><em>t</em></sub></span>, the meter encrypts <span class="math inline"><em>m</em><sub><em>i</em></sub></span> using the following modified scheme of Paillier: <span class="math inline"><em>E</em><sub><em>P</em><sub><em>k</em></sub></sub>(<em>m</em><sub><em>i</em></sub>)=<em>g</em><sup><em>m</em><sub><em>i</em></sub></sup> ⋅ <em>h</em><sub><em>t</em></sub><sup><em>R</em><sub><em>i</em></sub></sup></span>. Then, this encrypted measurement is disclosed to all other <span class="math inline"><em>N</em> − 1</span> meters.</p></li>
<li><p>Finally, after receiving all the encrypted measurements of the other meters, the meter calculates <span class="math inline">$E_{P_k}(M) = \prod\limits_{i = 1}^N E_{P_k}(m_i) = 
    E_{P_k}(\sum\limits_{i=1}^N m_i)$</span>. This is true due the homomorphic property.</p></li>
</ol>
<p>Possessing <span class="math inline"><em>E</em><sub><em>P</em><sub><em>k</em></sub></sub>(<em>M</em>)</span>, the meter can decrypt this value and then send the total consumption in the region <span class="math inline"><em>M</em></span> to the aggregator. This way, the total consumption is computed and privacy is preserved, for the meter does not have access to the other measurements in plaintext.</p>
<p>The protocol works because in step 5, the meter computes:</p>
<p><br /><span class="math display">$${E_{P_k}(M) = g^{m_1 + m_2 + \dots + m_N}} \cdot {h_t^{(\sum\limits_{i=1}^N n) + 
  (\sum\limits_{i=1}^N \sum\limits_{j \neq i}^N r_{(i \to j)}) - (\sum\limits_{i=1}^N
  \sum\limits_{j \neq i}^N r_{(j \to i)}) }} \text{ ,}$$</span><br /></p>
<p>and <br /><span class="math display"><em>E</em><sub><em>P</em><sub><em>k</em></sub></sub>(<em>M</em>)=<em>g</em><sup><em>M</em></sup> ⋅ <em>h</em><sub><em>t</em></sub><sup><em>N</em> ⋅ <em>n</em></sup> .</span><br /> Considering that <span class="math inline"><em>r</em> = <em>h</em><sub><em>t</em></sub><sup><em>N</em></sup></span>, this configuration represents the original paillier cryptosystem.</p>

<h3 id="sec:performance">Performance Evaluation of Privacy Techniques</h3>

<p>In order to analyze and compare solutions, we describe the performance aspects that are considered in our studies. This analysis is important because, for example, solutions might excel at low computational complexity but their installation and usage has high costs and harms the environment. Thus, the need to consider different aspects of performance. In this section, we present an experiment that aims to compare the response time (which is related to computational complexity) of the approaches. We also discuss other aspects, such as: scalability, meters’ independence, cost, environmental impact and accuracy. Table [tab:relatedWork] presents a summary and comparison of the discussed approaches.</p>
<p><span>M<span>0.32</span>|M<span>0.17</span>|M<span>0.17</span>|M<span>0.11</span></span> &amp; <strong>NA &amp; <strong>RB &amp; <strong>HE<br />
Low complexity &amp; &amp; &amp;<br />
Scalability &amp; &amp; &amp;<br />
Meters’ independence &amp; &amp; &amp;<br />
Low cost &amp; &amp; &amp;<br />
Low environmental impact &amp; &amp; &amp;<br />
Accuracy &amp; &amp; &amp;<br />
</strong></strong></strong></p>
<p>Legend:</p>
<ul>
<li><p><strong>NA</strong>: Noise Addition <span class="citation">(Barbosa, Brito, and Almeida 2015)</span>;</p></li>
<li><p><strong>RB</strong>: Rechargeable Batteries <span class="citation">(McLaughlin, McDaniel, and Aiello 2011)</span>;</p></li>
<li><p><strong>HE</strong>: Homomorphic Encryption <span class="citation">(Busom et al. 2015; Garcia and Jacobs 2010; Erkin and Tsudik 2012)</span>;</p></li>
</ul>
<h4 id="computational-complexity">Computational Complexity</h4>
<p>Low complexity is desired mainly because most of the deployed smart meters are low-cost microcontrollers and with limited computational resources. Through the analysis of the solutions’ running time growth order, we have the complexities presented in Table [tab:complexities]. We consider that, regarding computational complexity, the noise addition and rechargeable batteries approaches stand in relation to the homomorphic encryption approaches.</p>
<table>
<caption>Complexity analysis for different privacy preserving approaches in smart metering.<span data-label="tab:complexities"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Operation</strong></td>
<td align="center">SM</td>
<td align="center">AG</td>
<td align="center">SM</td>
<td align="center">AG</td>
<td align="center">SM</td>
<td align="center">AG</td>
<td align="center">SM</td>
<td align="center">AG</td>
<td align="center">SM</td>
<td align="center">AG</td>
</tr>
<tr class="even">
<td align="left">Encryption</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center">-</td>
</tr>
<tr class="odd">
<td align="left">Decryption</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(<em>M</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center">-</td>
</tr>
<tr class="even">
<td align="left">Transmission</td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em><sup>2</sup>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center">-</td>
</tr>
<tr class="odd">
<td align="left">Sum</td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(1)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center">-</td>
</tr>
<tr class="even">
<td align="left">Product</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center">-</td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em><sup>2</sup>)</span></td>
<td align="center"><span class="math inline"><em>O</em>(<em>N</em>)</span></td>
<td align="center">-</td>
</tr>
</tbody>
</table>
<p>Legend:</p>
<ul>
<li><p><strong>NA</strong>: Noise Addition <span class="citation">(Barbosa, Brito, and Almeida 2015)</span>;</p></li>
<li><p><strong>RB</strong>: Rechargeable Batteries <span class="citation">(McLaughlin, McDaniel, and Aiello 2011)</span>;</p></li>
<li><p><strong>MEE</strong>: Modified ElGamal Encryption <span class="citation">(Busom et al. 2015)</span>;</p></li>
<li><p><strong>PESS</strong>: Paillier Encryption and Secret Sharing <span class="citation">(Garcia and Jacobs 2010)</span>;</p></li>
<li><p><strong>MPE</strong>: Modified Paillier Encryption <span class="citation">(Erkin and Tsudik 2012)</span>;</p></li>
<li><p><strong>SM</strong>: Smart Meter;</p></li>
<li><p><strong>AG</strong>: Aggregator;</p></li>
<li><p><strong>N</strong>: Number of consumption measurements;</p></li>
<li><p><strong>M</strong>: Total (aggregate) consumption value.</p></li>
</ul>



<p>Although estimation through asymptotic complexity is a good way to estimate computational complexity, we claim that experimental analysis is essential to present concrete results when comparing different proposals. Therefore, we implemented simulators<a href="#fn6" class="footnoteRef" id="fnref6"><sup>6</sup></a> in the <em>C</em> programming language. These simulators make use of a few functions from the <em>libgmp</em><a href="#fn7" class="footnoteRef" id="fnref7"><sup>7</sup></a>, <em>libpaillier</em><a href="#fn8" class="footnoteRef" id="fnref8"><sup>8</sup></a> and <em>libcrypto</em><a href="#fn9" class="footnoteRef" id="fnref9"><sup>9</sup></a> libraries to implement algorithms that mimic the protocols described in this section and in Appendix [ap:rb_he]. The simulators were executed in a machine with 1.6 GHz Intel Core i5 processor, 6 GB of RAM memory and the Ubuntu 14.04 operating system.</p>
<p>In our simulations, using different configuration scenarios (number of meters, ranging from 1 to 200) to calculate the total consumption in the region, we measured the processing time of each meter (Figure 13) and the aggregator (Figure 14).</p>

<div class="figure">
<center>
<img src="figs/SMTimeComparison.png" />
<p class="caption">Figure 13: Processing time of smart meters in 5 different privacy preserving approaches.</p>
</center>
</div>

<div class="figure">
<center>
<img src="figs/AGTimeComparison.png" />
<p class="caption">Figure 14: Processing time of the aggregator in 5 different privacy preserving approaches.</p>
</center>
</div>

<p>Each scenario was executed 10 times and the average values were considered. This amount of repetitions were enough to get precise average values. Due to the very low obtained variations, the confidence intervals are being omitted here, except for the aggregation in the approach proposed by Busom <em>et al</em>. <span class="citation">(Busom et al. 2015)</span>, which needs a trial and error mechanism to solve the discrete logarithm problem. The confidence intervals in these cases are of 95%.</p>

<p>From these measurements, we conclude that the noise addition approach and the one that uses rechargeable batteries presented very low response times, whereas the homomorphic encryption approaches presented considerable delays. It is also important to note that there are many message exchanges in the homomorphic encryption approaches, but we are not considering possible network delays in our experiments.</p>
<h4 id="cost-and-environmental-impact">Cost and Environmental Impact</h4>
<p>As mentioned, usage of rechargeable batteries can help to diminish many privacy issues. Nevertheless, it is hard to ignore the environmental effects and the costs of using batteries. Mclaughlin <em>et al</em>. <span class="citation">(McLaughlin, McDaniel, and Aiello 2011)</span> stipulate that a lead-acid battery of 50 Ah which operates at 12 V may cost approximately $100, and to achieve a typical residential nominal voltage of 120 V it is required 10 of such batteries (aprox. $1,000). The lifetime of each battery is approximately two years. Therefore, these solutions can not be considered low cost and cause a high environmental impact. Noise addition and homomorphic encryption approaches do not have these limitations.</p>
<h4 id="meters-independence-and-scalability">Meters’ Independence and Scalability</h4>
<p>In order to exchange randomly generated numbers, keys and secret shares, the homomorphic encryption protocols require communication between meters and/or the power provider. Some solutions even require a large distribution of keys and certification. For this reason, in these approaches, the meters are not independent. This overhead can be the bottleneck of the smart metering system. Hence, actually optimizing communication at the meters is a hard task that has not been fully addressed in homomorphic encryption approaches. Additionally, if one meter fails in any message exchange, the aggregation may become impossible because it requires computations using all distributed keys or secret shares. Therefore, these solutions may raise scalability issues when used in an area with a large number of meters. Noise addition and rechargeable batteries approaches do not have these limitations.</p>
<h4 id="accuracy">Accuracy</h4>
<p>As mentioned, noise addition masks the data and introduces some error in an aggregation operation. This error is controlled and usually smaller than an acceptable value. Also, allowing the enabling or disabling of masking would make errors smaller in both dimensions: for billing, since a consumer would not mask all the time, and for load monitoring in a region, since not all consumers would mask in an instant of time. However, the noise addition privacy preserving approach is still not considered one hundred percent accurate. In the case of Section [sec:noise], the use of noise will introduce errors in the billing reports. These errors tend to be cancelled over time, but there is a probability that a higher value can occur. Rechargeable batteries and homomorphic encryption approaches do not have this limitation.</p>
<h3 id="sec:discussionsmartmetering">Discussion</h3>
<p>We reviewed five solutions, one based on the use of noise addition, other based on the use of rechargeable batteries and three others based on homomorphic encryption schemes. We evaluated these approaches considering the main needed performance aspects and conclude that each solution has its advantages and disadvantages, but the noise addition stands out with relation to the others. Therefore, we choose to implement the noise addition in the LiteMe system.</p>
<p>To validate the utility, many utilities or benefits that use metering data were listed and evaluated to check whether they are still supported when using masked data. Since the noise addition approach preserves the aggregated values, the procedure to check if a feature is supported can be mapped as a checking if the feature uses only aggregated values or also uses individual values.</p>
<p>Table [tab:utilities2] presents the list from Table [tab:utilities1] but with an additional column (supported or not). The check if a utility uses only aggregated values (and thus if it is supported) can be found in the references. From the features that are not supported, “load forecasting for individual consumers” and “individual data analytics” can be considered as privacy threats that were solved. Since the approach masks the profile using noise addition, the individual demand or consumption levels are not original and the feature “demand-based rates” is not supported. Therefore, if the power provider wants to use this feature, it will see this as a limitation.</p>

<p><span>c|c|c</span> <strong>Feature / Benefit &amp;</strong></p>
<table>
<caption>Metering data utilities and the masking impact.<span data-label="tab:utilities2"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Privacy</strong></td>
</tr>
<tr class="even">
<td align="left"><strong>Risk?</strong></td>
</tr>
</tbody>
</table>
<p>&amp;<strong>Support<br />
Billing optimization <span class="citation">(Barbosa et al. 2014)</span> &amp; No &amp;<br />
Load monitoring and management for specific groups or regions <span class="citation">(Barbosa et al. 2014)</span> &amp; No &amp;<br />
Energy theft/losses detection <span class="citation">(Anas et al. 2012)</span> &amp; No &amp;<br />
Load forecasting for specific groups or regions <span class="citation">(Ilić et al. 2013)</span> &amp; No &amp;<br />
Load forecasting for individual consumers <span class="citation">(Ilić et al. 2013)</span> &amp; Yes &amp;<br />
Time-based rates (<em>e.g.</em>, different prices based on time of day and season) <span class="citation">(Barbosa et al. 2014)</span> &amp; No &amp;<br />
Demand-based rates (<em>e.g.</em> different prices based on demand levels) <span class="citation">(Procel 2011)</span> &amp; Yes &amp;<br />
Individual data analytics (<em>e.g.</em> <em>NIALM</em> and marketers) <span class="citation">(Barbosa, Brito, and Almeida 2015; NIST 2014)</span> &amp; Yes &amp;<br />
In-home feedback tools: estimated bills, device profiles etc <span class="citation">(Ying-Xun et al. 2013)</span> &amp; No &amp;<br />
</strong></p>
<p>We implemented the noise addition approach as a privacy switch in the smart meter, as presented in Figure 15. There are many components in this sensor, however the most important ones are:</p>

<ol>
<li><p><strong>ACS712</strong>: Hall-Effect-Based Linear Current Sensor. Able to measure <span class="math inline"><em>A</em><em>C</em>/<em>D</em><em>C</em></span> current up to <span class="math inline">30<em>A</em></span>.</p></li>
<li><p><strong>Switching power supply</strong>: Set as <span class="math inline">220<em>V</em></span> input and <span class="math inline">3.3<em>V</em></span> output - <span class="math inline">1<em>A</em></span>.</p></li>
<li><p><strong>CS5490</strong>: IC of power management. Two channels used for current and voltage. <span class="math inline">4<em>k</em><em>H</em><em>z</em></span> sampling rate and 24 bit resolution. Calculates powers (active, reactive and apparent), power factor, peak and RMS values.</p></li>
<li><p><strong>Voltage transformer</strong>: Set as <span class="math inline">220<em>V</em></span> primary and <span class="math inline">12<em>V</em></span> secondary.</p></li>
<li><p><strong>ESP8266</strong>: WiFi module with memory (<span class="math inline">512<em>K</em><em>B</em></span> flash storage) and processing capacity (<span class="math inline">80<em>M</em><em>H</em><em>z</em></span> CPU), GPIOs and ADC converter (not being used).</p></li>
<li><p><strong>Privacy switch</strong>: Allows enabling/disabling the data masking mechanism.</p></li>
</ol>

<div class="figure">
<center>
<img src="figs/sensor.png" alt="LiteMe sensor device." />
<p class="caption">Figure 15: LiteMe sensor device.</p>
</center>
</div>

<p>Our focus here is the privacy switch (number 6). This privacy implementation is in accordance with the privacy definition mentioned by Stallings <em>et al</em>. <span class="citation">(Stallings and Brawn 2015)</span>. When the switch is in the disabled position, the meter sends to the remote server the original power measurements. If the switch is in the enabled position, the meter sends to the remote server masked measurements. The pseudorandom number generator used in this implementation uses <span class="math inline">/<em>d</em><em>e</em><em>v</em>/<em>u</em><em>r</em><em>a</em><em>n</em><em>d</em><em>o</em><em>m</em></span>, which is considered cryptographically secure <span class="citation">(“Myths about /dev/urandom” 2018)</span>.</p>
<p>The implementation of the noise addition technique consists in an evidence of privacy. Table [tab:e2smartmetering2] describes a sheet for this evidence <span class="math inline"><em>E</em>2</span>. Since the evaluation and choice of the best evaluated techniques increase the confidence, we also have the evidence of privacy <span class="math inline"><em>E</em>3</span>, regarding the comparison of the privacy techniques, as presented in Table [tab:e3smartmetering]. The implemented noise addition approach provides differential privacy for appliances, as described in Section [sec:noise]. Therefore, there is another evidence of privacy, <span class="math inline"><em>E</em>4</span>, as described in the sheet of Table [tab:e4smartmetering].</p>

<p><span>p<span>0.7cm</span>|p<span>7.5cm</span>|p<span>1.2cm</span>|p<span>2.2cm</span>|p<span>1.2cm</span></span></p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>2</span>. Implementation of the privacy technique of noise addition.<span data-label="tab:e2smartmetering2"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>E2</strong></td>
</tr>
</tbody>
</table>
<p>&amp; &amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>2</span>. Implementation of the privacy technique of noise addition.<span data-label="tab:e2smartmetering2"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Status</strong>:</td>
</tr>
<tr class="even">
<td align="left">Done</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>2</span>. Implementation of the privacy technique of noise addition.<span data-label="tab:e2smartmetering2"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Review Date</strong>:</td>
</tr>
<tr class="even">
<td align="left">February 2015</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>2</span>. Implementation of the privacy technique of noise addition.<span data-label="tab:e2smartmetering2"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Weight</strong>:</td>
</tr>
<tr class="even">
<td align="left">8</td>
</tr>
</tbody>
</table>
<p><br />
<br />
<br />
<br />
<br />
</p>
<p><span>p<span>0.6cm</span>|p<span>8.2cm</span>|p<span>1.2cm</span>|p<span>2.2cm</span>|p<span>1.2cm</span></span></p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>3</span>. Performance evaluation of different privacy techniques.<span data-label="tab:e3smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>E3</strong></td>
</tr>
</tbody>
</table>
<p>&amp; &amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>3</span>. Performance evaluation of different privacy techniques.<span data-label="tab:e3smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Status</strong>:</td>
</tr>
<tr class="even">
<td align="left">Done</td>
</tr>
</tbody>
</table>
<p>&amp;</p>

<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>3</span>. Performance evaluation of different privacy techniques.<span data-label="tab:e3smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Review Date</strong>:</td>
</tr>
<tr class="even">
<td align="left">August 2015</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>3</span>. Performance evaluation of different privacy techniques.<span data-label="tab:e3smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Weight</strong>:</td>
</tr>
<tr class="even">
<td align="left">2</td>
</tr>
</tbody>
</table>
<p><br />
<br />
<br />
<br />
<br />
</p>

<p><span>p<span>0.7cm</span>|p<span>7.5cm</span>|p<span>1.2cm</span>|p<span>2.2cm</span>|p<span>1.2cm</span></span></p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>4</span>. Differential privacy for appliance usages.<span data-label="tab:e4smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>E4</strong></td>
</tr>
</tbody>
</table>
<p>&amp; &amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>4</span>. Differential privacy for appliance usages.<span data-label="tab:e4smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Status</strong>:</td>
</tr>
<tr class="even">
<td align="left">Done</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>4</span>. Differential privacy for appliance usages.<span data-label="tab:e4smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Review Date</strong>:</td>
</tr>
<tr class="even">
<td align="left">August 2015</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>4</span>. Differential privacy for appliance usages.<span data-label="tab:e4smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Weight</strong>:</td>
</tr>
<tr class="even">
<td align="left">8</td>
</tr>
</tbody>
</table>
<p><br />
<br />
<br />
<br />
<br />
</p>

<p>Figure 16 presents the third iteration of the construction of the <em>GSN</em> representation for this case study. The diagram now contains the representation of the evidences <span class="math inline"><em>E</em>2</span>, <span class="math inline"><em>E</em>3</span> and <span class="math inline"><em>E</em>4</span>.</p>


<div class="figure">
<center>
<img src="figs/gsn-smartmetering3.png" alt="Third iteration of the construction of the GSN representation for the privacy case of a smart metering application." />
<p class="caption">Figure 16: Third iteration of the construction of the <em>GSN</em> representation for the privacy case of a smart metering application.</p>
</center>
</div>

<h2 id="potential-attacks">Potential Attacks</h2>
<p>We evaluated three types of privacy attacks to the noise addition approach. The first is a filtering attack, based on the calculation of moving arithmetic means throughout the consumption profile. The second evaluated attack is a <em>Non-Intrusive Appliance Load Monitoring</em> (<em>NIALM</em>). Finally, the third attack is based on the hypothesis that a consumer tends to have a similar weekly behavior and, therefore, the attacker may collect the consumer’s data and calculate an expected week for this consumer.</p>
<h3 id="sec:filtering"><em>Filtering Attack</em></h3>
<p>In this section we present a filtering attack. It is based on the calculation of moving arithmetic means throughout the profile. The algorithm for the filtering attack works as follows:</p>
<ul>
<li><p>Let <span class="math inline"><em>T</em></span> be a time series, which represents the masked profile and <span class="math inline"><em>T</em><sub><em>f</em></sub></span> a new series (the resulting filtered profile).</p></li>
<li><p>The first <span class="math inline"><em>P</em></span> values from <span class="math inline"><em>T</em><sub><em>f</em></sub></span> will be equal to the first <span class="math inline"><em>P</em></span> values of <span class="math inline"><em>T</em></span> and the last <span class="math inline"><em>P</em></span> values from <span class="math inline"><em>T</em><sub><em>f</em></sub></span> will be equal to the last <span class="math inline"><em>P</em></span> values of <span class="math inline"><em>T</em></span>.</p></li>
<li><p>The value with index <span class="math inline"><em>P</em> + 1</span> from <span class="math inline"><em>T</em><sub><em>f</em></sub></span> will be the mean of the values with indexes from 1 to <span class="math inline">2<em>P</em> + 1</span> from <span class="math inline"><em>T</em></span>. The value with index <span class="math inline"><em>P</em> + 2</span> will be the mean of the values with indexes from 2 to <span class="math inline">2<em>P</em> + 2</span> from <span class="math inline"><em>T</em></span>, and so on for all remaining values. This procedure creates moveable means to eliminate the high-frequency noise.</p></li>
</ul>
<p>To analyze the attack effectiveness, we made experiments to verify if the Pearson correlation coefficient<a href="#fn10" class="footnoteRef" id="fnref10"><sup>10</sup></a> between the original profile and the masked profile is increased after the filtering. For example, using the masked profile from Figure 10, we verified if the added noise is removed and if the correlation with the original profile is increased. As presented in Table [tab:Pvalues], we made this procedure using different <span class="math inline"><em>P</em></span> values. In this example, the configuration which presented best result was <span class="math inline"><em>P</em> = 30</span>.</p>
<p>As observed in Table [tab:Pvalues], the effectiveness of filtering is increased when we increment the <span class="math inline"><em>P</em></span> value because the high frequency noise is increasingly eliminated. In fact, the correlation between the masked profile and the original profile is 0.2135, whereas filtering with <span class="math inline"><em>P</em> = 30</span> we obtain a correlation of 0.7368. In other words, we can consider that this attack has some effect on privacy. However, the attacker may not know which <span class="math inline"><em>P</em></span> value to choose and if the chosen one is greater than 30, the obtained correlation is dwindled due the filtering saturation. In this example, choosing <span class="math inline"><em>P</em></span> values greater than 30, the filter will eliminate not only the added noise, but also the original characteristics of the profile.</p>

<p><span>M<span>0.1</span>M<span>0.2</span>||M<span>0.1</span>M<span>0.2</span></span> <strong>P &amp; <strong>Correlation &amp; <strong>P &amp; <strong>Correlation<br />
0 &amp; 0.2135 &amp; 29 &amp; 0.7363<br />
2 &amp; 0.4154 &amp; 30 &amp; 0.7368<br />
4 &amp; 0.5101 &amp; 31 &amp; 0.7362<br />
8 &amp; 0.6149 &amp; 32 &amp; 0.7351<br />
16 &amp; 0.6859 &amp; 256 &amp; 0.4164<br />
</strong></strong></strong></strong></p>

<p>Experiments also showed that coarse-grained measurements (with longer time intervals) implies less filtering efficiency. This is because each measurement becomes less correlated with the adjacent measurements. For the same consumer of the previous example, the Figure 17 presents the mean of the best values of <span class="math inline"><em>P</em></span> (vertical axis) for different granularity of measurements (horizontal axis). As observed for this consumer, using measurement intervals of 36 minutes (or greater) will make filtering attacks ineffective because the best setting is using a <span class="math inline"><em>P</em></span> equals to 0 (<em>i.e</em>, no filtering). This means that with a granularity greater than or equals to 36 minutes, the original profile is more correlated with the masked profile than with the filtered profile. Therefore, after evaluating the experimental results of the filtering attack, we considered this attack as unsuccessful, and we have the evidence of privacy <span class="math inline"><em>E</em>5</span>, as presented in the sheet of Table [tab:e5smartmetering].</p>

<div class="figure">
<center>
<img src="figs/filterDifferentGranularity.png" />
<p class="caption">Figure 17: Filtering parameter (<span class="math inline"><em>P</em></span>) for different measurement granularities. The confidence intervals are of 95%.</p>
</center>
</div>

<p><span>p<span>0.7cm</span>|p<span>7.5cm</span>|p<span>1.2cm</span>|p<span>2.2cm</span>|p<span>1.2cm</span></span></p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>5</span>. Resilience to the filtering attack.<span data-label="tab:e5smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>E5</strong></td>
</tr>
</tbody>
</table>
<p>&amp; &amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>5</span>. Resilience to the filtering attack.<span data-label="tab:e5smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Status</strong>:</td>
</tr>
<tr class="even">
<td align="left">Done</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>5</span>. Resilience to the filtering attack.<span data-label="tab:e5smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Review Date</strong>:</td>
</tr>
<tr class="even">
<td align="left">June 2015</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>5</span>. Resilience to the filtering attack.<span data-label="tab:e5smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Weight</strong>:</td>
</tr>
<tr class="even">
<td align="left">3</td>
</tr>
</tbody>
</table>
<p><br />
<br />
<br />
<br />
<br />
</p>
<h3 id="sec:nialm"><em>NIALM</em></h3>
<p>We also performed some <em>NIALM</em> attacks and the results were evaluated. Figure 18 presents the workflow of this testing procedure. The noise addition approach is applied in the green task, whereas in the orange boxes, we applied the Improved <em>NIALM</em> using <em>load DIvision and Calibration</em> (<em>INDIC</em>) algorithm <span class="citation">(Batra, Dutta, and Singh 2013)</span>.</p>

<div class="figure">
<center>
<img src="figs/nialmWorkflow.png" />
<p class="caption">Figure 18: Workflow for privacy validation through <em>NIALM</em> attacks.</p>
</center>
</div>


<p>Figure 19 presents a weekly profile obtained from the popular <em>REDD</em> dataset <span class="citation">(Kolter and Johnson 2011)</span>. In this profile, there are many appliances being used, such as a microwave and a refrigerator. Figure 20 presents the real disaggregated microwave profile. A microwave was chosen as an example because in this profile it is a very characteristic appliance and one of the most difficult to be hidden (since it has many peak variations).</p>

<div class="figure">
<center>
<img src="figs/weeklyProfile.png" />
<p class="caption">Figure 19: Example week obtained from the <em>REDD</em> dataset (measurements are at each 1 minute).</p>
</center>
</div>

<div class="figure">
<center>
<img src="figs/microwave.png" />
<p class="caption">Figure 20: Real disaggregated microwave obtained from profile of Figure 19.</p>
</center>
</div>

<p>After applying the <em>INDIC</em> algorithm to perform <em>NIALM</em> on the profile from Figure 19, the appliances were disaggregated. Figure 21 presents the predicted microwave profile. As observed, this predicted profile is very similar with the real microwave profile (at least the peak moments and levels are almost the same).</p>

<div class="figure">
<center>
<img src="figs/predictedMicrowave.png" />
<p class="caption">Figure 21: Disaggregated microwave predicted by <em>INDIC</em> over profile of Figure 19.</p>
</center>
</div>

<p>We applied our noise addition approach and using an allowed error of (<span class="math inline"><em>e</em><sub><em>a</em></sub></span>) of 5% to mask the aggregated profile from Figure 19, the masked profile from Figure 22 was obtained. Because negative demand values are impossible and <em>NIALM</em> tools can not work with that, we vertically shifted the profile to perform the <em>NIALM</em> attack. This modification was simply the addition of the absolute minimum value to every measurement of the profile, i.e., <span class="math inline">∀<em>c</em> ∈ <em>P</em></span>, we made <span class="math inline"><em>c</em> = <em>c</em> + |<em>m</em><em>i</em><em>n</em>(<em>P</em>)|</span>, where <span class="math inline"><em>P</em></span> is the profile and <span class="math inline"><em>c</em></span> is an individual measurement. For the <em>NIALM</em> algorithm, this procedure should be the same as considering that an appliance which demands <span class="math inline">|<em>m</em><em>i</em><em>n</em>(<em>P</em>)|</span> was always on usage.</p>

<div class="figure">
<center>
<img src="figs/weeklyMaskedProfile.png" />
<p class="caption">Figure 22: Aggregated profile of Figure 19 masked using <span class="math inline"><em>e</em><sub><em>a</em></sub></span> of 5%.</p>
</center>
</div>

<p>After applying the same <em>INDIC</em> algorithm to perform the <em>NIALM</em>, we observed that the technique lost significantly its ability to detect appliance usages. Figure 23 presents the predicted microwave profile by the <em>INDIC</em> algorithm applied on the masked profile from Figure 22.</p>

<div class="figure">
<center>
<img src="figs/predictedMaskedMicrowave.png" />
<p class="caption">Figure 23: Disaggregated microwave predicted by <em>INDIC</em> over the masked profile of Figure 22.</p>
</center>
</div>

<p>To evaluate the potential of <em>NIALM</em> approaches in detecting appliance usages, Batra <em>et al.</em> <span class="citation">(Batra, Dutta, and Singh 2013)</span> use two metrics: <em>Mean Normalized Error</em> (<em>MNE</em>) and <em>Root Mean Square Error</em> (<em>RMS</em>). Lower values of <em>MNE</em> and <em>RMS</em> imply in better accuracy of the <em>NIALM</em>. Using different configurations, we evaluated the masking approach for the two most significant appliances of the profile from Figure 19, as presented in Table [tab:indicMNE] and Table [tab:indicRMS]. As observed, even using a high utility level and a low obfuscation (choosing a small <span class="math inline"><em>e</em><sub><em>a</em></sub></span>), the noise addition approach still affects significantly the <em>NIALM</em> potential to detect appliance usages (the <em>MNE</em> and <em>RMS</em> values are increased significantly). Therefore, we consider this attack as unsuccessful, and we have the evidence of privacy <span class="math inline"><em>E</em>6</span>, as presented in the sheet of Table [tab:e6smartmetering].</p>

<table>
<caption><em>MNE</em> values by <em>INDIC</em> using different masking configurations (no masking, masking with allowed error of 1%, 2% and 5%).<span data-label="tab:indicMNE"></span></caption>
<tbody>
<tr class="odd">
<td align="center"><strong>Appliance &amp; <strong>No Masking &amp; <span class="math inline"><em>e</em><sub><em>a</em></sub> = 1%</span> &amp; <span class="math inline"><em>e</em><sub><em>a</em></sub> = 2%</span> &amp; <span class="math inline"><em>e</em><sub><em>a</em></sub> = 5%</span><br />
Microwave &amp; 70.89 &amp; 225.69 &amp; 2976.94 &amp; 6768.89<br />
Refrigerator &amp; 28.09 &amp; 248.31 &amp; 247.59 &amp; 278.4<br />
</strong></strong></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
</tbody>
</table>

<table>
<caption><em>RMS</em> values by <em>INDIC</em> using different masking configurations (no masking, masking with allowed error of 1%, 2% and 5%).<span data-label="tab:indicRMS"></span></caption>
<tbody>
<tr class="odd">
<td align="center"><strong>Appliance &amp; <strong>No Masking &amp;<span class="math inline"><em>e</em><sub><em>a</em></sub> = 1%</span> &amp; <span class="math inline"><em>e</em><sub><em>a</em></sub> = 2%</span> &amp; <span class="math inline"><em>e</em><sub><em>a</em></sub> = 5%</span><br />
Microwave &amp; 54.16 &amp; 193.47 &amp; 649.45 &amp; 495.72<br />
Refrigerator &amp; 70.17 &amp; 143.34 &amp; 216.79 &amp; 189.67<br />
</strong></strong></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
</tbody>
</table>

<p><span>p<span>0.7cm</span>|p<span>7.5cm</span>|p<span>1.2cm</span>|p<span>2.2cm</span>|p<span>1.2cm</span></span></p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>6</span>. Resilience to the <em>NIALM</em> attack.<span data-label="tab:e6smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>E6</strong></td>
</tr>
</tbody>
</table>
<p>&amp; &amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>6</span>. Resilience to the <em>NIALM</em> attack.<span data-label="tab:e6smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Status</strong>:</td>
</tr>
<tr class="even">
<td align="left">Done</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>6</span>. Resilience to the <em>NIALM</em> attack.<span data-label="tab:e6smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Review Date</strong>:</td>
</tr>
<tr class="even">
<td align="left">June 2015</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>6</span>. Resilience to the <em>NIALM</em> attack.<span data-label="tab:e6smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Weight</strong>:</td>
</tr>
<tr class="even">
<td align="left">3</td>
</tr>
</tbody>
</table>
<p><br />
<br />
<br />
<br />
<br />
</p>

<h3 id="sec:weeklybehavior"><em>Weekly Behavior Attack</em></h3>

<p>This attack is based on the hypothesis that the consumer tends to have a similar weekly behavior (expected week). An expected week is composed by the seven expected days (from Sunday to Saturday), and an expected day is composed by the averages of each instant of time from this specific day (<em>e.g.</em>, the attacker calculates the expected Sunday from all available Sundays). Using the expected week, the attacker can try to predict the consumer behavior in future weeks. The attack effect is dependent on the amount of data available to the attacker.</p>
<p>From the CER dataset (real residential consumers of Ireland), we selected a consumer who always repeats his/her behavior and considered in our experiments. The results are presented in Table [tab:weeklybehavior]. The average Pearson correlation between masked weeks and real weeks was compared versus the average Pearson correlation between the expected week and real weeks to analyze the attack effect. We used confidence intervals with significance levels of 95%.</p>
<p>As it can be seen in Table [tab:weeklybehavior], when the number of weeks available to the attacker increases, the attack effect increases also, because the correlation between the expected week and real weeks is higher. But for our experiments, even choosing a consumer who repeats a behavior almost always and using a long period of observation (52 weeks or a full year), these correlations are less than the correlations between masked weeks and real weeks. It means that it is better to guess the consumer behavior from the own masked week than from the expected week. Therefore, we considered this attack as unsuccessful, and we have the evidence of privacy <span class="math inline"><em>E</em>7</span>, as presented in the sheet of Table [tab:e7smartmetering].</p>

<table>
<caption>Effect of the attack of the similar weekly behavior for a residential consumer.<span data-label="tab:weeklybehavior"></span></caption>
<tbody>
<tr class="odd">
<td align="center"><strong>Number of available</strong></td>
<td align="center"><strong>Average correlation between</strong></td>
<td align="center"><strong>Average correlation between</strong></td>
</tr>
<tr class="even">
<td align="center"><strong>weeks to the attacker</strong></td>
<td align="center"><strong>masked and real weeks</strong></td>
<td align="center"><strong>the expected and real weeks</strong></td>
</tr>
<tr class="odd">
<td align="center">2</td>
<td align="center">(0,499; 0,510)</td>
<td align="center">(-0,046; -0,033)</td>
</tr>
<tr class="even">
<td align="center">4</td>
<td align="center">(0,335; 0,344)</td>
<td align="center">(-0,005; 0,004)</td>
</tr>
<tr class="odd">
<td align="center">8</td>
<td align="center">(0,369; 0,374)</td>
<td align="center">(0,154; 0,166)</td>
</tr>
<tr class="even">
<td align="center">16</td>
<td align="center">(0,326; 0,331)</td>
<td align="center">(0,171; 0,180)</td>
</tr>
<tr class="odd">
<td align="center">32</td>
<td align="center">(0,436; 0,439)</td>
<td align="center">(0,182; 0,189)</td>
</tr>
<tr class="even">
<td align="center">52</td>
<td align="center">(0,432; 0,434)</td>
<td align="center">(0,316; 0,323)</td>
</tr>
</tbody>
</table>
<p><span>p<span>0.7cm</span>|p<span>7.5cm</span>|p<span>1.2cm</span>|p<span>2.2cm</span>|p<span>1.2cm</span></span></p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>7</span>. Resilience to the similar weekly behavior attack.<span data-label="tab:e7smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>E7</strong></td>
</tr>
</tbody>
</table>
<p>&amp; &amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>7</span>. Resilience to the similar weekly behavior attack.<span data-label="tab:e7smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Status</strong>:</td>
</tr>
<tr class="even">
<td align="left">Done</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>7</span>. Resilience to the similar weekly behavior attack.<span data-label="tab:e7smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Review Date</strong>:</td>
</tr>
<tr class="even">
<td align="left">June 2015</td>
</tr>
</tbody>
</table>
<p>&amp;</p>
<table>
<caption>Sheet for the evidence <span class="math inline"><em>E</em>7</span>. Resilience to the similar weekly behavior attack.<span data-label="tab:e7smartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"><strong>Weight</strong>:</td>
</tr>
<tr class="even">
<td align="left">3</td>
</tr>
</tbody>
</table>
<p><br />
<br />
<br />
<br />
<br />
</p>

<p>After performing the attacks and providing the evidences <span class="math inline"><em>E</em>5</span>, <span class="math inline"><em>E</em>6</span> and <span class="math inline"><em>E</em>7</span>, the <em>GSN</em> representation was expanded to the one presented in Figure 24.</p>

<div class="figure">
<center>
<img src="figs/gsn-smartmetering4.png" alt="Fourth iteration of the construction of the GSN representation for the privacy case of a smart metering application." />
<p class="caption">Figure 24: Fourth iteration of the construction of the <em>GSN</em> representation for the privacy case of a smart metering application.</p>
</center>
</div>

<h2 id="concluding-remarks">Concluding Remarks</h2>
<p>We validated the <em>Privacy by Evidence</em> (<em>PbE</em>) methodology through a case study of a smart metering application. Table [tab:checklistsmartmetering] shows the checklist with the collected artifacts in this case study.</p>

<table>
<caption>Checklist of the artifacts produced in the smart metering case study.<span data-label="tab:checklistsmartmetering"></span></caption>
<tbody>
<tr class="odd">
<td align="left"></td>
<td align="left">Engagement Report</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Datasets</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Summary of Norms</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Implementation of Norms</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Compliance Proofs</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Utilities List</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Perception Questionnaires</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Perception Report</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Privacy Concerns</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Adversary Model</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Privacy Policy</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Summary of Techniques</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Techniques Report</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Implementation of Techniques</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">New Utilities List</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Summary of Attacks</td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left">Attack Scripts</td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="left"></td>
<td align="left">Attacks Report</td>
<td align="center"></td>
</tr>
</tbody>
</table>

<p>Figure 24 presented the <em>GSN</em> for the privacy case of a smart metering application considering the mentioned adversary model. This representation is still to grow, according to the normal software evolution and our proposed methodology. In this application context, assuming that security assurances have been taken and thay the sensor is not an adversary, there is an argument that the privacy is being preserved according to the provided evidences. Every evidence has an identification to enable the traceability into the corresponding artifacts. There are other smart energy meter solutions such as OPower<a href="#fn11" class="footnoteRef" id="fnref11"><sup>11</sup></a> and Eyedro<a href="#fn12" class="footnoteRef" id="fnref12"><sup>12</sup></a>, however, we claim that LiteMe is the first application to consider techniques to preserve users’ privacy.</p>
<p>After validating the <em>Privacy by Evidence</em> (<em>PbE</em>) through a case study of a smart metering application, we conclude that this methodology can be regarded as an effective way to implement privacy protections mechanism. Seven privacy evidences were provided and the sum of their weights results in 28. Therefore, we positively support the research question <span class="math inline"><em>R</em><em>Q</em>1</span>. It is important to note that such mitigations must be an iterative work, and thus the stages in the methodology must happen in a constant cycle, once new risks can always be detected.</p>

<div class="footnotes">
<hr />
<ol>
<li id="fn1"><p><a href="http://liteme.com.br" class="uri">http://liteme.com.br</a><a href="#fnref1">↩</a></p></li>
<li id="fn2"><p><a href="http://www.smartiks.com" class="uri">http://www.smartiks.com</a><a href="#fnref2">↩</a></p></li>
<li id="fn3"><p>Combining appliance signatures it is possible to generate arbitrary large populations and measurement frequency. Several databases of appliance signatures are available online (<em>e.g.</em>, Tracebase <span class="citation">(Reinhardt et al. 2012)</span>).<a href="#fnref3">↩</a></p></li>
<li id="fn4"><p>ANEEL, Normative Resolution N<sup>o</sup> 502, Chapter III, Art. 7. <a href="www.aneel.gov.br/cedoc/ren2012502.pdf" class="uri">www.aneel.gov.br/cedoc/ren2012502.pdf</a><a href="#fnref4">↩</a></p></li>
<li id="fn5"><p>ANEEL, PRODIST, Module 5, Section 4.1.3.1. <a href="www.aneel.gov.br/arquivos/PDF/Modulo5_Revisao_2.pdf" class="uri">www.aneel.gov.br/arquivos/PDF/Modulo5_Revisao_2.pdf</a><a href="#fnref5">↩</a></p></li>
<li id="fn6"><p>The source codes can be found at our GitHub repository (<a href="https://git.lsd.ufcg.edu.br/pedroysb/privacy-performance-smart-metering/tree/master" class="uri">https://git.lsd.ufcg.edu.br/pedroysb/privacy-performance-smart-metering/tree/master</a>).<a href="#fnref6">↩</a></p></li>
<li id="fn7"><p><em>libgmp</em>: <a href="https://gmplib.org" class="uri">https://gmplib.org</a><a href="#fnref7">↩</a></p></li>
<li id="fn8"><p><em>libpaillier</em>: <a href="http://acsc.cs.utexas.edu/libpaillier" class="uri">http://acsc.cs.utexas.edu/libpaillier</a><a href="#fnref8">↩</a></p></li>
<li id="fn9"><p><em>libcrypto</em>: <a href="https://www.openssl.org/docs/manmaster/crypto/crypto.html" class="uri">https://www.openssl.org/docs/manmaster/crypto/crypto.html</a><a href="#fnref9">↩</a></p></li>
<li id="fn10"><p>The Pearson correlation coefficient is a measure of the linear dependence between two variables. It has a value between +1 and -1 inclusive, where 1 is total positive linear correlation, 0 is no linear correlation, and -1 is total negative linear correlation.<a href="#fnref10">↩</a></p></li>
<li id="fn11"><p>Opower, opower.com<a href="#fnref11">↩</a></p></li>
<li id="fn12"><p>Eyedro, eyedro.com<a href="#fnref12">↩</a></p></li>
</ol>
</div>

[Back to index](https://pedroysb.github.io/Privacy-by-Evidence)
