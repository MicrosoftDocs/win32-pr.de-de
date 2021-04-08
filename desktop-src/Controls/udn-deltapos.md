---
title: UDN_DELTAPOS Benachrichtigungs Code (kommctrl. h)
description: Wird vom Betriebssystem an das übergeordnete Fenster eines auf-ab-Steuer Elements gesendet, wenn sich die Position des-Steuer Elements ändert.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- Windows-Steuerelemente für UDN_DELTAPOS Benachrichtigungs
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741681"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="120eb-104">Udn- \_ Delta-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="120eb-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="120eb-105">Wird vom Betriebssystem an das übergeordnete Fenster eines auf-ab-Steuer Elements gesendet, wenn sich die Position des-Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="120eb-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="120eb-106">Dies geschieht, wenn der Benutzer eine Änderung des Werts anfordert, indem er den Pfeil nach oben oder nach unten drückt.</span><span class="sxs-lookup"><span data-stu-id="120eb-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="120eb-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="120eb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="120eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="120eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="120eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="120eb-110">Ein Zeiger auf eine [**nmupdown**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) -Struktur, die Informationen über die Positionsänderung enthält.</span><span class="sxs-lookup"><span data-stu-id="120eb-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="120eb-111">Der **IPOs** -Member dieser-Struktur enthält die aktuelle Position des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="120eb-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="120eb-112">Der **idelta** -Member der-Struktur ist eine Ganzzahl mit Vorzeichen, die die vorgeschlagene Änderung an der Position enthält.</span><span class="sxs-lookup"><span data-stu-id="120eb-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="120eb-113">Wenn der Benutzer auf die Schaltfläche "nach oben" geklickt hat, ist dies ein positiver Wert.</span><span class="sxs-lookup"><span data-stu-id="120eb-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="120eb-114">Wenn der Benutzer auf die Schaltfläche "nach unten" geklickt hat, ist dies ein negativer Wert.</span><span class="sxs-lookup"><span data-stu-id="120eb-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120eb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="120eb-115">Return value</span></span>

<span data-ttu-id="120eb-116">Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass die Position des Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="120eb-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="120eb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="120eb-117">Remarks</span></span>

<span data-ttu-id="120eb-118">Der udn- \_ Delta-Delta-Benachrichtigungs Code wird vor der [**WM- \_ VScroll**](wm-vscroll.md) -oder [**WM- \_ HScroll**](wm-hscroll.md) -Nachricht gesendet, die tatsächlich die Position des Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="120eb-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="120eb-119">Dies ermöglicht es Ihnen, die Änderung zu überprüfen, zuzulassen, zu ändern oder zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="120eb-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="120eb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="120eb-120">Requirements</span></span>



| <span data-ttu-id="120eb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="120eb-121">Requirement</span></span> | <span data-ttu-id="120eb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="120eb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="120eb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="120eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="120eb-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="120eb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="120eb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="120eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="120eb-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="120eb-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="120eb-127">Header</span><span class="sxs-lookup"><span data-stu-id="120eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="120eb-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="120eb-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120eb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="120eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120eb-130">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="120eb-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

