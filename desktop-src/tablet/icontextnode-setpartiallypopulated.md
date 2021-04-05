---
description: Ändert den Wert, der angibt, ob dieser icontextnode teilweise oder vollständig ausgefüllt ist.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Icontextnode:: setpartiallygefüllte-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041764"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="ab9e8-103">Icontextnode:: setpartiallygefüllte-Methode</span><span class="sxs-lookup"><span data-stu-id="ab9e8-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="ab9e8-104">Ändert den Wert, der angibt, ob dieser [**icontextnode**](icontextnode.md) teilweise oder vollständig ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab9e8-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="ab9e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab9e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9e8-107">nicht aufgefüllt  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9e8-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9e8-108">**Variant \_ TRUE** , wenn dieser [**icontextnode**](icontextnode.md) teilweise aufgefüllt ist. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9e8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab9e8-109">Return value</span></span>

<span data-ttu-id="ab9e8-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ab9e8-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9e8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab9e8-111">Remarks</span></span>

<span data-ttu-id="ab9e8-112">Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ab9e8-113">Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ab9e8-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="ab9e8-114">Wenn Sie die Dokumentstruktur virtualisieren, achten Sie darauf, den PropertyGuidsForContextNodes. rotatedboundingbox-Wert (mithilfe von ContextNode. addpropertyvalue) für alle ContextNode-Objekte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="ab9e8-115">Die rotatedboundingbox-Eigenschaft wird vom InkAnalyzer berechnet und sollte standardmäßig für alle geschriebenen ContextNodes lauten.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="ab9e8-116">Wenn Ihre Anwendung jedoch die Analyseergebnisse durch Festlegen der Eigenschaft partiallyaufgefüllt durch Festlegen der Eigenschaft PopulateContextNode verarbeitet, achten Sie darauf, die rotatedboundingbox-Eigenschaft aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="ab9e8-117">Wenn die rotatedboundingbox-Eigenschaft nicht festgelegt wird, werden möglicherweise mehr Dokument Daten im aktuellen Analyse Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="ab9e8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab9e8-118">Requirements</span></span>



| <span data-ttu-id="ab9e8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab9e8-119">Requirement</span></span> | <span data-ttu-id="ab9e8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ab9e8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9e8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab9e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab9e8-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab9e8-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ab9e8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab9e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab9e8-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab9e8-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ab9e8-125">Header</span><span class="sxs-lookup"><span data-stu-id="ab9e8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab9e8-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ab9e8-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ab9e8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ab9e8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab9e8-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab9e8-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ab9e8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab9e8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9e8-130">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="ab9e8-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ab9e8-131">**\_Ianalysisproxyevents::P opulatecontextnode**</span><span class="sxs-lookup"><span data-stu-id="ab9e8-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="ab9e8-132">**Icontextnode:: kreatepartiallypopulatedsubnode**</span><span class="sxs-lookup"><span data-stu-id="ab9e8-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="ab9e8-133">**Icontextnode:: getpartiallyaufgefüllt**</span><span class="sxs-lookup"><span data-stu-id="ab9e8-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="ab9e8-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ab9e8-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




