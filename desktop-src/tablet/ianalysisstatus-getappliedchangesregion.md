---
description: Ruft den Bereich des Dokuments ab, der den Änderungen entspricht, die in der Kontext Knoten Struktur des iinkanalyzer-Objekts als Ergebnis einer frei Hand Analyse vorgenommen wurden.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Ianalysisstatus:: getappliedchangesregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526546"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="aab77-103">Ianalysisstatus:: getappliedchangesregion-Methode</span><span class="sxs-lookup"><span data-stu-id="aab77-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="aab77-104">Ruft den Bereich des Dokuments ab, der den Änderungen entspricht, die in der Kontext Knoten Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts als Ergebnis einer frei Hand Analyse vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="aab77-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="aab77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aab77-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="aab77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aab77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab77-107">*pappliedchangesregion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aab77-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aab77-108">Ein Zeiger auf den [**ianalysisregion**](ianalysisregion.md) des Dokuments, in dem Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="aab77-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab77-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aab77-109">Return value</span></span>

<span data-ttu-id="aab77-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="aab77-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aab77-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aab77-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="aab77-112">Um einen Speicherplatz zu vermeiden, rufen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *pappliedchangesregion* auf, wenn Sie den Analysebereich nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="aab77-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="aab77-113">Diese Methode wird am häufigsten verwendet, wenn die Anwendung Informationen zu Debuggingzwecken empfängt und den Bereich für ungültig erklären muss, in dem Änderungen auftreten können, damit die Debuginformationen gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="aab77-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab77-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aab77-114">Requirements</span></span>



| <span data-ttu-id="aab77-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aab77-115">Requirement</span></span> | <span data-ttu-id="aab77-116">Wert</span><span class="sxs-lookup"><span data-stu-id="aab77-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab77-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aab77-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aab77-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aab77-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aab77-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aab77-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aab77-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aab77-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="aab77-121">Header</span><span class="sxs-lookup"><span data-stu-id="aab77-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab77-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="aab77-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aab77-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aab77-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aab77-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aab77-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="aab77-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aab77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab77-126">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="aab77-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="aab77-127">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="aab77-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="aab77-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="aab77-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

