---
description: Ereignis pro Benutzer zur Protokollierung der Initiierung von Konversationen durch Instant Messaging-Clients.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363661"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="3b061-103">Wpcevent \_ im- \_ Einladungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="3b061-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="3b061-104">Ereignis pro Benutzer zur Protokollierung der Initiierung von Konversationen durch Instant Messaging-Clients.</span><span class="sxs-lookup"><span data-stu-id="3b061-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="3b061-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b061-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b061-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="3b061-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-107">Der Name der Anwendung, die das Ereignis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="3b061-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-108">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="3b061-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-109">Die Versions Zeichenfolge für die Anwendung, die das Ereignis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="3b061-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="3b061-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-111">Die Identitäts Zeichenfolge für das Instant Messaging-Konto.</span><span class="sxs-lookup"><span data-stu-id="3b061-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-112">*Geseld*</span><span class="sxs-lookup"><span data-stu-id="3b061-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-113">Der Bezeichner für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="3b061-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-114">*Requestingip*</span><span class="sxs-lookup"><span data-stu-id="3b061-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-115">Eine Zeichenfolge, die die IP-Adresse des Computers enthält, von dem die Einladung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b061-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-116">*Sender*</span><span class="sxs-lookup"><span data-stu-id="3b061-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-117">Die Identitäts Zeichenfolge für das Instant Messaging-Konto für das Konto, von dem die Einladung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b061-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-118">*`Reason`*</span><span class="sxs-lookup"><span data-stu-id="3b061-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-119">Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3b061-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-120">*Anzahl der Mitarbeiter*</span><span class="sxs-lookup"><span data-stu-id="3b061-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-121">Die Anzahl der Empfänger, die die Einladung erhalten und deren Identitäten im Feld Empfänger definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3b061-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="3b061-122">*Recipient*</span><span class="sxs-lookup"><span data-stu-id="3b061-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="3b061-123">Eine durch Trennzeichen getrennte Zeichenfolge, die für die Empfänger der Einladung Instant Messaging-Konto Identitäts Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="3b061-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b061-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b061-124">Requirements</span></span>



| <span data-ttu-id="3b061-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b061-125">Requirement</span></span> | <span data-ttu-id="3b061-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3b061-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b061-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b061-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3b061-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b061-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b061-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b061-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3b061-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3b061-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="3b061-131">Header</span><span class="sxs-lookup"><span data-stu-id="3b061-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b061-132"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b061-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b061-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b061-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b061-134">Verwenden von Protokollierungs-APIs für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3b061-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="3b061-135">**WPC \_ args \_ Conversation ationinitevent**</span><span class="sxs-lookup"><span data-stu-id="3b061-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




