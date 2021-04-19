---
description: Stellt die Einstellungen eines zu importierenden virtuellen Systems dar. Wird von der Methode zum Aufheben der Einbindung der MSVM-Klasse "Zustell barkeit" verwendet \_ .
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Msvm_AssignableDeviceDismountSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364041"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="f902b-104">MSVM zugewiesen \_ abledevicedismountsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="f902b-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="f902b-105">Stellt die Einstellungen eines zu importierenden virtuellen Systems dar.</span><span class="sxs-lookup"><span data-stu-id="f902b-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="f902b-106">Wird von der [**Methode zum Aufheben der Einbindung**](msvm-assignabledeviceservice-dismountassignabledevice.md) der [**MSVM-Klasse " \_ Zustell barkeit**](msvm-assignabledeviceservice.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="f902b-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="f902b-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f902b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f902b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f902b-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="f902b-109">Member</span><span class="sxs-lookup"><span data-stu-id="f902b-109">Members</span></span>

<span data-ttu-id="f902b-110">Die **MSVM \_** -Klasse "zuder Klasse" weist die folgenden Member auf:</span><span class="sxs-lookup"><span data-stu-id="f902b-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f902b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f902b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f902b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f902b-112">Properties</span></span>

<span data-ttu-id="f902b-113">Die **MSVM \_** -Klasse "zuder Klasse" weist die folgenden Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="f902b-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f902b-114">**Gerätepfad**</span><span class="sxs-lookup"><span data-stu-id="f902b-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f902b-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f902b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f902b-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f902b-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f902b-117">PNP-Geräte Instanz-ID.</span><span class="sxs-lookup"><span data-stu-id="f902b-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="f902b-118">**Devicelocationpath**</span><span class="sxs-lookup"><span data-stu-id="f902b-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f902b-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f902b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f902b-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f902b-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f902b-121">PNP-Speicherort Pfad des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f902b-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="f902b-122">**Requirements acssupport**</span><span class="sxs-lookup"><span data-stu-id="f902b-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f902b-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f902b-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f902b-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f902b-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f902b-125">Gibt an, ob die erforderliche ACS-Unterstützung vorhanden sein sollte, bevor die Aufhebung der Einbindung zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="f902b-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="f902b-126">**Requirements deviceentschärgationen**</span><span class="sxs-lookup"><span data-stu-id="f902b-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f902b-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f902b-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f902b-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f902b-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f902b-129">Gibt an, ob Geräte entschärfungen vorhanden sein sollten, bevor die Aufhebung der Einbindung zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="f902b-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f902b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f902b-130">Requirements</span></span>



| <span data-ttu-id="f902b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f902b-131">Requirement</span></span> | <span data-ttu-id="f902b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f902b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f902b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f902b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f902b-134">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f902b-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f902b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f902b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f902b-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f902b-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f902b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f902b-137">Namespace</span></span><br/>                | <span data-ttu-id="f902b-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f902b-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f902b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f902b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f902b-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f902b-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f902b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f902b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f902b-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f902b-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f902b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f902b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f902b-144">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="f902b-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




