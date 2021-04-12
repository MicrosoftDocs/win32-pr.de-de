---
title: NM_RDBLCLK (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- NM_RDBLCLK (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478255"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a><span data-ttu-id="f5c5d-105">NM \_ rdblclk (Toolbar)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f5c5d-105">NM\_RDBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="f5c5d-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-106">Notifies a control's parent window that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="f5c5d-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f5c5d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5c5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c5d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5c5d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c5d-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="f5c5d-111">Wenn auf ein Symbolleisten Element auf die Maus geklickt wurde, enthält das Element **dwitemspec** den Element Bezeichner, und der **dwitemdata** -Member enthält die Elementdaten.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="f5c5d-112">Wenn die Maus auf ein Trennzeichen oder Leerraum auf der Symbolleiste geklickt wurde, enthält das Element **dwitemspec** -1.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c5d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5c5d-113">Return value</span></span>

<span data-ttu-id="f5c5d-114">Gibt **false** zurück, damit das Symbolleisten-Steuerelement die Standard Verarbeitung des Ereignisses ausführen kann, oder **true** , um zu verhindern, dass das Steuerelement das Ereignis verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c5d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5c5d-115">Requirements</span></span>



| <span data-ttu-id="f5c5d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5c5d-116">Requirement</span></span> | <span data-ttu-id="f5c5d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f5c5d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c5d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5c5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c5d-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5c5d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5c5d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5c5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c5d-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5c5d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5c5d-122">Header</span><span class="sxs-lookup"><span data-stu-id="f5c5d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c5d-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





