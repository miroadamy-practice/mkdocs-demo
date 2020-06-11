## Variables

The price of the product is {{ price }}.

See [more information on the website]({{ company.website }}).

See <a href="{{ company.website }}">more information on the website</a>.

## Input fields with macro

{% macro input(name, value='', type='text', size=20) -%}
    <input type="{{ type }}" name="{{ name }}" value="{{
        value|e }}" size="{{ size }}">
{%- endmacro %}

<p>{{ input('username') }}</p>
<p>{{ input('password', type='password') }}</p>


## Git information

{{ git.short_commit}} ({{ git.date}}) by {{ git.author}}