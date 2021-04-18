---
title: Vertrag
description: Ein Dienstvertrag enthält Metadaten, die definieren, wie ein Dienst Kanalnachrichten verarbeitet.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Vertragsweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104567808"
---
# <a name="contract"></a>Vertrag

Ein Dienstvertrag enthält Metadaten, die definieren, wie ein Dienst Kanalnachrichten verarbeitet.


Ein [**WS- \_ Dienst \_ Vertrag**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) enthält Metadaten für einen Dienst, der eine [WS- \_ Nachricht](ws-message.md)verarbeitet.

![Diagramm, das WS_SERVICE_CONTRACT Metadaten in einer Nachricht an einen Dienst Endpunkt zeigt.](images/servicecontractintro.png)

Sie verfügt über eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) und eine Funktions Tabelle. Eine Anwendung kann optional den [**\_ \_ \_ Empfangs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)für den WS-Dienst angeben.

Wenn eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) und eine Funktions Tabelle nicht angegeben werden, muss die Anwendung den [**\_ \_ \_ Empfangs \_ Rückruf für die WS-Dienst Nachricht**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)angeben.

![Das Diagramm zeigt die Vorgänge zum Addieren und Subtrahieren von Diensten im ICalculator-Dienstvertrag.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Weitere Informationen finden Sie im [Rechner](httpcalculatorserviceexample.md) Beispiel.

Vertragsbeschreibung

[**WS \_ Bei der Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) handelt es sich um Metadaten, die den typvertrag des Dienstanbieter definieren Wird von [wsutil.exe](web-service-compiler-tool.md)generiert.

Im Hinblick auf WSDL wird eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) einem WSDL: PortType zugeordnet. Für jeden WSDL: portType im WSDL-Dokument wird eine separate **WS- \_ Vertrags \_ Beschreibung** generiert.

Eine Vertragsbeschreibung besteht aus einem oder mehreren [Dienst Vorgängen](service-operation.md). Diese Vorgänge werden als Array von WS- [**\_ Vorgangs \_ Beschreibungen**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)angegeben.

![Diagramm, das eine WS_CONTRACT_DESCRIPTION als Array von WS_OPERATION_DESCRIPTIONs anzeigt.](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Ausführliche Informationen zur Konvertierung von WSDL: portType zur [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) finden Sie im [Abschnitt WSDL-Ausgabe](wsdl-support.md).

Beispiel: [ **WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Funktions Tabelle

Die Funktions Tabelle ist eine Struktur von Funktions Zeigern, die die einzelnen [Dienst Vorgänge](service-operation.md) im Dienstvertrag darstellen. Die Definition der Funktions Tabelle wird auch von [wsutil.exe](web-service-compiler-tool.md)generiert.

Beispiel: Funktions Tabelle

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

Verwenden des [ **WS- \_ Dienst- \_ Nachrichten \_ Empfangs \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ Der \_ \_ Empfangs \_ Rückruf für Dienst Nachrichten**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) hat eine zweiseitig ausschließende Rolle.

Wenn eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für den [**WS- \_ Dienst \_ Vertrag**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)angegeben wird, wird dies zum Standard Nachrichten Handler für alle Aktionen, die von der angegebenen **WS- \_ Vertrags \_ Beschreibung** nicht unterstützt werden. Andernfalls, wenn die **WS- \_ Vertrags \_ Beschreibung** für den WS **- \_ Dienst \_ Vertrag** nicht angegeben wird und der [**WS-Dienst- \_ \_ Nachrichten \_ Empfangs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) für den **WS- \_ Dienst \_ Vertrag** angegeben wird, werden alle in den kommenden [Nachrichten](ws-message.md) an diesen Rückruf weitergeleitet.

Weitere Beispiele finden Sie unter.

-   [Beispiel für nicht typisierten Dienst](untypedserviceexample.md)
-   [Beispiel für den Rechner Dienst](httpcalculatorserviceexample.md)
-   [Dienst Vorgänge](service-operation.md)

Die folgenden Rückrufe sind Teil des Vertrags:

-   [**WS- \_ Dienst- \_ Nachrichten \_ Empfangs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**WS- \_ Dienst- \_ Stub- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Die folgenden Strukturen sind Teil des Vertrags:

-   [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**WS- \_ Dienst \_ Vertrag**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




