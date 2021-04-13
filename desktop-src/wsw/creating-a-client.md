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
# <a name="creating-a-client"></a><span data-ttu-id="35bb5-103">Erstellen eines Clients</span><span class="sxs-lookup"><span data-stu-id="35bb5-103">Creating a Client</span></span>

<span data-ttu-id="35bb5-104">Das Erstellen eines Clients für Webdienste wird in wwsapi durch die [Dienstmodell](service-model-layer-overview.md) -API und das [WsUtil.exe](wsutil-compiler-tool.md) Tool erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="35bb5-104">Creating a client for Web services is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="35bb5-105">Das Dienstmodell stellt eine API zur Verfügung, die es dem Client ermöglicht, [Nachrichten](message.md) über einen [Kanal](channel.md) als C-Methodenaufrufe zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="35bb5-105">The Service Model provides an API that enables the client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="35bb5-106">Das Tool "wsutil" generiert Header und Hilfsprogramme zum Implementieren des Clients.</span><span class="sxs-lookup"><span data-stu-id="35bb5-106">The WsUtil tool generates headers and helpers for implementing the client.</span></span> <span data-ttu-id="35bb5-107">Diese Header enthalten die Typen und Funktionsprototypen für C-Funktionen, die die Dienste darstellen, die vom Zielweb Dienst angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="35bb5-107">These headers include the types and function prototypes for C functions representing the services offered by the target Web service.</span></span> <span data-ttu-id="35bb5-108">Die Hilfsprogramme werden zum Erstellen des Dienst Proxys verwendet, der die Bindungs Informationen und die [Endpunkt Adresse](endpoint-address.md) für den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="35bb5-108">The helpers are used to create the service proxy, which contains the binding information and [endpoint address](endpoint-address.md) for the service.</span></span>

## <a name="using-wsutil-to-generate-headers-and-helpers"></a><span data-ttu-id="35bb5-109">Verwenden von wsutil zum Generieren von Headern und Hilfsprogrammen</span><span class="sxs-lookup"><span data-stu-id="35bb5-109">Using WsUtil to Generate Headers and Helpers</span></span>

<span data-ttu-id="35bb5-110">Um die Header und Hilfsprogramme zu generieren, öffnet und liest wsutil die Metadatendateien für den Ziel Dienst – WSDL-und XSD-Dateien – und konvertiert sie in Header. Daher ist es erforderlich, die Metadatendateien für den Ziel Dienst vorab abzurufen, z. b. mithilfe von Svcutil, einem Teil der Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="35bb5-110">To generate the headers and helpers, WsUtil opens and reads the metadata files for the target service — wsdl and xsd files— and converts them into headers; therefore, it is necessary to retrieve the metadata files for the target service in advance, for example by using SvcUtil, a part of the Windows Communication Foundation.</span></span> <span data-ttu-id="35bb5-111">Aus Sicherheitsgründen ist es zwingend erforderlich, dass die Kopien dieser Dateien vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="35bb5-111">For security reasons, it is imperative that your copies of these files are trustworthy.</span></span> <span data-ttu-id="35bb5-112">(Weitere Informationen finden Sie im Abschnitt "Sicherheit" des Themas " [wsutil Compiler Tool](wsutil-compiler-tool.md) ".)</span><span class="sxs-lookup"><span data-stu-id="35bb5-112">(For more information, see the "Security" section of the [WsUtil Compiler Tool](wsutil-compiler-tool.md) topic.)</span></span>

<span data-ttu-id="35bb5-113">Verwenden Sie zum Ausführen von wsutil die folgende Befehlszeilen Syntax, wenn sich die WSDL-und XSD-Dateien für den Dienst in Ihrem eigenen Verzeichnis befinden: `WsUtil.exe *.wsdl *.xsd` .</span><span class="sxs-lookup"><span data-stu-id="35bb5-113">To run WsUtil, use the following command-line syntax if the WSDL and XSD files for the service are in their own directory: `WsUtil.exe *.wsdl *.xsd`.</span></span> <span data-ttu-id="35bb5-114">Alternativ können Sie die Dateien nach vollständigem Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="35bb5-114">Alternatively, you can specify the files by full name.</span></span>

<span data-ttu-id="35bb5-115">Wsutil generiert im Allgemeinen zwei Dateien für jede Metadatendatei: einen Header und eine C-Datei.</span><span class="sxs-lookup"><span data-stu-id="35bb5-115">WsUtil generally generates two files for each metadata file: a header and a C file.</span></span> <span data-ttu-id="35bb5-116">Fügen Sie dem Codierungs Projekt diese Dateien hinzu, und verwenden \# Sie include-Anweisungen, um Sie in den Code für den Client einzufügen.</span><span class="sxs-lookup"><span data-stu-id="35bb5-116">Add these files to your coding project, and use \#include statements to include them in the code for your client.</span></span> <span data-ttu-id="35bb5-117">(Die XSD-Dateien stellen Typen dar, und die WSDL-Dateien stellen Vorgänge dar.)</span><span class="sxs-lookup"><span data-stu-id="35bb5-117">(The XSD files represent types, and the WSDL files represent operations.)</span></span>

## <a name="creating-the-service-proxy"></a><span data-ttu-id="35bb5-118">Erstellen des Dienst Proxys</span><span class="sxs-lookup"><span data-stu-id="35bb5-118">Creating the Service Proxy</span></span>

<span data-ttu-id="35bb5-119">Der von wsutil generierte Header enthält eine Hilfsroutine zum Erstellen des Dienst Proxys mit der erforderlichen Bindung.</span><span class="sxs-lookup"><span data-stu-id="35bb5-119">The header generated by WsUtil contains a helper routine for creating the service proxy with the required binding.</span></span> <span data-ttu-id="35bb5-120">Diese Routine ist im Abschnitt "Richtlinien Hilfsroutinen" der generierten Header Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="35bb5-120">This routine is included in the "Policy helper routines" section of the generated header file.</span></span> <span data-ttu-id="35bb5-121">Beispielsweise enthält die generierte Kopfzeile für den Rechner Dienst, der im [httpcalculatorclientexample](httpcalculatorclientexample.md) -Beispiel veranschaulicht wird, den folgenden Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="35bb5-121">For example, the generated header for the calculator service illustrated in the [httpcalculatorclientexample](httpcalculatorclientexample.md) example will contain the following function prototype.</span></span>


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



<span data-ttu-id="35bb5-122">Integrieren Sie dieses Hilfsprogramm in Ihren Code, und übergeben Sie ein [WS- \_ Dienst \_ Proxy](ws-service-proxy.md) handle, um das Handle für den erstellten Dienst Proxy zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="35bb5-122">Incorporate this helper in your code and pass a [WS\_SERVICE\_PROXY](ws-service-proxy.md) handle to receive the handle to the created service proxy.</span></span> <span data-ttu-id="35bb5-123">Im einfachsten Szenario, in dem nur ein Dienst Proxy Handle und ein Fehler Objekt an die Funktion übermittelt werden, sieht der-Befehl wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="35bb5-123">In the simplest scenario, in which only a service proxy handle and an error object are passed to the function, the call looks like the following.</span></span>


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



<span data-ttu-id="35bb5-124">Um den Adress Teil des Dienst Proxys zu erstellen, rufen Sie [**wsopenserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) mit einem Handle für den Dienst Proxy und einen Zeiger auf eine [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) mit der Adresse des Dienst Endpunkts auf, mit der Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="35bb5-124">To create the address portion of the service proxy, call [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) with a handle to the service proxy and a pointer to a [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) containing the service endpoint address to which you wish to connect.</span></span>

## <a name="implementing-the-client-with-function-prototypes"></a><span data-ttu-id="35bb5-125">Implementieren des Clients mit Funktionsprototypen</span><span class="sxs-lookup"><span data-stu-id="35bb5-125">Implementing the Client with Function Prototypes</span></span>

<span data-ttu-id="35bb5-126">Die aus den WSDL-Dateien des Diensts generierten Header enthalten auch C-Funktionsprototypen, die die vom Webdienst verfügbaren Dienste darstellen und die für die erforderliche Bindung spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="35bb5-126">The headers generated from the service WSDL files also contain C function prototypes representing the services available from the Web service and specific to the binding required.</span></span> <span data-ttu-id="35bb5-127">Beispielsweise enthält ein Header, der für den in httpcalculatorserviceexample dargestellten Rechner Dienst generiert wird, den folgenden Prototyp für den Multiplikations Vorgang dieses dienstanders.</span><span class="sxs-lookup"><span data-stu-id="35bb5-127">For example, a header generated for the calculator service illustrated in HttpCalculatorServiceExample will contain the following prototype for that service's multiplication operation.</span></span>

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

<span data-ttu-id="35bb5-128">Sie können die Prototypen kopieren und als Vorlagen verwenden, um die Funktionsaufrufe in Ihrem Client zu codieren. in jedem Fall übergeben Sie das Handle an den Dienst Proxy.</span><span class="sxs-lookup"><span data-stu-id="35bb5-128">You can copy the prototypes and use them as templates for coding the function calls in your client, in each case passing the handle to service proxy.</span></span> <span data-ttu-id="35bb5-129">Wenn Sie mit dem Dienst Proxy fertig sind, wenden Sie sich an [**wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="35bb5-129">When you are finished with the service proxy, call [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span></span>

 

 




