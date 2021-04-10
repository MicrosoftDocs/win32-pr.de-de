---
title: RBN_LAYOUTCHANGED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer das Layout der Bänder eines Steuer Elements ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- Windows-Steuerelemente für RBN_LAYOUTCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104769"
---
# <a name="rbn_layoutchanged-notification-code"></a><span data-ttu-id="e7a02-105">RBN \_ layoutchanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e7a02-105">RBN\_LAYOUTCHANGED notification code</span></span>

<span data-ttu-id="e7a02-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer das Layout der Bänder eines Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="e7a02-106">Sent by a rebar control when the user changes the layout of the control's bands.</span></span> <span data-ttu-id="e7a02-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="e7a02-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e7a02-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7a02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7a02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7a02-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="e7a02-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7a02-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7a02-111">Return value</span></span>

<span data-ttu-id="e7a02-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7a02-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a02-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7a02-113">Requirements</span></span>



| <span data-ttu-id="e7a02-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7a02-114">Requirement</span></span> | <span data-ttu-id="e7a02-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e7a02-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a02-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7a02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a02-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7a02-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7a02-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7a02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a02-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7a02-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7a02-120">Header</span><span class="sxs-lookup"><span data-stu-id="e7a02-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7a02-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a02-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





