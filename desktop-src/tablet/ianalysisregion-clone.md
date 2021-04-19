---
description: Erstellt eine Kopie von ianalysisregion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'Ianalysisregion:: Clone-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348796"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="537ae-103">Ianalysisregion:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="537ae-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="537ae-104">Erstellt eine Kopie von [**ianalysisregion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="537ae-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="537ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="537ae-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="537ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="537ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="537ae-107">*pclonedregion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="537ae-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="537ae-108">Ein Zeiger auf eine Kopie von [**ianalysisregion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="537ae-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="537ae-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="537ae-109">Return value</span></span>

<span data-ttu-id="537ae-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="537ae-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="537ae-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="537ae-111">Remarks</span></span>

<span data-ttu-id="537ae-112">Diese Methode ist eqivalente in die Thesystem. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone-Methode im .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="537ae-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="537ae-113">Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) in \* *pclonedregion* aufrufen, wenn Sie den geklonten Analysebereich nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="537ae-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="537ae-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="537ae-114">Requirements</span></span>



| <span data-ttu-id="537ae-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="537ae-115">Requirement</span></span> | <span data-ttu-id="537ae-116">Wert</span><span class="sxs-lookup"><span data-stu-id="537ae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="537ae-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="537ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="537ae-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="537ae-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="537ae-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="537ae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="537ae-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="537ae-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="537ae-121">Header</span><span class="sxs-lookup"><span data-stu-id="537ae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="537ae-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="537ae-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="537ae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="537ae-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="537ae-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="537ae-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="537ae-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="537ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537ae-126">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="537ae-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="537ae-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="537ae-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

