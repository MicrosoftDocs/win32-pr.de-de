---
title: DL_DROPPED Benachrichtigungs Code (kommctrl. h)
description: Signalisiert, dass der Benutzer einen Zieh Vorgang durch Loslassen der linken Maustaste abgeschlossen hat. Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster. Weitere Informationen finden Sie unter Drag List Box Messages.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- Windows-Steuerelemente für DL_DROPPED Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859356"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="7cb36-106">Benachrichtigungs Code für gelöschte DL \_</span><span class="sxs-lookup"><span data-stu-id="7cb36-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="7cb36-107">Signalisiert, dass der Benutzer einen Zieh Vorgang durch Loslassen der linken Maustaste abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="7cb36-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="7cb36-108">Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="7cb36-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="7cb36-109">Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="7cb36-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7cb36-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cb36-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb36-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7cb36-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cb36-112">Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den gelöschten DL \_ -Benachrichtigungs Code, das Handle für das Zieh Listenfeld und die Cursorposition enthält.</span><span class="sxs-lookup"><span data-stu-id="7cb36-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cb36-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cb36-113">Return value</span></span>

<span data-ttu-id="7cb36-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7cb36-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb36-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cb36-115">Remarks</span></span>

<span data-ttu-id="7cb36-116">Dieser Benachrichtigungs Code wird normalerweise verarbeitet, indem das Element eingefügt wird, das vor dem Element unter dem Cursor in die Liste eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7cb36-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="7cb36-117">Um den Index des Elements an der Cursorposition abzurufen, verwenden Sie die [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7cb36-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="7cb36-118">Beachten Sie, dass der \_ gesendete DL-Benachrichtigungs Code auch dann gesendet wird, wenn sich der Cursor nicht in einem Listenelement befindet.</span><span class="sxs-lookup"><span data-stu-id="7cb36-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="7cb36-119">In diesem Fall gibt **lbitemfrompt** -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb36-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb36-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cb36-120">Requirements</span></span>



| <span data-ttu-id="7cb36-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cb36-121">Requirement</span></span> | <span data-ttu-id="7cb36-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7cb36-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb36-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cb36-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb36-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cb36-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7cb36-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cb36-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb36-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cb36-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7cb36-127">Header</span><span class="sxs-lookup"><span data-stu-id="7cb36-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb36-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cb36-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





