---
description: Stellt die Einstellungen einer MSVM- \_ resourcepool-Instanz dar, die nicht zugeordnet sind.
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Msvm_AbstractResourcePoolSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9109bd428797c8c4f1073577e015bf4b9eddcc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960072"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="329a1-103">MSVM \_ abstractresourcepoolsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="329a1-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="329a1-104">Stellt die Einstellungen einer [**MSVM- \_ resourcepool**](msvm-resourcepool.md) -Instanz dar, die nicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="329a1-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="329a1-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="329a1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="329a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="329a1-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="329a1-107">Member</span><span class="sxs-lookup"><span data-stu-id="329a1-107">Members</span></span>

<span data-ttu-id="329a1-108">Die **MSVM \_ abstractresourcepoolsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="329a1-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="329a1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="329a1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="329a1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="329a1-110">Properties</span></span>

<span data-ttu-id="329a1-111">Die **MSVM \_ abstractresourcepoolsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="329a1-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="329a1-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="329a1-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="329a1-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="329a1-115">A short description of the object.</span></span> <span data-ttu-id="329a1-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="329a1-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="329a1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="329a1-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="329a1-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="329a1-120">A description of the object.</span></span> <span data-ttu-id="329a1-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="329a1-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="329a1-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="329a1-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="329a1-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="329a1-125">A display name for the object.</span></span> <span data-ttu-id="329a1-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="329a1-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="329a1-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="329a1-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="329a1-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="329a1-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="329a1-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="329a1-132">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="329a1-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="329a1-133">**Loadbalancingbehavior**</span><span class="sxs-lookup"><span data-stu-id="329a1-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="329a1-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="329a1-136">Gibt die Zuordnungs Strategie an, die vom Ressourcenpool verwendet wird, um die Ressourcennutzung über die aggregierten Ressourcen hinweg auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="329a1-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="329a1-137">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="329a1-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="329a1-138">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="329a1-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="329a1-139">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="329a1-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="329a1-140">**Verteilt** (4)</span><span class="sxs-lookup"><span data-stu-id="329a1-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="329a1-141">**Konsolidiert** (5)</span><span class="sxs-lookup"><span data-stu-id="329a1-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="329a1-142">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="329a1-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="329a1-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-145">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md)".**Mappingbehavior**")</span><span class="sxs-lookup"><span data-stu-id="329a1-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="329a1-146">Gibt an, ob der Ressourcenpool versuchen kann, andere Host Ressourcen zu verwenden, um die Zuordnungs Anforderung zu erfüllen, wenn die gewünschten Ressourcen nicht zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="329a1-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="329a1-147">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="329a1-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="329a1-148">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="329a1-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="329a1-149">**Dediziert** (3)</span><span class="sxs-lookup"><span data-stu-id="329a1-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="329a1-150">**Weiche Affinität** (4)</span><span class="sxs-lookup"><span data-stu-id="329a1-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="329a1-151">**Harte Affinität** (5)</span><span class="sxs-lookup"><span data-stu-id="329a1-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="329a1-152">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="329a1-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="329a1-153">**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="329a1-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="329a1-154">**Mappingorder**</span><span class="sxs-lookup"><span data-stu-id="329a1-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-155">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="329a1-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="329a1-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-157">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ resourcepoolsettingdata**](msvm-resourcepoolsettingdata.md).**Mappingbehavior**")</span><span class="sxs-lookup"><span data-stu-id="329a1-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="329a1-158">Gibt die Reihenfolge an, in der die über diesen Pool verfügbaren Host Ressourcen ausgewählt werden, wenn versucht wird, eine Zuordnungs Anforderung zu erfüllen, und die angeforderte Host Ressource ist nicht verfügbar, oder es wurde keine Host Ressource angegeben.</span><span class="sxs-lookup"><span data-stu-id="329a1-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="329a1-159">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="329a1-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="329a1-162">Vom Endbenutzer bereitgestellte Notizen zu diesem Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="329a1-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="329a1-163">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="329a1-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-166">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcepool**](cim-resourcepool.md)".**Otherresourcetype**")</span><span class="sxs-lookup"><span data-stu-id="329a1-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="329a1-167">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** auf 0 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="329a1-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="329a1-168">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="329a1-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-171">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcepool**](cim-resourcepool.md)".**Poolid**")</span><span class="sxs-lookup"><span data-stu-id="329a1-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="329a1-172">Ein Bezeichner für den Pool.</span><span class="sxs-lookup"><span data-stu-id="329a1-172">An identifier for the pool.</span></span> <span data-ttu-id="329a1-173">Diese Eigenschaft wird verwendet, um die Korrelation Zwischenspeichern und Wiederherstellen von Konfigurationsdaten im zugrunde liegenden permanenten Speicher bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="329a1-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="329a1-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="329a1-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="329a1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-177">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcepool**](cim-resourcepool.md)".**Resourcesubtype**")</span><span class="sxs-lookup"><span data-stu-id="329a1-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="329a1-178">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diesen Pool beschreibt.</span><span class="sxs-lookup"><span data-stu-id="329a1-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="329a1-179">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="329a1-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="329a1-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="329a1-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329a1-181">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="329a1-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="329a1-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="329a1-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329a1-183">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcepool**](cim-resourcepool.md)".**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="329a1-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="329a1-184">Der Typ der Ressource, die dieser Ressourcenpool zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="329a1-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="329a1-185">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="329a1-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="329a1-186">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="329a1-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="329a1-187">**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="329a1-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="329a1-188">Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="329a1-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="329a1-189">**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="329a1-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="329a1-190">**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="329a1-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="329a1-191">**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="329a1-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="329a1-192">**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="329a1-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="329a1-193">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="329a1-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="329a1-194">**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="329a1-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="329a1-195">**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="329a1-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="329a1-196">E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="329a1-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="329a1-197">E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="329a1-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="329a1-198">**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="329a1-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="329a1-199">**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="329a1-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="329a1-200">**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="329a1-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="329a1-201">**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="329a1-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="329a1-202">**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="329a1-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="329a1-203">**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="329a1-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="329a1-204">**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="329a1-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="329a1-205">**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="329a1-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="329a1-206">**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="329a1-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="329a1-207">**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="329a1-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="329a1-208">**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="329a1-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="329a1-209">**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="329a1-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="329a1-210">**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="329a1-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="329a1-211">**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="329a1-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="329a1-212">**Energie** (28)</span><span class="sxs-lookup"><span data-stu-id="329a1-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="329a1-213">**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="329a1-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="329a1-214">**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="329a1-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="329a1-215">**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="329a1-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="329a1-216">**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="329a1-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="329a1-217">**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="329a1-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="329a1-218">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="329a1-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="329a1-219">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="329a1-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="329a1-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="329a1-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="329a1-221">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="329a1-221">Requirements</span></span>



| <span data-ttu-id="329a1-222">Anforderung</span><span class="sxs-lookup"><span data-stu-id="329a1-222">Requirement</span></span> | <span data-ttu-id="329a1-223">Wert</span><span class="sxs-lookup"><span data-stu-id="329a1-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329a1-224">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="329a1-224">Minimum supported client</span></span><br/> | <span data-ttu-id="329a1-225">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="329a1-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="329a1-226">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="329a1-226">Minimum supported server</span></span><br/> | <span data-ttu-id="329a1-227">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="329a1-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="329a1-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="329a1-228">Namespace</span></span><br/>                | <span data-ttu-id="329a1-229">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="329a1-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="329a1-230">MOF</span><span class="sxs-lookup"><span data-stu-id="329a1-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="329a1-231"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="329a1-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="329a1-232">DLL</span><span class="sxs-lookup"><span data-stu-id="329a1-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="329a1-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="329a1-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

