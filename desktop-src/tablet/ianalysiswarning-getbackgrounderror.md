---
description: Ruft den Fehlercode für den Vorgang der Hintergrund Handschrift Analyse ab, wenn ein Fehler aufgetreten ist.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Ianalysiswarning:: getbackgrounderror-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214677"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="42bf2-103">Ianalysiswarning:: getbackgrounderror-Methode</span><span class="sxs-lookup"><span data-stu-id="42bf2-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="42bf2-104">Ruft den Fehlercode für den Vorgang der Hintergrund Handschrift Analyse ab, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="42bf2-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="42bf2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42bf2-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="42bf2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42bf2-106">Parameters</span></span>

<span data-ttu-id="42bf2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="42bf2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42bf2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42bf2-108">Return value</span></span>

<span data-ttu-id="42bf2-109">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="42bf2-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="42bf2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42bf2-110">Remarks</span></span>

<span data-ttu-id="42bf2-111">Wenn ein Fehler in einem Hintergrundanalyse Vorgang auftritt, kann [**iinkanalyzer**](iinkanalyzer.md) den Fehlercode nicht zurückgeben, da er in einem anderen Thread auftritt.</span><span class="sxs-lookup"><span data-stu-id="42bf2-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="42bf2-112">Stattdessen erhält der [**\_ ianalysisevents:: results**](-ianalysisevents-results.md) -Ereignishandler einen [**ianalysisstatus**](ianalysisstatus.md) , der eine [**ianalysiswarning**](ianalysiswarning.md) mit einem [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) von **AnalysisWarningCode \_ BackgroundException** enthält.</span><span class="sxs-lookup"><span data-stu-id="42bf2-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="42bf2-113">Dieses **ianalysiswarning** -Element enthält den Fehlercode für den Hintergrundanalyse Vorgang.</span><span class="sxs-lookup"><span data-stu-id="42bf2-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="42bf2-114">Im Allgemeinen gibt der **\_ ianalysisevents:: results** -Ereignishandler diesen Fehlercode zurück, sodass er an anderer Stelle in der Anwendung behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="42bf2-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="42bf2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42bf2-115">Requirements</span></span>



| <span data-ttu-id="42bf2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42bf2-116">Requirement</span></span> | <span data-ttu-id="42bf2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="42bf2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bf2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42bf2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42bf2-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42bf2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="42bf2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42bf2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42bf2-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="42bf2-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="42bf2-122">Header</span><span class="sxs-lookup"><span data-stu-id="42bf2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42bf2-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="42bf2-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="42bf2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="42bf2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42bf2-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42bf2-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="42bf2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42bf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42bf2-127">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="42bf2-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="42bf2-128">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="42bf2-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="42bf2-129">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="42bf2-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="42bf2-130">**\_Ianalysil Vents:: results**</span><span class="sxs-lookup"><span data-stu-id="42bf2-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="42bf2-131">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="42bf2-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="42bf2-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="42bf2-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

