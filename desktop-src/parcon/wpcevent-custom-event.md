---
description: Pro Benutzer-Ereignis, das bis zu drei Felder unterstützt.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215869"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="17687-103">Benutzerdefiniertes wpcevent- \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="17687-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="17687-104">Pro Benutzer-Ereignis, das bis zu drei Felder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17687-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="17687-105">Ereignisse werden in der **Aktivitäts** Anzeige im **anderen** Abschnitt mit der folgenden Hierarchie angezeigt:</span><span class="sxs-lookup"><span data-stu-id="17687-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="17687-106">Publisher</span><span class="sxs-lookup"><span data-stu-id="17687-106">Publisher</span></span>

2.  <span data-ttu-id="17687-107">Application</span><span class="sxs-lookup"><span data-stu-id="17687-107">Application</span></span>

3.  <span data-ttu-id="17687-108">Ereignis</span><span class="sxs-lookup"><span data-stu-id="17687-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="17687-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="17687-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17687-110">*Publisher*</span><span class="sxs-lookup"><span data-stu-id="17687-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-111">Der Herausgeber des Ereignisses (z. b. ein Firmenname).</span><span class="sxs-lookup"><span data-stu-id="17687-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="17687-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="17687-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-113">Der Name der Anwendung, die das Ereignis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="17687-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="17687-114">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="17687-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-115">Die Version der Anwendung, die das Ereignis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="17687-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="17687-116">*Event*</span><span class="sxs-lookup"><span data-stu-id="17687-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-117">Der Name des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="17687-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="17687-118">*Value1*</span><span class="sxs-lookup"><span data-stu-id="17687-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-119">Benutzerdefiniertes Feld 1.</span><span class="sxs-lookup"><span data-stu-id="17687-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="17687-120">*Value2*</span><span class="sxs-lookup"><span data-stu-id="17687-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-121">Benutzerdefiniertes Feld 2.</span><span class="sxs-lookup"><span data-stu-id="17687-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="17687-122">*Wert3*</span><span class="sxs-lookup"><span data-stu-id="17687-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-123">Benutzerdefiniertes Feld 3.</span><span class="sxs-lookup"><span data-stu-id="17687-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="17687-124">*Gesperrt*</span><span class="sxs-lookup"><span data-stu-id="17687-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-125">Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="17687-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="17687-126">*`Reason`*</span><span class="sxs-lookup"><span data-stu-id="17687-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="17687-127">Eine benutzerdefinierte Zeichenfolge, die zusätzliche Informationen über den Grund für das Blockieren oder nicht blockieren bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="17687-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17687-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17687-128">Requirements</span></span>



| <span data-ttu-id="17687-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17687-129">Requirement</span></span> | <span data-ttu-id="17687-130">Wert</span><span class="sxs-lookup"><span data-stu-id="17687-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17687-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17687-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17687-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17687-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17687-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17687-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17687-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="17687-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="17687-135">Header</span><span class="sxs-lookup"><span data-stu-id="17687-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="17687-136"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="17687-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17687-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17687-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17687-138">Verwenden von Protokollierungs-APIs für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="17687-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="17687-139">**WPC \_ args \_ Conversation ationinitevent**</span><span class="sxs-lookup"><span data-stu-id="17687-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




