![Nonlinear PCA](http://www.nlpca.org/fig_nlpca_nonlinear_PCA_autoencoder_3d_small.png "Nonlinear PCA")

# Nonlinear PCA toolbox for Matlab #

[Nonlinear principal component analysis (NLPCA)](http://www.nlpca.org/) based on auto-associative neural networks (autoencoder).

### Syntax ###

```
[pc, net] = nlpca(data, k)

pc = nlpca_get_components(net, data)
data_reconstruction = nlpca_get_data(net, pc)
```

### Description ###

`pc = nlpca(data,k)` extracts k nonlinear components from the data set. `pc` represents the estimated component values (scores).

`net` is a data structure explaining the neural network parameters for the nonlinear transformation from data space to component space and reverse.

`net` can be used in `nlpca_get_components` and `nlpca_get_data` to obtain component values (scores) for new data or reconstructed data for any component value. 

### Example ###

Nonlinear PCA (circular PCA) applied to artificial data of a noisy circle.

```
% generate circular data
t=linspace(-pi , +pi , 100);  % angular value t=-pi,...,+pi
data = [sin(t);cos(t)];       % circle
data = data + 0.2*randn(size(data));    % add noise

% nonlinear PCA (circular PCA, inverse network architecture)
[pc,net]=nlpca(data, 1,  'type','inverse',  'circular','yes' );
              
% plot components
nlpca_plot(net)
```

### Demos ###

* `demo_hierarchical_NLPCA_StarData.m` demo of hierarchical nonlinear PCA
* `demo_circular_PCA.m` 	demo of circular units (Circular PCA)
* `demo_inverse_NLPCA.m` 	demo of inverse network architecture
* `demo_missing_data.m` 	demo of missing data estimation


### Download ###
* [Latest Version](https://github.com/matthias-scholz/nonlinear-pca/archive/master.zip)
```
wget https://github.com/matthias-scholz/nonlinear-pca/archive/master.zip
```

### Help ###
* [Frequently Asked Questions (FAQ)](http://faq.nlpca.org/)


### References ###

If you use this toolbox in a publication, please cite one of these articles.

 *  [Non-linear PCA: a missing data approach.](http://bioinformatics.oxfordjournals.org/content/21/20/3887.full)
    Matthias Scholz, Fatma Kaplan, Charles L. Guy, Joachim Kopka, and Joachim Selbig.
    Bioinformatics 21(20):3887-3895. 2005.
    
 *  [Nonlinear principal component analysis: neural network models and applications.](http://pca.narod.ru/2MainGorbanKeglWunschZin.pdf)
    Matthias Scholz, Martin Fraunholz, and Joachim Selbig.
    In Principal Manifolds for Data Visualization and Dimension Reduction, edited by Alexander N. Gorban, Balazs Kegl, Donald C. Wunsch, and Andrei Zinovyev. Volume 58 of LNCSE, pages 44-67. Springer Berlin Heidelberg, 2007.
   
 *  [Validation of nonlinear PCA.](http://www.matthias-scholz.de/scholz_NLPCA_validation_NeuralProcessLett2012.pdf)
    Matthias Scholz
    Neural Processing Letters, Volume 36, Number 1, Pages 21-30, 2012.
   
 *  [Nonlinear PCA: a new hierarchical approach.](http://www.matthias-scholz.de/scholz_vigario_NLPCA_esann2002.pdf)
    Matthias Scholz and Ricardo Vigario.
    In M. Verleysen, editor, Proceedings ESANN. 2002.
  
  * [Analysing periodic phenomena by circular PCA.](http://www.matthias-scholz.de/scholz_circularPCA_BIRD2007.pdf)
    Matthias Scholz.
    In S. Hochreiter and R. Wagner, editors, Proceedings of the Conference on Bioinformatics Research and Development BIRD'07, LNCS/LNBI Vol. 4414, pages 38-47. Springer-Verlag Berlin Heidelberg, 2007.
