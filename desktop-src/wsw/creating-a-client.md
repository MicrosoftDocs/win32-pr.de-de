---
title: Erstellen eines Clients
description: Das Erstellen eines Clients für Webdienste wird in wwsapi durch die Dienstmodell-API und das WsUtil.exe Tool erheblich vereinfacht.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388743"
---
# <a name="creating-a-client"></a>Erstellen eines Clients

Das Erstellen eines Clients für Webdienste wird in wwsapi durch die [Dienstmodell](service-model-layer-overview.md) -API und das [WsUtil.exe](wsutil-compiler-tool.md) Tool erheblich vereinfacht. Das Dienstmodell stellt eine API zur Verfügung, die es dem Client ermöglicht, [Nachrichten](message.md) über einen [Kanal](channel.md) als C-Methodenaufrufe zu senden und zu empfangen. Das Tool "wsutil" generiert Header und Hilfsprogramme zum Implementieren des Clients. Diese Header enthalten die Typen und Funktionsprototypen für C-Funktionen, die die Dienste darstellen, die vom Zielweb Dienst angeboten werden. Die Hilfsprogramme werden zum Erstellen des Dienst Proxys verwendet, der die Bindungs Informationen und die [Endpunkt Adresse](endpoint-address.md) für den Dienst enthält.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Verwenden von wsutil zum Generieren von Headern und Hilfsprogrammen

Um die Header und Hilfsprogramme zu generieren, öffnet und liest wsutil die Metadatendateien für den Ziel Dienst – WSDL-und XSD-Dateien – und konvertiert sie in Header. Daher ist es erforderlich, die Metadatendateien für den Ziel Dienst vorab abzurufen, z. b. mithilfe von Svcutil, einem Teil der Windows Communication Foundation. Aus Sicherheitsgründen ist es zwingend erforderlich, dass die Kopien dieser Dateien vertrauenswürdig sind. (Weitere Informationen finden Sie im Abschnitt "Sicherheit" des Themas " [wsutil Compiler Tool](wsutil-compiler-tool.md) ".)

Verwenden Sie zum Ausführen von wsutil die folgende Befehlszeilen Syntax, wenn sich die WSDL-und XSD-Dateien für den Dienst in Ihrem eigenen Verzeichnis befinden: `WsUtil.exe *.wsdl *.xsd` . Alternativ können Sie die Dateien nach vollständigem Namen angeben.

Wsutil generiert im Allgemeinen zwei Dateien für jede Metadatendatei: einen Header und eine C-Datei. Fügen Sie dem Codierungs Projekt diese Dateien hinzu, und verwenden \# Sie include-Anweisungen, um Sie in den Code für den Client einzufügen. (Die XSD-Dateien stellen Typen dar, und die WSDL-Dateien stellen Vorgänge dar.)

## <a name="creating-the-service-proxy"></a>Erstellen des Dienst Proxys

Der von wsutil generierte Header enthält eine Hilfsroutine zum Erstellen des Dienst Proxys mit der erforderlichen Bindung. Diese Routine ist im Abschnitt "Richtlinien Hilfsroutinen" der generierten Header Datei enthalten. Beispielsweise enthält die generierte Kopfzeile für den Rechner Dienst, der im [httpcalculatorclientexample](httpcalculatorclientexample.md) -Beispiel veranschaulicht wird, den folgenden Funktionsprototyp.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Integrieren Sie dieses Hilfsprogramm in Ihren Code, und übergeben Sie ein [WS- \_ Dienst \_ Proxy](ws-service-proxy.md) handle, um das Handle für den erstellten Dienst Proxy zu empfangen. Im einfachsten Szenario, in dem nur ein Dienst Proxy Handle und ein Fehler Objekt an die Funktion übermittelt werden, sieht der-Befehl wie folgt aus.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Um den Adress Teil des Dienst Proxys zu erstellen, rufen Sie [**wsopenserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) mit einem Handle für den Dienst Proxy und einen Zeiger auf eine [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) mit der Adresse des Dienst Endpunkts auf, mit der Sie eine Verbindung herstellen möchten.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementieren des Clients mit Funktionsprototypen

Die aus den WSDL-Dateien des Diensts generierten Header enthalten auch C-Funktionsprototypen, die die vom Webdienst verfügbaren Dienste darstellen und die für die erforderliche Bindung spezifisch sind. Beispielsweise enthält ein Header, der für den in httpcalculatorserviceexample dargestellten Rechner Dienst generiert wird, den folgenden Prototyp für den Multiplikations Vorgang dieses dienstanders.

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

Sie können die Prototypen kopieren und als Vorlagen verwenden, um die Funktionsaufrufe in Ihrem Client zu codieren. in jedem Fall übergeben Sie das Handle an den Dienst Proxy. Wenn Sie mit dem Dienst Proxy fertig sind, wenden Sie sich an [**wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).

 

 




