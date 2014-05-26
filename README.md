# Nonlinear PCA toolbox for Matlab #

[Nonlinear principal component analysis (NLPCA)](http://www.nlpca.org/) based on auto-associative neural networks (autoencoder).

### Syntax ###

`[pc, net] = nlpca(data, k)`

`pc = nlpca_get_components(net, data)`

`data_reconstruction = nlpca_get_data(net, pc)`


### Description ###

`pc = nlpca(data,k)` extracts k nonlinear components from the data set. `pc` represents the estimated component values (scores).

`net` is a data structure explaining the neural network parameters for the nonlinear transformation from data space to component space and reverse.

`net` can be used in `nlpca_get_components` and `nlpca_get_data` to obtain component values (scores) for new data or reconstructed data for any component value. 

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Cite ###

If you use this code in a publication, please cite one of these articles.

 *  [Non-linear PCA: a missing data approach.](http://bioinformatics.oxfordjournals.org/content/21/20/3887.full)
    Matthias Scholz, Fatma Kaplan, Charles L. Guy, Joachim Kopka, and Joachim Selbig.
    Bioinformatics 21(20):3887-3895. 2005.
    
 *  [Nonlinear principal component analysis: neural network models and applications.](http://pca.narod.ru/2MainGorbanKeglWunschZin.pdf)
    Matthias Scholz, Martin Fraunholz, and Joachim Selbig.
    In Principal Manifolds for Data Visualization and Dimension Reduction, edited by Alexander N. Gorban, Balázs Kégl, Donald C. Wunsch, and Andrei Zinovyev. Volume 58 of LNCSE, pages 44-67. Springer Berlin Heidelberg, 2007.
   
 *  [Validation of nonlinear PCA.](http://www.matthias-scholz.de/scholz_NLPCA_validation_NeuralProcessLett2012.pdf)
    Matthias Scholz
    Neural Processing Letters, Volume 36, Number 1, Pages 21-30, 2012.
   
 *  [Nonlinear PCA: a new hierarchical approach.](http://www.matthias-scholz.de/scholz_vigario_NLPCA_esann2002.pdf)
    Matthias Scholz and Ricardo Vigário.
    In M. Verleysen, editor, Proceedings ESANN. 2002.
  

  * [Analysing periodic phenomena by circular PCA.](http://www.matthias-scholz.de/scholz_circularPCA_BIRD2007.pdf)
    Matthias Scholz.
    In S. Hochreiter and R. Wagner, editors, Proceedings of the Conference on Bioinformatics Research and Development BIRD'07, LNCS/LNBI Vol. 4414, pages 38-47. Springer-Verlag Berlin Heidelberg, 2007.