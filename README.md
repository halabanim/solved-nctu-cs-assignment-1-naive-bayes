Download Link: https://assignmentchef.com/product/solved-nctu-cs-assignment-1-naive-bayes
<br>
<h2></h2>

There are two datasets that need to be analyzed. For each dataset, you have to do the following:

<ol>

 <li>Data Input – 5%</li>

 <li>Data Visualization – 5%

  <ul>

   <li>For mushroom dataset

    <ul>

     <li>Show the data distribution by <strong>value frequency</strong> of every feature.</li>

    </ul></li>

   <li>For Iris dataset

    <ul>

     <li>Show the data distribution by <strong>average, standard deviation, and value frequency(binning might be needed)</strong> of every feature.</li>

    </ul></li>

   <li>Split data based on their labels (targets) and show the data distribution of each feature again.</li>

  </ul></li>

 <li>Data Preprocessing – 5% + (10%)

  <ul>

   <li>Drop <strong>features</strong> with any missing value.</li>

   <li>Transform data format and shape so your model can process them.</li>

   <li><strong>Shuffle the data</strong>.</li>

   <li>Bonus: any other transformation boosts the final performance. – (10%)</li>

  </ul></li>

 <li>Model Construction – 20%

  <ul>

   <li>You must construct two Naïve Bayes classifiers for the two datasets.</li>

   <li>Naïve Bayes divider <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>M</mi></math>">MM</span> in log-space:

    <ul>

     <li><span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>M</mi><mo stretchy=&quot;false&quot;>(</mo><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi mathvariant=&quot;bold&quot;>q</mi></mrow><mo stretchy=&quot;false&quot;>)</mo><mo>=</mo><munder><mi>argmax</mi><mrow><mi>Y</mi><mo>&amp;#x2208;</mo><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi mathvariant=&quot;double-struck&quot;>T</mi></mrow></mrow></munder><mrow><mo>[</mo><mi>log</mi><mo>&amp;#x2061;</mo><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo><mo>+</mo><munderover><mo>&amp;#x2211;</mo><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>m</mi></mrow></munderover><mi>log</mi><mo>&amp;#x2061;</mo><mi>P</mi><mrow><mo>(</mo><msub><mi>X</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>i</mi></mrow></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo>)</mo></mrow><mo>]</mo></mrow></math>">M(q)=argmaxY∈T[logP(Y)+∑mi=1logP(Xi|Y)]M(q)=argmaxY</span>∈T[log⁡P(Y)+∑i=1mlog⁡P(Xi|Y)]

      <ul>

       <li>where <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi mathvariant=&quot;bold&quot;>q</mi></mrow><mo>=</mo><mo fence=&quot;false&quot; stretchy=&quot;false&quot;>{</mo><msub><mi>X</mi><mn>1</mn></msub><mo>,</mo><msub><mi>X</mi><mn>2</mn></msub><mo>,</mo><mo>.</mo><mo>.</mo><mo>.</mo><mo>,</mo><msub><mi>X</mi><mi>m</mi></msub><mo fence=&quot;false&quot; stretchy=&quot;false&quot;>}</mo></math>">q={X1,X2,…,Xm}q={X1,X2,…,Xm}</span> is a sample to be predicted, whose features are <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>X</mi><mn>1</mn></msub></math>">X1X1</span> to <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>X</mi><mi>m</mi></msub></math>">XmXm</span>. <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi mathvariant=&quot;double-struck&quot;>T</mi></mrow></math>">TT</span> is the set of all possible labels.</li>

      </ul></li>

    </ul></li>

   <li>For the mushroom dataset, whose features are all <strong>categorical</strong>, <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo></math>">P(Xi|Y)P(Xi|Y)</span> must be computed with and without Laplace smoothing for result comparison. – 10%

    <ul>

     <li>Without Laplace smoothing

      <ul>

       <li><span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo><mo>=</mo><mfrac><mrow><mi>N</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo></mrow><mrow><mi>N</mi><mo stretchy=&quot;false&quot;>(</mo><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo></mrow></mfrac></math>">P(Xi|Y)=N(Xi|Y)N(Y)P(Xi|Y)=N(Xi|Y)N(Y)</span></li>

      </ul></li>

     <li>Laplace smoothing

      <ul>

       <li><span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo><mo>=</mo><mfrac><mrow><mi>N</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo><mo>+</mo><mi>k</mi></mrow><mrow><mi>N</mi><mo stretchy=&quot;false&quot;>(</mo><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo><mo>+</mo><mi>k</mi><mi>&amp;#x03C4;</mi></mrow></mfrac></math>">P(Xi|Y)=N(Xi|Y)+kN(Y)+kτP(Xi|Y)=N(Xi|Y)+kN(Y)+kτ</span>

        <ul>

         <li>where <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>&amp;#x03C4;</mi></math>">ττ</span> is the number of all possible events of feature <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>X</mi><mi>i</mi></msub></math>">XiXi</span></li>

        </ul></li>

      </ul></li>

    </ul></li>

   <li>For Iris dataset, whose features are all <strong>numerical</strong>, assume <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo></math>">P(Xi|Y)P(Xi|Y)</span> follows a 1D-Normal(Gaussian) distribution. – 10%

    <ul>

     <li><span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mi>i</mi></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo stretchy=&quot;false&quot;>)</mo><mo>=</mo><mfrac><mn>1</mn><mrow><mi>&amp;#x03C3;</mi><msqrt><mn>2</mn><mi>&amp;#x03C0;</mi></msqrt></mrow></mfrac><msup><mi>e</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo>&amp;#x2212;</mo><mfrac><mrow><mo stretchy=&quot;false&quot;>(</mo><mi>x</mi><mo>&amp;#x2212;</mo><mi>&amp;#x03BC;</mi><msup><mo stretchy=&quot;false&quot;>)</mo><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mn>2</mn></mrow></msup></mrow><mrow><mn>2</mn><msup><mi>&amp;#x03C3;</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mn>2</mn></mrow></msup></mrow></mfrac></mrow></msup></math>">P(Xi|Y)=1σ2π√e−(x−μ)22σ2P(Xi|Y)=1σ2πe−(x−μ)22σ2</span>

      <ul>

       <li>where <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>&amp;#x03BC;</mi><mo>,</mo><mi>&amp;#x03C3;</mi></math>">μ,σμ,σ</span> are the mean and standard deviation of feature <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>X</mi><mi>i</mi></msub></math>">XiXi</span> respectively, while label <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>Y</mi></math>">YY</span> is determined.</li>

      </ul></li>

    </ul></li>

  </ul></li>

 <li>Train-Test-Split – 5%

  <ul>

   <li>Two validation methods need to be implemented.</li>

  </ul></li>

</ol>

<ol>

 <li><a href="https://en.wikipedia.org/wiki/Cross-validation_(statistics)#Holdout_method">Holdout validation</a> with the ratio <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>7</mn><mo>:</mo><mn>3</mn></math>">7:37:3</span></li>

</ol>

<ol>

 <li style="list-style-type: none;">

  <ul>

   <li style="list-style-type: none;">

    <ol>

     <li><a href="https://en.wikipedia.org/wiki/Cross-validation_(statistics)#k-fold_cross-validation">K-fold cross-validation</a> with <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>K</mi><mo>=</mo><mn>3</mn></math>">K=3K=3</span>

      <ul>

       <li>Obtain the final performance by <strong>averaging</strong> all folds’ performance.</li>

      </ul></li>

    </ol></li>

  </ul></li>

 <li>Results – 10%

  <ul>

   <li>Obtain the performances of all experiment settings <strong>in tables</strong> by the following metrics:

    <ol>

     <li>Confusion matrix</li>

     <li>Accuracy</li>

     <li>Sensitivity(Recall)</li>

     <li>Precision</li>

    </ol></li>

  </ul></li>

 <li>Comparison &amp; Conclusion – 5%</li>

 <li>Questions – 25%

  <ul>

   <li>For the mushroom dataset

    <ol>

     <li>Show <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mrow><mo>(</mo><msub><mi>X</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>s</mi><mi>t</mi><mi>a</mi><mi>l</mi><mi>k</mi><mo>&amp;#x2212;</mo><mi>c</mi><mi>o</mi><mi>l</mi><mi>o</mi><mi>r</mi><mo>&amp;#x2212;</mo><mi>b</mi><mi>e</mi><mi>l</mi><mi>o</mi><mi>w</mi><mo>&amp;#x2212;</mo><mi>r</mi><mi>i</mi><mi>n</mi><mi>g</mi></mrow></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo>=</mo><mi>e</mi><mo>)</mo></mrow></math>">P(Xstalk−color−below−ring|Y=e)P(Xstalk−color−below−ring|Y=e)</span> <strong>with</strong> and <strong>without</strong> Laplace smoothing by histograms – 10%</li>

    </ol></li>

   <li>For Iris dataset

    <ol>

     <li>What are the values of <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>&amp;#x03BC;</mi></math>">μμ</span> and <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>&amp;#x03C3;</mi></math>">σσ</span> of assumed <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>p</mi><mi>e</mi><mi>t</mi><mi>a</mi><mi>l</mi><mi mathvariant=&quot;normal&quot;>&amp;#x005F;</mi><mi>l</mi><mi>e</mi><mi>n</mi><mi>g</mi><mi>t</mi><mi>h</mi></mrow></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo>=</mo><mtext>Iris Versicolour</mtext><mo stretchy=&quot;false&quot;>)</mo></math>">P(Xpetal_length|Y=Iris Versicolour)P(Xpetal_length|Y=Iris Versicolour)</span>? – 5%</li>

     <li>Use a graph to show the probability density function of assumed <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>P</mi><mo stretchy=&quot;false&quot;>(</mo><msub><mi>X</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>p</mi><mi>e</mi><mi>t</mi><mi>a</mi><mi>l</mi><mi mathvariant=&quot;normal&quot;>&amp;#x005F;</mi><mi>l</mi><mi>e</mi><mi>n</mi><mi>g</mi><mi>t</mi><mi>h</mi></mrow></msub><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mo stretchy=&quot;false&quot;>|</mo></mrow><mi>Y</mi><mo>=</mo><mtext>Iris Versicolour</mtext><mo stretchy=&quot;false&quot;>)</mo></math>">P(Xpetal_length|Y=Iris Versicolour)P(Xpetal_length|Y=Iris Versicolour)</span> – 10%</li>

    </ol></li>

  </ul></li>

 <li>Finish during class – 20%

  <ul>

   <li>Submit your report and source codes to the newE3 system before class ends.</li>

   <li>Finish time will be determined by the submission time.</li>

  </ul></li>

</ol>

<h2 data-id="Data">Data</h2>

<h3 data-id="1-Mushroom-dataset">1. Mushroom dataset</h3>

<ul>

 <li>Data can be downloaded here:

  <ul>

   <li><a href="https://archive.ics.uci.edu/ml/datasets/mushroom">https://archive.ics.uci.edu/ml/datasets/mushroom</a></li>

  </ul></li>

 <li>Please <strong>NOTE</strong> that the first column is the label (edible=e, poisonous=p)</li>

 <li>Data Set Information

  <ul>

   <li>This data set includes descriptions of hypothetical samples corresponding to 23 species of gilled mushrooms in the Agaricus and Lepiota Family (pp. 500-525). Each species is identified as definitely edible, definitely poisonous, or of unknown edibility and not recommended. This latter class was combined with the poisonous one. The Guide clearly states that there is no simple rule for determining the edibility of a mushroom; no rule like ‘‘leaflets three, let it be’’ for Poisonous Oak and Ivy.</li>

  </ul></li>

 <li>Attribute Information</li>

</ul>

<ol>

 <li>cap-shape: bell=b,conical=c,convex=x,flat=f, knobbed=k,sunken=s</li>

</ol>

<ul>

 <li style="list-style-type: none;">

  <ol>

   <li>cap-surface: fibrous=f,grooves=g,scaly=y,smooth=s</li>

   <li>cap-color: brown=n,buff=b,cinnamon=c,gray=g,green=r, pink=p,purple=u,red=e,white=w,yellow=y</li>

   <li>bruises?: bruises=t,no=f</li>

   <li>odor: almond=a,anise=l,creosote=c,fishy=y,foul=f, musty=m,none=n,pungent=p,spicy=s</li>

   <li>gill-attachment: attached=a,descending=d,free=f,notched=n</li>

   <li>gill-spacing: close=c,crowded=w,distant=d</li>

   <li>gill-size: broad=b,narrow=n</li>

   <li>gill-color: black=k,brown=n,buff=b,chocolate=h,gray=g, green=r,orange=o,pink=p,purple=u,red=e, white=w,yellow=y</li>

   <li>stalk-shape: enlarging=e,tapering=t</li>

   <li>stalk-root: bulbous=b,club=c,cup=u,equal=e, rhizomorphs=z,rooted=r, <strong>missing=?</strong></li>

   <li>stalk-surface-above-ring: fibrous=f,scaly=y,silky=k,smooth=s</li>

   <li>stalk-surface-below-ring: fibrous=f,scaly=y,silky=k,smooth=s</li>

   <li>stalk-color-above-ring: brown=n,buff=b,cinnamon=c,gray=g,orange=o, pink=p,red=e,white=w,yellow=y</li>

   <li>stalk-color-below-ring: brown=n,buff=b,cinnamon=c,gray=g,orange=o, pink=p,red=e,white=w,yellow=y</li>

   <li>veil-type: partial=p,universal=u</li>

   <li>veil-color: brown=n,orange=o,white=w,yellow=y</li>

   <li>ring-number: none=n,one=o,two=t</li>

   <li>ring-type: cobwebby=c,evanescent=e,flaring=f,large=l, none=n,pendant=p,sheathing=s,zone=z</li>

   <li>spore-print-color: black=k,brown=n,buff=b,chocolate=h,green=r, orange=o,purple=u,white=w,yellow=y</li>

   <li>population: abundant=a,clustered=c,numerous=n, scattered=s,several=v,solitary=y</li>

   <li>habitat: grasses=g,leaves=l,meadows=m,paths=p, urban=u,waste=w,woods=d</li>

  </ol></li>

</ul>

<h3 data-id="2-Iris-dataset">2. Iris dataset</h3>

<ul>

 <li>Data can be downloaded here:

  <ul>

   <li><a href="https://archive.ics.uci.edu/ml/datasets/iris">https://archive.ics.uci.edu/ml/datasets/iris</a></li>

  </ul></li>

 <li>Data Set Information

  <ul>

   <li>This is perhaps the best known database to be found in the pattern recognition literature. Fisher’s paper is a classic in the field and is referenced frequently to this day. (See Duda &amp; Hart, for example.) The data set contains 3 classes of 50 instances each, where each class refers to a type of iris plant. One class is linearly separable from the other 2; the latter are NOT linearly separable from each other. Predicted attribute: class of iris plant. This is an exceedingly simple domain.</li>

  </ul></li>

 <li>Attribute Information</li>

</ul>

<ul>

 <li style="list-style-type: none;">

  <ol>

   <li>sepal length in cm</li>

   <li>sepal width in cm</li>

   <li>petal length in cm</li>

   <li>petal width in cm</li>

   <li>class:

    <ul>

     <li>Iris Setosa</li>

     <li>Iris Versicolour</li>

     <li>Iris Virginica</li>

    </ul></li>

  </ol></li>

</ul>