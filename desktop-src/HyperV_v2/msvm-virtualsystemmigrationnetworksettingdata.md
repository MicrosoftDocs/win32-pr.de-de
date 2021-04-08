---
description: Stellt das Netzwerk dar, auf dem der Dienst für die Migration des virtuellen Systems auf die Migration eingehender virtueller Systeme lauscht.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Msvm_VirtualSystemMigrationNetworkSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862059"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="22a9b-103">MSVM \_ virtualsystemmigrationnetworksettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="22a9b-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="22a9b-104">Stellt das Netzwerk dar, auf dem der Dienst für die Migration des virtuellen Systems auf die Migration eingehender virtueller Systeme lauscht.</span><span class="sxs-lookup"><span data-stu-id="22a9b-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="22a9b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="22a9b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a9b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="22a9b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="22a9b-107">Member</span><span class="sxs-lookup"><span data-stu-id="22a9b-107">Members</span></span>

<span data-ttu-id="22a9b-108">Die **MSVM \_ virtualsystemmigrationnetworksettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="22a9b-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="22a9b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22a9b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22a9b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22a9b-110">Properties</span></span>

<span data-ttu-id="22a9b-111">Die **MSVM \_ virtualsystemmigrationnetworksettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="22a9b-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22a9b-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="22a9b-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22a9b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="22a9b-115">A short description of the object.</span></span> <span data-ttu-id="22a9b-116">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="22a9b-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22a9b-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22a9b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="22a9b-120">A description of the object.</span></span> <span data-ttu-id="22a9b-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22a9b-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22a9b-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22a9b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="22a9b-125">A display name for the object.</span></span> <span data-ttu-id="22a9b-126">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="22a9b-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22a9b-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22a9b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="22a9b-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="22a9b-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22a9b-132">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22a9b-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-133">**Metrik**</span><span class="sxs-lookup"><span data-stu-id="22a9b-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22a9b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-136">Die Prioritäts Metrik dieses Netzwerks für die Migration.</span><span class="sxs-lookup"><span data-stu-id="22a9b-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="22a9b-137">Niedrigere Werte sind höher als die Priorität.</span><span class="sxs-lookup"><span data-stu-id="22a9b-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-138">**PrefixLength**</span><span class="sxs-lookup"><span data-stu-id="22a9b-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-139">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="22a9b-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-141">Die Länge des Subnetzpräfixes des Migrationsnetzwerks.</span><span class="sxs-lookup"><span data-stu-id="22a9b-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-142">**Subnetnumber**</span><span class="sxs-lookup"><span data-stu-id="22a9b-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22a9b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-145">Die Subnetznummer des Migrationsnetzwerks.</span><span class="sxs-lookup"><span data-stu-id="22a9b-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="22a9b-146">**Tags**</span><span class="sxs-lookup"><span data-stu-id="22a9b-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a9b-147">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="22a9b-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22a9b-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22a9b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a9b-149">Ein Array von Tags, die darstellen, welches Verwaltungssystem dieses Netzwerk für den Dienst für die virtuelle System Migration festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="22a9b-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22a9b-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22a9b-150">Requirements</span></span>



| <span data-ttu-id="22a9b-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22a9b-151">Requirement</span></span> | <span data-ttu-id="22a9b-152">Wert</span><span class="sxs-lookup"><span data-stu-id="22a9b-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a9b-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22a9b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="22a9b-154">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22a9b-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22a9b-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22a9b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="22a9b-156">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22a9b-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22a9b-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="22a9b-157">Namespace</span></span><br/>                | <span data-ttu-id="22a9b-158">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="22a9b-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22a9b-159">MOF</span><span class="sxs-lookup"><span data-stu-id="22a9b-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22a9b-160"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="22a9b-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22a9b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="22a9b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22a9b-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22a9b-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22a9b-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22a9b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a9b-164">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="22a9b-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="22a9b-165">**Modifynetworksettings**</span><span class="sxs-lookup"><span data-stu-id="22a9b-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

