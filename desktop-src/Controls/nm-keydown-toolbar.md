---
title: NM_KEYDOWN (Symbolleiste) Benachrichtigungscode (Commctrl.h)
description: 'NM_KEYDOWN Benachrichtigungscode (Symbolleiste): Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN (Symbolleiste) Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112358"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="5fd57-105">NM \_ KEYDOWN-Benachrichtigungscode (Symbolleiste)</span><span class="sxs-lookup"><span data-stu-id="5fd57-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="5fd57-106">Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="5fd57-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="5fd57-107">Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="5fd57-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5fd57-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fd57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd57-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fd57-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd57-110">Zeiger auf eine [**NMKEY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmkey) die zusätzliche Informationen über den Schlüssel enthält, der den Benachrichtigungscode verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="5fd57-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd57-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fd57-111">Return value</span></span>

<span data-ttu-id="5fd57-112">Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement den Schlüssel verarbeitet, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5fd57-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd57-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fd57-113">Remarks</span></span>

<span data-ttu-id="5fd57-114">Derzeit sendet nur das Symbolleisten-Steuerelement diesen Benachrichtigungscode.</span><span class="sxs-lookup"><span data-stu-id="5fd57-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd57-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fd57-115">Requirements</span></span>



| <span data-ttu-id="5fd57-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fd57-116">Requirement</span></span> | <span data-ttu-id="5fd57-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5fd57-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd57-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fd57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd57-119">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fd57-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fd57-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fd57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd57-121">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fd57-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fd57-122">Header</span><span class="sxs-lookup"><span data-stu-id="5fd57-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd57-123"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd57-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





