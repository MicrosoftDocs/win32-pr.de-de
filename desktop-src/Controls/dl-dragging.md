---
title: DL_DRAGGING Benachrichtigungs Code (kommctrl. h)
description: Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- Windows-Steuerelemente für DL_DRAGGING Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519335"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="51e40-104">DL- \_ Zieh Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="51e40-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="51e40-105">Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat.</span><span class="sxs-lookup"><span data-stu-id="51e40-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="51e40-106">\_Das Ziehen von DL wird auch in regelmäßigen Abständen beim Ziehen gesendet, auch wenn die Maus nicht bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="51e40-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="51e40-107">Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="51e40-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="51e40-108">Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="51e40-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="51e40-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="51e40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e40-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51e40-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e40-111">Der Steuerelement Bezeichner des Zieh Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="51e40-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="51e40-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51e40-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e40-113">Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den \_ Benachrichtigungs Code für die DL-Zieh Vorgänge, das Handle für das Zieh Listenfeld und die Cursorposition enthält.</span><span class="sxs-lookup"><span data-stu-id="51e40-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e40-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51e40-114">Return value</span></span>

<span data-ttu-id="51e40-115">Der Rückgabewert bestimmt den Typ des Mauszeigers, der von der Zieh Liste festgelegt werden soll. Dabei kann es sich um den DL- \_ stopcursortyp, den DL- \_ copycursor-oder den DL- \_ Wert von "-"</span><span class="sxs-lookup"><span data-stu-id="51e40-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="51e40-116">Wenn ein anderer Wert zurückgegeben wird, ändert sich der Cursor nicht.</span><span class="sxs-lookup"><span data-stu-id="51e40-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e40-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51e40-117">Remarks</span></span>

<span data-ttu-id="51e40-118">Eine Fenster Prozedur verarbeitet in der Regel den \_ Benachrichtigungs Code für die DL-Zieh Vorgänge, indem Sie das Element unter dem Cursor bestimmt und dann ein Einfügesymbol</span><span class="sxs-lookup"><span data-stu-id="51e40-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="51e40-119">Um das Element unter dem Cursor abzurufen, verwenden Sie die [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion, und geben Sie **true** für den *bautescroll* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="51e40-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="51e40-120">Diese Option bewirkt, dass das Zieh Listenfeld regelmäßig einen Bildlauf durchführen kann, wenn der Cursor oberhalb oder unterhalb des Client Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="51e40-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="51e40-121">Um das Einfügesymbol zu zeichnen, verwenden Sie die [**drawinsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="51e40-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e40-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51e40-122">Requirements</span></span>



| <span data-ttu-id="51e40-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51e40-123">Requirement</span></span> | <span data-ttu-id="51e40-124">Wert</span><span class="sxs-lookup"><span data-stu-id="51e40-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51e40-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51e40-125">Minimum supported client</span></span><br/> | <span data-ttu-id="51e40-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51e40-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51e40-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51e40-127">Minimum supported server</span></span><br/> | <span data-ttu-id="51e40-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51e40-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51e40-129">Header</span><span class="sxs-lookup"><span data-stu-id="51e40-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e40-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e40-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





