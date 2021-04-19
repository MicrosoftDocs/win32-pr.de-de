---
description: Aktualisiert den Bereich dieses icontextnode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'Icontextnode:: setLocation-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356778"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="04993-103">Icontextnode:: setLocation-Methode</span><span class="sxs-lookup"><span data-stu-id="04993-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="04993-104">Aktualisiert den Bereich dieses [**icontextnode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="04993-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04993-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04993-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="04993-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04993-107">*pianalysisregion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04993-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04993-108">Der [**ianalysisregion**](ianalysisregion.md) , der den Bereich beschreibt, in den der Speicherort des [**icontextnode**](icontextnode.md) -Objekts festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04993-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04993-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04993-109">Return value</span></span>

<span data-ttu-id="04993-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="04993-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04993-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04993-111">Remarks</span></span>

<span data-ttu-id="04993-112">Verwenden Sie diese Methode, um den Speicherort des Kontext Knotens zu aktualisieren (siehe [**icontextnode:: getLocation**](icontextnode-getlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="04993-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="04993-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04993-113">Requirements</span></span>



| <span data-ttu-id="04993-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04993-114">Requirement</span></span> | <span data-ttu-id="04993-115">Wert</span><span class="sxs-lookup"><span data-stu-id="04993-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04993-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04993-116">Minimum supported client</span></span><br/> | <span data-ttu-id="04993-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04993-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04993-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04993-118">Minimum supported server</span></span><br/> | <span data-ttu-id="04993-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="04993-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04993-120">Header</span><span class="sxs-lookup"><span data-stu-id="04993-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="04993-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="04993-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04993-122">DLL</span><span class="sxs-lookup"><span data-stu-id="04993-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04993-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04993-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04993-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04993-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04993-125">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="04993-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="04993-126">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="04993-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="04993-127">**Icontextnode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="04993-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="04993-128">**Icontextnode:: getpartiallyaufgefüllt**</span><span class="sxs-lookup"><span data-stu-id="04993-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="04993-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="04993-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




