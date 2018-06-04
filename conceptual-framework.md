[Back to index](https://pedroysb.github.io/Privacy-by-Evidence)

# Conceptual Framework

<p>In this section we describe the key concepts when dealing with privacy. The goal is to generate a manageable knowledge that is used in our proposed methodology. The conceptual framework with the key concepts identified by us is presented in Figure [fig:conceptualFramework]. We describe these concepts in the next sections.</p>
<div class="figure">
<img src="figs/conceptualFramework.png" alt="Key concepts when dealing with privacy." />
<p class="caption">Key concepts when dealing with privacy.<span data-label="fig:conceptualFramework"></span></p>
</div>
<h2 id="participants">Participants</h2>
<p>Figure [fig:participants] presents the possible participants/stakeholders in a typical scenario when developing a privacy-friendly application. They are:</p>
<ul>
<li><p><em>User</em>: The user of the application. Software and sensors may collect sensitive data from the user and transmit to remote servers.</p></li>
<li><p><em>Product Owner</em>: Entity that represents the executives. Initiates the project, finances it, contracts it out, and benefits from its output(s). Part of an owner responsibility is to have a vision of the requirements, and convey that vision to the development team.</p></li>
<li><p><em>Development Team</em>: Responsible for developing and delivering the project in accordance to the requirements (including data privacy and utility requirements).</p></li>
<li><p><em>Regulatory Agency</em>: Responsible for exercising autonomous authority and establishing privacy guidelines and rules. These preventive rules combined with penalty mechanisms can help preventing potentially dangerous activities.</p></li>
<li><p><em>Privacy Engineer</em>: Responsible for risk analysis, development and evaluation of privacy techniques, provision of evidences, simulation of attacks and assurance that the privacy norms established by the regulatory agencies are being followed.</p></li>
<li><p><em>Adversary</em>: Entity which seeks to violate the users privacy obtaining sensitive information. May perform many attacks depending on the application context, data format and privacy techniques.</p></li>
<li><p><em>Data Recipient</em>: Third party who is interested in the published data and may conduct data analysis in sensitive data.</p></li>
</ul>
<div class="figure">
<img src="figs/participants.png" alt="Possible participants when developing a privacy-friendly application." />
<p class="caption">Possible participants when developing a privacy-friendly application.<span data-label="fig:participants"></span></p>
</div>
<p>The application environment contains the building blocks of the system, such as sensors, servers, service APIs and databases. It may collect the data from users and publish to third parties or the public. A typical scenario of data collection and publishing is, for example, in health care. Through smart health devices, a hospital collects data from patients and publishes these records to an external medical center. In this example, the devices and the hospital are in the application environment, patients are users, and the medical center is the data recipient. The data analysis conducted at the medical center could be any task from a simple count of the number of men with diabetes to a sophisticated cluster analysis to make health insurances more profitable.</p>
<p>An adversary model may consider that the data recipient is untrusted. If the environment is trusted and users are willing to provide their personal information, there may be still a problem if the trust is transitive, <em>i.e.</em>, the data recipient be untrusted. In practice, different contexts may have different adversary assumptions and requirements.</p>
<h2 id="application-context">Application Context</h2>
<p>In different application contexts, the privacy and utility requirements may differ. Smart energy meters, social networks, geolocation systems, finance, and medical applications are some examples of application contexts. The identification of the context is essential, since different utilities can be provided when processing the data. More importantly, different application contexts can be target of different attacks and privacy violations, and therefore, the usage of different privacy protection techniques is required.</p>
<h2 id="data-format">Data Format</h2>
<p>In order to provide their features more precisely and specific for each individual, applications may collect large amounts of data. This data can exist in different formats; table records, time series, network traffic, graphs, text, images, among many others. The format in which the data is presented usually is related to the application context and different privacy protection techniques may be applied to different data formats.</p>
<h2 id="data-sensitivity">Data Sensitivity</h2>
<p>In the most basic form, a data unit may be or contain one of the following:</p>
<ul>
<li><p><strong>Explicit Identifier</strong>: Set of attributes, such as name, email, phone number and IP address, containing information that explicitly identifies users.</p></li>
<li><p><strong>Quasi Identifier</strong>: Set of attributes that could potentially identify users such as ZIP code, sex and date of birth. We call <span class="math inline"><em>Q</em><em>I</em><em>D</em></span> the set of attributes and <span class="math inline"><em>q</em><em>i</em><em>d</em></span> the values of this set.</p></li>
<li><p><strong>Sensitive</strong>: Consist of sensitive person-specific information such as disease, energy consumption, salary, and disability status.</p></li>
<li><p><strong>Non-Sensitive</strong>: Consist of all information that do not fall into the previous three categories.</p></li>
</ul>
<p>More importantly, the sensitive data also possess different sensitivity levels (<em>e.g.</em>, low, medium and high). There are some standards of classification of sensitive data <span class="citation">(Stweart, Chapple, and Gibson 2015)</span>, however, in practice, the classification depends on the context and population. Improper collection and usage of sensitive data may be a privacy violation.</p>
<h2 id="sec:norms">Privacy Norms and Legislation</h2>
<p>Establishing norms to restrict the usage of sensitive data is one of the preventive methods for privacy protection. Preventive norms combined with punishing mechanisms (such as reporting violations to authorities) can help preventing potentially dangerous activities. Many regulatory agencies have proposed privacy norms that must be followed.</p>
<p>As an example, the <em>HIPAA</em> (<em>Health Insurance Portability and Accountability Act</em>) <span class="citation">(<em>Guidance Regarding Methods for De-identification of Protected Health Information in Accordance with The Health Insurance Portability and Accountability Act (HIPAA), Privacy Rule</em> 2012)</span> established the <em>Safe Harbor</em> standard, which is a precise method for anonymization of health information. It stipulates the removal or generalization of 18 variables from a data set:</p>
<ol>
<li><p>Names;</p></li>
<li><p>All geographic subdivisions smaller than a state, including street address, city, county, precinct, ZIP code, and their equivalent geocodes, except for the initial three digits of a ZIP code if, according to the current publicly available data from the Bureau of the Census:</p>
<ol style="list-style-type: lower-alpha">
<li><p>The geographic unit formed by combining all ZIP codes with the same three initial digits contains more than 20,000 people.</p></li>
<li><p>The initial three digits of a ZIP code for all such geographic units containing 20,000 or fewer people is changed to 000.</p></li>
</ol></li>
<li><p>All elements of dates (except year) for dates directly related to an individual, including birth date, admission date, discharge date, and date of death; and all ages over 89 and all elements of dates (including year) indicative of such age, except that such ages and elements may be aggregated into a single category of age 90 or older;</p></li>
<li><p>Telephone numbers;</p></li>
<li><p>Fax numbers;</p></li>
<li><p>Electronic mail addresses;</p></li>
<li><p>Social security numbers;</p></li>
<li><p>Medical record numbers;</p></li>
<li><p>Health plan beneficiary numbers;</p></li>
<li><p>Account numbers;</p></li>
<li><p>Certificate/ license numbers;</p></li>
<li><p>Vehicle identifiers and serial numbers, including license plate numbers;</p></li>
<li><p>Device identifiers and serial numbers;</p></li>
<li><p>Web universal resource locators (URLs);</p></li>
<li><p>Internet protocol (IP) address numbers;</p></li>
<li><p>Biometric identifiers, including finger and voice prints;</p></li>
<li><p>Full face photographic images and any comparable images;</p></li>
<li><p>Any other unique identifying number, characteristic, or code.</p></li>
</ol>
<p>The certainty and simplicity of <em>Safe Harbor</em> makes it quite attractive for health information custodians when disclosing data without patient consent, and it is used quite often in practice <span class="citation">(Emam 2013)</span>.</p>
<p>Another regulation is the <em>GDPR</em> (<em>General Data Protection Regulation</em>) <span class="citation">(“The EU General Data Protection Regulation (GDPR)” 2018)</span>, which became enforceable in the European Union on 25 May 2018. The aim of the <em>GDPR</em> is to “protect all European citizens from privacy and data breaches”, and has the following key points:</p>
<ul>
<li><p><em>Territorial Scope</em>: The <em>GDPR</em> applies to the processing of personal data of Europen ciyizens by controllers and processors, regardless their locations;</p></li>
<li><p><em>Penalties</em>: Organizations in breach of <em>GDPR</em> can be imposed for the infringements;</p></li>
<li><p><em>Consent</em>: Users consent must be clear and distinguishable from other matters and provided in an intelligible and easily accessible form, using clear and plain language.</p></li>
</ul>
<p>Beyond the key points, <em>GDPR</em> stipulates <em>Privacy by Design</em> as a legal requirement during the development, and the European citizens have the following rights: the right to be notified when a data breach occurs, the right to access their data (and in a portable format), the right to be forgotten, and the right to restriction of processing.</p>
<p>Unfortunately, norms or regulations such as <em>GDPR</em> and <em>HIPAA</em> usually are not enough to guide developers in developing privacy-friendly applications. This is why the provision of concrete evidences of privacy and the implementation of other counter-measures such as conducting privacy perception studies, implementing privacy techniques, and evaluating potential attacks, become necessary.</p>
<h2 id="users-perception-of-privacy">Users Perception of Privacy</h2>
<p>Different people usually exhibit different perceptions of privacy, <em>i.e.</em>, they associate the word privacy with a diversity of meanings. For example, some people believe that privacy is the right to control what information about them may be made public <span class="citation">(Mekovec 2010; Yao, Rice, and Wallis 2007)</span>. Other people believe that if someone cares about privacy is because he/she is involved in wrongdoing <span class="citation">(Beckwith 2003)</span>.</p>
<p>Different perceptions of privacy originate different types of concerns about privacy. For example, some people tend to provide the information requested by the system only if it presents a privacy policy. Privacy policy is a legal document and software artifact that fulfills a legal requirement to protect the user privacy. It answers important questions about the software’s operation, including what personal identifiable information is collected, for what purpose is it used, and with whom is it shared <span class="citation">(Bhatia, Breaux, and Schaub 2016)</span>.</p>
<p>The application of surveys and/or the conduction of interviews may cover and help to understand many privacy aspects, such as: (i) general perceptions, beliefs and attitudes; (ii) perceptions about data collection and control; (iii) perceptions about information inference; (iv) perception about information usage; and (v) perceptions about possibilities of data exchange (not only leakage) <span class="citation">(Ponciano et al. 2017)</span>.</p>
<h2 id="sec:techniques">Privacy Techniques</h2>
<p>The raw data usually does not satisfy specified privacy requirements and it must be modified before the disclosure. The modification is done by applying privacy techniques which may come in several flavors, like anonymization <span class="citation">(Dalenius 1986)</span>, generalization <span class="citation">(Sweeney 2002)</span>, noise addition <span class="citation">(Barbosa et al. 2014)</span>, zero-knowledge proofs <span class="citation">(Gehrke, Lui, and Pass 2011)</span> and the usage of homomorphic encryption <span class="citation">(Lauter, Naehrig, and Vaikuntanathan 2011)</span>. As an example, anonymization refers to the approach that seeks to hide the identity of users, assuming that sensitive data must be retained for data analysis. Clearly, explicit identifiers of users must be removed.</p>
<p>Several techniques may work for the same context and data format. The objective of such techniques is to protect sensitive user data from possible privacy violations. It may also include the provision of the control of what information may be disclosed to the service, data recipients or other users.</p>
<h2 id="attacks">Attacks</h2>
<p>A privacy attack is an attempt to expose, steal or gain unauthorized access to sensitive data. Unfortunately, applying norms and privacy techniques may not be enough and real attackers may have success in violating the user privacy when exploiting flaws in the norms and privacy techniques. Thus, before the deployment of the application, privacy engineers may simulate attacks, seeking to explore and fix additional privacy breaches. Attack simulation reports may also assess potential impacts to the organization and suggest countermeasures to reduce risks.</p>
<p>As an example of attack, even with all explicit identifiers removed, an individual’s name in a public voter list may be linked with his record in a published medical database through the combination of ZIP code, date of birth, and sex, as shown in Figure [fig:linkingAttack]. Each of these attributes does not uniquely identify a user, but their combination, called the quasi-identifier (<span class="math inline"><em>q</em><em>i</em><em>d</em></span> value), often singles out a unique or a small number of users. Research showed that 87% of the U.S. population had reported characteristics that made them unique based on only such quasi-identifiers <span class="citation">(Sweeney 2000)</span>.</p>
<div class="figure">
<embed src="figs/linkingAttack.pdf" />
<p class="caption">Linking attack to re-identify users <span class="citation">(Sweeney 2002)</span>.<span data-label="fig:linkingAttack"></span></p>
</div>
<p>In the example of Figure [fig:linkingAttack], the user is re-identified by linking his <span class="math inline"><em>q</em><em>i</em><em>d</em></span>. To perform such linking attacks, the attacker needs two pieces of prior knowledge: the victim’s record in the released data and the <span class="math inline"><em>q</em><em>i</em><em>d</em></span> of the victim. Such knowledge can be obtained by observations. For example, the attacker noticed that his boss was hospitalized, and, therefore, knew that his boss’s medical record would appear in the released patient database. In another example, it is not difficult for an adversary to obtain his boss’s ZIP code, date of birth, and sex, which could serve as the quasi-identifier in linking attacks.</p>
<p>Besides linking attacks, other examples of attacks may include filtering (when applying noise addition techniques), integer factorization and discrete logarithm computation (when applying homomorphic encryption, for example), and side-channel attacks.</p>
<h2 id="privacy-models">Privacy Models</h2>
<p>To prevent attacks such as linkage through quasi-identifiers and to quantify the privacy levels, it is necessary to validate the privacy technique using formal privacy models. Sweeney <em>et al</em>. <span class="citation">(Sweeney 2000)</span> propose the notion of <span class="math inline"><em>k</em></span>-anonymity: If one user has some value <span class="math inline"><em>q</em><em>i</em><em>d</em></span>, at least <span class="math inline"><em>k</em> − 1</span> other records also have the value <span class="math inline"><em>q</em><em>i</em><em>d</em></span>. In other words, the minimum equivalence group size on <span class="math inline"><em>Q</em><em>I</em><em>D</em></span> is at least <span class="math inline"><em>k</em></span>. A data set satisfying this requirement is called <span class="math inline"><em>k</em></span>-anonymous. In a <span class="math inline"><em>k</em></span>-anonymous data set, each user is indistinguishable from at least <span class="math inline"><em>k</em> − 1</span> other records with respect to <span class="math inline"><em>Q</em><em>I</em><em>D</em></span>. Consequently, the probability of linking a victim to a specific user through <span class="math inline"><em>Q</em><em>I</em><em>D</em></span> is at most <span class="math inline">1/<em>k</em></span>.</p>
<p>Another insightful privacy model is the <span class="math inline"><em>ϵ</em></span>-differential privacy: the risk to the user’s privacy should not substantially increase as a result of participating in a statistical database. Dwork <span class="citation">(Dwork 2006)</span> proposes to compare the risk with and without the user’s data in the published data. Consequently, the privacy model called <span class="math inline"><em>ϵ</em></span>-differential privacy ensures that the removal or addition of a single element does not significantly affect the outcome of any analysis.</p>
<p>Considering a data set as a set of participants, we say data sets <span class="math inline"><em>D</em>1</span> and <span class="math inline"><em>D</em>2</span> differ in at most one element if one is a proper subset of the other and the larger data set contains just one additional participant. Therefore, a randomized function <span class="math inline"><em>F</em></span> gives <span class="math inline"><em>ϵ</em></span>-differential privacy if for all data sets <span class="math inline"><em>D</em>1</span> and <span class="math inline"><em>D</em>2</span> differing on at most one element, and all <span class="math inline"><em>S</em> ⊆ <em>R</em><em>a</em><em>n</em><em>g</em><em>e</em>(<em>F</em>)</span>, <span class="math inline"><em>P</em><em>r</em>[<em>F</em>(<em>D</em>1)∈<em>S</em>]≤<em>e</em><em>x</em><em>p</em>(<em>ϵ</em>)×<em>P</em><em>r</em>[<em>F</em>(<em>D</em>2)∈<em>S</em>]</span>, where the probability is taken over the randomness of function <span class="math inline"><em>F</em></span> <span class="citation">(Dwork 2006)</span>.</p>
<p>The <span class="math inline"><em>ϵ</em></span> value is the privacy metric and for better privacy, a small value is desirable. A mechanism <span class="math inline"><em>F</em></span> satisfying this definition addresses concerns that any participant might have about the leakage of his personal information: even if the participant removed his data from the data set, no outputs (and thus consequences of outputs) would become significantly more or less likely.</p>
<p>Differential privacy is achieved by the addition of noise whose magnitude is a function of the largest change a single user could have on the output to the query function; this quantity is referred as the sensitivity of the function.</p>
<p>Besides <span class="math inline"><em>k</em></span>-anonymity and <span class="math inline"><em>ϵ</em></span>-differential privacy, there are many other privacy models, as presented in Table [tab:privacyModels]. The privacy model to use depends on the attack model, application context, data format, privacy technique, and other factors.</p>
<table>
<caption>Privacy Models <span class="citation">(Fung et al. 2010)</span>. A tick represents the coverage of an attack model.<span data-label="tab:privacyModels"></span></caption>
<tbody>
<tr class="odd">
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center"></td>
<td align="center">Record</td>
<td align="center">Attribute</td>
<td align="center">Table</td>
<td align="center">Probabilistic</td>
</tr>
<tr class="odd">
<td align="center"></td>
<td align="center">linkage</td>
<td align="center">linkage</td>
<td align="center">linkage</td>
<td align="center">attack</td>
</tr>
<tr class="even">
<td align="center"><span class="math inline"><em>k</em></span>-Anonymity <span class="citation">(Sweeney 2002)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center">MultiR <span class="math inline"><em>k</em></span>-Anonymity <span class="citation">(M. E. Nergiz, Clifton, and Nergiz 2009)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center"><span class="math inline"><em>l</em></span>-Diversity <span class="citation">(Machanavajjhala et al. 2007)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center">Confidence Bounding <span class="citation">(Wang, Fung, and Yu 2007)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center">(<span class="math inline"><em>a</em></span>, <span class="math inline"><em>k</em></span>)-Anonymity <span class="citation">(Wong et al. 2006)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center">(<span class="math inline"><em>X</em></span>, <span class="math inline"><em>Y</em></span>)-Privacy <span class="citation">(Wang and Fung 2006)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center">(<span class="math inline"><em>k</em></span>, <span class="math inline"><em>e</em></span>)-Anonymity <span class="citation">(Koudas et al. 2007)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center">(<span class="math inline"><em>ϵ</em></span>, <span class="math inline"><em>m</em></span>)-Anonymity <span class="citation">(Li, Tao, and Xiao 2008)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center">Personalized Privacy <span class="citation">(Xiao and Tao 2006)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center"><span class="math inline"><em>t</em></span>-Closeness <span class="citation">(Ninghui, Tiancheng, and Venkatasubramanian 2007)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center"><span class="math inline"><em>δ</em></span>-Presence <span class="citation">(M. E. Nergiz, Clifton, and Nergiz 2009)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center">(<span class="math inline"><em>c</em></span>, <span class="math inline"><em>t</em></span>)-Isolation <span class="citation">(Chawla et al. 2005)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center"><span class="math inline"><em>ϵ</em></span>-Differential Privacy <span class="citation">(Dwork 2006)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="odd">
<td align="center">(<span class="math inline"><em>d</em></span>, <span class="math inline"><em>γ</em></span>)-Privacy <span class="citation">(Rastogi, Suciu, and Hong 2007)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr class="even">
<td align="center">Distributional Privacy <span class="citation">(Blum, Ligett, and Roth 2008)</span></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
<td align="center"></td>
</tr>
</tbody>
</table>
<h2 id="data-utility">Data Utility</h2>
<p>We consider data utility as the usefulness of the data for the achievement of the primary features of the application. A <em>utility metric</em> may measure the quality and the business value attributed to data within specific usage contexts.</p>
<p>In the previous sections, we presented only concepts regarding privacy. However, regarding utility, in order to provide their features more precisely and specific for each individual, applications may collect a large of data which may be useful for many purposes. Privacy preventive measures may have the potential to limit the data utility, or even prevent the operation of some feature. Thus, we are facing a Utility vs. Privacy trade-off. In the development of an application, it is necessary to ensure that the privacy of the users will not be compromised and still allow the largest possible number of the services keep functioning.</p>
<h2 id="security">Security</h2>
<p>Despite the focus in privacy, it is necessary to notice the fact that the security of the system is also vitally important. It is known that privacy is a sub-area of security, more specifically, in confidentiality. In fact, it is very common to see even professionals of Information Technology mixing the concepts between security and privacy. However, more recently, research on privacy are taking different directions than research on security. For example, data analysis for infering human behavior is considered a hot topic in privacy, whereas software vulnerabilities is a hot topic in security.</p>
<p>A system with security vulnerabilities transitively compromises the data privacy and if an attacker seizes control of the application, the privacy will be at risk. To address these concerns, it is necessary the inclusion of practices used in security assurance methodologies, such as the execution of penetration testing to detect vulnerabilities in the involved elements. To ensure that privacy is present in the whole communication process, it is necessary to take preventive security measures, such as encrypting the data in transit and using signed certificates to avoid man-in-the-middle attacks (MiTM) <span class="citation">(Stallings and Brawn 2015)</span>.</p>
