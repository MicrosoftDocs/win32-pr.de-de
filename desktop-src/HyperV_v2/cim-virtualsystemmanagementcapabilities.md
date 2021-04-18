---
description: Stellt die Funktionen eines CIM \_ virtualsystemmanagementservice-Objekts dar.
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: CIM_VirtualSystemManagementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343830"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="f3fc5-103">CIM \_ virtualsystemmanagementfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="f3fc5-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="f3fc5-104">Stellt die Funktionen eines [**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md) -Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="f3fc5-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3fc5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3fc5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="f3fc5-106">Member</span><span class="sxs-lookup"><span data-stu-id="f3fc5-106">Members</span></span>

<span data-ttu-id="f3fc5-107">Die **CIM \_ virtualsystemmanagementfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f3fc5-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f3fc5-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3fc5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3fc5-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3fc5-109">Properties</span></span>

<span data-ttu-id="f3fc5-110">Die **CIM \_ virtualsystemmanagementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3fc5-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3fc5-111">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="f3fc5-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3fc5-112">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f3fc5-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3fc5-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3fc5-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3fc5-114">Ein Array, das Methodennamen für die [**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md) -Klassen Methoden enthält, die für asynchrone Vorgänge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f3fc5-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="f3fc5-115">**Definesystemsupported** (2)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="f3fc5-116">**Destroysystemsupported** (3)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="f3fc5-117">**Destroysystemconfigurationsupported** (4)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="f3fc5-118">**Modifyresourcesettingssupported** (5)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="f3fc5-119">**Modifysystemsettingssupported** (6)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="f3fc5-120">**Removeresourcessupported** (7)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="f3fc5-121">**Selectsystemconfigurationsupported** (8)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="f3fc5-122">**Snapshotsystemsupported** (9)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="f3fc5-123">**Adresssourcessupported** (10)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3fc5-124">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3fc5-125">**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3fc5-126">**Unterstützt**</span><span class="sxs-lookup"><span data-stu-id="f3fc5-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3fc5-127">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f3fc5-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3fc5-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3fc5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3fc5-129">Ein Array, das die unterstützten Anzeichen Typen der Implementierung enthält.</span><span class="sxs-lookup"><span data-stu-id="f3fc5-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="f3fc5-130">**Virtualresourcestatus echanginditerationssupported** (2)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="f3fc5-131">" **Concretejobstatus echangein" unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="f3fc5-132">**Virtualsystemstatus echangin-Unterstützung** (4)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3fc5-133">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3fc5-134">**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3fc5-135">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="f3fc5-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3fc5-136">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f3fc5-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3fc5-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3fc5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3fc5-138">Ein Array, das Methodennamen für die [**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md) -Klassen Methoden enthält, die für synchrone Vorgänge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f3fc5-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="f3fc5-139">**Definesystemsupported** (2)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="f3fc5-140">**Destroysystemsupported** (3)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="f3fc5-141">**Destroysystemconfigurationsupported** (4)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="f3fc5-142">**Modifyresourcesettingssupported** (5)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="f3fc5-143">**Modifysystemsettingssupported** (6)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="f3fc5-144">**Removeresourcessupported** (7)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="f3fc5-145">**Selectsystemconfigurationsupported** (8)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="f3fc5-146">**Snapshotsystemsupported** (9)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="f3fc5-147">**Adresssourcessupported** (10)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3fc5-148">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3fc5-149">**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3fc5-150">**Virtualsystemtypessupported**</span><span class="sxs-lookup"><span data-stu-id="f3fc5-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3fc5-151">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f3fc5-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3fc5-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3fc5-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3fc5-153">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md)".**Virtualsystemtype**")</span><span class="sxs-lookup"><span data-stu-id="f3fc5-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="f3fc5-154">Der Typ der virtuellen Systeme, die von der-Implementierung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f3fc5-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3fc5-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3fc5-155">Requirements</span></span>



| <span data-ttu-id="f3fc5-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3fc5-156">Requirement</span></span> | <span data-ttu-id="f3fc5-157">Wert</span><span class="sxs-lookup"><span data-stu-id="f3fc5-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3fc5-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f3fc5-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f3fc5-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f3fc5-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3fc5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f3fc5-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3fc5-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f3fc5-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3fc5-162">Namespace</span></span><br/>                | <span data-ttu-id="f3fc5-163">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f3fc5-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3fc5-164">MOF</span><span class="sxs-lookup"><span data-stu-id="f3fc5-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3fc5-165"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f3fc5-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3fc5-166">DLL</span><span class="sxs-lookup"><span data-stu-id="f3fc5-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3fc5-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3fc5-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3fc5-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3fc5-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3fc5-169">**CIM \_ enabledlogicalelementfunktionalitäten**</span><span class="sxs-lookup"><span data-stu-id="f3fc5-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

