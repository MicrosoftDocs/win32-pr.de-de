---
title: TCN_SELCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich die derzeit ausgewählte Registerkarte geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- Windows-Steuerelemente für TCN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739864"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="32b95-105">TCN \_ selChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="32b95-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="32b95-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich die derzeit ausgewählte Registerkarte geändert hat.</span><span class="sxs-lookup"><span data-stu-id="32b95-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="32b95-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="32b95-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="32b95-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32b95-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b95-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="32b95-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b95-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32b95-111">Return value</span></span>

<span data-ttu-id="32b95-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="32b95-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b95-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32b95-113">Remarks</span></span>

<span data-ttu-id="32b95-114">Um die aktuell ausgewählte Registerkarte zu ermitteln, verwenden Sie das [**tabstrg \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) -Makro.</span><span class="sxs-lookup"><span data-stu-id="32b95-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b95-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b95-115">Requirements</span></span>



| <span data-ttu-id="32b95-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32b95-116">Requirement</span></span> | <span data-ttu-id="32b95-117">Wert</span><span class="sxs-lookup"><span data-stu-id="32b95-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32b95-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32b95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32b95-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32b95-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32b95-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32b95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32b95-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32b95-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32b95-122">Header</span><span class="sxs-lookup"><span data-stu-id="32b95-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b95-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="32b95-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b95-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32b95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b95-125">TCN \_ selchanging</span><span class="sxs-lookup"><span data-stu-id="32b95-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





