{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/fabcoin-core/rpcs/rpcs/setnetworkactive.md" %}

##### SetNetworkActive
{% include helpers/subhead-links.md %}

{% assign summary_setNetworkActive="disables/enables all P2P network activity." %}

{% autocrossref %}

*Added in Fabcoin Core 0.14.0*

The `setnetworkactive` RPC {{summary_setNetworkActive}}

*Parameter #1---whether to disable or enable all P2P network activity*

{% itemplate ntpd1 %}
- n: "Activate"
  t: "bool"
  p: "Required<br>(exactly 1)"
  d: "Set to `true` to enable all P2P network activity. Set to `false` to disable all P2P network activity"

{% enditemplate %}

*Result---`null` or error on failure*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null`.  The JSON-RPC error field will be set only if you entered an invalid parameter"

{% enditemplate %}

*Example from Fabcoin Core 0.14.1*

{% highlight bash %}
fabcoin-cli setnetworkactive true
{% endhighlight %}

Result (no output from `fabcoin-cli` because result is set to `null`).

*See also*

* [GetNetworkInfo][rpc getnetworkinfo]: {{summary_getNetworkInfo}}

{% endautocrossref %}
