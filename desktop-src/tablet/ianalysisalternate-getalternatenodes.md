---
description: Ruft die icontextnode-Objekte ab, die mit dieser alternativen verknüpft sind.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Ianalysisalternate:: getalternatenodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345741"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="1a98e-103">Ianalysisalternate:: getalternatenodes-Methode</span><span class="sxs-lookup"><span data-stu-id="1a98e-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="1a98e-104">Ruft die [**icontextnode**](icontextnode.md) -Objekte ab, die mit dieser alternativen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1a98e-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a98e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a98e-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="1a98e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a98e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a98e-107">*ppalternative enodes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a98e-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a98e-108">Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) -Auflistung, die [**icontextnode**](icontextnode.md) -Objekte enthält, die mit dieser alternativen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1a98e-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a98e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a98e-109">Return value</span></span>

<span data-ttu-id="1a98e-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1a98e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a98e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a98e-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1a98e-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppalternativen enodes* , wenn Sie die Auflistung der Kontext Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="1a98e-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="1a98e-113">Diese Methode gibt die Blatt Kontext Knoten zurück, die dieser alternativen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1a98e-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="1a98e-114">Beispiele für Blattknoten sind InkWord-, textword-, Bild-, InkDrawing-und InkBullet-Kontext Knoten.</span><span class="sxs-lookup"><span data-stu-id="1a98e-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="1a98e-115">Weitere Informationen finden Sie unter [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="1a98e-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="1a98e-116">Da Sie mit alternativen übereinstimmen, sind diese [**icontextnode**](icontextnode.md) -Objekte keine Nachfolger des Stamm- **icontextnode** des [**iinkanalyzer**](iinkanalyzer.md) -Objekts (siehe [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)), es sei denn, Sie sind die obere Alternative, d. h. das erste Element in einer [**ianalysisalterors**](ianalysisalternates.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1a98e-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a98e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a98e-117">Requirements</span></span>



| <span data-ttu-id="1a98e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a98e-118">Requirement</span></span> | <span data-ttu-id="1a98e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1a98e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a98e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a98e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a98e-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a98e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1a98e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a98e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a98e-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1a98e-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1a98e-124">Header</span><span class="sxs-lookup"><span data-stu-id="1a98e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a98e-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1a98e-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1a98e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1a98e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a98e-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a98e-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1a98e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a98e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a98e-129">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="1a98e-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="1a98e-130">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="1a98e-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1a98e-131">**Icontextnodes**</span><span class="sxs-lookup"><span data-stu-id="1a98e-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="1a98e-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="1a98e-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="1a98e-133">System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. Alternativen</span><span class="sxs-lookup"><span data-stu-id="1a98e-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

