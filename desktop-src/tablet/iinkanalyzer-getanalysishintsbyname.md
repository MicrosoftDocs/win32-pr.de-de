---
description: Ruft alle Analysis Hint-icontextnode-Objekte ab, die an iinkanalyzer angefügt sind und den angegebenen Namen aufweisen.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Iinkanalyzer:: getanalysishintsbyname-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214662"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="bc7d5-103">Iinkanalyzer:: getanalysishintsbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="bc7d5-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="bc7d5-104">Ruft alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte ab, die an [**iinkanalyzer**](iinkanalyzer.md) angefügt sind und den angegebenen Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc7d5-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="bc7d5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc7d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc7d5-107">*hintname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc7d5-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7d5-108">Der Hinweis Name, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="bc7d5-109">*ppanalysishints* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc7d5-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7d5-110">Der Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte in [**iinkanalyzer**](iinkanalyzer.md) mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc7d5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc7d5-111">Return value</span></span>

<span data-ttu-id="bc7d5-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md) die Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc7d5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc7d5-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bc7d5-114">Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppanalysishints* aufrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="bc7d5-115">Diese Methode gibt eine leere Auflistung zurück, wenn keine derartigen Analyse Hinweis Knoten an [**iinkanalyzer**](iinkanalyzer.md)angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="bc7d5-116">Ein Analyse Hinweis Knoten ist ein [**icontextnode**](icontextnode.md) mit dem Kontext Knotentyp AnalysisHint (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="bc7d5-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="bc7d5-117">Wenn Sie dem Hinweis Kontextinformationen hinzufügen möchten, verwenden Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) mit dem Parameter *ppropertydataid* , der auf einen der global eindeutigen Bezeichner (GUIDs) in den Eigenschaften Konstanten von [Analysis Hint](analysis-hint-properties.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bc7d5-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="bc7d5-118">Um zu ermitteln, welche Eigenschaftswerte für einen Kontext Knoten festgelegt werden, verwenden Sie [**icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="bc7d5-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="bc7d5-119">Um den Wert einer Eigenschaft zu suchen, verwenden Sie [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="bc7d5-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc7d5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc7d5-120">Requirements</span></span>



| <span data-ttu-id="bc7d5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc7d5-121">Requirement</span></span> | <span data-ttu-id="bc7d5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bc7d5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7d5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc7d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc7d5-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc7d5-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc7d5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc7d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc7d5-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc7d5-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bc7d5-127">Header</span><span class="sxs-lookup"><span data-stu-id="bc7d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc7d5-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bc7d5-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bc7d5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="bc7d5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc7d5-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc7d5-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bc7d5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc7d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc7d5-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="bc7d5-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="bc7d5-133">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="bc7d5-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="bc7d5-134">**Iinkanalyzer:: feateanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="bc7d5-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="bc7d5-135">**Iinkanalyzer::D eleteanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="bc7d5-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="bc7d5-136">**Iinkanalyzer:: GetAnalysisHints-Methode**</span><span class="sxs-lookup"><span data-stu-id="bc7d5-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="bc7d5-137">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="bc7d5-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

