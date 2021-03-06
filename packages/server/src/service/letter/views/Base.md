{% from "ContactMethod.md" import contactMethod %}

{% if warning %}
<p style='color:red;'>
The request was not sent from production.  <b>No email or fax was sent to an election official.</b>  Had this been sent from production, you would have continued to receive this email <b>and</b> the election official would have also been contacted as outlined below.  If you want to send an official request, do so from <a href='https://MailMyBallot.org'>MailMyBallot.org.</a><p>
<p>

{% endif %}

Dear Election Official,

I am writing to request an Absentee or Vote-by-Mail ballot through [{{brandName}}]({{brandUrl}}).  This letter conforms to the requirements set forth by {{guidance}}.

{{contactMethod(method)}}

{% block text %}
{% endblock %}

Sincerely,

{{name}}{% if signature %} (Signature Below and Attached)

<img style='max-width: 400px;' src='{{signature}}'/>
{% endif %}

<font style='font-size:75%;'>

[{{brandName}}]({{brandUrl}}) is a Vote at Home project.
[Vote at Home](https://voteathome.org/) is a non-partisan 501(c)3 that supports vote by mail.

Questions? Feedback? Email us at [{{feedbackEmail}}](mailto:{{feedbackEmail}}).

**Elections Officials**: do you want direct, secure access to your VBM requests?  Email us at [{{electionsEmail}}](mailto:{{electionsEmail}}) to become an the Election Offical Beta User.

Confirmation id: {{confirmationId}}

</font>
