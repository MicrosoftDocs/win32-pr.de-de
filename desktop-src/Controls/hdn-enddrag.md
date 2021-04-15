---
title: HDN_ENDDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang auf einem seiner Elemente beendet wurde. Dieser Benachrichtigungs Code wird als WM-Benachrichtigungs \_ Meldung gesendet. Nur Header Steuerelemente, die auf den HDS DragDrop-Stil festgelegt sind, \_ senden diesen Benachrichtigungs Code.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- Windows-Steuerelemente für HDN_ENDDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479455"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="123c1-106">Hdn- \_ EndDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="123c1-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="123c1-107">Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang auf einem seiner Elemente beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="123c1-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="123c1-108">Dieser Benachrichtigungs Code wird als [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="123c1-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="123c1-109">Nur Header Steuerelemente, die auf den [**HDS \_ DragDrop**](header-control-styles.md) -Stil festgelegt sind, senden diesen Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="123c1-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="123c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="123c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="123c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="123c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="123c1-112">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Element enthält, das gezogen wurde.</span><span class="sxs-lookup"><span data-stu-id="123c1-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="123c1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="123c1-113">Return value</span></span>

<span data-ttu-id="123c1-114">Damit das Steuerelement das Element automatisch platzieren und neu anordnen kann, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="123c1-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="123c1-115">Um zu verhindern, dass das Element platziert wird, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="123c1-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="123c1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="123c1-116">Remarks</span></span>

<span data-ttu-id="123c1-117">Wenn der Besitzer eine externe (manuelle) Drag & Drop-Verwaltung durchführt, muss er **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="123c1-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="123c1-118">Der Besitzer muss dann die Header Elemente manuell neu anordnen, indem er [**HDM \_**](hdm-setitem.md) -Server oder [**HDM-Server \_ Array**](hdm-setorderarray.md)sendet.</span><span class="sxs-lookup"><span data-stu-id="123c1-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="123c1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="123c1-119">Requirements</span></span>



| <span data-ttu-id="123c1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="123c1-120">Requirement</span></span> | <span data-ttu-id="123c1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="123c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="123c1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="123c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="123c1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="123c1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="123c1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="123c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="123c1-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="123c1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="123c1-126">Header</span><span class="sxs-lookup"><span data-stu-id="123c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="123c1-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="123c1-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





