# Discourse iframe theme component

Adds a button to the composer that allows users to add an iframe from a URL template
to a Discourse post. Clicking the 'Add Iframe' button adds a BBCode tag that contains a placeholder `IFRAME_ID` tag. When
the placeholder is replaced with the iframe's ID, the iframe will be rendered.

`[wrap=iframe id=IFRAME_ID][/wrap]`

## Configuration

See [How do I install a Theme or Theme Component?](https://meta.discourse.org/t/how-do-i-install-a-theme-or-theme-component/63682) for
installation and activation instructions.

Once the component has been installed, add your iframe template to the component's 'discourse iframe template' setting.
The iframe template should be the URL of your application's iframe source, with the `%{iframe_id}` substituted for the
iframe's ID.

As a simple example, to allow users to post iframes from a WordPress site that has its permalink structure set to
'Post name', the 'discourse iframe template' would be set to `https://www.example.com/%{iframe_id}/?embed=true`. Users
would replace the text set by the 'discourse_iframe.id_placeholder' with the post's WordPress slug.

Note: The base URL of your Discourse iframe template must be added to your Discourse 'allowed iframes' site setting in
order for the iframe to be displayed.

The component allows you to set the iframe width and height. It also allows you to set the iframe button text and the
text that is used for the id placeholder. The id placeholder text defaults to 'IFRAME_ID'. The text added to this setting
must not contain spaces.