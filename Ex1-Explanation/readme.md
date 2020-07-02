## BLOCK-readText

### Organizing Data With Tables

Many times there are some data that must be displayed in a form that is easy for users to read and digest. For example food ingredients, shopping items with price marks obtained in different subjects, etc. For such kind of data, the HTML table provides a straightforward way to structure the data in tabular form.

HTML tables were introduced to structure the data in a more digestible way. But in the past CSS was not widely supported HTML tables were only means by which websites were created. Mostly for positioning elements, creating multi-column layouts.

Fortunately, those were in the past. Now we have CSS supported in every browser. Today tables are used specifically for organizing data only.

#### Creating Tables

To introduce a table on a page `<table>` element is defined.

```html
<table>
  ...
</table>
```

The `<table>` element represents the data in tabular form that is contained within rows and columns.

**Table Row**

Once the `<table>` element is defined table-row `<tr>` is added. There can be numerous rows within a table.

```html
<table>
  <tr>
    ...
  </tr>
  <tr>
    ...
  </tr>
  <tr>
    ...
  </tr>
</table>
```

All the data inside a table comes inside table data. Once the table and table rows are defined table data is added using `<td>` elements inside rows. Adding multiple `<td>` elements in a row will create columns.

```html
<table>
  <tr>
    <td>Laptop</td>
    <td>Apple</td>
    <td>₹ 68,999</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>Apple</td>
    <td>₹ 5,973</td>
  </tr>
  <tr>
    <td>Keyboard</td>
    <td>Apple</td>
    <td>₹ 8,900</td>
  </tr>
</table>
```

**Table Header**

To provide hading to columns or rows of cells there comes table header, `<th>` elements. The table header is similar to `<td>`, `<th>` also creates cells. The exception is that `<th>` element signifies a heading for columns or rows, whereas `<td>` represents generic data.

In a simplest way, table header, `<th>` element can consider as similar to heading element(`<h1>` through `<h6>`), whereas `<td>` is similar to a `<p>` element.

```html
<table>
  <tr>
    <th>Accesories</th>
    <th>Brand</th>
    <th>Price in ₹</th>
  </tr>
  <tr>
    <td>Laptop</td>
    <td>Apple</td>
    <td>₹ 68,999</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>HP</td>
    <td>₹ 1,399</td>
  </tr>
  <tr>
    <td>Keyboard</td>
    <td>Apple</td>
    <td>₹ 8,900</td>
  </tr>
</table>
```

Additionally, the table header, `<th>` element comes with a `scope` attribute. Depending upon the data, the `scope` attribute allows us to use the `th` element for both rows and columns.

The scope attribute accepts values such as `col`, `row`, `colgroup`, and `rowgroup`. The most commonly used values are col and row. The `col` value indicates that every cell within the column relates directly to that table header, and the `row` value indicates that every cell within the row relates directly to that table header.

**The col value**

```html
<table>
  <tr>
    <th scope="col">Accesories</th>
    <th scope="col">Brand</th>
    <th scope="col">Price in ₹</th>
  </tr>
  <tr>
    <td>Laptop</td>
    <td>Apple</td>
    <td>₹ 68,999</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>HP</td>
    <td>₹ 1,399</td>
  </tr>
  <tr>
    <td>Keyboard</td>
    <td>Apple</td>
    <td>₹ 8,900</td>
  </tr>
</table>
```

**Col and Row Value**

```html
<table>
  <tr>
    <th scope="col">Name</th>
    <th scope="col">Phone</th>
    <th scope="col">City</th>
  </tr>
  <tr>
    <th scope="row">Joel Garner</th>
    <td>412-212-5421</td>
    <td>Pittsburgh</td>
  </tr>
  <tr>
    <th scope="row">Clive Lloyd</th>
    <td>410-306-1420</td>
    <td>Baltimore</td>
  </tr>
  <tr>
    <th scope="row">Gordon Greenidge</th>
    <td>281-564-6720</td>
    <td>Houston</td>
  </tr>
</table>
```

It is recommended to use the scope attribute that helps screen readers and other technologies.

Additionally, in most of the browsers, the table header is center aligned that can be reset using CSS.

#### Organizing Data and Table Structure

Getting introduced to creating tables, rows, columns, and table header was just the beginning. More importantly, organizing the data and provide a solid table structure is the rest of the work. Few additional elements help in organizing the data and structure the table. Also, these elements provide better semantic meaning to the table and its data. These additional elements are `<caption>`, `<thead>`, `<tbody>`, and `<tfoot>`.

**Table Caption**

Table caption, `<caption>` provides caption or title of the table, which is similar to a heading. The caption of the table helps the user to identify what kind of data the table is containing.

```html
<table>
  <caption>
    Pricing list of computer accessories
  </caption>
  ...
</table>
```

The content inside a table can be divided into multiple groups, like head `<thead>`, body `<tbody>`, and foot `<tfoot>` of the table. These elements help to structure the data in a more organized way.

**Table Head**

The table head, `<thead>` element wraps heading row of the table which consists of `<th>` elements. The thead element comes after the `<caption>` element.

**Table Body**

After the `<thead>` element `<tbody>` comes which contains all the generic data of the table.

**Table Foot**

The `<tfoot>` may contain the data that show the overall result of the table. For example the total cost of the items.

```html
<table>
  <caption>
    List of computer accessories bought
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Brand</th>
      <th scope="col">Price in ₹</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Laptop</td>
      <td>Apple</td>
      <td>₹ 68,999</td>
    </tr>
    <tr>
      <td>Mouse</td>
      <td>HP</td>
      <td>₹ 1,399</td>
    </tr>
    <tr>
      <td>Keyboard</td>
      <td>Apple</td>
      <td>₹ 8,900</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Subtotal</td>
      <td></td>
      <td>₹ 79,298</td>
    </tr>
    <tr>
      <td>Tax</td>
      <td></td>
      <td>₹ 899</td>
    </tr>
    <tr>
      <td>Total</td>
      <td></td>
      <td>₹ 80, 197</td>
    </tr>
  </tfoot>
</table>
```

**Combining Multiple Cells**

When working with the table, sometimes you may need to combine two or more cells. In the above table inside `<tfoot>` there are few empty cells, `<td>`. To avoid empty cells we can combine two or more cells next to each other using `colspan` or `rowspan` attribute. These two attributes can be applied to both `<td>` or `<th>`.

The `colspan` will span the single cell across multiple columns and `rowspan` will span the single-cell across the multiple rows.

```html
<table>
  <caption>
    List of computer accessories bought
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Brand</th>
      <th scope="col">Price in ₹</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Laptop</td>
      <td>Apple</td>
      <td>₹ 68,999</td>
    </tr>
    <tr>
      <td>Mouse</td>
      <td>HP</td>
      <td>₹ 1,399</td>
    </tr>
    <tr>
      <td>Keyboard</td>
      <td>Apple</td>
      <td>₹ 8,900</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Subtotal</td>
      <td>₹ 79,298</td>
    </tr>
    <tr>
      <td colspan="2">Tax</td>
      <td>₹ 899</td>
    </tr>
    <tr>
      <td colspan="2">Total</td>
      <td>₹ 80, 197</td>
    </tr>
  </tfoot>
</table>
```

#### Table Borders

To make the table more legible borders can be used around a table or individual cells. Borders around cells or tables have a large impact that helps the user to interpret the data more clearly. When working with table borders two properties come in handy: `border-collapse`, and `border-spacing`.

**Border Collapse Property**

When we apply border on `<table>` and it's nested `<th>` and `<td>` elements, those borders will stack up between the elements sitting next to each other. For example, if 2px of borders is applied on the entire table and additional 2px borders on around each table cell, there would be a 4px border around every cell in the table.

In this case, `border-collapse` property comes in handy. The border-collapse property accepts values: `collapse`, `separate`, and `inherit`. By default `separate` is the value means the border will stack up. However, the model can be changed using the `collapse` value. The collapse value will condense the border into one.

```css
table {
  border-collapse: collapse;
}
th,
td {
  border: 2px solid #272727;
  padding: 8px 16px;
}
```

**Border Spacing**

Another property that comes in handy with the table border model is `border-spacing`. The `border-spacing` works only when the `border-collapse` property is set to `separate`. The `border-spacing` property determines how much space will be between the borders.

```css
table {
  border-collapse: separate;
  border-spacing: 4px;
}
table,
th,
td {
  border: 2px solid #272727;
  padding: 8px 16px;
}
```

Additionally, the border-spacing` property can accept two values: the first value for horizontal spacing and a second value for vertical spacing.

```css
table {
  border-collapse: separate;
  border-spacing: 4px 8px;
}
table,
th,
td {
  border: 2px solid #272727;
  padding: 8px 16px;
}
```

**Adding Borders to Rows**

Working with table borders can be sometimes tricky. There are a few things that you will have to keep always in mind. For example the above two property `border-collapse` and `border-spacing`. In addition to that, there is one more thing you need to keep in mind that you cannot apply a border to table rows. Because `<tr>` elements do not accept border property. Some thought must be given when you try to apply borders to rows.

There is one thing that we can do is instead of applying borders to rows, we can apply the bottom border to `<td>` elements. Also do not forget to apply `border-collapse` property to `collapse` value.

```css
table {
  border-collapse: collapse;
}
th,
td {
  border-bottom: 1px solid #cecfd5;
  padding: 10px 15px;
}
```

#### Table Striping

One of the most popular styles when designing a table is to stripe its rows with alternate background colors.
This makes the data inside the table more legible and helps users to interpret the data more clearly.

One way to do so is to apply a class on every row and then define background-color on alternate rows. Another easy way to do so is by using the `:nth-child` pseudo-class with `odd` and `even` argument. For example:

```css
table {
  border-collapse: collapse;
}
th,
td {
  padding: 8px 16px;
}
thead {
  background: #bada55;
  color: #fff;
}
tbody tr:nth-child(even) {
  background: #f0f0f2;
}
td {
  border-bottom: 1px solid #272727;
  border-right: 1px solid #272727;
}
td:first-child {
  border-left: 1px solid #272727;
}
```
