---
title: VML-Einführung
description: VML-Einführung
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Vector Markup Language (VML), Referenz
- VML (Vector Markup Language), Referenz
- Vektorgrafiken, VML-Referenz
- Vektorgrafiken, Vector Markup Language (VML)
- Referenz für Vector Markup Language (VML)
- VML-Referenz
- Vector Markup Language (VML), Shape-Element
- VML (Vector Markup Language), Shape-Element
- Vektorgrafiken, Shape-Element
- Shape-Element
- VML-Elemente, Form
- Vector Markup Language (VML), VBScript
- VML (Vector Markup Language), VBScript
- Vector Markup Language (VML), JavaScript
- VML (Vector Markup Language), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390474"
---
# <a name="vml-introduction"></a><span data-ttu-id="764a6-118">VML-Einführung</span><span class="sxs-lookup"><span data-stu-id="764a6-118">VML Introduction</span></span>

<span data-ttu-id="764a6-119">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="764a6-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="764a6-120">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="764a6-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="764a6-121">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="764a6-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="764a6-122">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="764a6-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="764a6-123">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="764a6-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="764a6-124">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="764a6-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="764a6-125">Dieses Dokument enthält einen umfassenden detaillierten Verweis auf die Implementierung der Vector Markup Language (VML), die mit Microsoft Office 2000 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="764a6-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="764a6-126">Andere Implementierungen können variieren.</span><span class="sxs-lookup"><span data-stu-id="764a6-126">Other implementations may vary.</span></span> <span data-ttu-id="764a6-127">Weitere Informationen zu VML als Standard finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-datetime.html) .</span><span class="sxs-lookup"><span data-stu-id="764a6-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="764a6-128">VML ist als Satz von XML-Elementen und den entsprechenden Attributen für jedes Element definiert.</span><span class="sxs-lookup"><span data-stu-id="764a6-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="764a6-129">Da das **Shape** -Element der grundlegende Baustein von VML ist, klicken Sie [hier](shape-element--vml.md) , um den Verweis zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="764a6-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="764a6-130">Beachten Sie, dass dieser Verweis mehrere Beispiele und Demos enthält.</span><span class="sxs-lookup"><span data-stu-id="764a6-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="764a6-131">Sie müssen Microsoft Internet Explorer 5,0 oder höher installiert haben, um die Live-VML anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="764a6-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="764a6-132">Zusätzlich zu den Informationen zur Verwendung von Elementen und Attributen als XML-Tags, die HTML erweitern, enthält diese Referenz Syntax und Beispiele, die zeigen, wie die Skripterstellung und die Dokumentobjektmodell Features von Internet Explorer 5 oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="764a6-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="764a6-133">Die Verwendung von Skripts mit VML ermöglicht das dynamische Erstellen von Elementen und das Bearbeiten von Attributen in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="764a6-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="764a6-134">In diesen Beispielen in dieser Referenz werden VBScript und JavaScript verwendet.</span><span class="sxs-lookup"><span data-stu-id="764a6-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="764a6-135">Wenn Sie eine andere Skriptsprache verwenden, als in einem Beispiel gezeigt, müssen Sie die Groß-/Kleinschreibung aller Element-und Attributnamen vergleichen.</span><span class="sxs-lookup"><span data-stu-id="764a6-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="764a6-136">Der Verweis gibt Skript Syntax, die für Sprachen mit Unterscheidung nach Groß-/Kleinschreibung wie JavaScript korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="764a6-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="764a6-137">Wenn Sie sich im Zweifelsfall bezüglich des richtigen Zeichen Falls befinden, verwenden Sie einen Objektkatalog (z. b. OLEVIEW), um die VGX.DLL zu untersuchen, um die genaue Groß-/Kleinschreibung eines Elements oder</span><span class="sxs-lookup"><span data-stu-id="764a6-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="764a6-138">Beachten Sie, dass bei Verwendung von VML als XML-Tags die Groß-/Kleinschreibung abhängig vom Dokumenttyp des zugrunde liegenden Dokuments ist.</span><span class="sxs-lookup"><span data-stu-id="764a6-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="764a6-139">Wenn Sie einen Strict-Modus verwenden! Bei DOCTYPE, Elementen und Attributen wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="764a6-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="764a6-140">VML-Referenz</span><span class="sxs-lookup"><span data-stu-id="764a6-140">The VML Reference</span></span>](shape-element--vml.md)

 

 