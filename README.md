# gatsby-transformer-calculator
Grade Calculator Transformer for GatsbyJS

This transformer converts grades of assessment in text into Gatsby Node.

## install

```
npm install --save gatsby-transformer-calculator
```

## configuration

gatsby-config.js

```
module.exports = {
  plugins: [
    {
      resolve: `gatsby-source-filesystem`,
      options: {
        name: `data`,
        path: `${__dirname}/src/data/`,
      },
    },
    `gatsby-transformer-calculator`,
  ],
}
```

## expected input

The input file is expected to be CSV format. It could at least 2 columns.

* assessment name, it's optional
* grade, string, could be in percentage, letters or points
* weight, number

example:

```
quiz, 90, 20
midterm, 80, 30
homework, 85, 20
final, 90, 30
```

or 
```
A, 30
A-, 30
B, 40
```

The calculation will not be done here. Check for [Grade Calculator](https://10converters.com/calculators/grade-calculator) for a complete reference of the calculation.