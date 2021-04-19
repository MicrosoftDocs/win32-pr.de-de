---
title: NM_CHAR Benachrichtigungs Code (kommctrl. h)
description: Der nm \_ char-Benachrichtigungs Code wird von einem-Steuerelement gesendet, wenn eine Zeichen Taste verarbeitet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- Windows-Steuerelemente für NM_CHAR Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346773"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="e3c4d-105">NM \_ char-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e3c4d-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="e3c4d-106">Der nm \_ char-Benachrichtigungs Code wird von einem-Steuerelement gesendet, wenn eine Zeichen Taste verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e3c4d-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="e3c4d-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="e3c4d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e3c4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3c4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3c4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3c4d-110">Ein Zeiger auf eine [**nmchar**](/windows/win32/api/commctrl/ns-commctrl-nmchar) -Struktur, die zusätzliche Informationen über das Zeichen enthält, das den Benachrichtigungs Code verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="e3c4d-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c4d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3c4d-111">Return value</span></span>

<span data-ttu-id="e3c4d-112">Der Rückgabewert wird von den meisten Steuerelementen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e3c4d-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="e3c4d-113">Weitere Informationen finden Sie in der Dokumentation für die einzelnen Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e3c4d-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c4d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3c4d-114">Requirements</span></span>



| <span data-ttu-id="e3c4d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3c4d-115">Requirement</span></span> | <span data-ttu-id="e3c4d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c4d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c4d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3c4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3c4d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3c4d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3c4d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3c4d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3c4d-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3c4d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3c4d-121">Header</span><span class="sxs-lookup"><span data-stu-id="e3c4d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3c4d-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c4d-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c4d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3c4d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c4d-124">NM \_ char (Symbolleiste)</span><span class="sxs-lookup"><span data-stu-id="e3c4d-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 





