---
title: Informationen zu Windows-Webdiensten
description: Die Windows-Webdienste-API ist eine mehrschichtige API und kann wie folgt dargestellt werden.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104556006"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="9ebae-103">Informationen zu Windows-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="9ebae-103">About Windows Web Services</span></span>

<span data-ttu-id="9ebae-104">Die Windows-Webdienste-API ist eine mehrschichtige API und kann wie folgt dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9ebae-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![Das Diagramm zeigt die Ebenen und die bereichsübergreifenden Bereiche der Windows-Webdienste-API an.](images/apistack.png)

<span data-ttu-id="9ebae-106">Bei wwsapi handelt es sich um eine mehrschichtige API.</span><span class="sxs-lookup"><span data-stu-id="9ebae-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="9ebae-107">Wir gehen davon aus, dass die meisten Entwickler auf das Dienstmodell abzielen, bei dem es sich um ein Methoden basiertes Programmiermodell handelt.</span><span class="sxs-lookup"><span data-stu-id="9ebae-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="9ebae-108">Im Dienstmodell stellt der Dienst Host das serverseitige Programmiermodell bereit, während der Dienst Proxy das Client seitige Programmiermodell bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9ebae-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="9ebae-109">Jede Ebene macht einen Satz von APIs und Typen verfügbar, die mit APIs dieser Ebene verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9ebae-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="9ebae-110">Dienstmodell</span><span class="sxs-lookup"><span data-stu-id="9ebae-110">Service Model</span></span>

<span data-ttu-id="9ebae-111">Die Ebene der obersten Ebene, die als [Dienstmodell](service-model-layer-overview.md) bezeichnet wird, stellt ein Methoden basiertes Programmiermodell bereit, das am einfachsten zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="9ebae-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="9ebae-112">Im Dienstmodell stellt der [Dienst Host](service-host.md) das serverseitige Programmiermodell bereit, während der [Dienst Proxy](service-proxy.md) das Client seitige Programmiermodell bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9ebae-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="9ebae-113">Der [Kontext](context.md) wird innerhalb des Dienst Modells verwendet, um einen relevanten Zustand zu übergeben, der für den Dienst Vorgang und/oder den Rückruf verfügbar ist, wenn er aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9ebae-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="9ebae-114">Und [Dienstvertrag](contract.md) wird verwendet, um einen Dienstvertrag für einen Endpunkt anzugeben, der für den Dienst verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="9ebae-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="9ebae-115">Die folgenden Komponenten und Vorgänge sind Teil der Dienst Ebene:</span><span class="sxs-lookup"><span data-stu-id="9ebae-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="9ebae-116">Dienst Host</span><span class="sxs-lookup"><span data-stu-id="9ebae-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="9ebae-117">Dienst Proxy</span><span class="sxs-lookup"><span data-stu-id="9ebae-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="9ebae-118">Context</span><span class="sxs-lookup"><span data-stu-id="9ebae-118">Context</span></span>](context.md)
-   [<span data-ttu-id="9ebae-119">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="9ebae-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="9ebae-120">Dienstmetadaten</span><span class="sxs-lookup"><span data-stu-id="9ebae-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="9ebae-121">Kanal Ebene</span><span class="sxs-lookup"><span data-stu-id="9ebae-121">Channel Layer</span></span>

<span data-ttu-id="9ebae-122">Das Dienstmodell basiert auf einer Kanal Ebene, die vollständige Flexibilität bietet, aber schwieriger zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="9ebae-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="9ebae-123">Die folgenden Komponenten und Vorgänge sind Teil der Kanal Ebene:</span><span class="sxs-lookup"><span data-stu-id="9ebae-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="9ebae-124">Meldung</span><span class="sxs-lookup"><span data-stu-id="9ebae-124">Message</span></span>](message.md)
-   [<span data-ttu-id="9ebae-125">Kanal</span><span class="sxs-lookup"><span data-stu-id="9ebae-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="9ebae-126">Listener</span><span class="sxs-lookup"><span data-stu-id="9ebae-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="9ebae-127">Fehler</span><span class="sxs-lookup"><span data-stu-id="9ebae-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="9ebae-128">Url</span><span class="sxs-lookup"><span data-stu-id="9ebae-128">Url</span></span>](url.md)
-   [<span data-ttu-id="9ebae-129">Security</span><span class="sxs-lookup"><span data-stu-id="9ebae-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="9ebae-130">Metadatenimport</span><span class="sxs-lookup"><span data-stu-id="9ebae-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="9ebae-131">XML-Ebene</span><span class="sxs-lookup"><span data-stu-id="9ebae-131">XML Layer</span></span>

<span data-ttu-id="9ebae-132">Die Kanal Schicht basiert wiederum auf einem vereinfachten XML-Framework, das die Deserialisierung von C-Datentypen einschließt.</span><span class="sxs-lookup"><span data-stu-id="9ebae-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="9ebae-133">Die folgenden Komponenten und Vorgänge sind Teil der XML-Ebene:</span><span class="sxs-lookup"><span data-stu-id="9ebae-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="9ebae-134">XML-Writer</span><span class="sxs-lookup"><span data-stu-id="9ebae-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="9ebae-135">XML-Reader</span><span class="sxs-lookup"><span data-stu-id="9ebae-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="9ebae-136">XML-Puffer</span><span class="sxs-lookup"><span data-stu-id="9ebae-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="9ebae-137">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="9ebae-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="9ebae-138">XML-Sprachunterstützung</span><span class="sxs-lookup"><span data-stu-id="9ebae-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="9ebae-139">Alle Ebenen gemeinsam</span><span class="sxs-lookup"><span data-stu-id="9ebae-139">Common to all layers</span></span>

<span data-ttu-id="9ebae-140">Im folgenden finden Sie Themen, die für jede der drei Ebenen gelten:</span><span class="sxs-lookup"><span data-stu-id="9ebae-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="9ebae-141">Fehler</span><span class="sxs-lookup"><span data-stu-id="9ebae-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="9ebae-142">Asynchrones Modell</span><span class="sxs-lookup"><span data-stu-id="9ebae-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="9ebae-143">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="9ebae-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="9ebae-144">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="9ebae-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="9ebae-145">Abbruch</span><span class="sxs-lookup"><span data-stu-id="9ebae-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="9ebae-146">Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="9ebae-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="9ebae-147">Debuggen</span><span class="sxs-lookup"><span data-stu-id="9ebae-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="9ebae-148">Wsutil-Compilertool</span><span class="sxs-lookup"><span data-stu-id="9ebae-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="9ebae-149">Heap</span><span class="sxs-lookup"><span data-stu-id="9ebae-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="9ebae-150">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ebae-150">Examples</span></span>

<span data-ttu-id="9ebae-151">Weitere Informationen zu API-Elementen finden Sie unter [Referenz zu Windows-Webdiensten](windows-web-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9ebae-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="9ebae-152">Beispiele für die Verwendung der-API finden [Sie unter Verwenden von Windows-Webdiensten](using-windows-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="9ebae-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




