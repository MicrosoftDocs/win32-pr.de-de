---
description: 'Registry_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: d86412a950246bee4f9a692ab80e91b99d945c20
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106248"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="47313-104">Klasse \_ "Registry TypeGroup1"</span><span class="sxs-lookup"><span data-stu-id="47313-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="47313-105">Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="47313-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="47313-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="47313-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="47313-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47313-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="47313-108">Member</span><span class="sxs-lookup"><span data-stu-id="47313-108">Members</span></span>

<span data-ttu-id="47313-109">Die **Klasse \_ "Registry TypeGroup1"** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="47313-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="47313-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47313-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47313-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47313-111">Properties</span></span>

<span data-ttu-id="47313-112">Die **Klasse \_ Registry TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47313-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47313-113">Index</span><span class="sxs-lookup"><span data-stu-id="47313-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47313-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="47313-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47313-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47313-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47313-116">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="47313-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="47313-117">Der Unterschlüsselindex für den Registrierungsvorgang (z. B. EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="47313-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="47313-118">InitialTime</span><span class="sxs-lookup"><span data-stu-id="47313-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47313-119">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="47313-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="47313-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47313-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47313-121">Qualifizierer: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="47313-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="47313-122">Anfangszeit des Registrierungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="47313-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="47313-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="47313-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47313-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="47313-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47313-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47313-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47313-126">Qualifizierer: WmiDataId(4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="47313-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="47313-127">Handle für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="47313-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="47313-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="47313-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47313-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="47313-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47313-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47313-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47313-131">Qualifizierer: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="47313-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="47313-132">Der Name des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="47313-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="47313-133">Status</span><span class="sxs-lookup"><span data-stu-id="47313-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47313-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="47313-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47313-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47313-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47313-136">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="47313-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="47313-137">NTSTATUS-Wert des Registrierungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="47313-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47313-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47313-138">Requirements</span></span>



| <span data-ttu-id="47313-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47313-139">Requirement</span></span> | <span data-ttu-id="47313-140">Wert</span><span class="sxs-lookup"><span data-stu-id="47313-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47313-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47313-141">Minimum supported client</span></span><br/> | <span data-ttu-id="47313-142">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47313-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="47313-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47313-143">Minimum supported server</span></span><br/> | <span data-ttu-id="47313-144">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47313-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47313-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47313-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47313-146">**Registrierung**</span><span class="sxs-lookup"><span data-stu-id="47313-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




