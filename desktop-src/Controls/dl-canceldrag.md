---
title: DL_CANCELDRAG Benachrichtigungs Code (kommctrl. h)
description: Signalisiert, dass der Benutzer einen Zieh Vorgang abgebrochen hat, indem er auf die Rechte Maustaste klickt oder die ESC-Taste gedrückt hat.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- Windows-Steuerelemente für DL_CANCELDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106689"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="067f5-104">\_Benachrichtigungs Code zum Abbrechen von DL</span><span class="sxs-lookup"><span data-stu-id="067f5-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="067f5-105">Signalisiert, dass der Benutzer einen Zieh Vorgang abgebrochen hat, indem er auf die Rechte Maustaste klickt oder die ESC-Taste gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="067f5-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="067f5-106">Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="067f5-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="067f5-107">Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="067f5-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="067f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="067f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="067f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="067f5-110">Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den DL \_ -Abbruch Benachrichtigungs Code, das Handle für das Zieh Listenfeld und die Cursorposition enthält.</span><span class="sxs-lookup"><span data-stu-id="067f5-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067f5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="067f5-111">Return value</span></span>

<span data-ttu-id="067f5-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="067f5-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="067f5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="067f5-113">Remarks</span></span>

<span data-ttu-id="067f5-114">Durch die Verarbeitung des DL- \_ CancelDrag-Benachrichtigungs Codes kann eine Anwendung den internen Zustand zurücksetzen, um anzugeben, dass das ziehen nicht wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="067f5-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="067f5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="067f5-115">Requirements</span></span>



| <span data-ttu-id="067f5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="067f5-116">Requirement</span></span> | <span data-ttu-id="067f5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="067f5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="067f5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="067f5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="067f5-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="067f5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="067f5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="067f5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="067f5-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="067f5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="067f5-122">Header</span><span class="sxs-lookup"><span data-stu-id="067f5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="067f5-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="067f5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





