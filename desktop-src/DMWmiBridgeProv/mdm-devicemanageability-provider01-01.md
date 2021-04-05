---
title: MDM_DeviceManageability_Provider01_01-Klasse
description: Die MDM- \_ Klasse devicemanageability \_ Provider01 \_ 01 dient zum Abrufen der allgemeinen Informationen zu MDM-Konfigurationsfunktionen auf dem Gerät.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- MDM_DeviceManageability_Provider01_01-Klasse
- MDM_DeviceManageability_Provider01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859092"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="0db14-105">MDM \_ devicemanageability \_ Provider01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="0db14-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="0db14-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0db14-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0db14-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0db14-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0db14-108">Die MDM- \_ Klasse devicemanageability \_ Provider01 \_ 01 dient zum Abrufen der allgemeinen Informationen zu MDM-Konfigurationsfunktionen auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="0db14-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="0db14-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0db14-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db14-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0db14-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="0db14-111">Member</span><span class="sxs-lookup"><span data-stu-id="0db14-111">Members</span></span>

<span data-ttu-id="0db14-112">Die **MDM-Klasse \_ devicemanageability \_ Provider01 \_ 01** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0db14-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="0db14-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0db14-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0db14-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0db14-114">Properties</span></span>

<span data-ttu-id="0db14-115">Die **MDM-Klasse \_ devicemanageability \_ Provider01 \_ 01** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0db14-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0db14-116">Configinfo</span><span class="sxs-lookup"><span data-stu-id="0db14-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0db14-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0db14-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0db14-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0db14-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0db14-119">Sie müssen den Wert auf WMI \_ Bridge \_ Server festlegen.</span><span class="sxs-lookup"><span data-stu-id="0db14-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="0db14-120">Der Aufrufer kann die Anbieter-ID nicht dynamisch festlegen.</span><span class="sxs-lookup"><span data-stu-id="0db14-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="0db14-121">Registrierungs Info</span><span class="sxs-lookup"><span data-stu-id="0db14-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0db14-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0db14-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0db14-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0db14-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0db14-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0db14-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0db14-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0db14-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0db14-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0db14-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0db14-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0db14-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0db14-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0db14-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0db14-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0db14-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0db14-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0db14-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0db14-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0db14-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0db14-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0db14-132">Requirements</span></span>



| <span data-ttu-id="0db14-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0db14-133">Requirement</span></span> | <span data-ttu-id="0db14-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0db14-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db14-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0db14-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0db14-136">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0db14-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0db14-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0db14-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0db14-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0db14-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0db14-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0db14-139">Namespace</span></span><br/>                | <span data-ttu-id="0db14-140">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0db14-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="0db14-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0db14-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0db14-142"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0db14-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="0db14-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0db14-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db14-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db14-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

