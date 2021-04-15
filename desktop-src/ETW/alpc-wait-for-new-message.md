---
description: Diese Klasse ist die Ereignistyp Klasse für die ALPC-Wartezeit auf neue Nachrichten Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977736"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="82dad-104">ALPC- \_ Wartezeit \_ für \_ neue Message- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="82dad-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="82dad-105">Diese Klasse ist die Ereignistyp Klasse für die ALPC-Wartezeit auf neue Nachrichten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="82dad-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="82dad-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="82dad-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82dad-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="82dad-108">Member</span><span class="sxs-lookup"><span data-stu-id="82dad-108">Members</span></span>

<span data-ttu-id="82dad-109">Die **ALPC- \_ Wartezeit \_ für eine \_ neue \_ Message** -Klasse hat diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="82dad-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="82dad-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82dad-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82dad-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82dad-111">Properties</span></span>

<span data-ttu-id="82dad-112">Die **ALPC \_ Wait \_ for \_ New \_ Message** Class hat diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82dad-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82dad-113">**Isserverport**</span><span class="sxs-lookup"><span data-stu-id="82dad-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82dad-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82dad-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82dad-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82dad-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82dad-116">Gibt an, ob der Port ein Serverport ist.</span><span class="sxs-lookup"><span data-stu-id="82dad-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="82dad-117">**Portname**</span><span class="sxs-lookup"><span data-stu-id="82dad-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82dad-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82dad-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82dad-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82dad-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82dad-120">Eine Zeichenfolge, die den Namen des Ports enthält, auf den ALPC wartet.</span><span class="sxs-lookup"><span data-stu-id="82dad-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82dad-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82dad-121">Requirements</span></span>



| <span data-ttu-id="82dad-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82dad-122">Requirement</span></span> | <span data-ttu-id="82dad-123">Wert</span><span class="sxs-lookup"><span data-stu-id="82dad-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82dad-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82dad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="82dad-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82dad-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="82dad-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82dad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="82dad-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82dad-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




