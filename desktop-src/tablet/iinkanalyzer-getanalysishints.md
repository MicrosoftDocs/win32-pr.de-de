---
description: Ruft alle Analysis Hint-icontextnode-Objekte ab, die an iinkanalyzer angefügt sind.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'Iinkanalyzer:: GetAnalysisHints-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129456"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="e4ce2-103">Iinkanalyzer:: GetAnalysisHints-Methode</span><span class="sxs-lookup"><span data-stu-id="e4ce2-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="e4ce2-104">Ruft alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte ab, die an [**iinkanalyzer**](iinkanalyzer.md)angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="e4ce2-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ce2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ce2-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="e4ce2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4ce2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ce2-107">*ppanalysishints* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4ce2-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ce2-108">Ein Zeiger auf alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte in [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e4ce2-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ce2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4ce2-109">Return value</span></span>

<span data-ttu-id="e4ce2-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e4ce2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ce2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4ce2-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e4ce2-112">Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppanalysishints* aufrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e4ce2-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="e4ce2-113">Diese Methode gibt eine leere Auflistung zurück, wenn keine Analyse Hinweis Knoten an [**iinkanalyzer**](iinkanalyzer.md)angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="e4ce2-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="e4ce2-114">Ein Analyse Hinweis Knoten ist ein [**icontextnode**](icontextnode.md) mit dem Kontext Knotentyp AnalysisHint (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="e4ce2-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="e4ce2-115">Wenn Sie dem Hinweis Kontextinformationen hinzufügen möchten, verwenden Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) mit dem Parameter *ppropertydataid* , der auf einen der global eindeutigen Bezeichner (GUIDs) in den Eigenschaften Konstanten von [Analysis Hint](analysis-hint-properties.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e4ce2-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="e4ce2-116">Um zu ermitteln, welche Eigenschaftswerte für einen Kontext Knoten festgelegt werden, verwenden Sie [**icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="e4ce2-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="e4ce2-117">Um den Wert einer Eigenschaft zu suchen, verwenden Sie [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="e4ce2-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ce2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4ce2-118">Requirements</span></span>



| <span data-ttu-id="e4ce2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4ce2-119">Requirement</span></span> | <span data-ttu-id="e4ce2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e4ce2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ce2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4ce2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ce2-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4ce2-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4ce2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4ce2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ce2-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e4ce2-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e4ce2-125">Header</span><span class="sxs-lookup"><span data-stu-id="e4ce2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4ce2-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ce2-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e4ce2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e4ce2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4ce2-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4ce2-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e4ce2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4ce2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ce2-130">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="e4ce2-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e4ce2-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="e4ce2-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e4ce2-132">**Iinkanalyzer:: feateanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="e4ce2-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="e4ce2-133">**Iinkanalyzer::D eleteanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="e4ce2-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="e4ce2-134">**Iinkanalyzer:: getanalysishintsbyname-Methode**</span><span class="sxs-lookup"><span data-stu-id="e4ce2-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="e4ce2-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e4ce2-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

