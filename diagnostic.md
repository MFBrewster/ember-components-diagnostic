# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    A series of lists, each of which has several items, can be modeled as two
    components: one for the lists, and one for the list items
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    app/component/component-name/component.js: this file determines the
    attributes for the component, like what tag surrounds the component
    (e.g. 'ul') and what actions the component can perform

    app/component/component-name/template.hbs: this file determines how the
    component will be rendered on the page

    tests/integration/components/component-name/component-test.js: this file is
    generated with some useless tests, but you can write your own useful tests
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{my-contact}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{my-phone foo=bar}}

    {{!-- "bar" being some arbitrary data and "foo" being an
    arbitrary name to be used for the data in the child component --}}
    ```
