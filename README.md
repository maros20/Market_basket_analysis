# Transactional analysis of a computer store
The code presented in this project performs an analysis of electronic product sales transactions from two companies: Electronidex and Blackwell. 
The goal of the analysis is to identify improvement opportunities for Blackwell.

- The first step in the analysis is to conduct an exploration of the data. It is observed that the two companies use different product categories, 
  so they are unified. The 22 categories that match or are similar in both companies are selected.

- Next, association rules between product categories are calculated. These rules identify products that are commonly purchased together.

- Finally, transactions are segmented into two groups: B2B (business-to-business) and B2C (business-to-consumer). 
  The segmentation is based on the number of products from each category purchased in each transaction.

- Key results of the analysis:
  
  The best-selling product categories in both companies are laptops, monitors, and accessories.
  The most important association rules identify products that are often bought together, such as laptops and monitors, or printers and printer ink.
  B2B transactions tend to be larger than B2C transactions.

Product Sugestion Function:
The function Product_suggestion is a tool that allows suggesting complementary products to those the user is interested in purchasing. The function operates as follows:

The user enters the consumer type (business or consumer) and the product they wish to purchase.
The function verifies that the product is in the list of available products.
If the product is valid, the function generates a list of complementary products based on association rules.
The function displays to the user the list of complementary products, along with information about lift, confidence, and support of the association rules.
The Product_suggestion function is a useful tool for enhancing users' shopping experience. By suggesting complementary products, 
the function helps users discover new items that may be of interest to them.

Example of use:

Let's assume a user is interested in buying a laptop. The user enters the consumer type (consumer) and the product (iMac). 
The function verifies that the product is in the list of available products and generates a list of complementary products. 
Example:
Product_suggestion()
Escoga entre Empresa o Consumidor: Empresa
Categoria compra:  Empresa 
Que producto desea comprar?HP Laptop
Productos encontrados:  HP Laptop 
Otros usuarios que han comprado HP Laptop también han comprado:    items                                            
[1] {Logitech Desktop MK120 Mouse and keyboard Combo}
[2] {Google Home}                                    
[3] {HP Black & Tri-color Ink}                       
[4] {Mackie CR Speakers}                             
[5] {Gaming Mouse Professional}                      
    lhs            rhs                                               support     confidence coverage  lift     count
[1] {HP Laptop} => {Logitech Desktop MK120 Mouse and keyboard Combo} 0.008563477 0.02602472 0.3290516 1.665226 40   
[2] {HP Laptop} => {Google Home}                                     0.008349390 0.02537411 0.3290516 1.646145 39   
[3] {HP Laptop} => {HP Black & Tri-color Ink}                        0.015842432 0.04814574 0.3290516 1.641524 74   
[4] {HP Laptop} => {Mackie CR Speakers}                              0.008135303 0.02472349 0.3290516 1.626527 38   
[5] {HP Laptop} => {Gaming Mouse Professional}                       0.003425391 0.01040989 0.3290516 1.519519 16   
[1] "Gracias por su visita"
