---
description: Ruft das ianalysisalternate-Objekt am angegebenen Index in der Collection ab.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Ianalysisalterors:: getanalysisalternate-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344464"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="75c02-103">Ianalysisalternate:: getanalysisalternate-Methode</span><span class="sxs-lookup"><span data-stu-id="75c02-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="75c02-104">Ruft das [**ianalysisalternate**](ianalysisalternate.md) -Objekt am angegebenen Index in der Collection ab.</span><span class="sxs-lookup"><span data-stu-id="75c02-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75c02-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="75c02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75c02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c02-107">*ulindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75c02-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c02-108">Der null basierte Index des abzurufenden [**ianalysisalternate**](ianalysisalternate.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="75c02-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="75c02-109">*ppalternate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75c02-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75c02-110">Ein Zeiger auf das [**ianalysisalternate**](ianalysisalternate.md) -Objekt am angegebenen Index in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="75c02-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c02-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75c02-111">Return value</span></span>

<span data-ttu-id="75c02-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="75c02-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75c02-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75c02-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="75c02-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppalternate* , wenn Sie die Alternative Analyse nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="75c02-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75c02-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75c02-115">Requirements</span></span>



| <span data-ttu-id="75c02-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75c02-116">Requirement</span></span> | <span data-ttu-id="75c02-117">Wert</span><span class="sxs-lookup"><span data-stu-id="75c02-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c02-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75c02-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75c02-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75c02-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75c02-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75c02-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75c02-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75c02-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75c02-122">Header</span><span class="sxs-lookup"><span data-stu-id="75c02-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75c02-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75c02-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75c02-124">DLL</span><span class="sxs-lookup"><span data-stu-id="75c02-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c02-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c02-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75c02-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75c02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c02-127">**Ianalysisalteraten**</span><span class="sxs-lookup"><span data-stu-id="75c02-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="75c02-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="75c02-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

