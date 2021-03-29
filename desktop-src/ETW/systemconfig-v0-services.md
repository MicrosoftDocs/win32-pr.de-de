---
description: Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c061c6a0c4cbb3e807bcb3418155b1194fcfa28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349319"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="0037b-103">SystemConfig \_ v0 \_ Services-Klasse</span><span class="sxs-lookup"><span data-stu-id="0037b-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="0037b-104">Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0037b-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="0037b-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="0037b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0037b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0037b-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="0037b-107">Member</span><span class="sxs-lookup"><span data-stu-id="0037b-107">Members</span></span>

<span data-ttu-id="0037b-108">Die Klasse " **SystemConfig \_ v0 \_ Services** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0037b-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="0037b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0037b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0037b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0037b-110">Properties</span></span>

<span data-ttu-id="0037b-111">Die **SystemConfig \_ v0 \_ Services** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0037b-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0037b-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0037b-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0037b-113">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="0037b-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="0037b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0037b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0037b-115">Qualifizierer: **wmidataid** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="0037b-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0037b-116">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0037b-116">Display name of the service.</span></span> <span data-ttu-id="0037b-117">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0037b-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="0037b-118">Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="0037b-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="0037b-119">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="0037b-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0037b-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0037b-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0037b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0037b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0037b-122">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="0037b-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="0037b-123">Der Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0037b-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="0037b-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="0037b-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0037b-125">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="0037b-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="0037b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0037b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0037b-127">Qualifizierer: **wmidataid** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="0037b-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="0037b-128">Der Name des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0037b-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="0037b-129">**Service Name**</span><span class="sxs-lookup"><span data-stu-id="0037b-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0037b-130">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="0037b-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="0037b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0037b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0037b-132">Qualifizierer: **wmidataid** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="0037b-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="0037b-133">Eindeutiger Bezeichner des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0037b-133">Unique identifier of the service.</span></span> <span data-ttu-id="0037b-134">Der Bezeichner gibt Aufschluss über die Funktionen, die der Dienst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0037b-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0037b-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0037b-135">Requirements</span></span>



| <span data-ttu-id="0037b-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0037b-136">Requirement</span></span> | <span data-ttu-id="0037b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0037b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0037b-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0037b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0037b-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0037b-139">None supported</span></span><br/>                            |
| <span data-ttu-id="0037b-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0037b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0037b-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0037b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0037b-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0037b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0037b-143">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0037b-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




