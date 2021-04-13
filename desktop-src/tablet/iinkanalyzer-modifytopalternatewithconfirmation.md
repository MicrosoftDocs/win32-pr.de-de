---
description: Ändert die aktuelle obere Alternative in den angegebenen ianalysisalternate.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343689"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="11333-103">Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode</span><span class="sxs-lookup"><span data-stu-id="11333-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="11333-104">Ändert die aktuelle obere Alternative in den angegebenen [**ianalysisalternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="11333-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="11333-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11333-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="11333-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11333-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11333-107">*Alternative* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11333-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11333-108">Die Alternative zur Analyse, die als neue obere Alternative festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11333-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="11333-109">*Bestätigung automatisch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11333-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11333-110">**Variant \_ TRUE** , um alle frei Hand Blatt Kontext-Knoten, die der Analyse entsprechen, auf den Bestätigungs Typ **ConfirmationType \_ NodeTypeAndProperties** festzulegen (siehe [**icontextnode:: isconfirmed**](icontextnode-isconfirmed.md) und [**ConfirmationType**](confirmationtype.md)); **Variant \_ "False** ", um alle frei Hand Blatt Kontext Knoten festzulegen, die der Analyse entsprechen, in den Bestätigungs Typ " **ConfirmationType \_ None**".</span><span class="sxs-lookup"><span data-stu-id="11333-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11333-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11333-111">Return value</span></span>

<span data-ttu-id="11333-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="11333-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11333-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11333-113">Remarks</span></span>

<span data-ttu-id="11333-114">Um Analyse Alternativen zu erhalten, verwenden Sie die [**iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md), die [**iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)oder die [**iinkanalyzer:: getalternatesforstriche-Methode**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="11333-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="11333-115">Verwenden Sie die [**ianalysisalternate:: getalternatenodes-Methode**](ianalysisalternate-getalternatenodes.md), um die einem alternativen Analyse zugeordneten Kontext Knoten Objekte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="11333-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="11333-116">Verwenden Sie [**icontextnode:: Confirm**](icontextnode-confirm.md), um den bestätentyp für einen Kontext Knoten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="11333-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11333-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11333-117">Requirements</span></span>



| <span data-ttu-id="11333-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11333-118">Requirement</span></span> | <span data-ttu-id="11333-119">Wert</span><span class="sxs-lookup"><span data-stu-id="11333-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11333-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11333-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11333-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11333-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11333-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11333-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11333-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11333-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="11333-124">Header</span><span class="sxs-lookup"><span data-stu-id="11333-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11333-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="11333-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11333-126">DLL</span><span class="sxs-lookup"><span data-stu-id="11333-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11333-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11333-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="11333-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11333-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11333-129">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="11333-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="11333-130">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="11333-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="11333-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="11333-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="11333-132">**Bestätigungs Analyse ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="11333-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="11333-133">Verweis</span><span class="sxs-lookup"><span data-stu-id="11333-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




