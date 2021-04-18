---
description: Diese Klasse ist die Ereignistyp Klasse für Registrierungs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Registry_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bfbf0157141473be4cc2460659912dc662ef7c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977816"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="f3156-104">Registry \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="f3156-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="f3156-105">Diese Klasse ist die Ereignistyp Klasse für Registrierungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f3156-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="f3156-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f3156-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3156-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3156-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="f3156-108">Member</span><span class="sxs-lookup"><span data-stu-id="f3156-108">Members</span></span>

<span data-ttu-id="f3156-109">Die **\_ TypeGroup1-Registrierungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f3156-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f3156-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3156-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3156-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3156-111">Properties</span></span>

<span data-ttu-id="f3156-112">Die **\_ TypeGroup1-Registrierungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3156-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3156-113">Index</span><span class="sxs-lookup"><span data-stu-id="f3156-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3156-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3156-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3156-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3156-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3156-116">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="f3156-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f3156-117">Der Unterschlüssel Index für den Registrierungsvorgang (z. b. enumeratekey).</span><span class="sxs-lookup"><span data-stu-id="f3156-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="f3156-118">Initialtime</span><span class="sxs-lookup"><span data-stu-id="f3156-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3156-119">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="f3156-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3156-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3156-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3156-121">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="f3156-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f3156-122">Anfängliche Zeit des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="f3156-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3156-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="f3156-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3156-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3156-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3156-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3156-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3156-126">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f3156-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f3156-127">Handle für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="f3156-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="f3156-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="f3156-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3156-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3156-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3156-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3156-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3156-131">Qualifizierer: wmidataid (5), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="f3156-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="f3156-132">Der Name des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="f3156-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="f3156-133">Status</span><span class="sxs-lookup"><span data-stu-id="f3156-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3156-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3156-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3156-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3156-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3156-136">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f3156-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f3156-137">Der NTSTATUS-Wert des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="f3156-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3156-138">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f3156-138">Requirements</span></span>



| <span data-ttu-id="f3156-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3156-139">Requirement</span></span> | <span data-ttu-id="f3156-140">Wert</span><span class="sxs-lookup"><span data-stu-id="f3156-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3156-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3156-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f3156-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3156-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3156-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3156-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f3156-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3156-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3156-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3156-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3156-146">**Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f3156-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




