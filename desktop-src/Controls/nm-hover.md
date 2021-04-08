---
title: NM_HOVER Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Steuerelement gesendet, wenn mit dem Mauszeiger auf ein Element gezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- Windows-Steuerelemente für NM_HOVER Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739928"
---
# <a name="nm_hover-notification-code"></a><span data-ttu-id="ef6f4-105">NM- \_ Hover-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ef6f4-105">NM\_HOVER notification code</span></span>

<span data-ttu-id="ef6f4-106">Wird von einem Steuerelement gesendet, wenn mit dem Mauszeiger auf ein Element gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef6f4-106">Sent by a control when the mouse hovers over an item.</span></span> <span data-ttu-id="ef6f4-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ef6f4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ef6f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef6f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef6f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef6f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef6f4-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="ef6f4-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef6f4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef6f4-111">Return value</span></span>

<span data-ttu-id="ef6f4-112">Sofern nicht anders angegeben, wird NULL zurückgegeben, damit das Steuerelement den Mauszeiger Normal verarbeiten kann, oder ungleich NULL, um zu verhindern, dass der Mauszeiger verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef6f4-112">Unless otherwise specified, return zero to allow the control to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef6f4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef6f4-113">Requirements</span></span>



| <span data-ttu-id="ef6f4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef6f4-114">Requirement</span></span> | <span data-ttu-id="ef6f4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ef6f4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6f4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef6f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef6f4-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef6f4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef6f4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef6f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef6f4-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef6f4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef6f4-120">Header</span><span class="sxs-lookup"><span data-stu-id="ef6f4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef6f4-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef6f4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





