---
title: Anhang (VML)
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Webworkshop, Namespaces
- Webworkshop, Verhaltens Stile
- Entwerfen von Webseiten, Namespaces
- Entwerfen von Webseiten, Verhaltens Stilen
- Vector Markup Language (VML), Namespaces
- VML (Vector Markup Language), Namespaces
- Vektorgrafiken, Namespaces
- Vector Markup Language (VML), Verhaltens Stile
- VML (Vector Markup Language), Verhaltens Stile
- Vektorgrafiken, Verhaltens Stile
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391423"
---
# <a name="appendix-vml"></a><span data-ttu-id="912ef-114">Anhang (VML)</span><span class="sxs-lookup"><span data-stu-id="912ef-114">Appendix (VML)</span></span>

<span data-ttu-id="912ef-115">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="912ef-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="912ef-116">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="912ef-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="912ef-117">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="912ef-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="912ef-118">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="912ef-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="912ef-119">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="912ef-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="912ef-120">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="912ef-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="912ef-121">Wenn Sie den Browsern mitteilen möchten, wie Daten an einen VML-spezifischen Prozessor übergeben werden, müssen Sie einige Informationen eingeben, z. b. Namespaces und Verhaltens Stile.</span><span class="sxs-lookup"><span data-stu-id="912ef-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="912ef-122">Anschließend können Sie mit VML Grafiken in der Region eingeben `<BODY>` .</span><span class="sxs-lookup"><span data-stu-id="912ef-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="912ef-123">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="912ef-123">In this topic:</span></span>

-   [<span data-ttu-id="912ef-124">Namespaces</span><span class="sxs-lookup"><span data-stu-id="912ef-124">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="912ef-125">Verhaltens Stile</span><span class="sxs-lookup"><span data-stu-id="912ef-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="912ef-126">Namespaces</span><span class="sxs-lookup"><span data-stu-id="912ef-126">Namespaces</span></span>

<span data-ttu-id="912ef-127">Ein XML-Mechanismus gibt den Namespace an, aus dem ein Element stammt.</span><span class="sxs-lookup"><span data-stu-id="912ef-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="912ef-128">Wenn Sie von der XML-Datei zur XML-Verarbeitung wechseln, gibt dieser Mechanismus den Switch innerhalb von HTML an.</span><span class="sxs-lookup"><span data-stu-id="912ef-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="912ef-129">Fragen Sie den Hersteller des VML-Prozessors, welche Informationen für den XML-Namespace erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="912ef-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="912ef-130">Wenn Sie Microsoft Internet Explorer zum Rendering von VML verwenden, geben Sie immer die folgende Zeile im- `<HTML>` Tag ein:</span><span class="sxs-lookup"><span data-stu-id="912ef-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="912ef-131">Mit diesen Informationen wird Internet Explorer aufgefordert, zum Namespace "urn: Schemas-Microsoft-com: VML" zu wechseln, wenn ein XML-Tag mit einem Präfix `v:` und die resultierenden Daten an den VML-Prozessor übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="912ef-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="912ef-132">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="912ef-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="912ef-133">Verhaltens Stile</span><span class="sxs-lookup"><span data-stu-id="912ef-133">Behavior Styles</span></span>

<span data-ttu-id="912ef-134">VML ist in Microsoft Internet Explorer als Standardverhalten definiert.</span><span class="sxs-lookup"><span data-stu-id="912ef-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="912ef-135">Geben Sie zum Rendering von VML immer die folgenden Zeilen in der `<HEAD>` Region ein:</span><span class="sxs-lookup"><span data-stu-id="912ef-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="912ef-136">VML wird in Internet Explorer über VGX.DLL implementiert.</span><span class="sxs-lookup"><span data-stu-id="912ef-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="912ef-137">Wenn die anfängliche Installation des Browsers kein VML-Verhalten enthielt, müssen Sie es möglicherweise als Option hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="912ef-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="912ef-138">Sie müssen kein-Tag hinzufügen `<object>` .</span><span class="sxs-lookup"><span data-stu-id="912ef-138">You do not need to add an `<object>` tag.</span></span>

 

 
