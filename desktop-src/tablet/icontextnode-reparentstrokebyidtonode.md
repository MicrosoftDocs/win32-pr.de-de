---
description: Verschiebt die Strich Daten aus diesem icontextnode in den angegebenen icontextnode.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Icontextnode:: Analyse-strokebyidtonode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360053"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="ff607-103">Icontextnode:: Analyse-strokebyidtonode-Methode</span><span class="sxs-lookup"><span data-stu-id="ff607-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="ff607-104">Verschiebt die Strich Daten aus diesem [**icontextnode**](icontextnode.md) in den angegebenen **icontextnode**.</span><span class="sxs-lookup"><span data-stu-id="ff607-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff607-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff607-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="ff607-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff607-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff607-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff607-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff607-108">Der Bezeichner des zu verschiebenden Strichs.</span><span class="sxs-lookup"><span data-stu-id="ff607-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="ff607-109">*pcontextnode Destination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff607-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff607-110">Das [**icontextnode**](icontextnode.md) -Objekt, in das die Strich Daten verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff607-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff607-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff607-111">Return value</span></span>

<span data-ttu-id="ff607-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ff607-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff607-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff607-113">Remarks</span></span>

<span data-ttu-id="ff607-114">Das angegebene [**icontextnode**](icontextnode.md) -Objekt muss einer der folgenden Typen aus den [Kontext Knoten Typen](context-node-types.md) Konstanten sein: **InkWord**, **InkDrawing**, **InkBullet** oder **unclassimeedink**.</span><span class="sxs-lookup"><span data-stu-id="ff607-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="ff607-115">Der Versuch, einen Strich in einen anderen Typ von **icontextnode** -Objekten zu verschieben, führt zu einem Rückgabewert von **E \_ invalidArg**.</span><span class="sxs-lookup"><span data-stu-id="ff607-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="ff607-116">Diese Methode kann von einem beliebigen [**icontextnode**](icontextnode.md) -Objekt aus aufgerufen werden, einschließlich nicht frei Hand Blatts **icontextnode** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="ff607-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="ff607-117">Auf den angegebenen Strich muss von einem der nachfolgenden Elemente dieses **icontextnode** -Objekts verwiesen werden, oder **E \_ invalidArg** wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff607-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="ff607-118">Wenn entweder dieser [**icontextnode**](icontextnode.md) oder der **icontextnode** in *pcontextnodebug-Ziel* bestätigt wird, wird **E \_ invalidArg** zurückgegeben (siehe [**icontextnode:: isconfirmed**](icontextnode-isconfirmed.md)).</span><span class="sxs-lookup"><span data-stu-id="ff607-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="ff607-119">Leere Kontext Knoten werden von der frei Hand Analyse nicht als Antwort auf diese Methode aus der Ergebnis Struktur gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ff607-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="ff607-120">Ein frei Hand Blattknoten, der nicht auf hubdaten verweist, ist ein leerer Knoten.</span><span class="sxs-lookup"><span data-stu-id="ff607-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="ff607-121">Ein Container Knoten, der nicht auf untergeordnete Knoten verweist, ist ein leerer Knoten.</span><span class="sxs-lookup"><span data-stu-id="ff607-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="ff607-122">Ein leerer Knoten generiert Fehler, wenn er während eines frei Hand Analyse Vorgangs in der Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="ff607-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="ff607-123">Um einen Knoten aus der Struktur der Ink Analyzer zu entfernen, müssen Sie die [**icontextnode::D eletesubnode**](icontextnode-deletesubnode.md) -Methode des übergeordneten Knotens aufrufen (siehe [**icontextnode:: getParser Node**](icontextnode-getparentnode.md)).</span><span class="sxs-lookup"><span data-stu-id="ff607-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff607-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff607-124">Requirements</span></span>



| <span data-ttu-id="ff607-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff607-125">Requirement</span></span> | <span data-ttu-id="ff607-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ff607-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff607-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff607-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ff607-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff607-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ff607-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff607-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ff607-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff607-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ff607-131">Header</span><span class="sxs-lookup"><span data-stu-id="ff607-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff607-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ff607-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ff607-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ff607-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff607-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff607-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ff607-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff607-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff607-136">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="ff607-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ff607-137">**Icontextnode:: setstrokes**</span><span class="sxs-lookup"><span data-stu-id="ff607-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="ff607-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ff607-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




