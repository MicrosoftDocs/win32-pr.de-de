---
description: Diese Klasse ist die Ereignistyp Klasse für ALPC SendMessage-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: ALPC_Send_Message-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130008"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="a2b30-104">ALPC \_ Send \_ Message-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2b30-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="a2b30-105">Diese Klasse ist die Ereignistyp Klasse für ALPC SendMessage-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a2b30-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="a2b30-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a2b30-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b30-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2b30-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="a2b30-108">Member</span><span class="sxs-lookup"><span data-stu-id="a2b30-108">Members</span></span>

<span data-ttu-id="a2b30-109">Die **ALPC \_ Send \_ Message** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a2b30-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="a2b30-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2b30-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2b30-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2b30-111">Properties</span></span>

<span data-ttu-id="a2b30-112">Die **ALPC \_ Send \_ Message** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2b30-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2b30-113">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="a2b30-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2b30-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2b30-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2b30-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2b30-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2b30-116">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="a2b30-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2b30-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a2b30-117">Requirements</span></span>



| <span data-ttu-id="a2b30-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2b30-118">Requirement</span></span> | <span data-ttu-id="a2b30-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a2b30-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2b30-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2b30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b30-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b30-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a2b30-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2b30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b30-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b30-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




