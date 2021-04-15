---
title: NM_RELEASEDCAPTURE (Registerkarte) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- Windows-Steuerelemente (Registerkarte) NM_RELEASEDCAPTURE
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
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477553"
---
# <a name="nm_releasedcapture-tab-notification-code"></a><span data-ttu-id="585fc-105">NM \_ releasedcapture (Registerkarte)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="585fc-105">NM\_RELEASEDCAPTURE (tab) notification code</span></span>

<span data-ttu-id="585fc-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt.</span><span class="sxs-lookup"><span data-stu-id="585fc-106">Notifies a tab control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="585fc-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="585fc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="585fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="585fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="585fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="585fc-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="585fc-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="585fc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="585fc-111">Return value</span></span>

<span data-ttu-id="585fc-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="585fc-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="585fc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="585fc-113">Requirements</span></span>



| <span data-ttu-id="585fc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="585fc-114">Requirement</span></span> | <span data-ttu-id="585fc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="585fc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="585fc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="585fc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="585fc-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="585fc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="585fc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="585fc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="585fc-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="585fc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="585fc-120">Header</span><span class="sxs-lookup"><span data-stu-id="585fc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="585fc-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="585fc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





