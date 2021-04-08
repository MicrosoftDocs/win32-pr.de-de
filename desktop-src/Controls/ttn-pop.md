---
title: TTN_POP Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das Besitzer Fenster, dass eine QuickInfo ausgeblendet werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- Windows-Steuerelemente für TTN_POP Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741448"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="28c7f-105">TTN- \_ Pop-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="28c7f-105">TTN\_POP notification code</span></span>

<span data-ttu-id="28c7f-106">Benachrichtigt das Besitzer Fenster, dass eine QuickInfo ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="28c7f-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="28c7f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="28c7f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="28c7f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28c7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c7f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28c7f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28c7f-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="28c7f-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c7f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28c7f-111">Return value</span></span>

<span data-ttu-id="28c7f-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="28c7f-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c7f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28c7f-113">Requirements</span></span>



| <span data-ttu-id="28c7f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28c7f-114">Requirement</span></span> | <span data-ttu-id="28c7f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="28c7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28c7f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28c7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28c7f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28c7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28c7f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28c7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28c7f-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28c7f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28c7f-120">Header</span><span class="sxs-lookup"><span data-stu-id="28c7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c7f-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c7f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





