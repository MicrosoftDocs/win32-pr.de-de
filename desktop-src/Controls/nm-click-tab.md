---
title: NM_CLICK (Registerkarte) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Windows-Steuerelemente (Registerkarte) NM_CLICK
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106640"
---
# <a name="nm_click-tab-notification-code"></a><span data-ttu-id="baaee-105">Anzeige von "nm \_ Click (Tab)"</span><span class="sxs-lookup"><span data-stu-id="baaee-105">NM\_CLICK (tab) notification code</span></span>

<span data-ttu-id="baaee-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="baaee-106">Notifies the parent window of a tab control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="baaee-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="baaee-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="baaee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="baaee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baaee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baaee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baaee-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="baaee-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baaee-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baaee-111">Return value</span></span>

<span data-ttu-id="baaee-112">Der Rückgabewert wird vom Registerkarten-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="baaee-112">The return value is ignored by the tab control.</span></span>

## <a name="requirements"></a><span data-ttu-id="baaee-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baaee-113">Requirements</span></span>



| <span data-ttu-id="baaee-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baaee-114">Requirement</span></span> | <span data-ttu-id="baaee-115">Wert</span><span class="sxs-lookup"><span data-stu-id="baaee-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baaee-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="baaee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="baaee-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baaee-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baaee-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="baaee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="baaee-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baaee-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="baaee-120">Header</span><span class="sxs-lookup"><span data-stu-id="baaee-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="baaee-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="baaee-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





