---
description: 'Registry_V1_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Registry_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab0326f92d1b084f471f3dc1b57322f69aa645fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106158"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="b1721-104">Registry \_ V1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="b1721-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="b1721-105">Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="b1721-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="b1721-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b1721-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1721-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1721-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="b1721-108">Member</span><span class="sxs-lookup"><span data-stu-id="b1721-108">Members</span></span>

<span data-ttu-id="b1721-109">Die **Klasse Registry \_ V1 \_ TypeGroup1** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1721-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b1721-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1721-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1721-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1721-111">Properties</span></span>

<span data-ttu-id="b1721-112">Die **Klasse Registry \_ V1 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1721-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1721-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="b1721-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1721-114">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="b1721-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1721-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1721-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1721-116">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="b1721-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="b1721-117">Verstrichene Zeit des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="b1721-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1721-118">Index</span><span class="sxs-lookup"><span data-stu-id="b1721-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1721-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1721-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1721-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1721-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1721-121">Qualifizierer: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="b1721-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="b1721-122">Der Unterschlüsselindex für den Registrierungsvorgang (z. B. EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="b1721-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="b1721-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="b1721-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1721-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1721-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1721-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1721-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1721-126">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b1721-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b1721-127">Handle für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b1721-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="b1721-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="b1721-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1721-129">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="b1721-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1721-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1721-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1721-131">Qualifizierer: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="b1721-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b1721-132">Der Name des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="b1721-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="b1721-133">Status</span><span class="sxs-lookup"><span data-stu-id="b1721-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1721-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1721-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1721-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1721-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1721-136">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b1721-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b1721-137">NTSTATUS-Wert des Registrierungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="b1721-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1721-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1721-138">Requirements</span></span>



| <span data-ttu-id="b1721-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1721-139">Requirement</span></span> | <span data-ttu-id="b1721-140">Wert</span><span class="sxs-lookup"><span data-stu-id="b1721-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b1721-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1721-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b1721-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1721-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1721-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1721-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b1721-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1721-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b1721-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1721-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1721-146">**Registrierung**</span><span class="sxs-lookup"><span data-stu-id="b1721-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="b1721-147">**Registrierung \_ V1**</span><span class="sxs-lookup"><span data-stu-id="b1721-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




