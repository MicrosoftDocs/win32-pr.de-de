---
title: NM_RELEASEDCAPTURE (Pager)-Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigegeben hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- NM_RELEASEDCAPTURE (Pager)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858959"
---
# <a name="nm_releasedcapture-pager-notification-code"></a><span data-ttu-id="098b0-105">NM \_ releasedcapture (Pager)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="098b0-105">NM\_RELEASEDCAPTURE (pager) notification code</span></span>

<span data-ttu-id="098b0-106">Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="098b0-106">Notifies a pager control's parent window that the control has released the mouse capture.</span></span> <span data-ttu-id="098b0-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="098b0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="098b0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="098b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="098b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="098b0-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="098b0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="098b0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="098b0-111">Return value</span></span>

<span data-ttu-id="098b0-112">Der Rückgabewert wird vom Pager-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="098b0-112">The return value is ignored by the pager control.</span></span>

## <a name="requirements"></a><span data-ttu-id="098b0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="098b0-113">Requirements</span></span>



| <span data-ttu-id="098b0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="098b0-114">Requirement</span></span> | <span data-ttu-id="098b0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="098b0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="098b0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="098b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="098b0-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="098b0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="098b0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="098b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="098b0-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="098b0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="098b0-120">Header</span><span class="sxs-lookup"><span data-stu-id="098b0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="098b0-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="098b0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





