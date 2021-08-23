---
title: Dienstvorgang
description: Dienstvorgang ist der Code und die Metadaten, die einem bestimmten Vorgang eines Diensts zugeordnet sind.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Service Operation Web Services für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acde0c2151dea483a3e82f45c7031fa201614076f7a5ea624926fbe08e7588b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026263"
---
# <a name="service-operation"></a>Dienstvorgang

Dienstvorgang ist der Code und die Metadaten, die einem bestimmten Vorgang eines Diensts zugeordnet sind.


Im Hinblick auf WSDL ist jeder wsdl:operation, der im WSDL-Dokument für einen bestimmten portType definiert ist, ein Dienstvorgang.

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

Jeder Dienstvorgang innerhalb des Dienstmodells wird als [**WS \_ OPERATION DESCRIPTION \_ angegeben.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) WS \_ OPERATION DESCRIPTION wird von \_wsutil.exe. [ ](web-service-compiler-tool.md)

Für jeden wsdl:operation generiert das Tool eine separate [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagramm, das zeigtwsutil.exe wie ein WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

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

Im Hinblick auf den Code ist jedem Dienstvorgang eine Funktion zugeordnet. Die Definition dieser Funktion ist für Client und Server unterschiedlich.

Dienstvorgänge werden in

-   [Clientseitige Dienstvorgänge](client-side-service-operations.md)
-   [Serverseitige Dienstvorgänge](server-side-service-operations.md)

Diese Klassifizierung basiert hauptsächlich auf dem Signaturlayout des Servers und den clientseitigen Implementierungen von Dienstvorgängen.

Weitere Informationen finden Sie [auch im Abschnitt zur WSDL-Unterstützung.](wsdl-support.md)

Die folgenden Enumerationen werden mit Dienstvorgängen verwendet:

-   [**\_WS-PARAMETERTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**WS \_ SERVICE \_ CANCEL \_ REASON**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**\_MELDUNGSOPTION \_ "WS-DIENSTVORGANG" \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Die folgenden Strukturen werden mit Dienstvorgängen verwendet:

-   [**\_WS-NACHRICHTENBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**\_WS-VORGANGSBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**\_WS-PARAMETERBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




