---
title: Richtlinienunterstützung
description: Wsutil verarbeitet die in Eingabemetadaten angegebene Richtlinie und generiert Hilfsroutinen für die Unterstützung von Dienstmodellen.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Richtlinienunterstützungswebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347265d4081216a227b5040fc73f272181bdccfe09ca7500b81078a6a57ed7bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838640"
---
# <a name="policy-support"></a>Richtlinienunterstützung

Wsutil verarbeitet die in Eingabemetadaten angegebene Richtlinie und generiert Hilfsroutinen für die Unterstützung von Dienstmodellen.

## <a name="how-to-use-policy-support-in-wsutil"></a>Verwenden der Richtlinienunterstützung in wsutil

Entwickler sollten die folgenden Schritte ausführen, um die Richtlinienunterstützung im wsutil-Compiler zu verwenden:

-   Sammeln Sie alle Eingabemetadatendateien, die für den Zielwebdienst erforderlich sind.
-   Kompilieren Sie alle gesammelten WSDL-/XSD-/Richtliniendateien mithilfe wsutil.exe. Wsutil generiert einen Satz von Stubdateien und Headerdateien für jede WSDL- und XSD-Eingabedatei.
-   Überprüfen Sie die generierte Headerdatei. Alle Namen der Richtlinienhilfsprogrammroutinen werden am Anfang der Headerdatei im Kommentarabschnitt aufgeführt.
-   Verwenden Sie die Hilfsroutine bindingName \_ CreateServiceProxy, um einen Dienstproxy zu erstellen.
-   Verwenden Sie die Hilfsroutine bindingName \_ CreateServiceEndpoint, um einen Dienstendpunkt zu erstellen.
-   Füllen Sie die in der Methodensignatur angegebene WS \_ bindingTemplateType \_ BINDING \_ TEMPLATE-Struktur aus. Entwickler können bei Bedarf zusätzliche Kanaleigenschaften und/oder Sicherheitseigenschaften bereitstellen.
-   Rufen Sie die Hilfsroutinen auf, wenn ein erfolgreicher Rückgabedienstproxy oder Dienstendpunkt erstellt wurde.

In den folgenden Abschnitten werden verwandte Themen ausführlich beschrieben.

## <a name="handle-policy-input"></a>Behandeln von Richtlinieneingaben

Im Folgenden werden [Compileroptionen](web-service-compiler-tool.md) im Zusammenhang mit der Richtlinienverarbeitung angezeigt.

Standardmäßig generiert wsutil immer Richtlinienvorlagen, es sei denn, es wird mit der Option "/nopolicy" aufgerufen. Die Richtlinie kann als Teil einer WSDL-Datei eingebettet oder separat als Richtlinienmetadatendatei erstellt werden, die wsutil als Eingabe verwendet. Die Compileroption "/wsp:" wird verwendet, um anzugeben, dass die angegebenen Eingabemetadaten eine Richtliniendatei sind. Wsutil generiert potenzielle richtlinienbezogene Hilfsmöglichkeiten mit der folgenden Kompilierung:

**wsutil /wsdl:trusted.wsdl /wsdl:trusted1.wsdl**

**wstuil /wsdl:input.wsdl /wsp:policy.wsp**

Es werden keine Richtlinienhilfshilfen generiert, wenn die Option "/nopolicy" wie im folgenden Beispiel verwendet wird.

**wsutil /nopolicy /wsdl:trusted.wsdl /wsdl:trusted1.wsdl**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Richtlinienbezogener Code, der vom wsutil-Compiler generiert wird

Auf der Seite [Metadatenzuordnung](metadata-mapping.md) wird die Zuordnung zwischen Metadatenkonstrukten mit unterschiedlichen Bindungstypen ausführlich erläutert.

Drei Kategorien von Richtlinieneinstellungen können in richtlinieneinstellungen angegeben werden:

-   Kanaleigenschaften. Derzeit werden nur die folgenden Kanaleigenschaften unterstützt: [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **WS CHANNEL PROPERTY ADDRESSING \_ \_ \_ \_ VERSION** und **WS CHANNEL PROPERTY ENVELOPE \_ \_ \_ \_ VERSION**.
-   Sicherheitseigenschaften. Derzeit werden nur die folgenden Sicherheitseigenschaften unterstützt: [**WS \_ SECURITY PROPERTY \_ \_ TIMESTAMP \_ USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), **WS SECURITY PROPERTY SECURITY \_ \_ HEADER \_ \_ \_ LAYOUT,** **WS SECURITY PROPERTY TRANSPORT \_ \_ PROTECTION \_ \_ \_ LEVEL** und **WS SECURITY PROPERTY SECURITY \_ \_ HEADER \_ \_ \_ VERSION**.
-   Sicherheitsbindung. Derzeit werden nur die folgenden Sicherheitsbindungen unterstützt: [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [**WS TCP \_ \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)und [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Bindungsvorlagentyp

Es gibt eine begrenzte Anzahl von Bindungen, die in wsutil unterstützt werden. Alle unterstützten Kombinationen dieser Bindungen sind in der [**WS \_ BINDING TEMPLATE \_ \_ TYPE-Definition**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) aufgeführt. Beispiel für die folgende Bindung in wsdl

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil generiert den [**Bindungsvorlagentyp WS \_ HTTP BINDING TEMPLATE \_ \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) für diese Bindung.

Richtlinienbeschreibungen

Mit der Eingaberichtlinieneinstellung generiert wsutil eine Reihe von Richtlinienbeschreibungen, die die Eingaberichtlinie beschreiben, einschließlich des Vorlagentyps sowie der in der Richtlinie angegebenen Werte. Zum Beispiel für die Eingabe

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil generiert eine Beschreibung der Channeleigenschaft wie folgt:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Alle Richtlinieneinstellungen (Kanaleigenschaften, Sicherheitseigenschaften und Sicherheitsbindungseigenschaften) in einer Bindung werden in einer \_ WS-BindungTemplateType \_ POLICY \_ DESCRIPTION-Struktur aggregiert. [**WS \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) gibt die verschiedenen Bindungsrichtlinienkombinationen an, die wsutil unterstützt.

Vorlagenstruktur, die nach Anwendung ausgefüllt werden soll

Die Richtlinienbeschreibung enthält alle Richtlinieninformationen, die in den Eingabemetadaten für eine bestimmte Bindung angegeben sind. Es gibt jedoch Informationen, die in der Richtlinie noch nicht dargestellt werden können und benutzereingaben erfordern, wenn diese Richtlinieneinstellung zum Erstellen eines Dienstproxys und/oder Dienstendpunkts verwendet wird. Beispielsweise muss die Anwendung Anmeldeinformationen für die HTTP-Headerauthentifizierung bereitstellen.

Die Anwendung muss die Vorlagenstruktur namens WS \_ bindingTemplateType \_ BINDING TEMPLATE für jeden anderen \_ Bindungsvorlagentyp ausfüllen, der in webservices.h definiert ist:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

Die Liste der Sicherheitsbindungsvorlagen ist optional und hängt von der übereinstimmenden Sicherheitsbindung ab. Beispielsweise wird das Feld [**WS \_ SSL TRANSPORT SECURITY BINDING \_ \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) in [**der \_ WS-HTTP-SSL-BINDUNGSVORLAGE \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) für die Anwendung angezeigt, um SSL-bezogene Sicherheitsbindungsinformationen einschließlich der Anmeldeinformationen bereitzustellen.

Die Anwendung muss alle Felder in dieser Struktur ausfüllen, bevor webservices-Vorlagen-APIs aufgerufen werden. Zusätzliche Sicherheitseigenschaften sowie Sicherheitsbindungseigenschaften, die in der Richtlinie nicht darstellbar sind, müssen ausgefüllt werden, und Webdienst-APIs führen die beiden Eigenschaften zur Laufzeit zusammen. Felder können ggf. auf null gesetzt werden. Beispielsweise können securityProperties auf null gesetzt werden, wenn keine zusätzlichen Sicherheitseigenschaften erforderlich sind.

Hilfsroutinen und Richtlinienbeschreibungsdeklaration in Headerdateien

wsutil erstellt eine Hilfsroutine, um eine bessere Unterstützung auf Dienstmodellebene zu ermöglichen, sodass die Anwendung Dienstproxy und Dienstendpunkt einfacher erstellen kann. Die Richtlinienbeschreibung wird auch verfügbar gemacht, sodass sie von der Anwendung direkt verwendet werden können. Eine CreateSerivceProxy-Hilferoutine sieht wie folgt aus:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Entwicklern wird empfohlen, diese Hilfsroutinen zu verwenden, sie können jedoch auch direkt die von webservices.dll bereitgestellte Laufzeitroutine verwenden. Entwicklern wird nicht empfohlen, die Richtlinienbeschreibungen direkt zu verwenden, wenn sie mithilfe der [Dienstmodellebene](service-model-layer-overview.md) programmieren.

Verweise auf Richtlinienbeschreibungen werden auch im Header für erweiterte Benutzer generiert. Wenn Entwickler keine Dienstmodellfunktionen verwenden, können sie die Richtlinienbeschreibungen direkt verwenden.

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

Definition von Prototypen in Stubdateien

Ein einzelnes Richtlinienbeschreibungsstrukturfeld pro Bindung und die zugehörigen intern referenzierten Hilfsbeschreibungen werden in der lokalen Prototypstruktur erstellt. Die Richtlinienbeschreibungen werden in der Datei generiert, in der die [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) generiert wird. Im Allgemeinen müssen Entwickler die Stubdatei während der Entwicklung nicht überprüfen, obwohl die Stubdatei alle Details zu den Richtlinienspezifikationen enthält.

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Implementierung von Hilfsroutinen in den Stubdateien

Wsutil generiert Hilfsprogrammroutinen, um Anwendungsaufrufe von [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) zu vereinfachen und [**WS \_ SERVICE \_ ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) auf Grundlage der Informationen in den Richtlinieneinstellungen zu erstellen.

Abhängig von den Bindungseinschränkungen, die für den angegebenen Port angegeben sind, unterscheidet sich das erste Argument je nach Vorlagenstruktur. Im folgenden Beispiel wird von HTTP-Transport ausgegangen. Die Signatur für die Erstellung des Dienstproxys ähnelt einem zusätzlichen Kanaltypparameter.

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>Unterstützte Richtlinieneinstellungen

In der folgenden Tabelle sind alle unterstützten Bindungsvorlagentypen, die übereinstimmenden Sicherheitsbindungen, die für den Typ erforderlich sind, die Vorlagenstruktur, die von der Anwendung für den Typ ausgefüllt werden soll, und der Typ der übereinstimmenden Beschreibung aufgeführt. Die Anwendung muss die Vorlagenstruktur ausfüllen, während Anwendungsentwickler verstehen sollten, welche Sicherheitsbindungen in der angegebenen Richtlinie erforderlich sind.



| [**\_WS-BINDUNGSVORLAGENTYP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Sicherheitsbindungskombinationen                                                                                                                                                                                                                                                                                                               | Vorlagenstruktur, die nach Anwendung ausgefüllt werden soll                                                                                            | Richtlinienbeschreibung                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ WS-HTTP-BINDUNGSVORLAGENTYP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**\_ \_ WS-HTTP-BINDUNGSVORLAGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**\_WS-HTTP-RICHTLINIENBESCHREIBUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**\_ \_ WS-HTTP-SSL-BINDUNGSVORLAGENTYP \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_ \_ WS-SSL-TRANSPORTSICHERHEITSBINDUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**\_ \_ WS-HTTP-SSL-BINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**BESCHREIBUNG DER \_ WS-HTTP-SSL-RICHTLINIE \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**VORLAGENTYP DER \_ WS-HTTP-HEADER-AUTHENTIFIZIERUNGSBINDUNG \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**WS \_ HTTP \_ HEADER \_ AUTH SECURITY BINDING (WS-HTTP-HEADER-AUTHENTIFIZIERUNGSSICHERHEITSBINDUNG) \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_ \_ \_ WS-HTTP-HEADER-AUTHENTIFIZIERUNGSBINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**BESCHREIBUNG DER \_ WS-HTTP-HEADERAUTHENTIFIZIERUNGSRICHTLINIE \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**VORLAGENTYP DER \_ WS-HTTP-SSL-HEADER-AUTHENTIFIZIERUNGSBINDUNG \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ \_ \_ \_ SSL-TRANSPORTSICHERHEITSBINDUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) UND [ **\_ WS-HTTP-HEADERAUTHENTIFIZIERUNGSSICHERHEITSBINDUNG \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**WS \_ HTTP SSL HEADER AUTH BINDING TEMPLATE (WS-HTTP-SSL-HEADER-AUTHENTIFIZIERUNGSVORLAGE) \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**BESCHREIBUNG DER \_ AUTHENTIFIZIERUNGSRICHTLINIE FÜR DEN WS-HTTP-SSL-HEADER \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**VORLAGENTYP FÜR DIE \_ WS-HTTP-SSL-BENUTZERNAMENBINDUNG \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ \_ \_ \_ SSL-TRANSPORTSICHERHEITSBINDUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) UND [ **\_ WS-BENUTZERNAME \_ \_ NACHRICHTENSICHERHEITSBINDUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**WS \_ HTTP \_ SSL \_ USERNAME \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**WS \_ HTTP \_ SSL \_ USERNAME \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**WS \_ HTTP SSL KERBEROS APREQ BINDING TEMPLATE TYPE (WS-HTTP-SSL-KERBEROS-APREQ-BINDUNGSVORLAGENTYP) \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ \_ \_ \_ SSL-TRANSPORTSICHERHEITSBINDUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) UND [ **WS \_ \_ KERBEROS-APREQ-NACHRICHTENSICHERHEITSBINDUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**WS \_ HTTP SSL KERBEROS APREQ BINDING TEMPLATE (WS-HTTP-SSL-KERBEROS-APREQ-BINDUNGSVORLAGE) \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**\_ \_ WS-TCP-BINDUNGSVORLAGENTYP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**\_ \_ WS-TCP-BINDUNGSVORLAGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**\_ \_ WS-TCP-RICHTLINIENBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**\_ \_ WS-TCP-SSPI-BINDUNGSVORLAGENTYP \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_ \_ WS-TCP-SSPI-TRANSPORTSICHERHEITSBINDUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**\_ \_ WS-TCP-SSPI-BINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**\_ \_ WS-TCP-SSPI-RICHTLINIENBESCHREIBUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**WS \_ TCP \_ SSPI \_ USERNAME \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ \_ \_ TCP-SSPI-TRANSPORTSICHERHEITSBINDUNG \_ \_ UND**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [ **WS \_ USERNAME MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**WS TCP SSPI USERNAME BINDING TEMPLATE (WS-VORLAGE FÜR DIE \_ \_ TCP-SSPI-BENUTZERNAMENBINDUNG) \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**WS \_ TCP \_ SSPI \_ USERNAME \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ \_ \_ TCP-SSPI-TRANSPORTSICHERHEITSBINDUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) UND [ **WS \_ \_ KERBEROS-APREQ-NACHRICHTENSICHERHEITSBINDUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**WS \_ TCP \_ SSPI KERBEROS APREQ BINDING TEMPLATE (WS-TCP-SSPI-KERBEROS-APREQ-BINDUNGSVORLAGE) \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**WS \_ HTTP \_ SSL \_ USERNAME \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ SSL \_ TRANSPORT SECURITY BINDING \_ \_ und**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) with [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) in bootstrap channel                         | [**WS \_ HTTP \_ SSL \_ USERNAME \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**WS \_ HTTP \_ SSL \_ USERNAME \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ SSL \_ TRANSPORT SECURITY BINDING \_ \_ und**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) with [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) in bootstrap channel            | [**WS \_ HTTP SSL KERBEROS APREQ SECURITY CONTEXT BINDING TEMPLATE (WS-HTTP \_ SSL \_ \_ KERBEROS-APREQ-SICHERHEITSKONTEXTBINDUNGSVORLAGE) \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING und**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) with [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) in bootstrap channel              | [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING und**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) with [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) in bootstrap channel | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Beispielsweise gibt [**WS \_ HTTP SSL BINDING TEMPLATE \_ \_ \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) an, dass die Eingaberichtlinie für die Bindung HTTP-Transport und [**WS SSL TRANSPORT SECURITY \_ BINDING \_ \_ \_ angibt.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Die Anwendung muss die [**\_ WS-HTTP-SSL-BINDUNGSVORLAGE-Struktur \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) ausfüllen, bevor die Hilfsroutinen aufrufen, und die entsprechende Richtlinienbeschreibung lautet [**WS \_ HTTP SSL \_ POLICY \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). Genauer gesagt enthält der Bindungsabschnitt in WSDL die folgenden Segmente:

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>Unterstützung des Sicherheitskontexts

Im [Sicherheitskontext](security-context.md)wird der Bootstrapkanal erstellt, um die sichere Konversation im Dienstkanal zu erstellen. Wsutil unterstützt nur das Szenario, in dem der Bootstrapkanal mit dem Dienstkanal identisch ist und dieselben Kanaleigenschaften und Sicherheitseigenschaften aufweist. Transportsicherheit ist für die Bindung von Sicherheitskontextnachrichten erforderlich. wsutil unterstützt Bootstrapkanäle mit anderen Nachrichtensicherheitsbindungen, unterstützt jedoch nur den Sicherheitskontext als einzige Nachrichtensicherheitsbindung im Dienstkanal, ohne Kombination mit anderen Nachrichtensicherheitsbindungen. Entwickler können diese Kombinationen außerhalb der Richtlinienvorlagenunterstützung unterstützen.

Die folgende Enumeration ist Teil der Richtlinienunterstützung:

-   [**\_WS-BINDUNGSVORLAGENTYP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Die folgenden Funktionen sind Teil der Richtlinienunterstützung:

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Die folgenden Strukturen sind Teil der Richtlinienunterstützung:

-   [**\_ \_ WS-HTTP-BINDUNGSVORLAGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**\_ \_ \_ WS-HTTP-HEADERAUTHENTIFIZIERUNGSBINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**BESCHREIBUNG DER \_ WS-HTTP-HEADERAUTHENTIFIZIERUNGSRICHTLINIE \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**BESCHREIBUNG DER \_ WS-HTTP-HEADERAUTHENTIFIZIERUNGSSICHERHEITSBINDUNGSRICHTLINIE \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**SICHERHEITSBINDUNGSVORLAGE FÜR \_ \_ \_ WS-HTTP-HEADERAUTHENTIFIZIERUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**\_ \_ WS-HTTP-RICHTLINIENBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**\_ \_ \_ WS-HTTP-SSL-BINDUNGSVORLAGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**\_ \_ \_ \_ WS-HTTP-SSL-HEADERAUTHENTIFIZIERUNGSBINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**BESCHREIBUNG DER \_ \_ WS-HTTP-SSL-HEADERAUTHENTIFIZIERUNGSRICHTLINIE \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**WS \_ HTTP SSL KERBEROS APREQ BINDING TEMPLATE (WS-HTTP-SSL-KERBEROS-APREQ-BINDUNGSVORLAGE) \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**WS \_ HTTP SSL KERBEROS APREQ SECURITY CONTEXT BINDING TEMPLATE (WS-HTTP \_ SSL \_ \_ KERBEROS-APREQ-SICHERHEITSKONTEXTBINDUNGSVORLAGE) \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**WS \_ HTTP SSL POLICY DESCRIPTION (WS-HTTP-SSL-RICHTLINIENBESCHREIBUNG) \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**WS \_ HTTP SSL USERNAME BINDING TEMPLATE (WS-VORLAGE FÜR DIE \_ HTTP-SSL-BENUTZERNAMENBINDUNG) \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**WS \_ HTTP \_ SSL \_ USERNAME \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**WS \_ HTTP \_ SSL \_ USERNAME \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**WS \_ HTTP \_ SSL \_ USERNAME \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**WS \_ \_ KERBEROS-APREQ-NACHRICHTENSICHERHEITSBINDUNGSVORLAGE \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**BESCHREIBUNG DER \_ SICHERHEITSBINDUNGSRICHTLINIE \_ FÜR \_ \_ WS-SICHERHEITSKONTEXTNACHRICHTEN \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**\_ \_ \_ \_ WS-SICHERHEITSKONTEXTMELDUNGS-SICHERHEITSBINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**BESCHREIBUNG DER \_ \_ WS-SICHERHEITSKONTEXT-SICHERHEITSBINDUNGSRICHTLINIE \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**\_ \_ \_ WS-SICHERHEITSKONTEXT-SICHERHEITSBINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**BESCHREIBUNG DER \_ WS-SSL-TRANSPORTSICHERHEITSBINDUNGSRICHTLINIE \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**WS \_ \_ SSL-TRANSPORTSICHERHEITSBINDUNGSVORLAGE \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**BESCHREIBUNG DER \_ WS SSPI-TRANSPORTSICHERHEITSBINDUNGSRICHTLINIE \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**\_ \_ WS-TCP-BINDUNGSVORLAGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**\_ \_ WS-TCP-RICHTLINIENBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**\_ \_ WS-TCP-SSPI-BINDUNGSVORLAGE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**WS \_ TCP \_ SSPI KERBEROS APREQ BINDING TEMPLATE (WS-TCP-SSPI-KERBEROS-APREQ-BINDUNGSVORLAGE) \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**\_ \_ WS-TCP-SSPI-RICHTLINIENBESCHREIBUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**\_ \_ \_ WS-TCP-SSPI-TRANSPORTSICHERHEITSBINDUNGSVORLAGE \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**WS TCP SSPI USERNAME BINDING TEMPLATE (WS-VORLAGE FÜR DIE \_ \_ TCP-SSPI-BENUTZERNAMENBINDUNG) \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**WS \_ TCP \_ SSPI \_ USERNAME \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**WS \_ USERNAME \_ MESSAGE \_ SECURITY \_ BINDING \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**WS \_ USERNAME \_ MESSAGE \_ SECURITY \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




