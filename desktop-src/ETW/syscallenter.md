---
description: Diese Klasse ist die Ereignistyp Klasse für Systemaufrufe von Enter-Ereignissen. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Syscallenter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980080"
---
# <a name="syscallenter-class"></a><span data-ttu-id="f1ef0-104">Syscallenter-Klasse</span><span class="sxs-lookup"><span data-stu-id="f1ef0-104">SysCallEnter class</span></span>

<span data-ttu-id="f1ef0-105">Diese Klasse ist die Ereignistyp Klasse für Systemaufrufe von Enter-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="f1ef0-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="f1ef0-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f1ef0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ef0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1ef0-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="f1ef0-108">Member</span><span class="sxs-lookup"><span data-stu-id="f1ef0-108">Members</span></span>

<span data-ttu-id="f1ef0-109">Die **syscallenter** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f1ef0-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="f1ef0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1ef0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1ef0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1ef0-111">Properties</span></span>

<span data-ttu-id="f1ef0-112">Die **syscallenter** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1ef0-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1ef0-113">**Syscalladdress**</span><span class="sxs-lookup"><span data-stu-id="f1ef0-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ef0-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1ef0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1ef0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1ef0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1ef0-116">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f1ef0-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f1ef0-117">Adresse des eingegebenen NT-Funktions Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="f1ef0-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1ef0-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f1ef0-118">Requirements</span></span>



| <span data-ttu-id="f1ef0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1ef0-119">Requirement</span></span> | <span data-ttu-id="f1ef0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f1ef0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1ef0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1ef0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ef0-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1ef0-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1ef0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1ef0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ef0-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1ef0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




