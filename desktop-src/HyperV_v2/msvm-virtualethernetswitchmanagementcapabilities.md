---
description: Beschreibt die Funktionen des zugeordneten MSVM \_ virtualethernetzwitchmanagementservice.
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Msvm_VirtualEthernetSwitchManagementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373115"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="7e5bd-103">MSVM \_ virtualethernetzwitchmanagementfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e5bd-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="7e5bd-104">Beschreibt die Funktionen des zugeordneten [**MSVM \_ virtualethernetzwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md).</span><span class="sxs-lookup"><span data-stu-id="7e5bd-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="7e5bd-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e5bd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="7e5bd-107">Member</span><span class="sxs-lookup"><span data-stu-id="7e5bd-107">Members</span></span>

<span data-ttu-id="7e5bd-108">Die **MSVM \_ virtualethernetzwitchmanagementfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e5bd-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="7e5bd-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e5bd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e5bd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e5bd-110">Properties</span></span>

<span data-ttu-id="7e5bd-111">Die **MSVM \_ virtualethernetzwitchmanagementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e5bd-112">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-113">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7e5bd-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. asynchronousmethodssupported")</span><span class="sxs-lookup"><span data-stu-id="7e5bd-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-116">Ein Array von Methoden bezeichgern, von denen jedes eine Methode der [**MSVM \_ virtualethernettwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md) -Klasse identifiziert, die asynchron von der-Implementierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="7e5bd-117">Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="7e5bd-118">**Definesystem** (2)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="7e5bd-119">**Destroysystem** (3)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="7e5bd-120">**Destroysystemconfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="7e5bd-121">**Modifyresourcesettings** (5)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="7e5bd-122">**Modifysystemsettings** (6)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="7e5bd-123">**Removeresources** (7)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="7e5bd-124">**Selectsystemconfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="7e5bd-125">**Snapshotsystem** (9)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="7e5bd-126">**Adressquellen** (10)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e5bd-127">**Addfeaturesettingssupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e5bd-128">**Modifyfeaturesettingssupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e5bd-129">**Removefeaturesettingssupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e5bd-130">**Addfeaturesettingssupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e5bd-131">**Modifyfeaturesettingssupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e5bd-132">**Removefeaturesettingssupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e5bd-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-136">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-136">A short description of the object.</span></span> <span data-ttu-id="7e5bd-137">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual Ethernet Switch Management Service-Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-141">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-141">A description of the object.</span></span> <span data-ttu-id="7e5bd-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Definieren von Verwaltungsdienst Funktionen für virtuelle Ethernet-Switches" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-146">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-146">A display name for the object.</span></span> <span data-ttu-id="7e5bd-147">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual Ethernet Switch Management Service-Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-148">**Elementnameeditsupported**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-149">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7e5bd-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-151">Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="7e5bd-152">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-153">**Elementnamemask**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-156">Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="7e5bd-157">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-158">**Unterstützt**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-159">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7e5bd-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-161">Ein Array von Indikator Bezeichner, das jeweils einen von der-Implementierung unterstützten Hinweis identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="7e5bd-162">Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="7e5bd-163">Wert</span><span class="sxs-lookup"><span data-stu-id="7e5bd-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="7e5bd-164">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7e5bd-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="7e5bd-165"><dt>**Virtualresourcestatuechanginattribuationssupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7e5bd-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7e5bd-166">Gibt an, ob die Implementierung Benachrichtigungen zu Zustandsänderungen von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Instanzen unterstützt, die Ressourcen von virtuellen Systemen darstellen.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="7e5bd-167">" <dt>**Concretejobstatus echangeinge-unterstützt**</dt> <dt>3</dt> "</span><span class="sxs-lookup"><span data-stu-id="7e5bd-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="7e5bd-168">Gibt an, ob die Implementierung Benachrichtigungen zu Zustandsänderungen von [**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85)) -Instanzen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="7e5bd-169"><dt>**Virtualsystemstatuechangin-Unterstützung**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7e5bd-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="7e5bd-170">Gibt an, ob die Implementierung Benachrichtigungen zu Zustandsänderungen von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanzen unterstützt, die virtuelle Systeme darstellen.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="7e5bd-171"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="7e5bd-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="7e5bd-172"><dt> **Hersteller reserviert**</dt> <dt>32767.65535</dt></span><span class="sxs-lookup"><span data-stu-id="7e5bd-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="7e5bd-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-176">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-177">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7e5bd-178">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-179">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7e5bd-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-182">Ein boolescher Wert, der angibt, ob die e/a-Virtualisierung (IOV) von der Plattform unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="7e5bd-183">Wenn der Wert **true** ist, wird IOV von der Plattform unterstützt, und **iovsupporschatzist** leer.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="7e5bd-184">Andernfalls gibt die **iovsuppor-** Eigenschaft die Gründe dafür, warum IOV nicht unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-185">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-186">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7e5bd-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-188">Ein Array von Zeichen folgen, das die möglichen Gründe angibt, warum IOV nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="7e5bd-189">Wenn der Wert von **iovsupport** den Wert **true** hat, ist dieses Array leer.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-190">**Maxelementnamelen**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-191">Datentyp: **unit16**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-193">Qualifizierer: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-194">Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="7e5bd-195">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-196">**Requestedstaatunter stützt**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-197">Datentyp: **unit16** Array</span><span class="sxs-lookup"><span data-stu-id="7e5bd-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-199">Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="7e5bd-200">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt und ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7e5bd-201">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-202">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7e5bd-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-204">Ein Array von Methoden bezeichgern, von denen jedes eine Methode der [**MSVM \_ virtualethernettwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md) -Klasse identifiziert, die von der-Implementierung synchron unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="7e5bd-205">Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="7e5bd-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**Definesystem** (2)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**Destroysystem** (3)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**Destroysystemconfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**Modifyresourcesettings** (5)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**Modifysystemsettings** (6)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**Removeresources** (7)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**Selectsystemconfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**Snapshotsystem** (9)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**Adressquellen** (10)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**Addfeaturesettings** (32779)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**Modifyfeaturesettings** (32780)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**Removefeaturesettings** (32781)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e5bd-218">**Virtualsystemtypessupported**</span><span class="sxs-lookup"><span data-stu-id="7e5bd-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e5bd-219">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7e5bd-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7e5bd-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e5bd-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e5bd-221">Ein Array von Zeichen folgen, die jeweils einen virtuellen Systemtyp festlegen, der von der Implementierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="7e5bd-222">Der Wert jedes Array Elements, das nicht **null** ist, muss mit dem Format übereinstimmen, das für die **virtualsystemtype** -Eigenschaft der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="7e5bd-223">Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e5bd-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e5bd-224">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e5bd-224">Requirements</span></span>



| <span data-ttu-id="7e5bd-225">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e5bd-225">Requirement</span></span> | <span data-ttu-id="7e5bd-226">Wert</span><span class="sxs-lookup"><span data-stu-id="7e5bd-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e5bd-227">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-227">Minimum supported client</span></span><br/> | <span data-ttu-id="7e5bd-228">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e5bd-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7e5bd-229">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e5bd-229">Minimum supported server</span></span><br/> | <span data-ttu-id="7e5bd-230">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e5bd-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e5bd-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e5bd-231">Namespace</span></span><br/>                | <span data-ttu-id="7e5bd-232">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e5bd-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7e5bd-233">MOF</span><span class="sxs-lookup"><span data-stu-id="7e5bd-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e5bd-234"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e5bd-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e5bd-235">DLL</span><span class="sxs-lookup"><span data-stu-id="7e5bd-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e5bd-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e5bd-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

