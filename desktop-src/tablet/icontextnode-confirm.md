---
description: Ändert den bestäalisierungstyp, der steuert, was das iinkanalyzer-Objekt über den icontextnode ändern kann.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Icontextnode:: Confirm-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345080"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="e5efb-103">Icontextnode:: Confirm-Methode</span><span class="sxs-lookup"><span data-stu-id="e5efb-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="e5efb-104">Ändert den bestäalisierungstyp, der steuert, was das [**iinkanalyzer**](iinkanalyzer.md) -Objekt über den [**icontextnode**](icontextnode.md)ändern kann.</span><span class="sxs-lookup"><span data-stu-id="e5efb-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5efb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5efb-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="e5efb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5efb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5efb-107">*confirmedtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5efb-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5efb-108">Der [**ConfirmationType**](confirmationtype.md) , der auf den Knoten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5efb-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5efb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5efb-109">Return value</span></span>

<span data-ttu-id="e5efb-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e5efb-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5efb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5efb-111">Remarks</span></span>

<span data-ttu-id="e5efb-112">Verwenden Sie diese Methode, um dem Endbenutzer zu ermöglichen, zu bestätigen, dass die Striche von [**iinkanalyzer**](iinkanalyzer.md) ordnungsgemäß analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e5efb-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="e5efb-113">Nachdem **icontextnode:: Confirm** aufgerufen wurde, werden die [**icontextnode**](icontextnode.md) -Objekte für diese Striche von **iinkanalyzer** während der späteren Analyse nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="e5efb-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="e5efb-114">Verwenden Sie **icontextnode:: Confirm** , wenn der Benutzer die Analyseergebnisse bestätigt hat und nicht möchten, dass [**iinkanalyzer**](iinkanalyzer.md) einen [**icontextnode**](icontextnode.md) während der späteren Analyse ändert.</span><span class="sxs-lookup"><span data-stu-id="e5efb-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="e5efb-115">Wenn der Benutzer z. b. das Wort "in" schreibt und die Anwendung die [**iinkanalyzer::**](iinkanalyzer-analyze.md)Analytics-Methode aufruft, generiert die Ink Analyzer einen inkWord-Knoten mit dem Wert "to".</span><span class="sxs-lookup"><span data-stu-id="e5efb-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="e5efb-116">Wenn der Benutzer dann "Me" nach "to" als ein Wort hinzufügt und die Anwendung die **iinkanalyzer:: Analysis-Methode** erneut aufruft, kann der Ink Analyzer den vorherigen "InkWord"-Knoten entfernen und einen neuen inkWord-Knoten mit dem Wert "Tome" erstellen.</span><span class="sxs-lookup"><span data-stu-id="e5efb-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="e5efb-117">Wenn jedoch nach dem ersten **iinkanalyzer**-Ansichts Befehl: Analysemethode: die Anwendung ruft **icontextnode:: Confirm** für den inkWord-Knoten für "to" mit dem [**ConfirmationType**](confirmationtype.md) -Wert **NodeTypeAndProperties** auf, bevor der Benutzer "Me" hinzufügt. wenn die Anwendung die **iinkanalyzer::** Analytics-Methode aufruft, wird der "to"-Knoten von der Ink Analyzer nicht entfernt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="e5efb-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="e5efb-118">Stattdessen erkennt der Ink Analyzer möglicherweise zwei inkWord-Knoten für "to" und "Me".</span><span class="sxs-lookup"><span data-stu-id="e5efb-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="e5efb-119">[**Icontextnode**](icontextnode.md) kann nur Objekte des Typs InkWord und InkDrawing bestätigen (siehe [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="e5efb-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="e5efb-120">**Icontextnode:: Confirm** gibt **E \_ invalidArg** zurück, wenn der Knoten kein Blattknoten ist.</span><span class="sxs-lookup"><span data-stu-id="e5efb-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="e5efb-121">Die [**iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md) und die [**iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md) löschen jeden Knoten, von dem Sie die Strich Daten entfernen.</span><span class="sxs-lookup"><span data-stu-id="e5efb-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="e5efb-122">[**Icontextnode:: setstrokes**](icontextnode-setstrokes.md), [**iinkanalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)und [**iinkanalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) geben **Core \_ E \_ InvalidOperation** zurück, wenn das [**icontextnode**](icontextnode.md) -Objekt bereits bestätigt ist.</span><span class="sxs-lookup"><span data-stu-id="e5efb-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="e5efb-123">[**Icontextnode::**](icontextnode-reparentstrokebyidtonode.md) Analyse Name gibt einen Fehler zurück, wenn der Quell-oder Zielknoten bestätigt ist.</span><span class="sxs-lookup"><span data-stu-id="e5efb-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5efb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5efb-124">Requirements</span></span>



| <span data-ttu-id="e5efb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5efb-125">Requirement</span></span> | <span data-ttu-id="e5efb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e5efb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5efb-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5efb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e5efb-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5efb-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e5efb-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5efb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e5efb-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5efb-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e5efb-131">Header</span><span class="sxs-lookup"><span data-stu-id="e5efb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5efb-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e5efb-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e5efb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e5efb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5efb-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5efb-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e5efb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5efb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5efb-136">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="e5efb-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e5efb-137">**Icontextnode:: isconfirmed**</span><span class="sxs-lookup"><span data-stu-id="e5efb-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="e5efb-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e5efb-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




