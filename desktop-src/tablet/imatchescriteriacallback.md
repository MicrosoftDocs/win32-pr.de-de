---
description: Macht eine Methode verfügbar, um auszuwerten, ob ein icontextnode-Objekt bestimmte Kriterien erfüllt oder nicht.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Imatchescriteria-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525319"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="4891a-103">Imatchescriteria-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4891a-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="4891a-104">Macht eine Methode verfügbar, um auszuwerten, ob ein [**icontextnode**](icontextnode.md) -Objekt bestimmte Kriterien erfüllt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="4891a-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="4891a-105">Member</span><span class="sxs-lookup"><span data-stu-id="4891a-105">Members</span></span>

<span data-ttu-id="4891a-106">Die **imatchescriteria** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4891a-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4891a-107">**Imatchescriteria acallback** weist auch diese Typen von Membern auf:</span><span class="sxs-lookup"><span data-stu-id="4891a-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="4891a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4891a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4891a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="4891a-109">Methods</span></span>

<span data-ttu-id="4891a-110">Die **imatcheskriteriacallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4891a-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="4891a-111">Methode</span><span class="sxs-lookup"><span data-stu-id="4891a-111">Method</span></span>                                                                      | <span data-ttu-id="4891a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4891a-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4891a-113">**Evaluatecontextnode**</span><span class="sxs-lookup"><span data-stu-id="4891a-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="4891a-114">Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein bestimmtes [**icontextnode**](icontextnode.md) -Objekt die Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4891a-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4891a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4891a-115">Remarks</span></span>

<span data-ttu-id="4891a-116">Um die [**iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md) oder die [**iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)zu verwenden, erstellen Sie eine Klasse, die **imatchescriteria acallback** implementiert.</span><span class="sxs-lookup"><span data-stu-id="4891a-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="4891a-117">Implementieren Sie [**imatchescriteria acallback:: evaluatecontextnode**](imatchescriteriacallback-evaluatecontextnode.md) , um **Variant \_ true** zurückzugeben, wenn das [**icontextnode**](icontextnode.md) -Objekt mit Ihren Kriterien übereinstimmt, und andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="4891a-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="4891a-118">Für einige Kriterien müssen Sie möglicherweise eine Möglichkeit zur Initialisierung oder Beibehaltung des Zustands Ihres **imatchescriteria** -Objekts bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4891a-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4891a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4891a-119">Requirements</span></span>



| <span data-ttu-id="4891a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4891a-120">Requirement</span></span> | <span data-ttu-id="4891a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4891a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4891a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4891a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4891a-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4891a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4891a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4891a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4891a-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4891a-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4891a-126">Header</span><span class="sxs-lookup"><span data-stu-id="4891a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4891a-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4891a-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4891a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4891a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4891a-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4891a-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4891a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4891a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4891a-131">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="4891a-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="4891a-132">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="4891a-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="4891a-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4891a-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

