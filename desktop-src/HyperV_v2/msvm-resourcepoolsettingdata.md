---
description: Stellt die Einstellungen einer MSVM- \_ resourcepool-Instanz dar, die nicht zugeordnet sind.
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Msvm_ResourcePoolSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37ec7dc6600dbc536ac50a2042e7d53ff8043242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348049"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="a864c-103">MSVM \_ resourcepoolsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="a864c-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="a864c-104">Stellt die Einstellungen einer [**MSVM- \_ resourcepool**](msvm-resourcepool.md) -Instanz dar, die nicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a864c-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="a864c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a864c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a864c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a864c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
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

## <a name="members"></a><span data-ttu-id="a864c-107">Member</span><span class="sxs-lookup"><span data-stu-id="a864c-107">Members</span></span>

<span data-ttu-id="a864c-108">Die **MSVM \_ resourcepoolsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a864c-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a864c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a864c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a864c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a864c-110">Properties</span></span>

<span data-ttu-id="a864c-111">Die **MSVM \_ resourcepoolsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a864c-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a864c-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a864c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a864c-115">A short description of the object.</span></span> <span data-ttu-id="a864c-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a864c-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a864c-120">A description of the object.</span></span> <span data-ttu-id="a864c-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a864c-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a864c-125">A display name for the object.</span></span> <span data-ttu-id="a864c-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a864c-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a864c-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a864c-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a864c-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a864c-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a864c-132">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-133">**Loadbalancingbehavior**</span><span class="sxs-lookup"><span data-stu-id="a864c-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a864c-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-136">Gibt die Zuordnungs Strategie an, die vom Ressourcenpool verwendet wird, um die Ressourcennutzung über die aggregierten Ressourcen hinweg auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="a864c-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="a864c-137">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="a864c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a864c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="a864c-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="a864c-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Verteilt** (4)</span><span class="sxs-lookup"><span data-stu-id="a864c-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Konsolidiert** (5)</span><span class="sxs-lookup"><span data-stu-id="a864c-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a864c-143">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="a864c-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a864c-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-146">Gibt an, ob der Ressourcenpool versuchen kann, andere Host Ressourcen zu verwenden, um die Zuordnungs Anforderung zu erfüllen, wenn die gewünschten Ressourcen nicht zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="a864c-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="a864c-147">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="a864c-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a864c-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="a864c-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (3)</span><span class="sxs-lookup"><span data-stu-id="a864c-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Weiche Affinität** (4)</span><span class="sxs-lookup"><span data-stu-id="a864c-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Harte Affinität** (5)</span><span class="sxs-lookup"><span data-stu-id="a864c-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a864c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="a864c-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a864c-155">**Mappingorder**</span><span class="sxs-lookup"><span data-stu-id="a864c-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-156">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a864c-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a864c-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-158">Gibt die Reihenfolge an, in der die über diesen Pool verfügbaren Host Ressourcen ausgewählt werden, wenn versucht wird, eine Zuordnungs Anforderung zu erfüllen, und die angeforderte Host Ressource ist nicht verfügbar, oder es wurde keine Host Ressource angegeben.</span><span class="sxs-lookup"><span data-stu-id="a864c-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="a864c-159">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-160">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="a864c-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-163">Vom Endbenutzer bereitgestellte Notizen zu diesem Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="a864c-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="a864c-164">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-165">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="a864c-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-168">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** auf 0 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a864c-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="a864c-169">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-170">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="a864c-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-173">Ein Bezeichner für den Pool.</span><span class="sxs-lookup"><span data-stu-id="a864c-173">An identifier for the pool.</span></span> <span data-ttu-id="a864c-174">Diese Eigenschaft wird verwendet, um die Korrelation Zwischenspeichern und Wiederherstellen von Konfigurationsdaten im zugrunde liegenden permanenten Speicher bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a864c-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="a864c-175">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a864c-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a864c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-179">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diesen Pool beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a864c-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="a864c-180">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a864c-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="a864c-181">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="a864c-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a864c-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a864c-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a864c-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a864c-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a864c-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a864c-185">Der Typ der Ressource, die dieser Ressourcenpool zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="a864c-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="a864c-186">Diese Eigenschaft wird von [**MSVM \_ abstractresourcepoolsettingdata**](msvm-abstractresourcepoolsettingdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a864c-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="a864c-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a864c-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="a864c-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="a864c-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="a864c-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="a864c-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="a864c-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="a864c-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="a864c-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="a864c-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="a864c-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="a864c-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="a864c-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="a864c-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="a864c-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="a864c-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="a864c-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="a864c-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="a864c-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="a864c-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="a864c-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="a864c-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="a864c-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="a864c-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="a864c-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="a864c-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="a864c-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="a864c-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energie** (28)</span><span class="sxs-lookup"><span data-stu-id="a864c-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="a864c-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="a864c-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="a864c-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="a864c-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="a864c-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a864c-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a864c-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="a864c-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a864c-222">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a864c-222">Requirements</span></span>



| <span data-ttu-id="a864c-223">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a864c-223">Requirement</span></span> | <span data-ttu-id="a864c-224">Wert</span><span class="sxs-lookup"><span data-stu-id="a864c-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a864c-225">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a864c-225">Minimum supported client</span></span><br/> | <span data-ttu-id="a864c-226">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a864c-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a864c-227">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a864c-227">Minimum supported server</span></span><br/> | <span data-ttu-id="a864c-228">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a864c-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a864c-229">Namespace</span><span class="sxs-lookup"><span data-stu-id="a864c-229">Namespace</span></span><br/>                | <span data-ttu-id="a864c-230">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a864c-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a864c-231">MOF</span><span class="sxs-lookup"><span data-stu-id="a864c-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a864c-232"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a864c-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a864c-233">DLL</span><span class="sxs-lookup"><span data-stu-id="a864c-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a864c-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a864c-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

