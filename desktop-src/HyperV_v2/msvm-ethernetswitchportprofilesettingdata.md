---
description: Stellt die Port Profileinstellungen dar.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Msvm_EthernetSwitchPortProfileSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369909"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="f67b1-103">MSVM \_ ethernetzwitchportprofilesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="f67b1-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="f67b1-104">Stellt die Port Profileinstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="f67b1-104">Represents the port profile settings.</span></span>

<span data-ttu-id="f67b1-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f67b1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f67b1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f67b1-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="f67b1-107">Member</span><span class="sxs-lookup"><span data-stu-id="f67b1-107">Members</span></span>

<span data-ttu-id="f67b1-108">Die **MSVM \_ ethernetzwitchportprofilesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f67b1-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f67b1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f67b1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f67b1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f67b1-110">Properties</span></span>

<span data-ttu-id="f67b1-111">Die **MSVM \_ ethernetzwitchportprofilesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f67b1-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f67b1-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f67b1-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f67b1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f67b1-115">A short description of the object.</span></span> <span data-ttu-id="f67b1-116">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Profile Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f67b1-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-117">**Cdnlabelid**</span><span class="sxs-lookup"><span data-stu-id="f67b1-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f67b1-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-120">Qualifizierer: **wmidataid** (11), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-121">Der Bezeichner für die CDN-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="f67b1-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-122">**Cdnlabelstring**</span><span class="sxs-lookup"><span data-stu-id="f67b1-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-125">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (12), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-126">Die Zeichenfolge für die CDN-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="f67b1-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f67b1-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f67b1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-130">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f67b1-130">A description of the object.</span></span> <span data-ttu-id="f67b1-131">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Port Profileinstellungen" fest.</span><span class="sxs-lookup"><span data-stu-id="f67b1-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f67b1-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f67b1-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-135">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f67b1-135">A display name for the object.</span></span> <span data-ttu-id="f67b1-136">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Profile Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f67b1-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f67b1-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f67b1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-140">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f67b1-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-141">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f67b1-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f67b1-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f67b1-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-143">**NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="f67b1-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-146">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-147">Ein eindeutiger Geräte Bezeichner der Unterschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f67b1-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-148">**Pcibusnumber**</span><span class="sxs-lookup"><span data-stu-id="f67b1-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f67b1-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-151">Qualifizierer: **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-152">Die PCI-Busnummer.</span><span class="sxs-lookup"><span data-stu-id="f67b1-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-153">**Pcidevicenumber**</span><span class="sxs-lookup"><span data-stu-id="f67b1-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f67b1-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-156">Qualifizierer: **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-157">Die PCI-Gerätenummer.</span><span class="sxs-lookup"><span data-stu-id="f67b1-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-158">**Pcifunctionnumber**</span><span class="sxs-lookup"><span data-stu-id="f67b1-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f67b1-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-161">Qualifizierer: **wmidataid** (10), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-162">Die PCI-Funktions Nummer.</span><span class="sxs-lookup"><span data-stu-id="f67b1-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-163">**Pcisegmentnumber**</span><span class="sxs-lookup"><span data-stu-id="f67b1-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-164">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f67b1-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-166">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-167">Die PCI-Segment Nummer.</span><span class="sxs-lookup"><span data-stu-id="f67b1-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-168">**ProfileData**</span><span class="sxs-lookup"><span data-stu-id="f67b1-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-169">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f67b1-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-171">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-172">Zusätzliche Daten für das Port Profil.</span><span class="sxs-lookup"><span data-stu-id="f67b1-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-173">**Profil**</span><span class="sxs-lookup"><span data-stu-id="f67b1-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-176">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-177">Der Bezeichner des Port Profils.</span><span class="sxs-lookup"><span data-stu-id="f67b1-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-178">**Profile Name**</span><span class="sxs-lookup"><span data-stu-id="f67b1-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-181">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-182">Der Name des Port Profils.</span><span class="sxs-lookup"><span data-stu-id="f67b1-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-183">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="f67b1-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-186">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-187">Der Bezeichner des Anbieters, der das Profil definiert.</span><span class="sxs-lookup"><span data-stu-id="f67b1-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="f67b1-188">**VendorName**</span><span class="sxs-lookup"><span data-stu-id="f67b1-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67b1-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f67b1-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f67b1-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f67b1-191">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f67b1-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f67b1-192">Der Name des Herstellers, der das Profil definiert.</span><span class="sxs-lookup"><span data-stu-id="f67b1-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f67b1-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f67b1-193">Requirements</span></span>



| <span data-ttu-id="f67b1-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f67b1-194">Requirement</span></span> | <span data-ttu-id="f67b1-195">Wert</span><span class="sxs-lookup"><span data-stu-id="f67b1-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67b1-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f67b1-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f67b1-197">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f67b1-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f67b1-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f67b1-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f67b1-199">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f67b1-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f67b1-200">Namespace</span><span class="sxs-lookup"><span data-stu-id="f67b1-200">Namespace</span></span><br/>                | <span data-ttu-id="f67b1-201">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f67b1-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f67b1-202">MOF</span><span class="sxs-lookup"><span data-stu-id="f67b1-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f67b1-203"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f67b1-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f67b1-204">DLL</span><span class="sxs-lookup"><span data-stu-id="f67b1-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f67b1-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f67b1-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

