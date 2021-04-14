---
description: Diese Klasse ist die Ereignistyp Klasse für Registrierungs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9a72a0d6ddfe5e441b21dff4ba58fa3bb37457a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977632"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="42910-104">Registry \_ v0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="42910-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="42910-105">Diese Klasse ist die Ereignistyp Klasse für Registrierungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="42910-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="42910-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="42910-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="42910-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42910-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="42910-108">Member</span><span class="sxs-lookup"><span data-stu-id="42910-108">Members</span></span>

<span data-ttu-id="42910-109">Die **Registrierungs Klasse " \_ v0 \_ TypeGroup1** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="42910-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="42910-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42910-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42910-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42910-111">Properties</span></span>

<span data-ttu-id="42910-112">Die **Registrierungs Klasse " \_ v0 \_ TypeGroup1** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42910-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42910-113">Verweilzeit</span><span class="sxs-lookup"><span data-stu-id="42910-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42910-114">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="42910-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="42910-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42910-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42910-116">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="42910-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="42910-117">Verstrichene Zeit des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="42910-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="42910-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="42910-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42910-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42910-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42910-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42910-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42910-121">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="42910-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="42910-122">Handle für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="42910-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="42910-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="42910-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42910-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42910-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42910-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42910-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42910-126">Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="42910-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="42910-127">Der Name des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="42910-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="42910-128">Status</span><span class="sxs-lookup"><span data-stu-id="42910-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42910-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42910-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42910-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42910-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42910-131">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="42910-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="42910-132">Der NTSTATUS-Wert des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="42910-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42910-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="42910-133">Requirements</span></span>



| <span data-ttu-id="42910-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42910-134">Requirement</span></span> | <span data-ttu-id="42910-135">Wert</span><span class="sxs-lookup"><span data-stu-id="42910-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42910-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42910-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42910-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42910-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="42910-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42910-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42910-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42910-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42910-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42910-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42910-141">**Registrierung \_ v0**</span><span class="sxs-lookup"><span data-stu-id="42910-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




