---
title: NM_KEYDOWN Benachrichtigungscode (Commctrl.h)
description: 'NM_KEYDOWN Benachrichtigungscode: Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112348"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="993fb-105">NM \_ KEYDOWN-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="993fb-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="993fb-106">Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="993fb-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="993fb-107">Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="993fb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="993fb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="993fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="993fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="993fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="993fb-110">Ein Zeiger auf eine [**NMKEY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmkey) die zusätzliche Informationen über den Schlüssel enthält, der den Benachrichtigungscode verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="993fb-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="993fb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="993fb-111">Return value</span></span>

<span data-ttu-id="993fb-112">Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement den Schlüssel verarbeitet, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="993fb-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="993fb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="993fb-113">Requirements</span></span>



| <span data-ttu-id="993fb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="993fb-114">Requirement</span></span> | <span data-ttu-id="993fb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="993fb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="993fb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="993fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="993fb-117">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="993fb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="993fb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="993fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="993fb-119">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="993fb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="993fb-120">Header</span><span class="sxs-lookup"><span data-stu-id="993fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="993fb-121"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="993fb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





