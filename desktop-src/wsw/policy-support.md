---
title: Richtlinien Unterstützung
description: Wsutil verarbeitet die in den Eingabe Metadaten angegebene Richtlinie und generiert Hilfsroutinen für die Dienstmodell Unterstützung.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Richtlinien Support-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aafcd481fd4ea8a8cc6782a5dc50655fb9255c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310575"
---
# <a name="policy-support"></a>Richtlinien Unterstützung

Wsutil verarbeitet die in den Eingabe Metadaten angegebene Richtlinie und generiert Hilfsroutinen für die Dienstmodell Unterstützung.

## <a name="how-to-use-policy-support-in-wsutil"></a>Verwenden der Richtlinien Unterstützung in wsutil

Entwickler sollten die folgenden Schritte ausführen, um die Richtlinien Unterstützung im wsutil-Compiler zu verwenden:

-   Sammeln Sie alle Eingabe Metadatendateien, die für den Zielweb Dienst erforderlich sind.
-   Kompilieren Sie alle gesammelten WSDL-/XSD-/Richtliniendateien mit wsutil.exe. Wsutil generiert einen Satz von Stub-Datei-und Header Dateien für jede WSDL-und XSD-Eingabedatei.
-   Generierte Header Datei untersuchen: alle Namen der Richtlinien Hilfsobjekte werden im Kommentar Abschnitt am Anfang der Header Datei aufgeführt.
-   Verwenden \_ Sie zum Erstellen des Dienst Proxys die Hilfsroutine bindingName von "dedienst Proxy".
-   Verwenden \_ Sie zum Erstellen eines Dienst Endpunkts die Hilfsroutine bindingName "kreateserviceendpoint".
-   Fügen Sie \_ die Bindungs Vorlagen Struktur von WS bindingtemplatetype ein, \_ \_ die in der Methoden Signatur angegeben ist. Entwickler können nach Bedarf zusätzliche Channeleigenschaften und/oder Sicherheitseigenschaften bereitstellen.
-   Ruft die hilfroutinen auf, wenn ein erfolgreicher Rückgabe Dienst Proxy oder Dienst Endpunkt erstellt wurde.

In den folgenden Abschnitten werden verwandte Themen ausführlich beschrieben.

## <a name="handle-policy-input"></a>Behandeln von Richtlinien Eingaben

Im folgenden finden Sie [Compileroptionen](web-service-compiler-tool.md) im Zusammenhang mit der Richtlinien Verarbeitung.

Standardmäßig generiert wsutil immer Richtlinien Vorlagen, es sei denn, Sie werden mit der Option "/nopolicy" aufgerufen. Die Richtlinie kann als Teil einer WSDL-Datei eingebettet werden oder separat als eine Richtlinien Metadatendatei erstellt werden, die von wsutil als Eingabe benötigt wird. Die Compileroption "/wsp:" wird verwendet, um anzugeben, dass es sich bei den angegebenen Eingabe Metadaten um eine Richtlinien Datei handelt. Wsutil generiert mögliche Richtlinien bezogene Hilfsprogramme mit der folgenden Kompilierung:

**wsutil/WSDL: Trusted. WSDL/WSDL: trusted1. WSDL**

**wstuil/WSDL: Input. WSDL/wsp: Policy. wsp**

Wenn die Option "/nopolicy" verwendet wird, werden keine Richtlinien Hilfen generiert, wie im folgenden Beispiel gezeigt.

**wsutil/nopolicy/WSDL: Trusted. WSDL/WSDL: trusted1. WSDL**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Vom wsutil-Compiler generierter Richtlinien bezogener Code

Die Seite " [metadatenzuordnung](metadata-mapping.md) " beschreibt die Zuordnung zwischen Metadatenkonstrukten mit unterschiedlichen Bindungs Typen

In den Richtlinien Einstellungen können drei Kategorien von Richtlinien Einstellungen angegeben werden:

-   Kanaleigenschaften. Zurzeit werden nur die folgenden Kanaleigenschaften unterstützt: [**WS- \_ \_ channeleigenschaftencodierung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **\_ \_ \_ \_ Versions Adressierung von WS-Kanälen** und **\_ \_ \_ Umschlag \_ Version der WS-Channeleigenschaft**.
-   Sicherheitseigenschaften. Zurzeit werden nur die folgenden Sicherheitseigenschaften unterstützt: die [**Verwendung der WS- \_ Sicherheits \_ Eigenschaft \_ \_ Zeitstempel**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), das Sicherheits **\_ \_ \_ \_ Header \_ Layout der WS-Sicherheits Eigenschaft**, die WS- **\_ Sicherheits \_ Eigenschaft \_ Transport \_ Schutz \_ Ebene** und die Sicherheits **\_ \_ \_ \_ Header \_ Version der WS-Sicherheits Eigenschaft**
-   Sicherheitsbindung. Zurzeit werden nur die folgenden Sicherheits Bindungen unterstützt: WS-HTTP-Header Authentifizierung- [**\_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding), [**WS-SSL- \_ \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding), [**WS TCP- \_ \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding), [**WS \_ username \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), [**WS \_ Kerberos \_ apreq \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)und [**WS \_ Security \_ context \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Bindungs Vorlagentyp

Es gibt eine begrenzte Anzahl von Bindungen, die in wsutil unterstützt werden. Alle unterstützten Kombinationen dieser Bindungen sind unter [**WS \_ Binding \_ template \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) Definition aufgeführt. Beispielsweise für die folgende Bindung in WSDL

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil generiert [**den \_ \_ \_ \_ typbindungs**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) Vorlagentyp der WS http-Bindungs Vorlage für diese Bindung.

Richtlinien Beschreibungen

Mit der Eingabe Richtlinien Einstellung generiert wsutil eine Reihe von Richtlinien Beschreibungen, die die Eingabe Richtlinie beschreiben, einschließlich des Vorlagen Typs sowie der in der Richtlinie angegebenen Werte. Beispielsweise für die Eingabe

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil generiert die Beschreibung einer Kanal Eigenschaft wie folgt:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Alle Richtlinien Einstellungen (Kanaleigenschaften, Sicherheitseigenschaften und Eigenschaften der Sicherheitsbindung) in einer Bindung werden in einer WS \_ bindingtemplatetype- \_ Richtlinien \_ Beschreibungs Struktur aggregiert. [**WS \_ Bindungs \_ \_ Vorlagentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) gibt die verschiedenen Kombinationen von Bindungs Richtlinien an, die wsutil unterstützt

Vorlagen Struktur, die von der Anwendung ausgefüllt werden soll

Die Richtlinien Beschreibung enthält alle Richtlinien Informationen, die in den Eingabe Metadaten für eine bestimmte Bindung angegeben sind. es gibt jedoch Informationen, die in der Richtlinie nicht dargestellt werden können, erfordert jedoch eine Benutzereingabe, wenn diese Richtlinien Einstellung zum Erstellen eines Dienst Proxys und/oder Dienst Endpunkts verwendet Beispielsweise muss die Anwendung Anmelde Informationen für die HTTP-Header Authentifizierung bereitstellen.

Die Anwendung muss die Vorlagen Struktur mit dem Namen "WS \_ bindingtemplatetype \_ Binding \_ Template" für jeden anderen Bindungs Vorlagentyp ausfüllen, der in "Webservices. h" definiert ist:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

Die Liste der sicherheitsbindungs Vorlagen ist optional, abhängig von der übereinstimmenden Sicherheitsbindung. Beispielsweise wird das Feld [**WS \_ SSL- \_ Transport \_ \_ sicherheitsbindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) in der [**WS HTTP-SSL- \_ \_ \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) für die Anwendung zur Bereitstellung von SSL-bezogenen sicherheitsbindungs Informationen, einschließlich der Anmelde Informationen, angezeigt.

Die Anwendung muss alle Felder in dieser Struktur ausfüllen, bevor Sie Webservices-Vorlagen-APIs aufrufen können. Zusätzliche Sicherheitseigenschaften sowie Eigenschaften von Sicherheits Bindungen, die in der Richtlinie nicht dargestellt werden können, müssen ausgefüllt werden, und Webdienst-APIs führt die beiden Eigenschaften in der Laufzeit zusammen. Felder können bei nicht zutreffend nulgeriert werden. Beispielsweise können securityproperties nulgeriert werden, wenn keine zusätzlichen Sicherheitseigenschaften erforderlich sind.

Hilfsroutinen und Richtlinien Beschreibungs Deklaration in Header Dateien

wsutil erstellt eine Hilfsroutine, um eine bessere Unterstützung in der Dienstmodell Ebene zu ermöglichen, damit die Anwendung den Dienst Proxy und Dienst Endpunkt vereinfachen kann. Die Richtlinien Beschreibung wird auch so verfügbar gemacht, dass Sie von der Anwendung direkt verwendet werden kann. Eine Hilfe Routine für "kreateserivceproxy" sieht wie folgt aus:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Entwicklern wird empfohlen, diese Hilfsroutinen zu verwenden, aber Sie können auch die untergeordnete Lauf Zeit Routine direkt verwenden, die von webservices.dll bereitgestellt wird. Entwicklern wird nicht empfohlen, die Richtlinien Beschreibungen direkt beim Programmieren mit der [Dienstmodell](service-model-layer-overview.md) Ebene zu verwenden.

Richtlinien Beschreibungs Verweise werden auch in der Kopfzeile für Advanced User generiert. Wenn Entwickler keine Dienstmodell Funktionen verwenden, können Sie die Richtlinien Beschreibungen direkt verwenden.

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

Definitions Prototypen in Stubdateien

In der lokalen prototypstruktur werden ein einzelnes Richtlinien Beschreibungs Strukturfeld pro Bindung und die intern referenzierten hilfsbeschreibungen erstellt. Die Richtlinien Beschreibungen werden in der Datei generiert, in der die [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) generiert wird. Im Allgemeinen müssen Entwickler die Stub-Datei während der Entwicklung nicht überprüfen, obwohl die Stub-Datei alle Details zu den Richtlinien Spezifikationen enthält.

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

Implementierung von Hilfsroutinen in den Stub-Dateien

Wsutil generiert Hilfsroutinen zum Vereinfachen von Anwendungs Aufrufen an [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) und zum Erstellen einer [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Basis anhand der Informationen in den Richtlinien Einstellungen.

Hängt von den Bindungs Einschränkungen ab, die für den angegebenen Port angegeben werden, das erste Argument unterscheidet sich entsprechend der Vorlagen Struktur. Im folgenden Beispiel wird die HTTP-Übertragung angenommen, die Signatur für die Erstellung des Dienst Proxys ähnelt einem zusätzlichen kanaltypparameter.

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

In der folgenden Tabelle sind alle unterstützten Bindungs Vorlagen Typen aufgeführt, die entsprechenden Sicherheits Bindungen, die im-Typ erforderlich sind, die Vorlagen Struktur, die von der Anwendung für den-Typ ausgefüllt werden soll, und der entsprechende Beschreibungs Typ. Die Anwendung muss die Vorlagen Struktur ausfüllen, während der Anwendungsentwickler wissen sollte, welche Sicherheits Bindungen in der angegebenen Richtlinie erforderlich sind.



| [**Typ der WS- \_ Bindungs \_ Vorlage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Kombinationen von Sicherheits Bindungen                                                                                                                                                                                                                                                                                                               | Vorlagen Struktur, die von der Anwendung ausgefüllt werden soll                                                                                            | Richtlinien Beschreibung                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Typ der WS- \_ http- \_ Bindungs \_ Vorlage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**WS- \_ http- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**Beschreibung der WS \_ http- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**Typ der WS \_ http- \_ SSL- \_ Bindungs \_ Vorlage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**WS \_ http- \_ SSL- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**Beschreibung der WS \_ http \_ SSL- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**\_ \_ \_ \_ Bindungs \_ \_ Vorlagentyp der WS-HTTP-Header Authentifizierung**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_ \_ \_ \_ Bindungs \_ Vorlage für die WS-HTTP-Header Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**Beschreibung der WS- \_ http- \_ Header Authentifizierungs \_ \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**\_ \_ \_ \_ \_ Bindungs \_ \_ Vorlagentyp der WS HTTP-SSL-Header Authentifizierung**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ Sicherheitsbindung für SSL- \_ Transport \_ \_ Sicherheit**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) und [ **WS-http- \_ \_ Header \_ \_ \_** Authentifizierung](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**\_ \_ \_ \_ \_ Bindungs \_ Vorlage für WS HTTP-SSL-Header Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**Beschreibung der WS \_ http \_ SSL-Header Authentifizierungs \_ \_ \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**\_ \_ \_ \_ Bindungs \_ \_ Vorlagentyp für WS HTTP-SSL-Benutzername**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) und [ **WS \_ username Message- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**\_Bindungs Vorlage für WS http- \_ SSL- \_ Benutzername \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**Beschreibung der WS \_ http- \_ SSL- \_ Benutzernamen \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**WS \_ http- \_ SSL- \_ Kerberos- \_ apreq- \_ Bindungs \_ \_ Vorlagentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) und [ **WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ \_ Sicherheitsbindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**WS \_ http- \_ SSL- \_ Kerberos- \_ apreq- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**Beschreibung der WS \_ http \_ SSL- \_ Kerberos- \_ apreq- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**Typ der WS- \_ TCP- \_ Bindungs \_ Vorlage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**WS- \_ TCP- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**Beschreibung der WS \_ TCP- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**WS \_ TCP \_ SSPI \_ Binding- \_ \_ Vorlagentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**WS- \_ TCP- \_ SSPI- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**Beschreibung der WS \_ TCP- \_ SSPI- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**WS \_ TCP \_ SSPI \_ username \_ Binding \_ template \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) und [ **WS \_ username \_ Message- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**WS \_ TCP \_ SSPI \_ username \_ Binding- \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**Beschreibung der WS \_ TCP \_ SSPI- \_ Benutzernamen \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Bindungs \_ \_ Vorlagentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) und [ **WS \_ Kerberos \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**Beschreibung der WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**WS \_ http \_ SSL \_ username \_ Security \_ context \_ Binding \_ template \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) und [**WS- \_ Sicherheits \_ Kontext Nachrichten \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) -Sicherheitsbindung mit [**WS \_ username \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) in Bootstrap Channel                         | [**WS \_ http \_ SSL \_ username- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**Beschreibung der WS \_ http \_ SSL \_ username- \_ Sicherheits \_ Kontext \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**WS \_ http \_ SSL \_ Kerberos \_ apreq- \_ Sicherheits \_ Kontext Bindungs \_ Vorlagentyp \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) und [**WS- \_ Sicherheits \_ Kontext \_ Nachrichten \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) -Sicherheitsbindung mit [**WS \_ Kerberos \_ apreq \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) in Bootstrap Channel            | [**WS \_ http \_ SSL \_ Kerberos \_ apreq- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**Beschreibung der WS \_ http \_ SSL \_ Kerberos \_ apreq- \_ Sicherheits \_ Kontext \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**WS \_ TCP \_ SSPI \_ username \_ Security \_ context \_ Binding \_ template \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) und [**WS- \_ Sicherheits \_ Kontext \_ Nachrichten \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) -Sicherheitsbindung mit [**WS \_ username \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) in Bootstrap Channel              | [**WS \_ TCP \_ SSPI \_ username- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**Beschreibung der WS \_ TCP \_ SSPI \_ username \_ Security \_ context- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Sicherheits \_ Kontext \_ Bindungs \_ \_ Vorlagentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) und [**WS- \_ Sicherheits \_ Kontext \_ Nachrichten \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) -Sicherheitsbindung mit [**WS \_ Kerberos \_ apreq \_ Message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) in Bootstrap Channel | [**WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**Beschreibung der WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Sicherheits \_ Kontext \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Beispielsweise gibt [**der \_ Typ der WS HTTP-SSL- \_ \_ Bindungs \_ \_ Vorlage**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) an, dass die Eingabe Richtlinie für die Bindung den HTTP-Transport und die [**WS SSL- \_ \_ Transport \_ \_ Sicherheitsbindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)angibt. Die Anwendung muss die [**WS \_ http- \_ SSL- \_ Bindungs \_ Vorlagen**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) Struktur ausfüllen, bevor die hilfroutinen aufgerufen werden, und die abgleichsrichtlinienbeschreibung lautet [**WS HTTP-SSL- \_ \_ \_ Richtlinien \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). Genauer gesagt enthält der Abschnitt Bindung in WSDL folgende Segmente:

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

## <a name="security-context-support"></a>Unterstützung von Sicherheits Kontexten

Im [Sicherheitskontext](security-context.md)wird der Bootstrap-Kanal erstellt, um die sichere Konversation im Dienst Kanal einzurichten. Wsutil unterstützt nur das Szenario, in dem Bootstrap-Channel mit den gleichen Kanaleigenschaften und Sicherheitseigenschaften identisch ist wie der Dienst Kanal. Die Transport Sicherheit ist für die Nachrichten Bindung im Sicherheitskontext erforderlich. wsutil unterstützt Bootstrap-Kanäle mit anderen Nachrichten Sicherheits Bindungen, unterstützt jedoch nur den Sicherheitskontext als die einzige Nachrichten Sicherheitsbindung im Dienst Kanal ohne Kombination mit anderen Nachrichten Sicherheits Bindungen. Entwickler können diese Kombinationen außerhalb der Unterstützung der Richtlinien Vorlage unterstützen.

Die folgende Enumeration ist Teil der Richtlinien Unterstützung:

-   [**Typ der WS- \_ Bindungs \_ Vorlage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Die folgenden Funktionen sind Teil der Richtlinien Unterstützung:

-   [**Wscreateserviceendpointfromtemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**Wscreateserviceproxyfromtemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Die folgenden Strukturen sind Teil der Richtlinien Unterstützung:

-   [**WS- \_ http- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**\_ \_ \_ \_ Bindungs \_ Vorlage für die WS-HTTP-Header Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**Beschreibung der WS- \_ http- \_ Header Authentifizierungs \_ \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**\_Beschreibung der \_ \_ \_ \_ \_ Richtlinie \_ zur Authentifizierung der WS-HTTP-Header Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**Beschreibung der WS \_ http- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**WS \_ http- \_ SSL- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**\_ \_ \_ \_ \_ Bindungs \_ Vorlage für WS HTTP-SSL-Header Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**Beschreibung der WS \_ http \_ SSL-Header Authentifizierungs \_ \_ \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**WS \_ http- \_ SSL- \_ Kerberos- \_ apreq- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**Beschreibung der WS \_ http \_ SSL- \_ Kerberos- \_ apreq- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**WS \_ http \_ SSL \_ Kerberos \_ apreq- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**Beschreibung der WS \_ http \_ SSL \_ Kerberos \_ apreq- \_ Sicherheits \_ Kontext \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**Beschreibung der WS \_ http \_ SSL- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**\_Bindungs Vorlage für WS http- \_ SSL- \_ Benutzername \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**Beschreibung der WS \_ http- \_ SSL- \_ Benutzernamen \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**WS \_ http \_ SSL \_ username- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**Beschreibung der WS \_ http \_ SSL \_ username- \_ Sicherheits \_ Kontext \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**Beschreibung der WS \_ Kerberos \_ apreq \_ Message \_ Security \_ Binding- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**Beschreibung der WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**Beschreibung der WS- \_ Sicherheits \_ Kontext- \_ Sicherheits \_ Bindungs \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**WS- \_ Sicherheits \_ Kontext- \_ \_ sicherheitsbindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**Beschreibung der WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**WS \_ SSL \_ - \_ Transport \_ sicherheitsbindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**Beschreibung der WS \_ SSPI- \_ Transport \_ \_ sicherheitsbindungs \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**WS- \_ TCP- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**Beschreibung der WS \_ TCP- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**WS- \_ TCP- \_ SSPI- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**Beschreibung der WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**Beschreibung der WS \_ TCP \_ SSPI- \_ Kerberos- \_ apreq- \_ Sicherheits \_ Kontext \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**Beschreibung der WS \_ TCP- \_ SSPI- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**WS \_ TCP \_ SSPI \_ - \_ Transport \_ sicherheitsbindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**WS \_ TCP \_ SSPI \_ username \_ Binding- \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**Beschreibung der WS \_ TCP \_ SSPI- \_ Benutzernamen \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**WS \_ TCP \_ SSPI \_ username- \_ Sicherheits \_ Kontext \_ Bindungs \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**Beschreibung der WS \_ TCP \_ SSPI \_ username \_ Security \_ context- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**Beschreibung der WS \_ username \_ Message \_ Security \_ Binding- \_ Richtlinie \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**WS \_ username \_ Message \_ Security \_ Binding- \_ Vorlage**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




