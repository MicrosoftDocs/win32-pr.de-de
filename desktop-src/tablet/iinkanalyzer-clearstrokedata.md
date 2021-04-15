---
description: Löscht hubpaketdaten aus iinkanalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'Iinkanalyzer:: ClearStrokeData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485083"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="88d89-103">Iinkanalyzer:: ClearStrokeData-Methode</span><span class="sxs-lookup"><span data-stu-id="88d89-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="88d89-104">Löscht hubpaketdaten aus [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="88d89-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88d89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88d89-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="88d89-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88d89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d89-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d89-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d89-108">Der Bezeichner des Strichs, für den die Paketdaten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="88d89-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d89-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88d89-109">Return value</span></span>

<span data-ttu-id="88d89-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="88d89-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88d89-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88d89-111">Remarks</span></span>

<span data-ttu-id="88d89-112">Verwenden Sie diese Methode, wenn sich die Paketdaten für einen Strich ändern, z. b. Wenn ein Strich verschoben oder anderweitig transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="88d89-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="88d89-113">Der [**iinkanalyzer**](iinkanalyzer.md) löst das [**\_ ianalysitsvents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis aus, wenn er Stroke Packet-Daten von einem Strich benötigt, für den die Paketdaten gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="88d89-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d89-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88d89-114">Requirements</span></span>



| <span data-ttu-id="88d89-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88d89-115">Requirement</span></span> | <span data-ttu-id="88d89-116">Wert</span><span class="sxs-lookup"><span data-stu-id="88d89-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d89-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88d89-117">Minimum supported client</span></span><br/> | <span data-ttu-id="88d89-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88d89-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88d89-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88d89-119">Minimum supported server</span></span><br/> | <span data-ttu-id="88d89-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88d89-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="88d89-121">Header</span><span class="sxs-lookup"><span data-stu-id="88d89-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d89-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="88d89-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88d89-123">DLL</span><span class="sxs-lookup"><span data-stu-id="88d89-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d89-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88d89-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="88d89-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88d89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d89-126">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="88d89-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="88d89-127">**Iinkanalyzer:: UpdateStrokesData-Methode**</span><span class="sxs-lookup"><span data-stu-id="88d89-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="88d89-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="88d89-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




