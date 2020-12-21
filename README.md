<img src="logos/Qcat-logo.png" alt="Qcat is fat and lazy like me" style="float: left; margin-right: 10px;" />

**Transparent, Vendor Agnostic Messaging for Lazy Cats and Some Humans**


A Spring Boot Starter that automates much of the boiler plate tasks associated with messaging based application development. The core is vendor neutral and lends itself to integration with most brokers.

Qcat grew out of fustration with more mainstream annotation based system that either were more complex than the underlying framework or not yet supporting Java 11.

## <img src="logos/Q-logo-32.png" alt="Qcat is fat and lazy like me" />cat for S<img src="logos/Q-logo-32.png" alt="Qcat is fat and lazy like me" />S (qcat4sqs)

The first Provider for Qcat is for AWS SQS Java 2.x API. Simply configure a Spring Bean for the service and annotate you listeners and you are off to another cat nap instead of banging your head against walls.

Example Configuration;

```
package net.subnoize.examples;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import software.amazon.awssdk.services.sqs.SqsAsyncClient;

@Configuration
public class SqsConfiguration {
	
	@Bean
	public SqsAsyncClient getSqsAsyncClient() {
		return SqsAsyncClient.create();
	}
	
}
```