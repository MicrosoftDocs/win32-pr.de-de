---
title: DTN_FORMAT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) zum Anfordern von Text gesendet, der in einem Rückruf Feld angezeigt werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- Windows-Steuerelemente für DTN_FORMAT Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477634"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="bfe85-105">DTN- \_ Format-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bfe85-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="bfe85-106">Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) zum Anfordern von Text gesendet, der in einem Rückruf Feld angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfe85-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="bfe85-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bfe85-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bfe85-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfe85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfe85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfe85-110">Ein Zeiger auf eine [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) -Struktur, die Informationen zu dieser Instanz des Benachrichtigungs Codes enthält.</span><span class="sxs-lookup"><span data-stu-id="bfe85-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="bfe85-111">Die Struktur enthält die Teil Zeichenfolge, die das Rückruf Feld definiert, und empfängt die formatierte Zeichenfolge, die vom Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bfe85-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe85-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfe85-112">Return value</span></span>

<span data-ttu-id="bfe85-113">Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bfe85-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe85-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfe85-114">Remarks</span></span>

<span data-ttu-id="bfe85-115">Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements eine benutzerdefinierte Zeichenfolge bereitstellen, die vom Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bfe85-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="bfe85-116">(Weitere Informationen zu Rückruf Feldern finden Sie unter [Rückruf Felder](date-and-time-picker-controls.md).)</span><span class="sxs-lookup"><span data-stu-id="bfe85-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe85-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfe85-117">Requirements</span></span>



| <span data-ttu-id="bfe85-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfe85-118">Requirement</span></span> | <span data-ttu-id="bfe85-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bfe85-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe85-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfe85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe85-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfe85-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfe85-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfe85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe85-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfe85-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfe85-124">Header</span><span class="sxs-lookup"><span data-stu-id="bfe85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe85-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe85-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bfe85-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bfe85-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bfe85-127">**Dtn \_ Formatw** (Unicode) und **Dtn \_ Formata** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bfe85-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 





