# SHAP (SHapley Additive exPlanations)
## _A notebook for SHAP in python_

SHAP (SHapley Additive exPlanations) is a game theoretic approach to explain the output of any machine learning model. It connects optimal credit allocation with local explanations using the classic Shapley values from game theory and their related extensions.

## Main Idea

The main idea of SHAP rests upon the following equation where it captures the average marginal contribution of a feature value (player) across all possible coalitions (society).

<img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/bc8ed8adc24cb67b8a19d5f9488287f4449cc075" alt="Shapley value formula" title="Shapley value formula" class="center">

where n is the total number of players and the sum extends over all subsets S of N not containing player i. The formula can be interpreted as follows: imagine the coalition being formed one actor at a time, with each actor demanding their contribution 
$$ v(S \cup {i}) - v(S) $$ as a fair compensation, and then for each actor take the average of this contribution over the possible different permutations in which the coalition can be formed.

## Enviornment
The enviornment is as follows:
- python 3.6.x
- windows 10

## Sample Dataset
The dataset used in this notebook is taken from the [Kaggle-titanic](https://www.kaggle.com/c/titanic) competition.