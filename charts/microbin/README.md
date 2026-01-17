# microbin



![Version: 0.2.0](https://img.shields.io/badge/Version-0.2.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.1.0](https://img.shields.io/badge/AppVersion-2.1.0-informational?style=flat-square)



Microbin - File sharing made easy



**Homepage:** <https://github.com/james-otten/microbin-helm>



## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| james-otten | <info@jamesotten.com> |  |




## Source Code

* <https://github.com/james-otten/microbin-helm>




## Values



<h1>image</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[image.repository](./values.yaml#L3)

</td><td>str</td><td><code>`docker.io/danielszabo99/microbin`</code></td><td><p><code> microbin image repository</code></p></td></tr><tr style="" ><td>

[image.pullPolicy](./values.yaml#L5)

</td><td>str</td><td><code>`IfNotPresent`</code></td><td><p><code> microbin image pull policy</code></p></td></tr><tr style="" ><td>

[image.tag](./values.yaml#L7)

</td><td>str</td><td><code>`latest`</code></td><td><p><code> microbin image tag</code></p></td></tr><tr style="" ><td>

[image.pullSecretName](./values.yaml#L9)

</td><td>str</td><td><code>``</code></td><td><p><code> image pull secret name</code></p></td></tr>
</table>

<h1>env</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[env[0]](./values.yaml#L11)

</td><td>dict</td><td><code>`{'name': 'MICROBIN_BIND', 'value': '0.0.0.0'}`</code></td><td></td></tr>
</table>

<h1>secret</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[secret.create](./values.yaml#L87)

</td><td>bool</td><td><code>`False`</code></td><td><p><code> enable secret creation</code></p></td></tr><tr style="" ><td>

[secret.name](./values.yaml#L89)

</td><td>str</td><td><code>`microbin`</code></td><td><p><code> secret name for sensitive configuration values</code></p></td></tr>
</table>

<h1>nameOverride</h1><p><code> This is to override the chart name</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[nameOverride](./values.yaml#L98)

</td><td>str</td><td><code>``</code></td><td><p><code> This is to override the chart name</code></p></td></tr>
</table>

<h1>fullnameOverride</h1><p><code> This is to override the full name</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[fullnameOverride](./values.yaml#L100)

</td><td>str</td><td><code>``</code></td><td><p><code> This is to override the full name</code></p></td></tr>
</table>

<h1>podAnnotations</h1><p><code> podAnnotations</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>

<h1>podLabels</h1><p><code> podLabels</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>

<h1>podSecurityContext</h1><p><code> podSecurityContext</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>

<h1>service</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[service.type](./values.yaml#L113)

</td><td>str</td><td><code>`ClusterIP`</code></td><td><p><code> Service type to expose the microbin pod to cluster. Options are ClusterIP, NodePort, LoadBalancer, or ExternalName</code></p></td></tr><tr style="" ><td>

[service.port](./values.yaml#L115)

</td><td>int</td><td><code>`80`</code></td><td><p><code> Port to expose microbin service on</code></p></td></tr><tr style="" ><td>

[service.containerPort](./values.yaml#L117)

</td><td>int</td><td><code>`8080`</code></td><td><p><code> Target port for the microbin container</code></p></td></tr>
</table>

<h1>hostname</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[hostname](./values.yaml#L119)

</td><td>str</td><td><code>`chart-example.local`</code></td><td></td></tr>
</table>

<h1>ingress</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[ingress.enabled](./values.yaml#L123)

</td><td>bool</td><td><code>`False`</code></td><td><p><code> Enable Ingress controller for microbin</code></p></td></tr><tr style="" ><td>

[ingress.className](./values.yaml#L125)

</td><td>str</td><td><code>``</code></td><td><p><code> Ingress class to use, e.g., for GKE Ingress use "gce", for NGINX Ingress use "nginx". If using an Ingress class other than the default, ensure your cluster has the corresponding Ingress controller installed and configured.</code></p></td></tr><tr style="" ><td>

[ingress.tls.enabled](./values.yaml#L132)

</td><td>bool</td><td><code>`False`</code></td><td><p><code> Enable tls for microbin</code></p></td></tr><tr style="" ><td>

[ingress.tls.secretName](./values.yaml#L134)

</td><td>str</td><td><code>`microbin-tls`</code></td><td><p><code> Secret name for tls</code></p></td></tr>
</table>

<h1>resources</h1><p><code> microbin resources</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>

<h1>persistence</h1>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
<tr style="" ><td>

[persistence.enabled](./values.yaml#L147)

</td><td>bool</td><td><code>`True`</code></td><td><p><code> Enable persistence for microbin</code></p></td></tr><tr style="" ><td>

[persistence.mountPath](./values.yaml#L149)

</td><td>str</td><td><code>`/app/microbin_data`</code></td><td><p><code> Mount path for the microbin_data directory</code></p></td></tr><tr style="" ><td>

[persistence.accessMode](./values.yaml#L151)

</td><td>str</td><td><code>`ReadWriteOnce`</code></td><td><p><code> Access mode for the microbin volume</code></p></td></tr><tr style="" ><td>

[persistence.size](./values.yaml#L153)

</td><td>str</td><td><code>`1Gi`</code></td><td><p><code> Size of the microbin PVC</code></p></td></tr><tr style="" ><td>

[persistence.storageClass](./values.yaml#L155)

</td><td>str</td><td><code>`standard`</code></td><td><p><code> Storage class of the microbin PVC</code></p></td></tr>
</table>

<h1>nodeSelector</h1><p><code> nodeSelector</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>

<h1>tolerations</h1><p><code> tolerations</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>

<h1>affinity</h1><p><code> affinity</code></p>
<table style="">
    <tr>
        <th>Key</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>

</table>


