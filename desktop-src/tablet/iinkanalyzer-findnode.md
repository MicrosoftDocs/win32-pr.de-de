---
description: Ruft das icontextnode-Objekt für eine angegebene Globally Unique Identifier (GUID) ab.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'Iinkanalyzer:: FindNode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041761"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="428f0-103">Iinkanalyzer:: FindNode-Methode</span><span class="sxs-lookup"><span data-stu-id="428f0-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="428f0-104">Ruft das [**icontextnode**](icontextnode.md) -Objekt für eine angegebene Globally Unique Identifier (GUID) ab.</span><span class="sxs-lookup"><span data-stu-id="428f0-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="428f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="428f0-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="428f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="428f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="428f0-107">*pId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="428f0-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428f0-108">Der Bezeichner für das [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="428f0-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="428f0-109">*ppcontextnode found* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="428f0-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="428f0-110">Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt mit dem *pId* -Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="428f0-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="428f0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="428f0-111">Return value</span></span>

<span data-ttu-id="428f0-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="428f0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="428f0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="428f0-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="428f0-114">Um einen Speichermangel zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnounfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="428f0-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="428f0-115">Wenn kein solches [**icontextnode**](icontextnode.md) -Objekt als Nachfolger des Stamm Knotens [**iinkanalyzer**](iinkanalyzer.md) vorhanden ist, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="428f0-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="428f0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="428f0-116">Requirements</span></span>



| <span data-ttu-id="428f0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="428f0-117">Requirement</span></span> | <span data-ttu-id="428f0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="428f0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="428f0-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="428f0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="428f0-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="428f0-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="428f0-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="428f0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="428f0-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="428f0-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="428f0-123">Header</span><span class="sxs-lookup"><span data-stu-id="428f0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="428f0-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="428f0-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="428f0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="428f0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="428f0-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="428f0-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="428f0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="428f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="428f0-128">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="428f0-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="428f0-129">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="428f0-130">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="428f0-131">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="428f0-132">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="428f0-133">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="428f0-134">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="428f0-135">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="428f0-136">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="428f0-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="428f0-137">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="428f0-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

