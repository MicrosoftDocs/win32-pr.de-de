---
title: NM_KEYDOWN (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040094"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="875b6-105">NM- \_ KeyDown-Benachrichtigungs Code (Symbolleiste)</span><span class="sxs-lookup"><span data-stu-id="875b6-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="875b6-106">Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="875b6-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="875b6-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="875b6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="875b6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="875b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="875b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="875b6-110">Ein Zeiger auf eine [**nmkey**](/windows/win32/api/commctrl/ns-commctrl-nmkey) -Struktur, die zusätzliche Informationen über den Schlüssel enthält, der den Benachrichtigungs Code verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="875b6-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875b6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="875b6-111">Return value</span></span>

<span data-ttu-id="875b6-112">Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement den Schlüssel verarbeitet, andernfalls</span><span class="sxs-lookup"><span data-stu-id="875b6-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="875b6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="875b6-113">Remarks</span></span>

<span data-ttu-id="875b6-114">Derzeit sendet nur das Symbolleisten-Steuerelement diesen Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="875b6-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="875b6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="875b6-115">Requirements</span></span>



| <span data-ttu-id="875b6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="875b6-116">Requirement</span></span> | <span data-ttu-id="875b6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="875b6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="875b6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="875b6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="875b6-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="875b6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="875b6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="875b6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="875b6-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="875b6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="875b6-122">Header</span><span class="sxs-lookup"><span data-stu-id="875b6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="875b6-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="875b6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





