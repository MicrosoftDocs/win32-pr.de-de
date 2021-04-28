---
description: 'Registry_V0_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106188"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="414f8-104">Registry \_ V0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="414f8-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="414f8-105">Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="414f8-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="414f8-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="414f8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="414f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="414f8-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="414f8-108">Member</span><span class="sxs-lookup"><span data-stu-id="414f8-108">Members</span></span>

<span data-ttu-id="414f8-109">Die **Klasse Registry \_ V0 \_ TypeGroup1** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="414f8-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="414f8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="414f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="414f8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="414f8-111">Properties</span></span>

<span data-ttu-id="414f8-112">Die **Klasse Registry \_ V0 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="414f8-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="414f8-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="414f8-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="414f8-114">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="414f8-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="414f8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="414f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="414f8-116">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="414f8-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="414f8-117">Verstrichene Zeit des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="414f8-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="414f8-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="414f8-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="414f8-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="414f8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="414f8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="414f8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="414f8-121">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="414f8-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="414f8-122">Handle für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="414f8-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="414f8-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="414f8-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="414f8-124">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="414f8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="414f8-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="414f8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="414f8-126">Qualifizierer: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="414f8-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="414f8-127">Der Name des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="414f8-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="414f8-128">Status</span><span class="sxs-lookup"><span data-stu-id="414f8-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="414f8-129">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="414f8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="414f8-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="414f8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="414f8-131">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="414f8-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="414f8-132">NTSTATUS-Wert des Registrierungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="414f8-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="414f8-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="414f8-133">Requirements</span></span>



| <span data-ttu-id="414f8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="414f8-134">Requirement</span></span> | <span data-ttu-id="414f8-135">Wert</span><span class="sxs-lookup"><span data-stu-id="414f8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="414f8-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="414f8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="414f8-137">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="414f8-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="414f8-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="414f8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="414f8-139">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="414f8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="414f8-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="414f8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414f8-141">**Registrierung \_ V0**</span><span class="sxs-lookup"><span data-stu-id="414f8-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




