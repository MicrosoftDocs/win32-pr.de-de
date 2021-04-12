---
description: Ruft den Wert ab, der angibt, ob ein icontextnode-Objekt teilweise aufgefüllt oder vollständig ausgefüllt ist.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'Icontextnode:: getpartiallygefüllte-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129501"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="02773-103">Icontextnode:: getpartiallygefüllte-Methode</span><span class="sxs-lookup"><span data-stu-id="02773-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="02773-104">Ruft den Wert ab, der angibt, ob ein [**icontextnode**](icontextnode.md) -Objekt teilweise aufgefüllt oder vollständig ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="02773-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="02773-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02773-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="02773-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02773-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02773-107">*pfpartiallyausgefüllt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="02773-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02773-108">**Variant \_ TRUE** , wenn dieses [**icontextnode**](icontextnode.md) -Objekt keine kompletten Daten enthält. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="02773-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02773-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02773-109">Return value</span></span>

<span data-ttu-id="02773-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="02773-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02773-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02773-111">Remarks</span></span>

<span data-ttu-id="02773-112">Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="02773-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="02773-113">Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="02773-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02773-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02773-114">Requirements</span></span>



| <span data-ttu-id="02773-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02773-115">Requirement</span></span> | <span data-ttu-id="02773-116">Wert</span><span class="sxs-lookup"><span data-stu-id="02773-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02773-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02773-117">Minimum supported client</span></span><br/> | <span data-ttu-id="02773-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02773-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="02773-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02773-119">Minimum supported server</span></span><br/> | <span data-ttu-id="02773-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="02773-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="02773-121">Header</span><span class="sxs-lookup"><span data-stu-id="02773-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="02773-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02773-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02773-123">DLL</span><span class="sxs-lookup"><span data-stu-id="02773-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02773-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02773-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="02773-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02773-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02773-126">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="02773-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="02773-127">**Icontextnode:: setpartiallyaufgefüllt**</span><span class="sxs-lookup"><span data-stu-id="02773-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="02773-128">**Icontextnode:: kreatepartiallypopulatedsubnode**</span><span class="sxs-lookup"><span data-stu-id="02773-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="02773-129">**\_Ianalysisproxyevents::P opulatecontextnode**</span><span class="sxs-lookup"><span data-stu-id="02773-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="02773-130">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="02773-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




