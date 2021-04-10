---
description: Erstellt einen neuen benutzerdefinierten Erkennungs Knoten für iinkanalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Iinkanalyzer:: kreatecustomerkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214665"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="a1204-103">Iinkanalyzer:: kreatecustomerkenzer-Methode</span><span class="sxs-lookup"><span data-stu-id="a1204-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="a1204-104">Erstellt einen neuen benutzerdefinierten Erkennungs Knoten für [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a1204-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1204-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1204-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="a1204-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1204-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1204-107">*pinkanalysiserkenzerid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1204-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1204-108">Die Globally Unique Identifier (GUID) des [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Elements, für das ein Knoten erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1204-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="a1204-109">*ppcontextnode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1204-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1204-110">Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt, das den neuen benutzerdefinierten Erkennungs Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1204-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1204-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1204-111">Return value</span></span>

<span data-ttu-id="a1204-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a1204-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1204-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1204-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a1204-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf ppcontextnode, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a1204-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a1204-115">Diese Methode erstellt einen neuen [**icontextnode**](icontextnode.md) mit dem Typ customerkenzer (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="a1204-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="a1204-116">Anschließend wird der neue benutzerdefinierte Erkennungs Knoten der subknotenauflistung des Stamm Knotens des [**iinkanalyzer**](iinkanalyzer.md) -Objekts hinzugefügt (Weitere Informationen finden Sie unter [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) und [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="a1204-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1204-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1204-117">Requirements</span></span>



| <span data-ttu-id="a1204-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1204-118">Requirement</span></span> | <span data-ttu-id="a1204-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a1204-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1204-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1204-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1204-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1204-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1204-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1204-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1204-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1204-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a1204-124">Header</span><span class="sxs-lookup"><span data-stu-id="a1204-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1204-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1204-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1204-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a1204-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1204-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1204-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a1204-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1204-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1204-129">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="a1204-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a1204-130">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="a1204-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a1204-131">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="a1204-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a1204-132">**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1204-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="a1204-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a1204-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

