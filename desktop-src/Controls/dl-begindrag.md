---
title: DL_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster des Zieh Listen Felds, dass der Benutzer mit der linken Maustaste auf ein Element geklickt hat. Ein Drag-Listenfeld sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht. Weitere Informationen finden Sie unter Drag List Box Messages.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- Windows-Steuerelemente für DL_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859355"
---
# <a name="dl_begindrag-notification-code"></a><span data-ttu-id="2ef75-106">DL \_ BeginDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2ef75-106">DL\_BEGINDRAG notification code</span></span>

<span data-ttu-id="2ef75-107">Benachrichtigt das übergeordnete Fenster des Zieh Listen Felds, dass der Benutzer mit der linken Maustaste auf ein Element geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="2ef75-107">Notifies the drag list box's parent window that the user has clicked the left mouse button on an item.</span></span> <span data-ttu-id="2ef75-108">Ein Drag-Listenfeld sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ef75-108">A drag list box sends this notification code in the form of a drag list message.</span></span> <span data-ttu-id="2ef75-109">Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="2ef75-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2ef75-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ef75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef75-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ef75-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef75-112">Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den DL \_ BeginDrag-Benachrichtigungs Code, das Handle für das Zieh Listenfeld und die Cursorposition enthält.</span><span class="sxs-lookup"><span data-stu-id="2ef75-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_BEGINDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef75-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ef75-113">Return value</span></span>

<span data-ttu-id="2ef75-114">Gibt **true** zurück, um den Zieh Vorgang zu starten, oder **false** , um den Zieh Vorgang zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="2ef75-114">Return **TRUE** to begin the drag operation, or **FALSE** to prevent the drag operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef75-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ef75-115">Remarks</span></span>

<span data-ttu-id="2ef75-116">Bei der Verarbeitung dieses Benachrichtigungs Codes bestimmt eine Fenster Prozedur in der Regel das Listenelement an der angegebenen Cursorposition mithilfe der [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2ef75-116">When processing this notification code, a window procedure typically determines the list item at the specified cursor position by using the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="2ef75-117">Anschließend wird " **true** " oder " **false**" zurückgegeben, je nachdem, ob das Element gezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ef75-117">It then returns **TRUE** or **FALSE**, depending on whether the item should be dragged.</span></span> <span data-ttu-id="2ef75-118">Vor der Rückgabe von **true** sollte die Fenster Prozedur den Index des Listen Elements speichern, damit die Anwendung weiß, welches Element verschoben oder kopiert werden soll, wenn der Zieh Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2ef75-118">Before returning **TRUE**, the window procedure should save the index of the list item so the application knows which item to move or copy when the drag operation is completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef75-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ef75-119">Requirements</span></span>



| <span data-ttu-id="2ef75-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ef75-120">Requirement</span></span> | <span data-ttu-id="2ef75-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2ef75-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef75-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ef75-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef75-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ef75-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ef75-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef75-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ef75-126">Header</span><span class="sxs-lookup"><span data-stu-id="2ef75-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ef75-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef75-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





