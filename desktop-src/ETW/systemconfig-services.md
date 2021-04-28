---
description: 'SystemConfig_Services-Klasse: Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.'
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
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106058"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="fb7b3-103">SystemConfig \_ Services-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb7b3-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="fb7b3-104">Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="fb7b3-105">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb7b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb7b3-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="fb7b3-107">Member</span><span class="sxs-lookup"><span data-stu-id="fb7b3-107">Members</span></span>

<span data-ttu-id="fb7b3-108">Die **SystemConfig \_ Services-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb7b3-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="fb7b3-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7b3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb7b3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7b3-110">Properties</span></span>

<span data-ttu-id="fb7b3-111">Die **SystemConfig \_ Services-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb7b3-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7b3-113">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7b3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-115">Qualifizierer: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="fb7b3-116">Anzeigename des Diensts.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-116">Display name of the service.</span></span> <span data-ttu-id="fb7b3-117">Der Name wird im Dienststeuerungs-Manager beibehalten.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="fb7b3-118">Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="fb7b3-119">**Processid**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7b3-120">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7b3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-122">Qualifizierer: **WmiDataId** (1), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="fb7b3-123">Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="fb7b3-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7b3-125">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7b3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-127">Qualifizierer: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="fb7b3-128">Name des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="fb7b3-129">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7b3-130">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7b3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-132">Qualifizierer: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="fb7b3-133">Eindeutiger Bezeichner des Diensts.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-133">Unique identifier of the service.</span></span> <span data-ttu-id="fb7b3-134">Der Bezeichner gibt einen Hinweis auf die Funktionalität an, die der Dienst bietet.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="fb7b3-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7b3-136">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7b3-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-138">Qualifizierer: **WmiDataId** (2), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="fb7b3-139">Aktueller Status des Diensts.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-139">Current state of the service.</span></span> <span data-ttu-id="fb7b3-140">Mögliche Werte finden Sie im **dwCurrentState-Member** von **SERVICE STATUS \_ \_ PROCESS.**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="fb7b3-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7b3-142">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7b3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7b3-144">Qualifizierer: **WmiDataId** (3), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="fb7b3-145">Identifiziert den Dienst.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb7b3-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb7b3-146">Requirements</span></span>



| <span data-ttu-id="fb7b3-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb7b3-147">Requirement</span></span> | <span data-ttu-id="fb7b3-148">Wert</span><span class="sxs-lookup"><span data-stu-id="fb7b3-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb7b3-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb7b3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fb7b3-150">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb7b3-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb7b3-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb7b3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fb7b3-152">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb7b3-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb7b3-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb7b3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb7b3-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




