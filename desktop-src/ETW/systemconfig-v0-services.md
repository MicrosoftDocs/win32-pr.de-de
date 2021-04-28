---
description: 'SystemConfig_V0_Services-Klasse: Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.'
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
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105928"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="b1aef-103">SystemConfig \_ V0 \_ Services-Klasse</span><span class="sxs-lookup"><span data-stu-id="b1aef-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="b1aef-104">Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="b1aef-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="b1aef-105">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b1aef-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1aef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1aef-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b1aef-107">Member</span><span class="sxs-lookup"><span data-stu-id="b1aef-107">Members</span></span>

<span data-ttu-id="b1aef-108">Die **SystemConfig \_ V0 \_ Services-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1aef-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="b1aef-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1aef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1aef-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1aef-110">Properties</span></span>

<span data-ttu-id="b1aef-111">Die **SystemConfig \_ V0 \_ Services-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1aef-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1aef-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="b1aef-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1aef-113">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="b1aef-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1aef-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-115">Qualifizierer: **WmiDataId** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="b1aef-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1aef-116">Anzeigename des Diensts.</span><span class="sxs-lookup"><span data-stu-id="b1aef-116">Display name of the service.</span></span> <span data-ttu-id="b1aef-117">Der Name wird im Dienststeuerungs-Manager beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b1aef-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="b1aef-118">Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="b1aef-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="b1aef-119">**Processid**</span><span class="sxs-lookup"><span data-stu-id="b1aef-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1aef-120">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1aef-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1aef-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-122">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="b1aef-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b1aef-123">Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1aef-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="b1aef-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="b1aef-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1aef-125">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="b1aef-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1aef-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-127">Qualifizierer: **WmiDataId** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="b1aef-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="b1aef-128">Name des Prozesses, in dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1aef-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="b1aef-129">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="b1aef-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1aef-130">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="b1aef-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1aef-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1aef-132">Qualifizierer: **WmiDataId** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="b1aef-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="b1aef-133">Eindeutiger Bezeichner des Diensts.</span><span class="sxs-lookup"><span data-stu-id="b1aef-133">Unique identifier of the service.</span></span> <span data-ttu-id="b1aef-134">Der Bezeichner gibt einen Hinweis auf die Funktionalität an, die der Dienst bietet.</span><span class="sxs-lookup"><span data-stu-id="b1aef-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1aef-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1aef-135">Requirements</span></span>



| <span data-ttu-id="b1aef-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1aef-136">Requirement</span></span> | <span data-ttu-id="b1aef-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b1aef-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1aef-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1aef-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b1aef-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b1aef-139">None supported</span></span><br/>                            |
| <span data-ttu-id="b1aef-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1aef-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b1aef-141">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1aef-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1aef-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1aef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1aef-143">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="b1aef-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




