---
description: Ruft das iinkanalysiserkenzer-Element am angegebenen Index ab.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Iinkanalysiserkenzers:: getinkanalysiserkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485091"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="992d9-103">Iinkanalysiserkenzers:: getinkanalysiserkenzer-Methode</span><span class="sxs-lookup"><span data-stu-id="992d9-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="992d9-104">Ruft das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="992d9-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="992d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="992d9-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="992d9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="992d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992d9-107">*ulindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="992d9-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992d9-108">Der null basierte Index des abzurufenden [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="992d9-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="992d9-109">*ppinkanalysiserkenzer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="992d9-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="992d9-110">Ein Zeiger auf [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="992d9-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992d9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="992d9-111">Return value</span></span>

<span data-ttu-id="992d9-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="992d9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="992d9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="992d9-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="992d9-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppinkanalysiserkenzer* , wenn Sie die Handschrifterkennung nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="992d9-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="992d9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="992d9-115">Requirements</span></span>



| <span data-ttu-id="992d9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="992d9-116">Requirement</span></span> | <span data-ttu-id="992d9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="992d9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992d9-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="992d9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="992d9-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="992d9-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="992d9-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="992d9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="992d9-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="992d9-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="992d9-122">Header</span><span class="sxs-lookup"><span data-stu-id="992d9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="992d9-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="992d9-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="992d9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="992d9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992d9-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992d9-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="992d9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="992d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992d9-127">**Inkanalysiserkenzers**</span><span class="sxs-lookup"><span data-stu-id="992d9-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="992d9-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="992d9-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

