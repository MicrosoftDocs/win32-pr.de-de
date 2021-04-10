---
title: Dienst Vorgang
description: Der Dienst Vorgang ist der Code und die Metadaten, die einem bestimmten Dienst Vorgang zugeordnet sind.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Dienst Vorgangs-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e7883c0988189db3d977a78615c024dc92df36
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "103961086"
---
# <a name="service-operation"></a>Dienst Vorgang

Der Dienst Vorgang ist der Code und die Metadaten, die einem bestimmten Dienst Vorgang zugeordnet sind.


Im Hinblick auf WSDL ist jeder WSDL:-Vorgang, der im WSDL-Dokument für einen bestimmten PortType definiert ist, ein Dienst Vorgang.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Jeder Dienst Vorgang innerhalb des Dienst Modells wird als [**WS- \_ Vorgangs \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)angegeben. Die \_ Beschreibung des WS-Vorgangs \_ wird von [wsutil.exe](web-service-compiler-tool.md)generiert.

Für jeden WSDL:-Vorgang generiert das Tool eine separate [**WS- \_ Vorgangs \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagramm, das zeigt, wie wsutil.exe eine WS_CONTRACT_DESCRIPTION generiert.](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

Im Hinblick auf den Code verfügt jeder Dienst Vorgang über eine zugeordnete Funktion. Die Definition dieser Funktion ist für Client und Server unterschiedlich.

Dienst Vorgänge werden in klassifiziert,

-   [Client seitige Dienst Vorgänge](client-side-service-operations.md)
-   [Server seitige Dienst Vorgänge](server-side-service-operations.md)

Diese Klassifizierung basiert hauptsächlich auf dem Signatur Layout des Servers und den Client seitigen Implementierungen von Dienst Vorgängen.

Siehe auch [Abschnitt WSDL-Unterstützung](wsdl-support.md).

Die folgenden Enumerationen werden bei Dienst Vorgängen verwendet:

-   [**WS \_ - \_ Parametertyp**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**Grund für WS- \_ Dienst \_ Abbruch \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**WS- \_ Dienst \_ Vorgangs \_ Nachrichten \_ Option**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Die folgenden Strukturen werden bei Dienst Vorgängen verwendet:

-   [**Beschreibung der WS- \_ Nachricht \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**Beschreibung des WS- \_ Vorgangs \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**Beschreibung der WS- \_ Parameter \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




