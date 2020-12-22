# Adding Custom Properties to APIs

Usually, APIs have a pre-defined set of properties such as the name, version, context, etc. However, there may be instances where you want to add specific custom properties to your API. You can do this in either of the following ways:

-   [Add custom properties via the API Publisher](#AddcustompropertiesviatheAPIPublisher)
-   [Add custom properties via the REST API](#AddcustompropertiesviatheRESTAPI)

When adding custom properties, note the following:

-   Property name should be unique.

-   Property name should not contain spaces.

-   Property name cannot be case-sensitive.

-   Property name cannot be any of the following as they are reserved keywords: provider, version, context, status, description, subcontext, doc, lcState, name, tags.

After the custom properties have been added, you can [search for APIs using custom property values](#Searchusingcustomproperties).

<a name="AddcustompropertiesviatheAPIPublisher"></a>

### Add custom properties via the API Publisher

1.  Sign in to the API Publisher as an API creator using the following URL: 
      
      `https://<localhost>:9443/publisher`

2.  [Create a new API]({{base_path}}/design-api/create-api/create-a-rest-api/) or edit an existing API.

3.  Click **Properties** and click **ADD NEW PROPERTY**.

      [![Add new property menu]({{base_path}}/assets/img/learn/properties-add-property.png)]({{base_path}}/assets/img/learn/properties-add-property.png)

4. Enter a custom property name and value (e.g., property name: environment, property value: preprod) and click **ADD** to add it.

      [![Add new property]({{base_path}}/assets/img/learn/add-new-property.png)]({{base_path}}/assets/img/learn/add-new-property.png)

5.  Click **SAVE** to save the API.

<a name="AddcustompropertiesviatheRESTAPI"></a>

### Add custom properties via the REST API

Use the [existing REST API]({{base_path}}/develop/product-apis/restful-apis/) to add a new API and in order to add the API with custom properties make sure to add the following element to the request body including the relevant properties.

`"additionalProperties : {"environment": "preprod", "secured": "true"}`

<a name="Searchusingcustomproperties"></a>

### Display custom properties on API overview page

!!! warning
    This feature is only available with the **WUM** updates and is effective from 7th December 2020 (2020-12-07). For more information on updating WSO2 API Manager, see [Updating WSO2 Products](https://www.google.com/url?q=https%3A%2F%2Fdocs.wso2.com%2Fdisplay%2FADMIN44x%2FUpdating%2BWSO2%2BProducts&sa=D&sntz=1&usg=AFQjCNEMvqxxFtu8Qv8K4YugxNXrTfNtUA)

1. Click **Properties** and click **ADD NEW PROPERTY**.

2. Enter the Custom Property Name and value. Set the `Visibility` and the `Show in Devportal` parameters as shown below. Click **ADD**.

    [![Add new property with display suffix]({{base_path}}/assets/img/learn/set-property-visibility-to-true.png)]({{base_path}}/assets/img/learn/set-property-visibility-to-true.png)

3. Click **SAVE** to save the API.

4. From the Developer Portal's API overview page, the changes will be displayed as follows.

    [![View custom properties on API overview page]({{base_path}}/assets/img/learn/view-properties-in-overview-page.png)]({{base_path}}/assets/img/learn/view-properties-in-overview-page.png)


### Search using custom properties

You can use the following format to search for an API using the custom properties:

`<property_name>:<property_value>        `

For example, if you want to search for the **environment** property with a specific value (e.g., preprod) in the Publisher, you can search as shown below:

[![Publisher search option]({{base_path}}/assets/img/learn/search-apis-with-custom-properties.png)]({{base_path}}/assets/img/learn/search-apis-with-custom-properties.png)

When you click on the name of the API in the above screen, the respective API Overview page appears. Click on the **Properties** tab to list the API properties that you added.

[![API Properties]({{base_path}}/assets/img/learn/view-custom-api-properties.png)]({{base_path}}/assets/img/learn/view-custom-api-properties.png)