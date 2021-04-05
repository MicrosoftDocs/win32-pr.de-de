---
title: NM_CLICK (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- NM_CLICK (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859339"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="f1626-105">NM \_ Click (Symbolleisten)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f1626-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="f1626-106">Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt.</span><span class="sxs-lookup"><span data-stu-id="f1626-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="f1626-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f1626-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f1626-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1626-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1626-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1626-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1626-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="f1626-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="f1626-111">Der **dwitemspec** -Member enthält den Index des Abschnitts, auf den geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1626-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1626-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1626-112">Return value</span></span>

<span data-ttu-id="f1626-113">Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System.</span><span class="sxs-lookup"><span data-stu-id="f1626-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="f1626-114">Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="f1626-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1626-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1626-115">Remarks</span></span>

<span data-ttu-id="f1626-116">Wenn Sie mit der linken Maustaste auf ein Element klicken, sendet die Symbolleiste eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht, bei der der auf das übergeordnete Fenster [ \_ geklickt](bn-clicked.md) hat.</span><span class="sxs-lookup"><span data-stu-id="f1626-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="f1626-117">Die nm- \_ Click-Benachrichtigung wird nach der **WM- \_ Befehls** Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f1626-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1626-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1626-118">Requirements</span></span>



| <span data-ttu-id="f1626-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1626-119">Requirement</span></span> | <span data-ttu-id="f1626-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f1626-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1626-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1626-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1626-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1626-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1626-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1626-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1626-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1626-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1626-125">Header</span><span class="sxs-lookup"><span data-stu-id="f1626-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1626-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1626-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

