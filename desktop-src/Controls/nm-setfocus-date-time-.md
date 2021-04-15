---
title: NM_SETFOCUS (Datum/Uhrzeit) des Benachrichtigungs Codes (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus erhalten hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS (Datum/Uhrzeit) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba80ea119056c131f1dd94cdf1f39a84371b7052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476068"
---
# <a name="nm_setfocus-date-time-notification-code"></a><span data-ttu-id="2b27a-105">NM \_ SetFocus-Benachrichtigungs Code (Datum und Uhrzeit)</span><span class="sxs-lookup"><span data-stu-id="2b27a-105">NM\_SETFOCUS (date time) notification code</span></span>

<span data-ttu-id="2b27a-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="2b27a-106">Notifies a date and time picker control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="2b27a-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="2b27a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2b27a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b27a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b27a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b27a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b27a-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="2b27a-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b27a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b27a-111">Return value</span></span>

<span data-ttu-id="2b27a-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2b27a-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b27a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b27a-113">Requirements</span></span>



| <span data-ttu-id="2b27a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b27a-114">Requirement</span></span> | <span data-ttu-id="2b27a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2b27a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b27a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b27a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b27a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b27a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b27a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b27a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b27a-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b27a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b27a-120">Header</span><span class="sxs-lookup"><span data-stu-id="2b27a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b27a-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b27a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





