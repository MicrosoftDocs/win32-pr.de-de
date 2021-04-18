---
title: MDM_DeviceStatus_Battery01-Klasse
description: Die MDM \_ DeviceStatus \_ Battery01-Klasse wird vom Unternehmen verwendet, um den Status der Akku Konformität von Geräten mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- MDM_DeviceStatus_Battery01-Klasse
- MDM_DeviceStatus_Battery01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344086"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="111fd-105">MDM \_ DeviceStatus \_ Battery01-Klasse</span><span class="sxs-lookup"><span data-stu-id="111fd-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="111fd-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="111fd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="111fd-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="111fd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="111fd-108">Die **MDM \_ DeviceStatus \_ Battery01** -Klasse wird vom Unternehmen verwendet, um den Status der Akku Konformität von Geräten mit ihren Unternehmensrichtlinien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="111fd-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="111fd-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="111fd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="111fd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="111fd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="111fd-111">Member</span><span class="sxs-lookup"><span data-stu-id="111fd-111">Members</span></span>

<span data-ttu-id="111fd-112">Die **MDM \_ DeviceStatus \_ Battery01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="111fd-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="111fd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="111fd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="111fd-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="111fd-114">Properties</span></span>

<span data-ttu-id="111fd-115">Die **MDM \_ DeviceStatus \_ Battery01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="111fd-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="111fd-116">Estimatedchargeremainung</span><span class="sxs-lookup"><span data-stu-id="111fd-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="111fd-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="111fd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="111fd-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="111fd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="111fd-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="111fd-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="111fd-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="111fd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="111fd-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="111fd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="111fd-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="111fd-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111fd-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111fd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111fd-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111fd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111fd-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="111fd-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="111fd-126">Der Knoten für die Akku Abfrage.</span><span class="sxs-lookup"><span data-stu-id="111fd-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="111fd-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="111fd-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111fd-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111fd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111fd-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111fd-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111fd-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="111fd-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="111fd-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="111fd-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="111fd-132">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="111fd-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="111fd-133">Status</span><span class="sxs-lookup"><span data-stu-id="111fd-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="111fd-134">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="111fd-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="111fd-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="111fd-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="111fd-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="111fd-136">Requirements</span></span>



| <span data-ttu-id="111fd-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="111fd-137">Requirement</span></span> | <span data-ttu-id="111fd-138">Wert</span><span class="sxs-lookup"><span data-stu-id="111fd-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111fd-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="111fd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="111fd-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="111fd-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="111fd-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="111fd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="111fd-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="111fd-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="111fd-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="111fd-143">Namespace</span></span><br/>                | <span data-ttu-id="111fd-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="111fd-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="111fd-145">MOF</span><span class="sxs-lookup"><span data-stu-id="111fd-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="111fd-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="111fd-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="111fd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="111fd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="111fd-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="111fd-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

