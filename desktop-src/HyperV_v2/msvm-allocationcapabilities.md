---
description: Definiert die Möglichkeiten, mit denen ein Client den gültigen Bereich der Standardeinstellungen für eine virtuelle Ressource ermitteln kann.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Msvm_AllocationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352703"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="3c60d-103">MSVM- \_ Klassen Zuordnung</span><span class="sxs-lookup"><span data-stu-id="3c60d-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="3c60d-104">Definiert die Möglichkeiten, mit denen ein Client den gültigen Bereich der Standardeinstellungen für eine virtuelle Ressource ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="3c60d-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="3c60d-105">Jedem Ressourcenpool ist ein **MSVM-Objekt \_ zugeordnet** .</span><span class="sxs-lookup"><span data-stu-id="3c60d-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="3c60d-106">Vier [**MSVM- \_ resourceallocationsettingdata**](msvm-resourceallocationsettingdata.md) -Objekte sind dem **MSVM \_ allocationfunktionalitäten** -Objekt zugeordnet, um die minimalen, maximalen, Standardwerte und inkrementellen Werte für die Zuordnung der angegebenen Ressource zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3c60d-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="3c60d-107">In dieser Klasse werden alle unterstützten Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3c60d-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="3c60d-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c60d-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c60d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c60d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="3c60d-110">Member</span><span class="sxs-lookup"><span data-stu-id="3c60d-110">Members</span></span>

<span data-ttu-id="3c60d-111">Die **MSVM \_** -Klasse "-Klasse" weist diese Typen von Membern auf:</span><span class="sxs-lookup"><span data-stu-id="3c60d-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="3c60d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c60d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c60d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c60d-113">Properties</span></span>

<span data-ttu-id="3c60d-114">Die **MSVM \_** -Klasse "Zuweisung von Klassen" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c60d-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c60d-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3c60d-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c60d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-118">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="3c60d-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-119">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3c60d-119">A short description of the object.</span></span> <span data-ttu-id="3c60d-120">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c60d-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c60d-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c60d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-124">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3c60d-124">A description of the object.</span></span> <span data-ttu-id="3c60d-125">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c60d-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3c60d-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c60d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-129">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-129">A display name for the object.</span></span> <span data-ttu-id="3c60d-130">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="3c60d-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="3c60d-131">Die [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) -Eigenschaft der **CIM \_ ManagedSystemElement** -Klasse wird auch als Anzeige Name definiert.</span><span class="sxs-lookup"><span data-stu-id="3c60d-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="3c60d-132">Sie wird jedoch häufig als Schlüssel untergeordnet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="3c60d-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="3c60d-133">Es ist nicht sinnvoll, dass dieselbe Eigenschaft ohne Inkonsistenzen sowohl Identität als auch einen anzeigen Amen vermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="3c60d-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="3c60d-134">Wenn [**Name**](msvm-keyboard.md) vorhanden und kein Schlüssel ist (z. b. für Instanzen eines logischen Geräts), können dieselben Informationen in den Eigenschaften **Name** und **ElementName** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3c60d-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="3c60d-135">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c60d-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c60d-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c60d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-139">Ein eindeutiger Bezeichner für diesen Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="3c60d-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="3c60d-140">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c60d-141">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="3c60d-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c60d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-144">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert "Other" hat.</span><span class="sxs-lookup"><span data-stu-id="3c60d-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="3c60d-145">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="3c60d-146">**Requesttypessupported**</span><span class="sxs-lookup"><span data-stu-id="3c60d-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c60d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-149">Gibt an, ob die Anforderung einer bestimmten Ressource unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3c60d-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="3c60d-150">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="3c60d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="3c60d-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="3c60d-152">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3c60d-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3c60d-153"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="3c60d-154">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="3c60d-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="3c60d-155"><dt>**Spezifisch**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3c60d-156">Die Anforderung kann eine Anforderung für eine bestimmte Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="3c60d-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="3c60d-157"><dt>**Allgemein**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="3c60d-158">Die Anforderung enthält keine Anforderung für eine bestimmte Ressource.</span><span class="sxs-lookup"><span data-stu-id="3c60d-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="3c60d-159"><dt>**Beide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="3c60d-160">Sowohl spezifische als auch allgemeine Anforderungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="3c60d-161">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3c60d-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c60d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-164">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="3c60d-165">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="3c60d-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="3c60d-166">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="3c60d-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3c60d-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c60d-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-170">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="3c60d-171">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="3c60d-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3c60d-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="3c60d-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="3c60d-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="3c60d-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="3c60d-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="3c60d-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="3c60d-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="3c60d-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="3c60d-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="3c60d-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="3c60d-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="3c60d-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="3c60d-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="3c60d-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="3c60d-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="3c60d-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="3c60d-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="3c60d-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="3c60d-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="3c60d-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="3c60d-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="3c60d-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="3c60d-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="3c60d-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="3c60d-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="3c60d-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energie** (28)</span><span class="sxs-lookup"><span data-stu-id="3c60d-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="3c60d-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="3c60d-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="3c60d-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="3c60d-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="3c60d-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3c60d-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3c60d-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c60d-207">**Sharingmode**</span><span class="sxs-lookup"><span data-stu-id="3c60d-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c60d-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-210">Gibt an, wie der Zugriff auf eine zugrunde liegende Ressource gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="3c60d-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="3c60d-211">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="3c60d-212">Wert</span><span class="sxs-lookup"><span data-stu-id="3c60d-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="3c60d-213">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3c60d-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3c60d-214"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="3c60d-215">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="3c60d-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="3c60d-216"><dt>**Dediziert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3c60d-217">Exklusiver Zugriff auf eine zugrunde liegende Ressource.</span><span class="sxs-lookup"><span data-stu-id="3c60d-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="3c60d-218">Frei <dt>**gegeben**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="3c60d-219">Freigegebene Verwendung einer zugrunde liegenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="3c60d-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="3c60d-220">**Supportedaddstates**</span><span class="sxs-lookup"><span data-stu-id="3c60d-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-221">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="3c60d-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-223">Gibt die Zustände an, die das System, dem die Ressource zugeordnet wird, beim Erstellen einer neuen Ressource aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="3c60d-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="3c60d-224">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="3c60d-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3c60d-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="3c60d-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3c60d-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="3c60d-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="3c60d-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="3c60d-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span><span class="sxs-lookup"><span data-stu-id="3c60d-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (10)</span><span class="sxs-lookup"><span data-stu-id="3c60d-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (11)</span><span class="sxs-lookup"><span data-stu-id="3c60d-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (12** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3c60d-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3c60d-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c60d-239">**Supportedremuvestates**</span><span class="sxs-lookup"><span data-stu-id="3c60d-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c60d-240">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="3c60d-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c60d-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c60d-242">Gibt die Zustände an, in denen sich das System, dem die Ressource zugeordnet ist, beim Entfernen der Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="3c60d-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="3c60d-243">Diese Eigenschaft wird von [**CIM- \_ Reservierungs Funktionen**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c60d-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="3c60d-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3c60d-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="3c60d-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3c60d-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="3c60d-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="3c60d-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="3c60d-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span><span class="sxs-lookup"><span data-stu-id="3c60d-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (10)</span><span class="sxs-lookup"><span data-stu-id="3c60d-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (11)</span><span class="sxs-lookup"><span data-stu-id="3c60d-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (12** )</span><span class="sxs-lookup"><span data-stu-id="3c60d-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3c60d-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3c60d-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3c60d-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c60d-258">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c60d-258">Remarks</span></span>

<span data-ttu-id="3c60d-259">Der Zugriff auf die **MSVM- \_ zugriffsfunktions** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="3c60d-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3c60d-260">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3c60d-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c60d-261">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c60d-261">Requirements</span></span>



| <span data-ttu-id="3c60d-262">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c60d-262">Requirement</span></span> | <span data-ttu-id="3c60d-263">Wert</span><span class="sxs-lookup"><span data-stu-id="3c60d-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c60d-264">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c60d-264">Minimum supported client</span></span><br/> | <span data-ttu-id="3c60d-265">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c60d-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3c60d-266">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c60d-266">Minimum supported server</span></span><br/> | <span data-ttu-id="3c60d-267">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c60d-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c60d-268">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c60d-268">Namespace</span></span><br/>                | <span data-ttu-id="3c60d-269">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3c60d-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3c60d-270">MOF</span><span class="sxs-lookup"><span data-stu-id="3c60d-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c60d-271"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c60d-272">DLL</span><span class="sxs-lookup"><span data-stu-id="3c60d-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c60d-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c60d-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c60d-274">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c60d-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c60d-275">**CIM- \_ Reservierungs Funktionen**</span><span class="sxs-lookup"><span data-stu-id="3c60d-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="3c60d-276">**CIM- \_ Reservierungs Funktionen**</span><span class="sxs-lookup"><span data-stu-id="3c60d-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="3c60d-277">**MSVM- \_ Zuweisung (v1)**</span><span class="sxs-lookup"><span data-stu-id="3c60d-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="3c60d-278">Ressourcen Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="3c60d-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

