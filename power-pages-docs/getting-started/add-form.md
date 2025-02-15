---
title: Add forms
description: Add forms to your page in Power Pages.
author: clromano
ms.topic: conceptual
ms.custom: 
ms.date: 10/08/2022
ms.subservice:
ms.author: clromano
ms.reviewer: ndoelman
contributors:
    - clromano
    - nickdoelman
    - ProfessorKendrick
---

# Add a form

A form is a data-driven configuration that collects data in Power Pages sites. Forms on pages are created from Dataverse table forms. Dataverse table forms can be created by using the [Data workspace](use-data-workspace.md) or from [model-driven apps created in Power Apps](/power-apps/maker/model-driven-apps/form-designer-overview/). You can use them on pages or with [lists](add-list.md) to build a complete web application.

> [!TIP]
> We've created a series of tutorials and videos for you to learn to use Power Pages and how create and add a form to a page. For more information, go to [Tutorial: Add a form to a page](tutorial-add-form-to-page.md).

To add a form:

1. Open the [design studio](use-design-studio.md) to edit the content and components of the site.

1. Go to the **Pages** workspace.

1. Select the page you want to edit.

1. Select the section you want to add the form component to.

1. Hover over any editable canvas area, then select the **Form** icon from the component panel.

    :::image type="content" source="media/common/component-options.png" alt-text="The add component menu options.":::

1. You can choose either to create a new form or use an existing form (if a maker has created one previously).

   If you choose to create a new form, you'll need to enter the following criteria.
  
    :::image type="content" source="media/first-page/add-form.png" alt-text="Add a form to a page.":::

    | Option | Description |
    | ----------- | ----------- |
    | Choose a table | Choose the table where data will be stored. |
    | Select a form | Select one of the Dataverse forms available for the selected table. |
    | Name your copy of the selected form| Give your copy of the form a name. |
    | Data | You can choose to have the data that's entered by a user create a new record, update existing records, or make the data read-only. |
    | On submit | You can choose optionally to show a success message. You must enter the options to redirect to a webpage and redirect to a URL. |
    | CAPTCHA | You can choose to show a captcha to anonymous users, authenticated users, or both. |
    | Attachments | Allows you to [enable and configure attachments](#enable-attachments-on-a-form) for the form. |

    > [!NOTE]
    > You'll need to enable [table permissions](../security/table-permissions.md) to ensure that users will be able to interact with the data on the forms.

1. You can select the ellipsis (**...**) to duplicate the form, move it up or down within the section, or delete it.

## Edit a text field on the form

You can edit text fields, including email, form title, and title section.

To edit a text field on the form:

1. Hover and select the text field from the canvas.
1. Edit the text field and style it as needed (bold, underline, or italic).
    :::image type="content" source="media/add-form/fill-details.png" alt-text="Styling options for text fields including bold, underline, and italic.  Bold is selected here.":::

## Edit and validate form fields

To edit a form field:

1. Hover over and select the field from the canvas.
1. Choose **Edit field** in the tool bar.
    :::image type="content" source="media/add-form/edit-text-field.png" alt-text="The edit text field menu.":::
1. From the Field Edit modal:
    - Update the field's label/display name.
    - Mark the field as required, then customize the error message to be shown when the field is required.
    - Add a description to the field and adjust its position (choices include above the field, below the field, and above the label).
    - Set the validation rules for the field.
        - Use the options to configure out-of-the-box validations.
        - Use the Regex option to enter custom validation using regular expressions.

## Enable attachments on a form

Users can upload an attachment with form submission.

To enable attachments on a form:

1. Add a form or edit an existing form.

1. In the **Add a form** modal, choose **Attachments** from the left panel. 

    - Configure the following options:

        - Turn on/off the **Enable attachments** toggle.
        - Turn on/off the **Attachment is required** toggle.
        - Turn on/off the **Allow multiple files** toggle.
        - Max file size allowed
            >[!NOTE] 
            > The following file types are allowed:
            >   - All
            >   - Audio
            >   - Document
            >   - Image
            >   - Video
            >   - Specific (comma separated values)
    
        :::image type="content" source="media/add-form/attach-file.png" alt-text="Menu options for enabling attachments on a form.":::

Once configured, the file upload placeholder will show in the canvas. 

:::image type="content" source="media/add-form/form-with-attachment.png" alt-text="Form with attachment option enabled.":::

### Enabling table permissions

When you add a new form, you'll be prompted to set permissions to allow site users to interact with the form. The settings for table permissions will be pre-populated (**create** and **append to**), but you'll still need to assign web roles and save the settings. The process will automatically create the child table permissions for the **note (annotations)** table, which contain the attachments.

:::image type="content" source="media/add-form/configure-table-permissions.png" alt-text="Configure table permissions.":::

You can also adjust the permissions and assign web roles based on your requirements in the **Set up** workspace.

:::image type="content" source="media/add-form/table-permissions.png" alt-text="Table permissions menu.":::

For more information, see [Configuring table permissions](../security/table-permissions.md).

## Enable code components on form fields

If a Dataverse form field has been configured to use a code component using the Data workspace or a model-driven app, you can enable the code component to be used when a form is used on a webpage.

To enable the code component:

1. Select the field and choose **Edit field**.

1. Select **Enable Power Apps Component Framework field**.

1. Select **OK**.

    :::image type="content" source="media/add-form/enable-code-component.png" alt-text="Enabling code component on webpage form.":::

The code component will now be available on the form.

### See also

- [Create and modify forms](../configure/data-workspace-forms.md)
- [Tutorial: Add a form to a page](tutorial-add-form-to-page.md)