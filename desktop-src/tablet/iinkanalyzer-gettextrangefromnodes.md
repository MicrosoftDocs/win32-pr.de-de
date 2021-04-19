---
description: Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von icontextnode-Objekten entspricht.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'Iinkanalyzer:: GetTextRangeFromNodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350454"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="7c6cf-103">Iinkanalyzer:: GetTextRangeFromNodes-Methode</span><span class="sxs-lookup"><span data-stu-id="7c6cf-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="7c6cf-104">Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von [**icontextnode**](icontextnode.md) -Objekten entspricht.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c6cf-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="7c6cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c6cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6cf-107">*plstart* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c6cf-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6cf-108">Eine 32-Bit-Ganzzahl mit Vorzeichen, die den Anfang des Text Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="7c6cf-109">Dieser Parameter wird nicht initialisiert übergeben.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="7c6cf-110">*pllength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c6cf-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6cf-111">Eine 32-Bit-Ganzzahl mit Vorzeichen, die die Länge des Text Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="7c6cf-112">Dieser Parameter wird nicht initialisiert übergeben.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="7c6cf-113">*pnodebug Search* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c6cf-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6cf-114">Die Auflistung von [**icontextnode**](icontextnode.md) -Objekten, für die der Textbereich gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6cf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c6cf-115">Return value</span></span>

<span data-ttu-id="7c6cf-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7c6cf-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c6cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c6cf-117">Remarks</span></span>

<span data-ttu-id="7c6cf-118">Wenn *pnodestosearch* [**icontextnode**](icontextnode.md) -Objekte enthält, die nicht angrenzenden sind, gibt diese Methode den kleinsten Textbereich zurück, der alle **icontextnode** -Objekte abdeckt.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="7c6cf-119">Diese Methode löst eine E \_ invalidArg-Ausnahme aus, wenn *pnodestosearch* einen [**icontextnode**](icontextnode.md) enthält, der nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6cf-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c6cf-120">Requirements</span></span>



| <span data-ttu-id="7c6cf-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c6cf-121">Requirement</span></span> | <span data-ttu-id="7c6cf-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7c6cf-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6cf-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c6cf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6cf-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c6cf-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7c6cf-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c6cf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6cf-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7c6cf-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7c6cf-127">Header</span><span class="sxs-lookup"><span data-stu-id="7c6cf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6cf-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7c6cf-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7c6cf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7c6cf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c6cf-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c6cf-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7c6cf-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c6cf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6cf-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="7c6cf-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




