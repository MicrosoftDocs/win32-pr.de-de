---
title: Symbolleisten-Schaltflächen Zustände (kommstrg. h)
description: In diesem Abschnitt sind die Zustände aufgeführt, die eine Symbolleisten-Schaltfläche haben
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371096"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="29529-103">Symbolleisten Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="29529-103">Toolbar Button States</span></span>

<span data-ttu-id="29529-104">In diesem Abschnitt sind die Zustände aufgeführt, die eine Symbolleisten-Schaltfläche haben</span><span class="sxs-lookup"><span data-stu-id="29529-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="29529-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="29529-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="29529-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29529-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="29529-107"><dt>**TBSTATE \_ aktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="29529-108">Die Schaltfläche hat den [**tbstyle- \_ prüfstil**](toolbar-control-and-button-styles.md) , auf den geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="29529-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="29529-109"><dt>**TBSTATE- \_ Ellipsen**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="29529-110">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="29529-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="29529-111">Der Text der Schaltfläche wird abgeschnitten, und es wird eine Ellipse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29529-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="29529-112"><dt>**TBSTATE \_ aktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="29529-113">Die Schaltfläche akzeptiert Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="29529-113">The button accepts user input.</span></span> <span data-ttu-id="29529-114">Eine Schaltfläche, die nicht über diesen Zustand verfügt, ist abgeblendet.</span><span class="sxs-lookup"><span data-stu-id="29529-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="29529-115"><dt>**TBSTATE \_ ausgeblendet**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="29529-116">Die Schaltfläche ist nicht sichtbar und kann keine Benutzereingaben empfangen.</span><span class="sxs-lookup"><span data-stu-id="29529-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="29529-117"><dt>**TBSTATE \_ unbestimmt**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="29529-118">Die Schaltfläche ist abgeblendet.</span><span class="sxs-lookup"><span data-stu-id="29529-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="29529-119"><dt>**TBSTATE \_ markiert**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="29529-120">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="29529-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="29529-121">Die Schaltfläche ist gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="29529-121">The button is marked.</span></span> <span data-ttu-id="29529-122">Die Interpretation eines markierten Elements hängt von der Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="29529-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="29529-123"><dt>**TBSTATE \_ gedrückt**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="29529-124">Auf die Schaltfläche wird geklickt.</span><span class="sxs-lookup"><span data-stu-id="29529-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="29529-125"><dt>**TBSTATE- \_ Wrap**</dt></span><span class="sxs-lookup"><span data-stu-id="29529-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="29529-126">Auf die Schaltfläche folgt ein Zeilenumbruch.</span><span class="sxs-lookup"><span data-stu-id="29529-126">The button is followed by a line break.</span></span> <span data-ttu-id="29529-127">Für die Schaltfläche muss außerdem der Status "TBSTATE" \_ aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="29529-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="29529-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29529-128">Remarks</span></span>

<span data-ttu-id="29529-129">Eine Symbolleiste kann eine Kombination aus Zuständen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="29529-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="29529-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29529-130">Requirements</span></span>



| <span data-ttu-id="29529-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29529-131">Requirement</span></span> | <span data-ttu-id="29529-132">Wert</span><span class="sxs-lookup"><span data-stu-id="29529-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29529-133">Header</span><span class="sxs-lookup"><span data-stu-id="29529-133">Header</span></span><br/> | <dl> <span data-ttu-id="29529-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="29529-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





