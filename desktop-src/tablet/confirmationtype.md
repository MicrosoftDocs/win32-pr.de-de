---
description: Gibt den Typ der Bestätigung an, der in einem icontextnode-Objekt auftreten kann.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: ConfirmationType-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345650"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="bd6c2-103">ConfirmationType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="bd6c2-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="bd6c2-104">Gibt den Typ der Bestätigung an, der in einem [**icontextnode**](icontextnode.md) -Objekt auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd6c2-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="bd6c2-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bd6c2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bd6c2-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ None**</span><span class="sxs-lookup"><span data-stu-id="bd6c2-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="bd6c2-108">Es wird keine Bestätigung angewendet.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-108">No confirmation is applied.</span></span> <span data-ttu-id="bd6c2-109">Der [**iinkanalyzer**](iinkanalyzer.md) kann einen Kontext Knoten oder einen seiner Nachfolger nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="bd6c2-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**</span><span class="sxs-lookup"><span data-stu-id="bd6c2-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="bd6c2-111">Der [**iinkanalyzer**](iinkanalyzer.md) kann den Typ oder keine Eigenschaften des angegebenen Kontext Knotens ändern.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="bd6c2-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType- \_ TopBorder**</span><span class="sxs-lookup"><span data-stu-id="bd6c2-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="bd6c2-113">Der [**iinkanalyzer**](iinkanalyzer.md) führt keine Vorgänge aus, z. b. das Hinzufügen von frei Hand Eingaben oder das Zusammenführen mit anderen [**ContextNodes**](icontextnodes.md), die bewirken, dass die topgrenze die aktuelle obere Grenze überschreitet.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="bd6c2-114">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bd6c2-114">For example:</span></span>

-   <span data-ttu-id="bd6c2-115">Eine Anwendung analysiert eine Menge von frei Hand Eingaben, und es wird ein ParagraphNode identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="bd6c2-116">Die Anwendung bestätigt die topgrenze dieses Absatzes.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="bd6c2-117">Der Benutzer der Anwendung schreibt neue frei Hand Eingaben oberhalb des aktuellen Absatzes.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="bd6c2-118">Wenn die Analyse erneut aufgerufen wird, wird die neue frei Hand Eingabe nicht in den bestätigten Absatz Knoten integriert.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="bd6c2-119">Da nur die obere Grenze bestätigt wird, kann der ContextNode weiterhin in andere Richtungen vergrößert werden.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="bd6c2-120">Das Löschen von Strichen kann bewirken, dass die obere Grenze nach unten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="bd6c2-121">Das Übersetzen von ContextNode kann dazu führen, dass sich der Speicherort ändert, aber keine weiteren frei Hand Eingaben an der neuen Position zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="bd6c2-122">Dieser ConfirmationType gilt nur für Absatz Knoten.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd6c2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd6c2-123">Remarks</span></span>

<span data-ttu-id="bd6c2-124">Sie können den **NoDebug typeandproperties** -Wert nur für frei Hand Wort-und frei Hand Zeichnungs Knoten verwenden (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="bd6c2-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="bd6c2-125">Andernfalls wird ein **E \_ invalidArg** von [**icontextnode:: Confirm**](icontextnode-confirm.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd6c2-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6c2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd6c2-126">Requirements</span></span>



| <span data-ttu-id="bd6c2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd6c2-127">Requirement</span></span> | <span data-ttu-id="bd6c2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bd6c2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6c2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd6c2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6c2-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd6c2-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd6c2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd6c2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6c2-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bd6c2-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bd6c2-133">Header</span><span class="sxs-lookup"><span data-stu-id="bd6c2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6c2-134"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bd6c2-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd6c2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd6c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6c2-136">**Icontextnode:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="bd6c2-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="bd6c2-137">**Icontextnode:: isconfirmed**</span><span class="sxs-lookup"><span data-stu-id="bd6c2-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




