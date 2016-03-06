# datadog-firehose-nozzle-release
BOSH release for datadog-firehose-nozzle

Follow the following steps to configure Datadog on your Pivotal Cloud Foundry instance:

- Deploy the datadog-firehose-nozzle-release : If you target bosh-lite, you can use the bosh-lite/stub.yml example. If you target a vpshere/bosh you can use the emea2/datadog-firehose-nozzle.yml. You have to configure the yml with you own datadog api key, uaa user and uaa password  (check https://github.com/cloudfoundry-incubator/datadog-firehose-nozzle for more information).

This nozzle will not provide bosh specific metrics (heatlhy, cpu, memory ..) In order to get these metrics, you have to configure the bosh health monitor to send metrics to datadog. You can find the emea2/health_monitor.yml example. You just need to enrich the plugins/datadog section with you api_key and application_key.

Then, you can build your own dashboard or import Stoplight Dashboard : https://github.com/pivotal-cf-experimental/datadog-config-oss

Erwan




