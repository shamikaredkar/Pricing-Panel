![ArtGallery Demo](https://github.com/shamikaredkar/ArtGallery/blob/main/ArtGalleryPreview.gif)
### Purpose:

The purpose of the Pricing-Plan Project is to present various service subscription options in a clear and appealing format, allowing potential customers to easily compare features and costs associated with each plan. The project aims to facilitate the decision-making process for users seeking to subscribe to a service, with emphasis on simplicity and ease of navigation.

---

### Features:

> Three distinct pricing tiers with unique icons and feature lists
> 

> Responsive design to ensure accessibility across different devices.
> 

> Interactive elements, such as hover effects, to enhance user experience.
>

> Clear call-to-action buttons for users to sign up or start a free trial.
> 
---

### Technology Stack:

HTML, CSS, External Fonts (Google Fonts)

---

### Code Documentation:

## HTML

</aside>

**index.html —** The document consists of a div with a class of panel pricing-table, which serves as the container for the individual pricing plans.

- **`<img>`**: Represents the tier's icon.
- **`<h2>`**: Plan's name.
- **`<ul>` with `<li>`**: Listing the features.
- **`<span>`**: Displaying the price
- **`<a>`**: Functioning as a signup or trial button

##CSS
</aside>

**app.css —**  This stylesheet applies custom styles to the pricing plans, including:

- Layout and positioning of pricing plans.
- Styling for icons, headers, and feature lists.
- Design of buttons and their interactive states.

**Features (`pricing-features`)**

```css
.pricing-features {
    list-style: none;
    padding: 0;
    margin-bottom: 1.5rem;
}
.pricing-features-item {
    margin-bottom: 0.5rem;
    text-align: left;
}
```

- **List Style**: Removes bullet points from the list for a cleaner look using `list-style`.
- **Padding and Margin**: Resets `padding` to 0 and adds `margin-bottom` to space out the list from the subsequent price display. Adds spacing between individual list items for legibility with `margin-bottom`.

**Price (`pricing-price`)**

```css
.pricing-price {
    font-size: 2rem;
    font-weight: bold;
    display: block;
    margin-bottom: 1.5rem;
}
```

- **Display**: Uses `display: block` to ensure the price appears on a new line.
- **Margin-Bottom**: Separates the price from the signup button with `margin-bottom`.

### Media Queries

```css
@media (min-width: 900px) {
    .panel {
        flex-direction: row;
    }

    .pricing-plan {
        border-bottom: none;
        border-right: 1px solid #e1f1ff;
        padding: 25px 50px;
    }

    .pricing-plan:last-child {
        border-right: none;
    }
}
```
***Panel Layout:***
- The `.panel` class changes the layout direction to a row using `flex-direction: row.` This means that on screens wider than 900 pixels, the pricing plans will be arranged side by side instead of stacking vertically.

***Individual Pricing Plan Style Adjustments:***

- The `.pricing-plan` class has its bottom border removed with `border-bottom: none`, ensuring there is no border at the bottom of each plan when side by side.
- A right border is added with `border-right: 1px solid #e1f1ff` to separate each plan visually.
- Padding is adjusted to `25px 50px` to provide more space inside each pricing plan, allowing for a more airy and less congested display of the plans' content.

***Last Pricing Plan Adjustment:***

- The `.pricing-plan:last-child` selector targets the last pricing plan to ensure that it does not have a right border with `border-right: none.` This prevents a border from appearing on the far right edge of the pricing table, which would be unnecessary and could disrupt the clean layout.
