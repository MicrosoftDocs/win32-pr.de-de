---
title: DTN_WMKEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer ein Rückruf Feld eingibt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- Windows-Steuerelemente für DTN_WMKEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103062"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="58643-105">DTN \_ wmKeyDown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="58643-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="58643-106">Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer ein Rückruf Feld eingibt.</span><span class="sxs-lookup"><span data-stu-id="58643-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="58643-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="58643-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="58643-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="58643-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58643-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58643-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58643-110">Ein Zeiger auf eine [**nmdatetimewmkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) -Struktur, die Informationen zu dieser Instanz des Benachrichtigungs Codes enthält.</span><span class="sxs-lookup"><span data-stu-id="58643-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="58643-111">Die Struktur enthält Informationen über den Schlüssel, den der Benutzer eingegeben hat, die Teil Zeichenfolge, die das Rückruf Feld definiert, und das aktuelle Systemdatum und die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="58643-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58643-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58643-112">Return value</span></span>

<span data-ttu-id="58643-113">Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="58643-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="58643-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58643-114">Remarks</span></span>

<span data-ttu-id="58643-115">Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruf Felder des Steuer Elements bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="58643-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="58643-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58643-116">Requirements</span></span>



| <span data-ttu-id="58643-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58643-117">Requirement</span></span> | <span data-ttu-id="58643-118">Wert</span><span class="sxs-lookup"><span data-stu-id="58643-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58643-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58643-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58643-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58643-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58643-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58643-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58643-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58643-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58643-123">Header</span><span class="sxs-lookup"><span data-stu-id="58643-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="58643-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="58643-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="58643-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="58643-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="58643-126">**Dtn \_ Wmkeydownw** (Unicode) und **Dtn \_ wmkeydowna** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="58643-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





