---
description: 'Tritt auf, wenn die iinkanalyzer:: Analysis-Methode oder die iinkanalyzer:: BackgroundAnalyze-Methode aufgerufen wird.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents:: Activity-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351818"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="6f6a2-103">\_Ianalysil Vents:: Activity-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6f6a2-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="6f6a2-104">Tritt auf, wenn die [**iinkanalyzer:: Analysis**](iinkanalyzer-analyze.md) -Methode oder die [**iinkanalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6a2-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="6f6a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f6a2-106">Parameters</span></span>

<span data-ttu-id="6f6a2-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f6a2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f6a2-108">Return value</span></span>

<span data-ttu-id="6f6a2-109">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f6a2-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6a2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f6a2-110">Remarks</span></span>

<span data-ttu-id="6f6a2-111">Dieses Ereignis zeigt an, dass [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="6f6a2-112">Dieses Ereignis weist nicht auf den Fortschritt des frei Hand Analyse Vorgangs hin.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="6f6a2-113">Implementieren Sie einen **\_ ianalysilvents:: Activity** -Ereignishandler, um einen der folgenden Schritte durchführen zu können:</span><span class="sxs-lookup"><span data-stu-id="6f6a2-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="6f6a2-114">Geben Sie dem Benutzer an, dass die Handschrift Analyse durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="6f6a2-115">Benutzereingaben während synchroner Analyse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="6f6a2-116">Empfangen von Benachrichtigungen über Systemanforderungen, z. b. das Neuzeichnen des Anwendungsfensters während der frei Hand Analyse.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="6f6a2-117">Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis häufig während der Layoutanalysephase und der Erstellungsphase für die Erstellung und Zeichnung der frei Hand Analyse aus.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="6f6a2-118">Der **iinkanalyzer** löst dieses Ereignis während der Handschrift Erkennungs Phase vor und nach dem Zugriff auf eine frei Handerkennung aus.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="6f6a2-119">Die Anzahl der Aktivitäts Ereignisse, die von [**iinkanalyzer**](iinkanalyzer.md) generiert werden, ist betroffen von:</span><span class="sxs-lookup"><span data-stu-id="6f6a2-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="6f6a2-120">Die frei Handerkennung, die der [**iinkanalyzer**](iinkanalyzer.md) für die frei Handerkennung anwendet.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="6f6a2-121">Die Anzahl und Länge der Striche, die von [**iinkanalyzer**](iinkanalyzer.md) analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="6f6a2-122">Die Anzahl der Striche, die als Schreibvorgänge klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="6f6a2-123">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f6a2-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6a2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f6a2-124">Requirements</span></span>



| <span data-ttu-id="6f6a2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f6a2-125">Requirement</span></span> | <span data-ttu-id="6f6a2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6f6a2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6a2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f6a2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6a2-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f6a2-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f6a2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f6a2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6a2-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6f6a2-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6f6a2-131">Header</span><span class="sxs-lookup"><span data-stu-id="6f6a2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f6a2-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6f6a2-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f6a2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6f6a2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f6a2-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f6a2-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6f6a2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f6a2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6a2-136">**\_Ianalysil Vents**</span><span class="sxs-lookup"><span data-stu-id="6f6a2-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="6f6a2-137">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="6f6a2-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="6f6a2-138">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="6f6a2-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6f6a2-139">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="6f6a2-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="6f6a2-140">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="6f6a2-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="6f6a2-141">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="6f6a2-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="6f6a2-142">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="6f6a2-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




