---
description: Stellt eine Zuordnung zwischen einem Protokoll Controller und einer verfügbar gemachten logischen Einheit dar.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: CIM_ProtocolControllerForUnit-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373165"
---
# <a name="cim_protocolcontrollerforunit-class"></a><span data-ttu-id="4ae94-103">CIM \_ protocolcontrollerforunit-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ae94-103">CIM\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="4ae94-104">Stellt eine Zuordnung zwischen einem Protokoll Controller und einer verfügbar gemachten logischen Einheit dar.</span><span class="sxs-lookup"><span data-stu-id="4ae94-104">Represents an association between a protocol controller and an exposed logical unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae94-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="4ae94-106">Member</span><span class="sxs-lookup"><span data-stu-id="4ae94-106">Members</span></span>

<span data-ttu-id="4ae94-107">Die **CIM \_ protocolcontrollerforunit** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ae94-107">The **CIM\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="4ae94-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ae94-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ae94-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ae94-109">Properties</span></span>

<span data-ttu-id="4ae94-110">Die **CIM \_ protocolcontrollerforunit** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ae94-110">The **CIM\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ae94-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="4ae94-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae94-112">Datentyp: **CIM \_ protocolcontroller**</span><span class="sxs-lookup"><span data-stu-id="4ae94-112">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="4ae94-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ae94-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ae94-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="4ae94-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4ae94-115">Der Protokoll Controller.</span><span class="sxs-lookup"><span data-stu-id="4ae94-115">The protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="4ae94-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="4ae94-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae94-117">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="4ae94-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4ae94-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ae94-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ae94-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="4ae94-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4ae94-120">Die logische Einheit, die dem Protokoll Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4ae94-120">The logical unit associated with the protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="4ae94-121">**Deviceaccess**</span><span class="sxs-lookup"><span data-stu-id="4ae94-121">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae94-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ae94-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ae94-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ae94-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ae94-124">Die Zugriffsrechte, die der logischen Einheit über den Protokoll Controller erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="4ae94-124">The access rights granted to the logical unit through the protocol controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ae94-125">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4ae94-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="4ae94-126">**Lese Schreibvorgang** (2)</span><span class="sxs-lookup"><span data-stu-id="4ae94-126">**Read Write** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="4ae94-127">Schreib **geschützt (3** )</span><span class="sxs-lookup"><span data-stu-id="4ae94-127">**Read-Only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

<span data-ttu-id="4ae94-128">**Kein Zugriff** (4)</span><span class="sxs-lookup"><span data-stu-id="4ae94-128">**No Access** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4ae94-129">**DMTF reserviert** (5.. 15999)</span><span class="sxs-lookup"><span data-stu-id="4ae94-129">**DMTF Reserved** (5..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4ae94-130">**Anbieter reserviert** (16000..)</span><span class="sxs-lookup"><span data-stu-id="4ae94-130">**Vendor Reserved** (16000..)</span></span>


<span data-ttu-id="4ae94-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4ae94-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4ae94-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ae94-132">Requirements</span></span>



| <span data-ttu-id="4ae94-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ae94-133">Requirement</span></span> | <span data-ttu-id="4ae94-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4ae94-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae94-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ae94-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae94-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ae94-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4ae94-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ae94-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae94-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ae94-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4ae94-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ae94-139">Namespace</span></span><br/>                | <span data-ttu-id="4ae94-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ae94-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ae94-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4ae94-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ae94-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ae94-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ae94-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4ae94-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ae94-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ae94-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ae94-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ae94-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae94-146">**CIM \_ protocolcontrollerfordevice**</span><span class="sxs-lookup"><span data-stu-id="4ae94-146">**CIM\_ProtocolControllerForDevice**</span></span>](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

