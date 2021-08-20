---
title: Vertrag
description: Ein Dienstvertrag enthält Metadaten, die definieren, wie ein Dienst Kanalnachrichten behandelt.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Vertragswebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69be302ace90c82b7b0db5666289cf4d312458e7283a04e2a1d892faa894ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026578"
---
# <a name="contract"></a>Vertrag

Ein Dienstvertrag enthält Metadaten, die definieren, wie ein Dienst Kanalnachrichten behandelt.


Ein [**\_ WS-DIENSTVERTRAG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) enthält Metadaten für einen Dienst zur Handhabung einer [ \_ WS-NACHRICHT.](ws-message.md)

![Diagramm, das WS_SERVICE_CONTRACT Metadaten in einer Nachricht an einen Dienstendpunkt zeigt.](images/servicecontractintro.png)

Sie verfügt über [**eine WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) und eine Funktionstabelle. Eine Anwendung kann optional [**WS \_ SERVICE MESSAGE RECEIVE \_ \_ \_ CALLBACK angeben.**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

Wenn keine [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) und eine Funktionstabelle angegeben werden, muss die Anwendung [**WS \_ SERVICE MESSAGE \_ RECEIVE \_ \_ CALLBACK angeben.**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

![Diagramm, das die Dienstvorgänge "Hinzufügen" und "Subtrahieren" im ICalculator-Dienstvertrag zeigt.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Weitere Informationen finden [Sie im](httpcalculatorserviceexample.md) Rechnerbeispiel.

Vertragsbeschreibung

[**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) sind Metadaten, die den Typvertrag des Diensts definieren. Wird von [wsutil.exe. ](web-service-compiler-tool.md)

Im Hinblick auf WSDL wird [**eine WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) einem wsdl:portType-Objekt (wsdl:portType) zuordnen. Für jeden wsdl:portType im WSDL-Dokument wird eine separate **WS \_ CONTRACT \_ DESCRIPTION** generiert.

Eine Vertragsbeschreibung besteht aus oder mehr [Dienstvorgängen.](service-operation.md) Diese Vorgänge werden als Array von [**WS \_ OPERATION DESCRIPTION \_ angegeben.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)

![Diagramm, das eine WS_CONTRACT_DESCRIPTION als Array von WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

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

Ausführliche Informationen zur Konvertierung von wsdl:portType in [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) finden Sie im [WSDL-Ausgabeabschnitt](wsdl-support.md).

Beispiel: [ **WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Funktionstabelle

Die Funktionstabelle ist eine Struktur von Funktionszedern, die die einzelnen [Dienstvorgänge](service-operation.md) im Dienstvertrag darstellen. Die Definition der Funktionstabelle wird auch von [wsutil.exe. ](web-service-compiler-tool.md)

Beispiel: Funktionstabelle

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

Verwenden des [ **WS \_ SERVICE \_ MESSAGE \_ \_ RECEIVE-RÜCKRUFS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ SERVICE \_ MESSAGE \_ RECEIVE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) hat eine zwei sich gegenseitig ausschließende Rolle.

Wenn eine [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für den [**WS SERVICE \_ \_ CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)angegeben wird, wird dies zum Standardmeldungshandler für alle Aktionen, die von der angegebenen WS CONTRACT DESCRIPTION nicht **unterstützt \_ \_ werden.** [](ws-message.md) Andernfalls, wenn **WS CONTRACT \_ \_ DESCRIPTION** nicht im **WS-DIENSTVERTRAG \_ \_** angegeben ist und der [**WS \_ SERVICE MESSAGE RECEIVE \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) im **\_ \_ WS-DIENSTVERTRAG** angegeben ist, werden alle in kommenden Nachrichten an diesen Rückruf übergeben.

Weitere Beispiele finden Sie unter

-   [Beispiel für einen nicht typisierten Dienst](untypedserviceexample.md)
-   [Beispiel für Rechnerdienst](httpcalculatorserviceexample.md)
-   [Dienstvorgänge](service-operation.md)

Die folgenden Rückrufe sind Teil des Vertrags:

-   [**WS \_ SERVICE \_ MESSAGE \_ RECEIVE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_ \_ WS-DIENSTSTUBRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Die folgenden Strukturen sind Teil des Vertrags:

-   [**\_WS-VERTRAGSBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**\_WS-DIENSTVERTRAG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




