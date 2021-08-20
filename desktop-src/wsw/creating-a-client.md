---
title: Erstellen eines Clients
description: Das Erstellen eines Clients für Webdienste wird in WWSAPI durch die Dienstmodell-API und das WsUtil.exe erheblich vereinfacht.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ca04ef5fbbeef76cd32a0b6523391deb19957479cd5f332715972f3b5bfbc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026558"
---
# <a name="creating-a-client"></a>Erstellen eines Clients

Das Erstellen eines Clients für Webdienste wird in [](service-model-layer-overview.md) WWSAPI durch die Dienstmodell-API und dasWsUtil.exe[erheblich](wsutil-compiler-tool.md) vereinfacht. Das Dienstmodell stellt eine API bereit, mit der [](channel.md) der Client Nachrichten über einen Kanal senden und [empfangen](message.md) kann, wenn die C-Methode aufruft. Das WsUtil-Tool generiert Header und Hilfsprogramm für die Implementierung des Clients. Diese Header enthalten die Typen und Funktionsprototypen für C-Funktionen, die die vom Zielwebdienst angebotenen Dienste darstellen. Die Hilfsdienste werden verwendet, um den Dienstproxy zu erstellen, der die Bindungsinformationen und die [Endpunktadresse für](endpoint-address.md) den Dienst enthält.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Verwenden von WsUtil zum Generieren von Headern und Hilfsdateien

Zum Generieren der Header und Hilfselemente öffnet WsUtil die Metadatendateien für den Zieldienst ( wsdl- und xsd-Dateien) und liest sie in Header. Daher ist es erforderlich, die Metadatendateien für den Zieldienst im Voraus abzurufen, z. B. mithilfe von SvcUtil, einem Teil der Windows Communication Foundation. Aus Sicherheitsgründen ist es zwingend erforderlich, dass Ihre Kopien dieser Dateien vertrauenswürdig sind. (Weitere Informationen finden Sie im Abschnitt "Sicherheit" des [Themas WsUtil Compiler Tool.)](wsutil-compiler-tool.md)

Verwenden Sie zum Ausführen von WsUtil die folgende Befehlszeilensyntax, wenn sich die WSDL- und XSD-Dateien für den Dienst in ihrem eigenen Verzeichnis befinden: `WsUtil.exe *.wsdl *.xsd` . Alternativ können Sie die Dateien mit dem vollständigen Namen angeben.

WsUtil generiert in der Regel zwei Dateien für jede Metadatendatei: einen Header und eine C-Datei. Fügen Sie diese Dateien Ihrem Codierungsprojekt hinzu, und verwenden Sie \# include-Anweisungen, um sie in den Code für Ihren Client ein beispielen zu lassen. (Die XSD-Dateien stellen Typen dar, und die WSDL-Dateien stellen Vorgänge dar.)

## <a name="creating-the-service-proxy"></a>Erstellen des Dienstproxys

Der von WsUtil generierte Header enthält eine Hilfsroutine zum Erstellen des Dienstproxys mit der erforderlichen Bindung. Diese Routine ist im Abschnitt "Richtlinien-Hilfsroutinen" der generierten Headerdatei enthalten. Beispielsweise enthält der generierte Header für den Rechnerdienst, der im [Beispiel httpcalculatorclientexample](httpcalculatorclientexample.md) veranschaulicht wird, den folgenden Funktionsprototyp.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Integrieren Sie dieses Hilfsdienst in Ihren Code, und übergeben Sie ein [WS \_ SERVICE \_ PROXY-Handle,](ws-service-proxy.md) um das Handle an den erstellten Dienstproxy zu empfangen. Im einfachsten Szenario, in dem nur ein Dienstproxyhand handle und ein Fehlerobjekt an die Funktion übergeben werden, sieht der Aufruf wie folgt aus.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Um den Adressteil des Dienstproxys zu erstellen, rufen Sie [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) mit einem Handle für den Dienstproxy und einem Zeiger auf eine [**\_ WS-ENDPUNKTADRESSE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) auf, die die Dienstendpunktadresse enthält, mit der Sie eine Verbindung herstellen möchten.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementieren des Clients mit Funktionsprototypen

Die headers, die aus den WSDL-Dienstdateien generiert werden, enthalten auch C-Funktionsprototypen, die die vom Webdienst verfügbaren und für die erforderliche Bindung spezifischen Dienste darstellen. Beispielsweise enthält ein Header, der für den in HttpCalculatorServiceExample dargestellten Rechnerdienst generiert wird, den folgenden Prototyp für den Multiplikationsvorgang dieses Diensts.

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

Sie können die Prototypen kopieren und als Vorlagen zum Codieren der Funktionsaufrufe in Ihrem Client verwenden, indem Sie in jedem Fall das Handle an den Dienstproxy übergeben. Wenn Sie mit dem Dienstproxy fertig sind, rufen [**Sie WsCloseServiceProxy auf.**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)

 

 




