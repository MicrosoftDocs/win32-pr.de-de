---
description: 'Msvm_AbstractResourcePoolSettingData Klasse: Stellt die Einstellungen einer Msvm \_ ResourcePool-Instanz dar, die nicht zuordnungsbezogen sind.'
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
ms.openlocfilehash: dca3da14ac74a8d6fab1ba96db98f9e2eccd74ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112118"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="91f3f-103">Msvm \_ AbstractResourcePoolSettingData-Klasse</span><span class="sxs-lookup"><span data-stu-id="91f3f-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="91f3f-104">Stellt die Einstellungen einer [**Msvm \_ ResourcePool-Instanz**](msvm-resourcepool.md) dar, die nicht zuordnungsbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="91f3f-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="91f3f-105">Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91f3f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f3f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f3f-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="91f3f-107">Member</span><span class="sxs-lookup"><span data-stu-id="91f3f-107">Members</span></span>

<span data-ttu-id="91f3f-108">Die **Msvm \_ AbstractResourcePoolSettingData-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="91f3f-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="91f3f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91f3f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91f3f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91f3f-110">Properties</span></span>

<span data-ttu-id="91f3f-111">Die **Msvm \_ AbstractResourcePoolSettingData-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91f3f-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91f3f-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="91f3f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-115">Eine kurze Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="91f3f-115">A short description of the object.</span></span> <span data-ttu-id="91f3f-116">Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="91f3f-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91f3f-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="91f3f-120">A description of the object.</span></span> <span data-ttu-id="91f3f-121">Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="91f3f-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="91f3f-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-125">Ein Anzeigename für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="91f3f-125">A display name for the object.</span></span> <span data-ttu-id="91f3f-126">Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="91f3f-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="91f3f-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="91f3f-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="91f3f-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="91f3f-132">Diese Eigenschaft wird von [**CIM \_ SettingData geerbt.**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91f3f-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="91f3f-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-134">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="91f3f-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-136">Gibt die Zuordnungsstrategie an, die vom Ressourcenpool verwendet werden soll, um die Ressourcennutzung über die aggregierten Ressourcen hinweg auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="91f3f-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91f3f-137">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="91f3f-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="91f3f-138">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="91f3f-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="91f3f-139">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="91f3f-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="91f3f-140">**Verteilt** (4)</span><span class="sxs-lookup"><span data-stu-id="91f3f-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="91f3f-141">**Konsolidiert** (5)</span><span class="sxs-lookup"><span data-stu-id="91f3f-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91f3f-142">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="91f3f-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-143">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="91f3f-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-145">Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="91f3f-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-146">Gibt an, ob der Ressourcenpool versuchen kann, andere Hostressourcen zu verwenden, um die Zuordnungsanforderung zu erfüllen, wenn die gewünschten Ressourcen nicht zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="91f3f-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91f3f-147">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="91f3f-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="91f3f-148">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="91f3f-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="91f3f-149">**Dedicated** (3)</span><span class="sxs-lookup"><span data-stu-id="91f3f-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="91f3f-150">**Soft Affinity** (4)</span><span class="sxs-lookup"><span data-stu-id="91f3f-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="91f3f-151">**Harte Affinität** (5)</span><span class="sxs-lookup"><span data-stu-id="91f3f-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="91f3f-152">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="91f3f-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="91f3f-153">**Reservierter Anbieter** (32767..65535)</span><span class="sxs-lookup"><span data-stu-id="91f3f-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91f3f-154">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="91f3f-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-155">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="91f3f-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-157">Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="91f3f-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-158">Gibt die Reihenfolge an, in der über diesen Pool verfügbare Hostressourcen ausgewählt werden, wenn versucht wird, eine Zuordnungsanforderung zu erfüllen, und die angeforderte Hostressource nicht verfügbar ist oder keine Hostressource angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="91f3f-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-159">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="91f3f-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-162">Vom Endbenutzer bereitgestellte Hinweise zu diesem Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="91f3f-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-163">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="91f3f-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-166">Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span><span class="sxs-lookup"><span data-stu-id="91f3f-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-167">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** auf 0 (Sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="91f3f-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-168">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="91f3f-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-171">Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolID**")</span><span class="sxs-lookup"><span data-stu-id="91f3f-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-172">Ein Bezeichner für den Pool.</span><span class="sxs-lookup"><span data-stu-id="91f3f-172">An identifier for the pool.</span></span> <span data-ttu-id="91f3f-173">Diese Eigenschaft wird verwendet, um die Korrelation zwischen dem Speichern und Wiederherstellen von Konfigurationsdaten im zugrunde liegenden persistenten Speicher zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="91f3f-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="91f3f-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91f3f-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-177">Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="91f3f-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-178">Eine Zeichenfolge, die einen implementierungsspezifischen Untertyp für diesen Pool beschreibt.</span><span class="sxs-lookup"><span data-stu-id="91f3f-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="91f3f-179">Dies kann beispielsweise verwendet werden, um verschiedene Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="91f3f-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="91f3f-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="91f3f-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91f3f-181">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="91f3f-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91f3f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91f3f-183">Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="91f3f-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="91f3f-184">Der Typ der Ressource, die dieser Ressourcenpool zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="91f3f-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91f3f-185">**Andere** (1)</span><span class="sxs-lookup"><span data-stu-id="91f3f-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="91f3f-186">**Computersystem** (2)</span><span class="sxs-lookup"><span data-stu-id="91f3f-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="91f3f-187">**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="91f3f-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="91f3f-188">**Arbeitsspeicher** (4)</span><span class="sxs-lookup"><span data-stu-id="91f3f-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="91f3f-189">**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="91f3f-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="91f3f-190">**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="91f3f-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="91f3f-191">**FC HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="91f3f-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="91f3f-192">**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="91f3f-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="91f3f-193">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="91f3f-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="91f3f-194">**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="91f3f-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="91f3f-195">**Anderer Netzwerkadapter** (11)</span><span class="sxs-lookup"><span data-stu-id="91f3f-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="91f3f-196">**E/A-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="91f3f-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="91f3f-197">**E/A-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="91f3f-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="91f3f-198">**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="91f3f-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="91f3f-199">**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="91f3f-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="91f3f-200">**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="91f3f-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="91f3f-201">**Laufwerk** (17)</span><span class="sxs-lookup"><span data-stu-id="91f3f-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="91f3f-202">**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="91f3f-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="91f3f-203">**Speicherumfang** (19)</span><span class="sxs-lookup"><span data-stu-id="91f3f-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="91f3f-204">**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="91f3f-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="91f3f-205">**Serieller Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="91f3f-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="91f3f-206">**Paralleler Port** (22)</span><span class="sxs-lookup"><span data-stu-id="91f3f-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="91f3f-207">**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="91f3f-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="91f3f-208">**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="91f3f-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="91f3f-209">**IEEE 1394 Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="91f3f-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="91f3f-210">**Partitionierbare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="91f3f-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="91f3f-211">**Partitionierbare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="91f3f-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="91f3f-212">**Stromversorgung** (28)</span><span class="sxs-lookup"><span data-stu-id="91f3f-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="91f3f-213">**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="91f3f-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="91f3f-214">**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="91f3f-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="91f3f-215">**Logischer Datenträger** (31)</span><span class="sxs-lookup"><span data-stu-id="91f3f-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="91f3f-216">**Speichervolume** (32)</span><span class="sxs-lookup"><span data-stu-id="91f3f-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="91f3f-217">**Ethernetverbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="91f3f-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="91f3f-218">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="91f3f-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="91f3f-219">**Reservierter Anbieter** (0x8000. 0xFFFF)</span><span class="sxs-lookup"><span data-stu-id="91f3f-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="91f3f-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="91f3f-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="91f3f-221">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91f3f-221">Requirements</span></span>



| <span data-ttu-id="91f3f-222">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91f3f-222">Requirement</span></span> | <span data-ttu-id="91f3f-223">Wert</span><span class="sxs-lookup"><span data-stu-id="91f3f-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f3f-224">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91f3f-224">Minimum supported client</span></span><br/> | <span data-ttu-id="91f3f-225">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91f3f-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="91f3f-226">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91f3f-226">Minimum supported server</span></span><br/> | <span data-ttu-id="91f3f-227">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91f3f-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91f3f-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="91f3f-228">Namespace</span></span><br/>                | <span data-ttu-id="91f3f-229">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="91f3f-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="91f3f-230">MOF</span><span class="sxs-lookup"><span data-stu-id="91f3f-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91f3f-231"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="91f3f-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="91f3f-232">DLL</span><span class="sxs-lookup"><span data-stu-id="91f3f-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91f3f-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="91f3f-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

