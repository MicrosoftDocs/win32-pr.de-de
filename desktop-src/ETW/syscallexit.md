---
description: Diese Klasse ist die Ereignistyp Klasse für Systemaufrufe von Beendigungs Ereignissen. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Syscallexit-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980073"
---
# <a name="syscallexit-class"></a><span data-ttu-id="135f8-104">Syscallexit-Klasse</span><span class="sxs-lookup"><span data-stu-id="135f8-104">SysCallExit class</span></span>

<span data-ttu-id="135f8-105">Diese Klasse ist die Ereignistyp Klasse für Systemaufrufe von Beendigungs Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="135f8-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="135f8-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="135f8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="135f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="135f8-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="135f8-108">Member</span><span class="sxs-lookup"><span data-stu-id="135f8-108">Members</span></span>

<span data-ttu-id="135f8-109">Die **syscallexit** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="135f8-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="135f8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="135f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="135f8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="135f8-111">Properties</span></span>

<span data-ttu-id="135f8-112">Die **syscallexit** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="135f8-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="135f8-113">**Syscallntstatus**</span><span class="sxs-lookup"><span data-stu-id="135f8-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135f8-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135f8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135f8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="135f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135f8-116">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="135f8-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="135f8-117">Der vom NT-System Aufrufwert zurückgegebene Status Code.</span><span class="sxs-lookup"><span data-stu-id="135f8-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="135f8-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="135f8-118">Requirements</span></span>



| <span data-ttu-id="135f8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="135f8-119">Requirement</span></span> | <span data-ttu-id="135f8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="135f8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="135f8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="135f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="135f8-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="135f8-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="135f8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="135f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="135f8-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="135f8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




