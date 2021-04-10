---
title: NM_TOOLTIPSCREATED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- Windows-Steuerelemente für NM_TOOLTIPSCREATED Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040435"
---
# <a name="nm_tooltipscreated-notification-code"></a><span data-ttu-id="2afc0-105">NM- \_ tooltipscreated-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2afc0-105">NM\_TOOLTIPSCREATED notification code</span></span>

<span data-ttu-id="2afc0-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement ein QuickInfo-Steuerelement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2afc0-106">Notifies a control's parent window that the control has created a tooltip control.</span></span> <span data-ttu-id="2afc0-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="2afc0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2afc0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2afc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2afc0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2afc0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2afc0-110">Ein Zeiger auf eine [**nmtooltipscreated**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="2afc0-110">A pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2afc0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2afc0-111">Return value</span></span>

<span data-ttu-id="2afc0-112">Sofern nicht anders angegeben, ignoriert das Steuerelement den Rückgabewert aus diesem Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="2afc0-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2afc0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2afc0-113">Requirements</span></span>



| <span data-ttu-id="2afc0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2afc0-114">Requirement</span></span> | <span data-ttu-id="2afc0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2afc0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2afc0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2afc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2afc0-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2afc0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2afc0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2afc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2afc0-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2afc0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2afc0-120">Header</span><span class="sxs-lookup"><span data-stu-id="2afc0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2afc0-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2afc0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





