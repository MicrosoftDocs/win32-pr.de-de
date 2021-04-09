---
description: 'Es gibt vier Ebenen zur Handschrift Analyse Bibliothek: Windows Forms, WPF, com und die Basisebene. In diesem Abschnitt wird beschrieben, wann jede Ebene verwendet werden soll.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Verwendung der frei Hand Analyse-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958763"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="ee05f-104">Verwendung der frei Hand Analyse-API</span><span class="sxs-lookup"><span data-stu-id="ee05f-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="ee05f-105">Es gibt vier Ebenen zur Handschrift Analyse Bibliothek: Windows Forms, WPF, com und die Basisebene.</span><span class="sxs-lookup"><span data-stu-id="ee05f-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="ee05f-106">In diesem Abschnitt wird beschrieben, wann jede Ebene verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee05f-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="ee05f-107">Übersicht über die Ink Analysis-API</span><span class="sxs-lookup"><span data-stu-id="ee05f-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="ee05f-108">Die frei Hand Analyse Bibliotheken sind für die Verwendung in einer Vielzahl von unterstützten Programmierumgebungen konzipiert.</span><span class="sxs-lookup"><span data-stu-id="ee05f-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="ee05f-109">Es gibt vier grundlegende Ebenen, in denen Ihre Anwendung die Handschrift Analyse nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="ee05f-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="ee05f-110">Diese Ebenen sind:</span><span class="sxs-lookup"><span data-stu-id="ee05f-110">These layers are:</span></span>

-   <span data-ttu-id="ee05f-111">Die Windows Forms Ebene</span><span class="sxs-lookup"><span data-stu-id="ee05f-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="ee05f-112">Die WPF-Ebene</span><span class="sxs-lookup"><span data-stu-id="ee05f-112">The WPF layer</span></span>
-   <span data-ttu-id="ee05f-113">Die com-Ebene</span><span class="sxs-lookup"><span data-stu-id="ee05f-113">The COM layer</span></span>
-   <span data-ttu-id="ee05f-114">Die Basisebene</span><span class="sxs-lookup"><span data-stu-id="ee05f-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="ee05f-115">Windows Forms-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ee05f-115">Windows Forms Applications</span></span>

<span data-ttu-id="ee05f-116">Sie können die frei Hand Analyse-API in Ihrem verwalteten Projekt verwenden, indem Sie einen Verweis auf die folgenden Bibliotheken hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ee05f-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="ee05f-117">Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)</span><span class="sxs-lookup"><span data-stu-id="ee05f-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="ee05f-118">Bibliothek für frei Hand Dokument Analyse (IACore.dll)</span><span class="sxs-lookup"><span data-stu-id="ee05f-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="ee05f-119">In Windows Forms Anwendungen verwenden Sie höchstwahrscheinlich die Bibliotheken in Verbindung mit den standardmäßigen Tablet PC-Platt Form Objekten, die in der Microsoft Tablet PC API v 1.7-Assembly gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ee05f-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="ee05f-120">Stellen Sie sicher, dass Sie auch über einen Verweis auf Folgendes verfügen:</span><span class="sxs-lookup"><span data-stu-id="ee05f-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="ee05f-121">Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)</span><span class="sxs-lookup"><span data-stu-id="ee05f-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="ee05f-122">Windows Presentation Framework-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ee05f-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="ee05f-123">Sie können die frei Hand Analyse-API in Ihrem WPF-Projekt verwenden, indem Sie einen Verweis auf die im System. Windows. Ink-Namespace definierten Elemente der Ink-Analyse in der IAWinFX.dll-Assembly hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ee05f-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="ee05f-124">Diese Assembly wird vom SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="ee05f-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="ee05f-125">COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ee05f-125">COM Applications</span></span>

<span data-ttu-id="ee05f-126">Nicht-Automation-com-Anwendungen sollten die com-Ebene der frei Hand Analyse-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee05f-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="ee05f-127">Typspezifische [ContextNode](/previous-versions/ms551996(v=vs.100)) -Objekte, z. b. " [ParagraphNode](/previous-versions/ms580136(v=vs.100))", " [InkWordNode](/previous-versions/ms580133(v=vs.100))" und andere, werden nicht in der com-Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee05f-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="ee05f-128">Stattdessen sollten Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) auf der standardmäßigen [**icontextnode**](icontextnode.md) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee05f-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="ee05f-129">Sie müssen \# "iacom. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="ee05f-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="ee05f-130">Wahrscheinlich verwenden Sie die Bibliotheken in Verbindung mit dem Tablet PC Platform Ink-Objekt. Daher sollten Sie auch \# "msink AUT. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="ee05f-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="ee05f-131">RTS und andere Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ee05f-131">RTS and Other Applications</span></span>

<span data-ttu-id="ee05f-132">Die Basisschicht der frei Hand Analyse funktioniert anders als die anderen, da Sie Punktdaten für die Analyse anstelle von [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekten benötigt.</span><span class="sxs-lookup"><span data-stu-id="ee05f-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="ee05f-133">Beispiele für die direkte Arbeit mit der Basisschicht anstelle der Windows Forms-oder com-Schichten sind Anwendungen, die keine Tablet PC Platform-Ink-Objekte der ersten Generation verwenden, oder Anwendungen, die die [**RealTimeStylus**](realtimestylus-class.md) -APIs verwenden, um Stift Eingaben zu verwalten, anstatt die Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) -Objekte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee05f-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="ee05f-134">nur 32-Bit-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ee05f-134">32-bit Support Only</span></span>

<span data-ttu-id="ee05f-135">Beachten Sie, dass die frei Hand Analyse Bibliotheken nur in 32-Bit-Prozessen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ee05f-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee05f-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee05f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee05f-137">Übersicht über die Link Analyse</span><span class="sxs-lookup"><span data-stu-id="ee05f-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="ee05f-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ee05f-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
