---
title: NM_RCLICK (Statusleiste) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (Statusleiste) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341368"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="dd068-105">NM \_ rclick-Benachrichtigungs Code (Statusleiste)</span><span class="sxs-lookup"><span data-stu-id="dd068-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="dd068-106">Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="dd068-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="dd068-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="dd068-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="dd068-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd068-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd068-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd068-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="dd068-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd068-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd068-111">Return value</span></span>

<span data-ttu-id="dd068-112">Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System.</span><span class="sxs-lookup"><span data-stu-id="dd068-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="dd068-113">Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="dd068-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd068-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd068-114">Requirements</span></span>



| <span data-ttu-id="dd068-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd068-115">Requirement</span></span> | <span data-ttu-id="dd068-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dd068-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd068-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd068-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd068-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd068-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd068-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd068-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd068-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd068-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd068-121">Header</span><span class="sxs-lookup"><span data-stu-id="dd068-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd068-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd068-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





