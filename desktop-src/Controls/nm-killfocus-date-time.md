---
title: NM_KILLFOCUS (Datum/Uhrzeit) des Benachrichtigungs Codes (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus verloren hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (Datum/Uhrzeit) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af47dca130d1025341e2a3c625c1bf7a9c44c42a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949414"
---
# <a name="nm_killfocus-date-time-notification-code"></a><span data-ttu-id="38770-105">NM- \_ killfokus (Date Time)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="38770-105">NM\_KILLFOCUS (date time) notification code</span></span>

<span data-ttu-id="38770-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="38770-106">Notifies a date and time picker control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="38770-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="38770-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="38770-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="38770-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38770-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38770-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38770-110">Die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="38770-110">The address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38770-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38770-111">Return value</span></span>

<span data-ttu-id="38770-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="38770-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="38770-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38770-113">Requirements</span></span>



| <span data-ttu-id="38770-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38770-114">Requirement</span></span> | <span data-ttu-id="38770-115">Wert</span><span class="sxs-lookup"><span data-stu-id="38770-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38770-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38770-116">Minimum supported client</span></span><br/> | <span data-ttu-id="38770-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38770-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38770-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38770-118">Minimum supported server</span></span><br/> | <span data-ttu-id="38770-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38770-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38770-120">Header</span><span class="sxs-lookup"><span data-stu-id="38770-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="38770-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="38770-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





