# Homework 1

```unix
MARCCAM-M-618J:data Computer$ head chipotle.tsv
order_id quantity item_name choice_description item_price
1 1 Chips and Fresh Tomato Salsa NULL $2.39
1 1 Izze [Clementine] $3.39
1 1 Nantucket Nectar [Apple] $3.39
1 1 Chips and Tomatillo-Green Chili Salsa NULL $2.39
2 2 Chicken Bowl [Tomatillo-Red Chili Salsa (Hot), [Black Beans, Rice, Cheese, Sour Cream]] $16.98
3 1 Chicken Bowl [Fresh Tomato Salsa (Mild), [Rice, Cheese, Sour Cream, Guacamole, Lettuce]] $10.98
3 1 Side of Chips NULL $1.69
4 1 Steak Burrito [Tomatillo Red Chili Salsa, [Fajita Vegetables, Black Beans, Pinto Beans, Cheese, Sour Cream, Guacamole, Lettuce]] $11.75
4 1 Steak Soft Tacos [Tomatillo Green Chili Salsa, [Pinto Beans, Cheese, Sour Cream, Lettuce]] $9.25
```

```unix
MARCCAM-M-618J:data Computer$ tail chipotle.tsv
1831 1 Carnitas Bowl [Fresh Tomato Salsa, [Fajita Vegetables, Rice, Black Beans, Cheese, Sour Cream, Lettuce]] $9.25
1831 1 Chips NULL $2.15
1831 1 Bottled Water NULL $1.50
1832 1 Chicken Soft Tacos [Fresh Tomato Salsa, [Rice, Cheese, Sour Cream]] $8.75
1832 1 Chips and Guacamole NULL $4.45
1833 1 Steak Burrito [Fresh Tomato Salsa, [Rice, Black Beans, Sour Cream, Cheese, Lettuce, Guacamole]] $11.75
1833 1 Steak Burrito [Fresh Tomato Salsa, [Rice, Sour Cream, Cheese, Lettuce, Guacamole]] $11.75
1834 1 Chicken Salad Bowl [Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Guacamole, Lettuce]] $11.25
1834 1 Chicken Salad Bowl [Fresh Tomato Salsa, [Fajita Vegetables, Lettuce]] $8.75
1834 1 Chicken Salad Bowl [Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Lettuce]] $8.75
```

##Question 1
1. order #, quantity, product, options, price  
2. 1834 orders  
from number of orders in column A  
3. 4623 lines  
```unix
MARCCAM-M-618J:data Computer$ wc -l chipotle.tsv
    4623 chipotle.tsv
```
4. chicken is more popular than steak  
```unix
MARCCAM-M-618J:data Computer$ grep -ic "steak burrito" chipotle.tsv
368
MARCCAM-M-618J:data Computer$ grep -ic "chicken burrito" chipotle.tsv
553
v. more black beans
MARCCAM-M-618J:data Computer$ grep -i "chicken burrito" chipotle.tsv | grep -ic "black beans"
282
MARCCAM-M-618J:data Computer$ grep -i "chicken burrito" chipotle.tsv | grep -ic "pinto beans"
105
```

##Question 2
```unix
MARCCAM-M-618J:dat7 Computer$ find . -name *.*sv
./data/airlines.csv
./data/chipotle.tsv
./data/drinks.csv
./data/hitters.csv
./data/imdb_1000.csv
./data/sms.tsv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.cs
```

##Question 3
Total= 29
```unix
./code/00_python_intermediate_workshop.py:9
./code/02_command_line.md:2
./code/03_file_reading.py:1
./code/03_python_homework_chipotle.py:4
./code/04_pandas.py:2
./code/15_natural_language_processing_nb.py:2
./code/19_advanced_sklearn.py:3
./data/yelp.csv:1
./data/yelp.json:1
./notebooks/15_natural_language_processing.ipynb:2
./project/README.md:1
./README.md:1

MARCCAM-M-618J:dat7 Computer$ grep -ric "dictionary" .
./.git/config:0
./.git/description:0
./.git/FETCH_HEAD:0
./.git/HEAD:0
./.git/hooks/applypatch-msg.sample:0
./.git/hooks/commit-msg.sample:0
./.git/hooks/post-update.sample:0
./.git/hooks/pre-applypatch.sample:0
./.git/hooks/pre-commit.sample:0
./.git/hooks/pre-push.sample:0
./.git/hooks/pre-rebase.sample:0
./.git/hooks/prepare-commit-msg.sample:0
./.git/hooks/update.sample:0
./.git/index:0
./.git/info/exclude:0
./.git/logs/HEAD:0
./.git/logs/refs/heads/master:0
./.git/logs/refs/remotes/origin/HEAD:0
./.git/objects/pack/pack-f887f548f765240da153b1438633bfd46c38ad46.idx:0
./.git/objects/pack/pack-f887f548f765240da153b1438633bfd46c38ad46.pack:0
./.git/packed-refs:0
./.git/refs/heads/master:0
./.git/refs/remotes/origin/HEAD:0
./.gitignore:0
./code/00_python_beginner_workshop.py:0
./code/00_python_intermediate_workshop.py:9
./code/02_command_line.md:2
./code/03_file_reading.py:1
./code/03_python_homework_chipotle.py:4
./code/04_pandas.py:2
./code/05_pandas_homework_imdb.py:0
./code/05_pandas_visualization.py:0
./code/06_human_learning_iris.py:0
./code/07_api.py:2
./code/07_web_scraping.py:3
./code/08_bias_variance_nb.py:0
./code/08_knn_sklearn_nb.py:0
./code/09_glass_id.py:0
./code/09_model_evaluation_nb.py:0
./code/10_linear_regression_nb.py:0
./code/10_yelp_reviews.py:1
./code/11_logistic_regression_nb.py:0
./code/11_titanic.py:0
./code/12_advanced_model_evaluation_nb.py:0
./code/14_naive_bayes.py:0
./code/14_yelp_text.py:0
./code/15_cross_validation_nb.py:0
./code/15_natural_language_processing_nb.py:2
./code/16_kaggle.py:0
./code/16_kaggle_minimal.py:0
./code/17_decision_trees_nb.py:0
./code/18_ensembling_nb.py:0
./code/19_advanced_sklearn.py:3
./code/19_clustering.py:0
./code/19_grid_exercise.py:0
./data/airlines.csv:0
./data/beer.txt:0
./data/chipotle.tsv:0
./data/drinks.csv:0
./data/example.html:0
./data/hitters.csv:0
./data/imdb_1000.csv:0
./data/imdb_ids.txt:0
./data/sms.tsv:4
./data/titanic.csv:0
./data/u.data:0
./data/u.item:0
./data/u.user:0
./data/ufo.csv:0
./data/vehicles_test.csv:0
./data/vehicles_train.csv:0
./data/yelp.csv:1
./data/yelp.json:1
./homework/09_bias_variance.md:0
./homework/09_glass_id.md:0
./homework/10_yelp_reviews.md:0
./homework/11_titanic.md:0
./homework/12_roc_auc.md:0
./homework/14_spam_filtering.md:0
./homework/14_yelp_text.md:0
./homework/15_cross_validation.md:0
./notebooks/08_bias_variance.ipynb:0
./notebooks/08_knn_sklearn.ipynb:0
./notebooks/09_model_evaluation.ipynb:0
./notebooks/10_linear_regression.ipynb:0
./notebooks/11_logistic_regression.ipynb:0
./notebooks/12_advanced_model_evaluation.ipynb:0
./notebooks/12_roc_auc_rank_ordering.ipynb:0
./notebooks/14_bayes_theorem_iris.ipynb:0
./notebooks/14_naive_bayes_spam.ipynb:0
./notebooks/15_cross_validation.ipynb:0
./notebooks/15_natural_language_processing.ipynb:2
./notebooks/17_decision_trees.ipynb:0
./notebooks/18_ensembling.ipynb:0
./notebooks/images/bias_variance.png:0
./notebooks/images/cross_validation_diagram.png:0
./notebooks/images/crowdflower_ensembling.jpg:0
./notebooks/images/driver_ensembling.png:0
./notebooks/images/estimating_coefficients.png:0
./notebooks/images/iris_01nn_map.png:0
./notebooks/images/iris_05nn_map.png:0
./notebooks/images/iris_15nn_map.png:0
./notebooks/images/iris_50nn_map.png:0
./notebooks/images/logistic_betas.png:0
./notebooks/images/obama_clinton_tree.jpg:0
./notebooks/images/r_squared.png:0
./notebooks/images/salary_color.png:0
./notebooks/images/salary_regions.png:0
./notebooks/images/salary_tree.png:0
./notebooks/images/salary_tree_annotated.png:0
./notebooks/images/salary_tree_deep.png:0
./notebooks/images/slope_intercept.png:0
./notebooks/images/supervised_learning.png:0
./notebooks/images/train_test_split.png:0
./notebooks/images/training_testing_error.png:0
./notebooks/images/tree_titanic.png:0
./notebooks/images/tree_vehicles.png:0
./notebooks/images/tree_vs_linear.png:0
./other/advice.md:0
./other/python_packages.md:0
./other/setup_checklist.md:0
./project/peer_review.md:0
./project/public_data.md:0
./project/README.md:1
./README.md:1
./slides/01_course_overview.pdf:0
./slides/01_course_overview.pptx:0
./slides/01_intro_to_data_science.pdf:0
./slides/01_intro_to_data_science.pptx:0
./slides/01_types_of_data.pdf:0
./slides/01_types_of_data.pptx:0
./slides/02_git_github.pdf:0
./slides/02_git_github.pptx:0
./slides/06_machine_learning.pdf:0
./slides/06_machine_learning.pptx:0
./slides/11_confusion_matrix.pdf:0
./slides/11_confusion_matrix.pptx:0
./slides/12_drawing_roc.pdf:0
./slides/12_drawing_roc.pptx:0
./slides/14_bayes_theorem.pdf:0
./slides/14_bayes_theorem.pptx:0
./slides/14_naive_bayes.pdf:0
./slides/14_naive_bayes.pptx:0
./slides/16_kaggle.pdf:0
./slides/16_kaggle.pptx:0
./slides/19_clustering.pdf:0
./slides/19_clustering.pptx:0
```