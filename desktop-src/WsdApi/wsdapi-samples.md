---
description: Im Windows SDK für Windows Server 2008 sind zwei WSDAPI-Beispiele enthalten.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: WSDAPI-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754960"
---
# <a name="wsdapi-samples"></a><span data-ttu-id="b04ce-103">WSDAPI-Beispiele</span><span class="sxs-lookup"><span data-stu-id="b04ce-103">WSDAPI Samples</span></span>

<span data-ttu-id="b04ce-104">Im Windows SDK für Windows Server 2008 sind zwei WSDAPI-Beispiele enthalten.</span><span class="sxs-lookup"><span data-stu-id="b04ce-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="b04ce-105">Den Quellcode für die Beispiele finden Sie unter <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b04ce-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="b04ce-106">Diese SDK-Version ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b04ce-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="b04ce-107">Die Beispiele sind im Windows Vista SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b04ce-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="b04ce-108">Das Aktienkurs Beispiel (in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ StockQuote) veranschaulicht einen Dienst mit grundlegenden Messaging Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b04ce-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="b04ce-109">Das Beispiel für den Datei Dienst (in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ Fileservice) veranschaulicht einen Dienst mit erweiterten Funktionen, wie z. b. asynchrones Messaging, Anlagen und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b04ce-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="b04ce-110">Beide Beispiele enthalten die folgenden Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="b04ce-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="b04ce-111">WSDL-Dateien, die die Dienst Beschreibungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b04ce-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="b04ce-112">[Wsdcodegen-Konfigurationsdateien](wsdcodegen-configuration-file.md) , die zum Generieren von WSDAPI-Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b04ce-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="b04ce-113">Generierte C++-Header-und-Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="b04ce-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="b04ce-114">Client-und Dienst Implementierungs Dateien.</span><span class="sxs-lookup"><span data-stu-id="b04ce-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="b04ce-115">Visual Studio-Projekt-und-Projektmappendateien.</span><span class="sxs-lookup"><span data-stu-id="b04ce-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="b04ce-116">Beide Beispiele implementieren Geräte Hosts ([**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), Geräte [**Proxys (iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) und Dienst [**Proxys (iwsdserviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span><span class="sxs-lookup"><span data-stu-id="b04ce-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="b04ce-117">Außerdem wird im Beispiel für den Datei Dienst die Verwendung von asynchronem Messaging ([**iwsdasynccallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**iwsdasynkresult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), Anlagen ([**iwsdinboundattachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**iwsdoutboundattachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) und Eventing veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b04ce-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="b04ce-118">Die Dateien "fileservicecontract. vcproj" und "stockquotecontract. vcproj", die in den Beispielen enthalten sind, rufen [wsdcodegen](web-services-for-devices-code-generator.md) auf, um den C++-Header und die Quelldateien aus der WSDL-Datei zu generieren</span><span class="sxs-lookup"><span data-stu-id="b04ce-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="b04ce-119">Dies bedeutet Folgendes: Wenn die WSDL-oder wsdcodegen-Beispielkonfigurationsdatei geändert und das Beispiel Projekt neu erstellt wird, generiert wsdcodegen automatisch neue Header-und Quelldateien, die die Änderungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="b04ce-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="b04ce-120">Dies ist die bevorzugte Methode zum Entwickeln von WSDAPI-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b04ce-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="b04ce-121">Wsdcodegen wird in der Regel von der Befehlszeile aus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b04ce-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="b04ce-122">Öffnen Sie die relevante \* VCPROJ-Datei, um die Beispiele für wsdcodegen-Befehlszeilen Aufrufe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b04ce-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b04ce-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b04ce-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b04ce-124">WSD-Anwendungsentwicklung unter Windows</span><span class="sxs-lookup"><span data-stu-id="b04ce-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



