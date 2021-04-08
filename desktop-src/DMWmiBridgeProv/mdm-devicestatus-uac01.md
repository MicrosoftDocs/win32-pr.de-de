---
title: MDM_DeviceStatus_UAC01-Klasse
description: Die MDM \_ DeviceStatus \_ UAC01-Klasse wird vom Unternehmen verwendet, um den UAC-Status von Geräten mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- MDM_DeviceStatus_UAC01-Klasse
- MDM_DeviceStatus_UAC01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742617"
---
# <a name="mdm_devicestatus_uac01-class"></a><span data-ttu-id="d8261-105">MDM \_ DeviceStatus \_ UAC01-Klasse</span><span class="sxs-lookup"><span data-stu-id="d8261-105">MDM\_DeviceStatus\_UAC01 class</span></span>

<span data-ttu-id="d8261-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d8261-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d8261-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d8261-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d8261-108">Die **MDM \_ DeviceStatus \_ UAC01** -Klasse wird vom Unternehmen verwendet, um den UAC-Status von Geräten mit ihren Unternehmensrichtlinien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="d8261-108">The **MDM\_DeviceStatus\_UAC01** class is used by the enterprise to query the UAC status of devices with their enterprise policies.</span></span>

<span data-ttu-id="d8261-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d8261-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8261-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8261-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="d8261-111">Member</span><span class="sxs-lookup"><span data-stu-id="d8261-111">Members</span></span>

<span data-ttu-id="d8261-112">Die **MDM \_ DeviceStatus \_ UAC01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8261-112">The **MDM\_DeviceStatus\_UAC01** class has these types of members:</span></span>

-   [<span data-ttu-id="d8261-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8261-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8261-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8261-114">Properties</span></span>

<span data-ttu-id="d8261-115">Die **MDM \_ DeviceStatus \_ UAC01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8261-115">The **MDM\_DeviceStatus\_UAC01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8261-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8261-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8261-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8261-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8261-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8261-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8261-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8261-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8261-120">Knoten für die UAC-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="d8261-120">Node for the UAC query.</span></span>

</dd> <dt>

<span data-ttu-id="d8261-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d8261-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8261-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8261-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8261-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8261-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8261-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8261-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8261-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="d8261-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="d8261-126">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="d8261-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="d8261-127">Status</span><span class="sxs-lookup"><span data-stu-id="d8261-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8261-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d8261-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8261-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8261-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8261-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8261-130">Requirements</span></span>



| <span data-ttu-id="d8261-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8261-131">Requirement</span></span> | <span data-ttu-id="d8261-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d8261-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8261-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8261-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d8261-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8261-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8261-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8261-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d8261-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8261-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d8261-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8261-137">Namespace</span></span><br/>                | <span data-ttu-id="d8261-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d8261-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d8261-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d8261-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8261-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d8261-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8261-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d8261-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8261-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8261-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

