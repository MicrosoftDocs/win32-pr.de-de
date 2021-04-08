---
description: Stellt eine Zuordnung zwischen einem logischen Gerät und einem Protokoll Controller dar, der mit dem Gerät verbunden ist.
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: CIM_ProtocolControllerForDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866735"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="38087-103">CIM \_ protocolcontrollerfordevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="38087-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="38087-104">Stellt eine Zuordnung zwischen einem logischen Gerät und einem Protokoll Controller dar, der mit dem Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="38087-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="38087-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38087-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="38087-106">Member</span><span class="sxs-lookup"><span data-stu-id="38087-106">Members</span></span>

<span data-ttu-id="38087-107">Die **CIM \_ protocolcontrollerfordevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="38087-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="38087-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38087-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38087-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38087-109">Properties</span></span>

<span data-ttu-id="38087-110">Die **CIM \_ protocolcontrollerfordevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="38087-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38087-111">**Accesspriority**</span><span class="sxs-lookup"><span data-stu-id="38087-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38087-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38087-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38087-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38087-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38087-114">Die Zugriffs Priorität, die dem Gerät über den Protokoll Controller zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="38087-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="38087-115">Die höchste Priorität hat den niedrigsten Wert.</span><span class="sxs-lookup"><span data-stu-id="38087-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="38087-116">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="38087-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38087-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38087-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38087-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38087-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38087-119">Der Zugriff auf das logische Gerät über den Protokoll Controller</span><span class="sxs-lookup"><span data-stu-id="38087-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38087-120">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="38087-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="38087-121">**Aktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="38087-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="38087-122">**Inaktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="38087-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="38087-123">**Replikation** wird ausgeführt (4)</span><span class="sxs-lookup"><span data-stu-id="38087-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="38087-124">**Mapping-Inkonsistenz** (5)</span><span class="sxs-lookup"><span data-stu-id="38087-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38087-125">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="38087-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38087-126">Datentyp: **CIM \_ protocolcontroller**</span><span class="sxs-lookup"><span data-stu-id="38087-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="38087-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38087-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38087-128">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="38087-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="38087-129">Der Protokoll Controller in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="38087-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="38087-130">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="38087-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38087-131">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="38087-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="38087-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38087-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38087-133">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="38087-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="38087-134">Das logische Gerät in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="38087-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="38087-135">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="38087-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38087-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38087-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38087-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="38087-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38087-138">Die Adresse des zugeordneten Geräts im Kontext des Protokoll Controllers.</span><span class="sxs-lookup"><span data-stu-id="38087-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38087-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38087-139">Requirements</span></span>



| <span data-ttu-id="38087-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38087-140">Requirement</span></span> | <span data-ttu-id="38087-141">Wert</span><span class="sxs-lookup"><span data-stu-id="38087-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38087-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38087-142">Minimum supported client</span></span><br/> | <span data-ttu-id="38087-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38087-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="38087-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38087-144">Minimum supported server</span></span><br/> | <span data-ttu-id="38087-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38087-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="38087-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="38087-146">Namespace</span></span><br/>                | <span data-ttu-id="38087-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="38087-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38087-148">MOF</span><span class="sxs-lookup"><span data-stu-id="38087-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38087-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="38087-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38087-150">DLL</span><span class="sxs-lookup"><span data-stu-id="38087-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38087-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38087-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38087-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38087-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38087-153">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="38087-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

