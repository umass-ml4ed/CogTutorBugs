# CogTutorBugs 5000+ Labeled Student Alegbra Mistakes

## About

A dataset of student errors observed while using a cognitive tutoring system. This dataset was formed by processing the 'Cog Tutor 2010 Equation Solving (sch_bd1124)' dataset accessed via DataShop (Koedinger et al., 2010). The exercises are Algebra I levels, for example:

`Solve for y in the following equation: -6=3+y/9`


## Data Format

The original tutoring system logs were parsed by filtering the interaction logs for items which were labeled as having an *outcome* of **BUG** and then taking the nearby interactions to build context for the error. In **BUG** interactions the tutoring system recognized the error that the student made and dispalyed feedback to guide the student, we've analyzed these feedback messages and grouped them into 19 unique categories.

```json
    {
        "Unnamed: 0.1": 0,
        "Unnamed: 0": 0,
        "eq1": "-6=3+y/9",
        "action": "DIV_SIDE",
        "Input": "9",
        "eq2": "-6/9=3+y/9/9",
        "Outcome": "BUG",
        "Previous Action": null,
        "Feedback": "To remove the coefficient of <expression>y/9</expression>, you need to divide by <expression>1/9</expression> or multiply by <expression>9</expression>.",
        "Filtered Feedback": "To remove the coefficient of , you need to divide by  or multiply by .",
        "label": 10,
        "Label Name": "DIVIDE_TO_SIMPLIFY"
    },
```


## Citation
If you would like to use this dataset in your work please cite our work:

Paper: [Algebra Error Classification with Large Language Models](https://arxiv.org/abs/2305.06163)

BibTeX:
```
@misc{mcnichols2023algebra,
      title={Algebra Error Classification with Large Language Models}, 
      author={Hunter McNichols and Mengxue Zhang and Andrew Lan},
      year={2023},
      eprint={2305.06163},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

## Contact
If you have any questions about our work please contact us at wmcnichols@umass.edu and mention the CogTutorBugs dataset.

## References
+ Koedinger, K.R., Baker, R.S.J.d., Cunningham, K., Skogsholm, A., Leber, B., Stamper, J. (2010) A Data Repository for the EDM community: The PSLC DataShop. In Romero, C., Ventura, S., Pechenizkiy, M., Baker, R.S.J.d. (Eds.) Handbook of Educational Data Mining. Boca Raton, FL: CRC Press.
+ Koedinger, K.R., Anderson, J.R., Hadley, W.H., Mark, M.A.: Intelligent tutoring goes to school in the big city. International Journal of Artificial Intelligence in Education 8, 30–43 (1997)
