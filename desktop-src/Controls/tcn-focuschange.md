---
title: TCN_FOCUSCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich der Schaltflächen Fokus geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- Windows-Steuerelemente für TCN_FOCUSCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739865"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="2a2ac-105">TCN \_ focuschange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2a2ac-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="2a2ac-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich der Schaltflächen Fokus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="2a2ac-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2a2ac-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a2ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a2ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a2ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a2ac-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a2ac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a2ac-111">Return value</span></span>

<span data-ttu-id="2a2ac-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a2ac-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a2ac-113">Requirements</span></span>



| <span data-ttu-id="2a2ac-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a2ac-114">Requirement</span></span> | <span data-ttu-id="2a2ac-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2a2ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2ac-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a2ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a2ac-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a2ac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a2ac-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a2ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a2ac-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a2ac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a2ac-120">Header</span><span class="sxs-lookup"><span data-stu-id="2a2ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a2ac-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a2ac-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





