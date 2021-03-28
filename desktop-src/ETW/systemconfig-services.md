---
description: Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97b4d2a56f2ed739403681875e0be4d9e21481ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977472"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="a1841-103">SystemConfig- \_ Dienstklasse</span><span class="sxs-lookup"><span data-stu-id="a1841-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="a1841-104">Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a1841-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="a1841-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a1841-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1841-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1841-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="a1841-107">Member</span><span class="sxs-lookup"><span data-stu-id="a1841-107">Members</span></span>

<span data-ttu-id="a1841-108">Die **SystemConfig \_ Services** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1841-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="a1841-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1841-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1841-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1841-110">Properties</span></span>

<span data-ttu-id="a1841-111">Die **SystemConfig \_ Services** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1841-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1841-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a1841-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1841-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a1841-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1841-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1841-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1841-115">Qualifizierer: **wmidataid** (5), **stringbeendigung ("nullterminiert")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="a1841-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="a1841-116">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="a1841-116">Display name of the service.</span></span> <span data-ttu-id="a1841-117">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a1841-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="a1841-118">Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="a1841-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="a1841-119">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="a1841-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1841-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1841-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1841-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1841-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1841-122">Qualifizierer: **wmidataid** (1), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="a1841-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="a1841-123">Der Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1841-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="a1841-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="a1841-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1841-125">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a1841-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1841-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1841-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1841-127">Qualifizierer: **wmidataid** (6), **stringbeendigung ("nullterminiert")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="a1841-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="a1841-128">Der Name des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1841-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="a1841-129">**Service Name**</span><span class="sxs-lookup"><span data-stu-id="a1841-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1841-130">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a1841-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1841-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1841-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1841-132">Qualifizierer: **wmidataid** (4), **stringbeendigung ("nullterminiert")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="a1841-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="a1841-133">Eindeutiger Bezeichner des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="a1841-133">Unique identifier of the service.</span></span> <span data-ttu-id="a1841-134">Der Bezeichner gibt Aufschluss über die Funktionen, die der Dienst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a1841-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="a1841-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="a1841-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1841-136">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1841-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1841-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1841-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1841-138">Qualifizierer: **wmidataid** (2), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="a1841-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="a1841-139">Aktueller Status des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="a1841-139">Current state of the service.</span></span> <span data-ttu-id="a1841-140">Mögliche Werte finden Sie unter dem **dwcurrentstate** -Member des **Dienst \_ Status \_ Prozesses**.</span><span class="sxs-lookup"><span data-stu-id="a1841-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="a1841-141">**Subprocesstag**</span><span class="sxs-lookup"><span data-stu-id="a1841-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1841-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1841-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1841-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1841-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1841-144">Qualifizierer: **wmidataid** (3), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="a1841-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="a1841-145">Identifiziert den Dienst.</span><span class="sxs-lookup"><span data-stu-id="a1841-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1841-146">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a1841-146">Requirements</span></span>



| <span data-ttu-id="a1841-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1841-147">Requirement</span></span> | <span data-ttu-id="a1841-148">Wert</span><span class="sxs-lookup"><span data-stu-id="a1841-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1841-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1841-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a1841-150">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1841-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1841-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1841-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a1841-152">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1841-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1841-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1841-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1841-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="a1841-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




