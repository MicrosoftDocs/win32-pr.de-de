---
description: Diese Klasse ist die Ereignistyp Klasse für die ALPC-Wartezeit auf Antwort Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: ALPC_Wait_For_Reply-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977729"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="19cef-104">ALPC \_ wartet \_ auf \_ Antwort Klasse</span><span class="sxs-lookup"><span data-stu-id="19cef-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="19cef-105">Diese Klasse ist die Ereignistyp Klasse für die ALPC-Wartezeit auf Antwort Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="19cef-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="19cef-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="19cef-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="19cef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19cef-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="19cef-108">Member</span><span class="sxs-lookup"><span data-stu-id="19cef-108">Members</span></span>

<span data-ttu-id="19cef-109">Die **ALPC \_ Wait \_ for \_ Reply** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="19cef-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="19cef-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19cef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19cef-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19cef-111">Properties</span></span>

<span data-ttu-id="19cef-112">Die **ALPC \_ Wait \_ for \_ Reply** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19cef-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19cef-113">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="19cef-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19cef-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19cef-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19cef-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="19cef-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19cef-116">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="19cef-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19cef-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="19cef-117">Requirements</span></span>



| <span data-ttu-id="19cef-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19cef-118">Requirement</span></span> | <span data-ttu-id="19cef-119">Wert</span><span class="sxs-lookup"><span data-stu-id="19cef-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19cef-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19cef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19cef-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19cef-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19cef-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19cef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19cef-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19cef-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




