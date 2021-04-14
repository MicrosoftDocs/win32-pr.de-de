---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse von ALPC-Empfangs Nachrichten. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977745"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="6c07d-104">ALPC- \_ Empfangs \_ Nachrichten Klasse</span><span class="sxs-lookup"><span data-stu-id="6c07d-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="6c07d-105">Diese Klasse ist die Ereignistyp Klasse für Ereignisse von ALPC-Empfangs Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6c07d-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="6c07d-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6c07d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c07d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c07d-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="6c07d-108">Member</span><span class="sxs-lookup"><span data-stu-id="6c07d-108">Members</span></span>

<span data-ttu-id="6c07d-109">Die **ALPC- \_ Empfangs \_ Nachrichten** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c07d-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="6c07d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c07d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c07d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c07d-111">Properties</span></span>

<span data-ttu-id="6c07d-112">Die **ALPC- \_ Empfangs \_ Nachrichten** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c07d-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c07d-113">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="6c07d-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c07d-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c07d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c07d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c07d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c07d-116">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="6c07d-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c07d-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6c07d-117">Requirements</span></span>



| <span data-ttu-id="6c07d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c07d-118">Requirement</span></span> | <span data-ttu-id="6c07d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6c07d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c07d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c07d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c07d-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c07d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c07d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c07d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c07d-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c07d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




