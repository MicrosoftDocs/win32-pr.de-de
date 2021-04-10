---
description: Im folgenden finden Sie die Flicks-Konstanten.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Flicks-Konstanten (tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129536"
---
# <a name="flicks-constants"></a><span data-ttu-id="c8a24-103">Flicks-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c8a24-103">Flicks Constants</span></span>

<span data-ttu-id="c8a24-104">Im folgenden finden Sie die Flicks-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c8a24-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="c8a24-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="c8a24-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="c8a24-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8a24-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="c8a24-107"><dt>**Flicke \_ Mit WM \_ behandelte \_ Maske**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="c8a24-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="c8a24-108">Der Wert, der nach der Verarbeitung der [**WM- \_ Tablet- \_ Nachricht**](wm-tablet-flick-message.md) zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8a24-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="c8a24-109">Wenn die von **Flick \_ WM \_ behandelte \_ Maske** zurückgegeben wird, erfolgt keine weitere Aktion.</span><span class="sxs-lookup"><span data-stu-id="c8a24-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="c8a24-110">Andernfalls sendet Windows nach Verfolgungs Benachrichtigungen, wie z. b. [**WM \_ appcommand**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VScroll**](/windows/desktop/Controls/wm-vscroll)oder [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown), je nachdem, welche Aktion dem Stift Flick zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c8a24-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="c8a24-111"><dt>**NUM \_ \_Richtung**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c8a24-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="c8a24-112">Die Anzahl der Richtungen, die in der [**flieration der flimerrichtung**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c8a24-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="c8a24-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8a24-113">Requirements</span></span>



| <span data-ttu-id="c8a24-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8a24-114">Requirement</span></span> | <span data-ttu-id="c8a24-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c8a24-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a24-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8a24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a24-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8a24-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c8a24-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8a24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a24-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8a24-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c8a24-120">Header</span><span class="sxs-lookup"><span data-stu-id="c8a24-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8a24-121"><dt>Tabflicks. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8a24-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a24-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8a24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a24-123">**Flickdirection-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c8a24-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="c8a24-124">**WM- \_ Tablet \_ Flick-Nachricht**</span><span class="sxs-lookup"><span data-stu-id="c8a24-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="c8a24-125">Gesten Flicks</span><span class="sxs-lookup"><span data-stu-id="c8a24-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="c8a24-126">[Reagieren auf Pen-Flicks](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8a24-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

