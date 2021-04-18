---
title: TCN_SELCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich die derzeit ausgewählte Registerkarte ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- Windows-Steuerelemente für TCN_SELCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341354"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="94d3f-105">TCN- \_ selchanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="94d3f-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="94d3f-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich die derzeit ausgewählte Registerkarte ändert.</span><span class="sxs-lookup"><span data-stu-id="94d3f-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="94d3f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="94d3f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="94d3f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94d3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d3f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94d3f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d3f-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="94d3f-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d3f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94d3f-111">Return value</span></span>

<span data-ttu-id="94d3f-112">Gibt **true** zurück, um zu verhindern, dass die Auswahl geändert wird, oder **false** , um die Auswahl zu ändern.</span><span class="sxs-lookup"><span data-stu-id="94d3f-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="94d3f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94d3f-113">Remarks</span></span>

<span data-ttu-id="94d3f-114">Um die aktuell ausgewählte Registerkarte zu ermitteln, verwenden Sie das [**tabstrg \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) -Makro.</span><span class="sxs-lookup"><span data-stu-id="94d3f-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d3f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94d3f-115">Requirements</span></span>



| <span data-ttu-id="94d3f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94d3f-116">Requirement</span></span> | <span data-ttu-id="94d3f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="94d3f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94d3f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94d3f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="94d3f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94d3f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94d3f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94d3f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="94d3f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94d3f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94d3f-122">Header</span><span class="sxs-lookup"><span data-stu-id="94d3f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d3f-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d3f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d3f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94d3f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d3f-125">TCN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="94d3f-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





