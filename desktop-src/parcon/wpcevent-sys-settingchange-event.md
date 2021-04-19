---
description: Das Ereignis auf System Ebene, das bei einer Änderung der Jugend Steuerungs Einstellung generiert wurde.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: WPCEVENT_SYS_SETTINGCHANGE-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362699"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="07656-103">Wpcevent \_ sys \_ settingchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="07656-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="07656-104">Das Ereignis auf System Ebene, das bei einer Änderung der Jugend Steuerungs Einstellung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="07656-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="07656-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="07656-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07656-106">*Klasse*</span><span class="sxs-lookup"><span data-stu-id="07656-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-107">Die Klasse, die das Ereignis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="07656-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="07656-108">*Einstellung*</span><span class="sxs-lookup"><span data-stu-id="07656-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-109">Ein Wert der **WPC- \_ Einstellungs** Enumeration.</span><span class="sxs-lookup"><span data-stu-id="07656-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="07656-110">*Besitzer*</span><span class="sxs-lookup"><span data-stu-id="07656-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-111">Die Sicherheits-ID des Benutzers, der das Ereignis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="07656-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="07656-112">*OLDVAL*</span><span class="sxs-lookup"><span data-stu-id="07656-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-113">Der vorherige Wert dieser Einstellung, wenn Sie gelöscht oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="07656-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="07656-114">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="07656-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-115">Der neue Wert dieser Einstellung, wenn hinzugefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="07656-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="07656-116">*`Reason`*</span><span class="sxs-lookup"><span data-stu-id="07656-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-117">Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="07656-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="07656-118">*Optional*</span><span class="sxs-lookup"><span data-stu-id="07656-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="07656-119">Ein optionales Feld.</span><span class="sxs-lookup"><span data-stu-id="07656-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07656-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07656-120">Requirements</span></span>



| <span data-ttu-id="07656-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07656-121">Requirement</span></span> | <span data-ttu-id="07656-122">Wert</span><span class="sxs-lookup"><span data-stu-id="07656-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07656-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07656-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07656-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07656-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07656-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07656-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07656-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="07656-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="07656-127">Header</span><span class="sxs-lookup"><span data-stu-id="07656-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07656-128"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="07656-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07656-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07656-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07656-130">Verwenden von Protokollierungs-APIs für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="07656-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="07656-131">**WPC \_ args \_ Conversation ationinitevent**</span><span class="sxs-lookup"><span data-stu-id="07656-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




