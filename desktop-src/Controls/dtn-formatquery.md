---
title: DTN_FORMATQUERY Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruf Feld angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- Windows-Steuerelemente für DTN_FORMATQUERY Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949466"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="5778b-105">DTN \_ formatQuery-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5778b-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="5778b-106">Wird von einem DTP-Steuerelement gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruf Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5778b-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="5778b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5778b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5778b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5778b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5778b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5778b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5778b-110">Ein Zeiger auf eine [**nmdatetimeformatquery**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) -Struktur, die Informationen über das Rückruf Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="5778b-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="5778b-111">Die-Struktur enthält eine Teil Zeichenfolge, die ein Rückruf Feld definiert und die maximal zulässige Größe der Zeichenfolge empfängt, die im Rückruf Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5778b-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5778b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5778b-112">Return value</span></span>

<span data-ttu-id="5778b-113">Der Besitzer des Steuer Elements muss die maximal mögliche Breite des Texts berechnen, der im Rückruf Feld angezeigt wird, den **szmax** -Member der [**nmdatetimeformatquery**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) -Struktur festlegen und 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5778b-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5778b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5778b-114">Remarks</span></span>

<span data-ttu-id="5778b-115">Durch die Behandlung dieses Benachrichtigungs Codes wird das Steuerelement so vorbereitet, dass es die maximale Größe der Zeichenfolge anpasst, die in einem bestimmten Rückruf Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5778b-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="5778b-116">Dies ermöglicht es dem Steuerelement, die Ausgabe jederzeit ordnungsgemäß anzuzeigen und das Flimmern innerhalb der Anzeige des Steuer Elements zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="5778b-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="5778b-117">(Weitere Informationen zu Rückruf Feldern finden Sie unter [Rückruf Felder](date-and-time-picker-controls.md).)</span><span class="sxs-lookup"><span data-stu-id="5778b-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="5778b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5778b-118">Requirements</span></span>



| <span data-ttu-id="5778b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5778b-119">Requirement</span></span> | <span data-ttu-id="5778b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5778b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5778b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5778b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5778b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5778b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5778b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5778b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5778b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5778b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5778b-125">Header</span><span class="sxs-lookup"><span data-stu-id="5778b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5778b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5778b-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5778b-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5778b-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5778b-128">**Dtn \_ Formatqueryw** (Unicode) und **Dtn \_ formatquerya** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5778b-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 





