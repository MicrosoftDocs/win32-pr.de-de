---
title: NM_RELEASEDCAPTURE (monthcal)-Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines monthcal-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- NM_RELEASEDCAPTURE (monthcal)-Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739920"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a><span data-ttu-id="11cc7-105">NM \_ releasedcapture (monthcal)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="11cc7-105">NM\_RELEASEDCAPTURE (monthcal) notification code</span></span>

<span data-ttu-id="11cc7-106">Benachrichtigt das übergeordnete Fenster eines monthcal-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt.</span><span class="sxs-lookup"><span data-stu-id="11cc7-106">Notifies a monthcal control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="11cc7-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="11cc7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="11cc7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11cc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11cc7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11cc7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11cc7-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="11cc7-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11cc7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11cc7-111">Return value</span></span>

<span data-ttu-id="11cc7-112">Das-Steuerelement ignoriert den Rückgabewert aus diesem Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="11cc7-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11cc7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11cc7-113">Requirements</span></span>



| <span data-ttu-id="11cc7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11cc7-114">Requirement</span></span> | <span data-ttu-id="11cc7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="11cc7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11cc7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11cc7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11cc7-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11cc7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11cc7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11cc7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11cc7-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11cc7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11cc7-120">Header</span><span class="sxs-lookup"><span data-stu-id="11cc7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11cc7-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="11cc7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





