---
description: Definiert die Möglichkeiten, mit denen ein Client den gültigen Bereich der Standardeinstellungen für eine Ethernet-Switchfunktion ermitteln kann.
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Msvm_EthernetSwitchFeatureCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349740"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="d875f-103">MSVM \_ ethernetzwitchfeaturecapabili-Klasse</span><span class="sxs-lookup"><span data-stu-id="d875f-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="d875f-104">Definiert die Möglichkeiten, mit denen ein Client den gültigen Bereich der Standardeinstellungen für eine Ethernet-Switchfunktion ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="d875f-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="d875f-105">Jedem virtuellen Ethernet-Switch ist ein MSVM-Objekt vom Typ " **\_ ethernetswitchfeaturecapabili"** für jede Funktion zugeordnet, die der Switch unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d875f-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="d875f-106">Vier [**MSVM- \_ ethernettwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) -Objekte sind dem **MSVM-Objekt " \_ ethernetzwitchfeaturecapabili"** zugeordnet, um die Mindest-, höchst-, Standard-und inkrementellen Werte für die Featurefunktionen des jeweiligen Switches zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d875f-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="d875f-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d875f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d875f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d875f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="d875f-109">Member</span><span class="sxs-lookup"><span data-stu-id="d875f-109">Members</span></span>

<span data-ttu-id="d875f-110">Die **MSVM-Klasse " \_ ethernetzwitchfeaturecapabili"** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d875f-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="d875f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d875f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d875f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d875f-112">Properties</span></span>

<span data-ttu-id="d875f-113">Die **MSVM-Klasse " \_ ethernetzwitchfeaturecapabili"** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d875f-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d875f-114">**Anwendbarkeit**</span><span class="sxs-lookup"><span data-stu-id="d875f-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-115">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d875f-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d875f-117">Hier wird beschrieben, ob diese Funktion auf einen Ethernet-Switch oder einen bestimmten Ethernet-Switchport angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d875f-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d875f-118">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="d875f-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="d875f-119">**Port** (1)</span><span class="sxs-lookup"><span data-stu-id="d875f-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="d875f-120">**Switch** (2)</span><span class="sxs-lookup"><span data-stu-id="d875f-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d875f-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d875f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d875f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d875f-124">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d875f-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d875f-125">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d875f-125">A short description of the object.</span></span> <span data-ttu-id="d875f-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d875f-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d875f-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d875f-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d875f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d875f-130">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d875f-130">A description of the object.</span></span> <span data-ttu-id="d875f-131">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d875f-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d875f-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d875f-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d875f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d875f-135">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d875f-135">A display name for the object.</span></span> <span data-ttu-id="d875f-136">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d875f-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d875f-137">**FeatureId**</span><span class="sxs-lookup"><span data-stu-id="d875f-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d875f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d875f-140">Der Bezeichner der Funktion, für die dieses Objekt Funktions Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d875f-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="d875f-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d875f-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d875f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d875f-144">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d875f-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d875f-145">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d875f-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d875f-146">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d875f-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d875f-147">**Version**</span><span class="sxs-lookup"><span data-stu-id="d875f-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d875f-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d875f-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d875f-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d875f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d875f-150">Die Version des Features im Format "Major. Minor", z. b. "2,0".</span><span class="sxs-lookup"><span data-stu-id="d875f-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d875f-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d875f-151">Requirements</span></span>



| <span data-ttu-id="d875f-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d875f-152">Requirement</span></span> | <span data-ttu-id="d875f-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d875f-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d875f-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d875f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d875f-155">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d875f-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d875f-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d875f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d875f-157">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d875f-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d875f-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="d875f-158">Namespace</span></span><br/>                | <span data-ttu-id="d875f-159">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d875f-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d875f-160">MOF</span><span class="sxs-lookup"><span data-stu-id="d875f-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d875f-161"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d875f-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d875f-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d875f-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d875f-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d875f-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

