---
description: Der Win32- \_ Systemslot &\# 32; Die WMI-Klasse stellt physische Verbindungspunkte einschließlich Ports, Motherboard-Slots und Peripheriegeräte sowie proprietäre Verbindungspunkte dar.
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Win32_SystemSlot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127593"
---
# <a name="win32_systemslot-class"></a><span data-ttu-id="21274-103">Win32 \_ Systemslot-Klasse</span><span class="sxs-lookup"><span data-stu-id="21274-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="21274-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Systemslot** stellt physische Verbindungspunkte einschließlich Ports, Motherboard-Slots und Peripheriegeräte sowie proprietäre Verbindungspunkte dar.</span><span class="sxs-lookup"><span data-stu-id="21274-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="21274-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21274-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="21274-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="21274-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="21274-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21274-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="21274-108">Member</span><span class="sxs-lookup"><span data-stu-id="21274-108">Members</span></span>

<span data-ttu-id="21274-109">Die **Win32- \_ systemslotklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="21274-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="21274-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21274-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21274-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21274-111">Properties</span></span>

<span data-ttu-id="21274-112">Die **Win32- \_ systemslotklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21274-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21274-113">**Busnummer**</span><span class="sxs-lookup"><span data-stu-id="21274-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21274-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-116">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| Bus Number")</span><span class="sxs-lookup"><span data-stu-id="21274-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="21274-117">SMBIOS-Busnummer.</span><span class="sxs-lookup"><span data-stu-id="21274-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="21274-118">Dieser Wert stammt aus dem **Busnummern** Element der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21274-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="21274-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="21274-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-123">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="21274-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="21274-124">Kurze Beschreibung eines Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="21274-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="21274-125">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-126">**Connectoriout**</span><span class="sxs-lookup"><span data-stu-id="21274-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21274-129">Eine frei Form Zeichenfolge, die die PIN-Konfiguration und die Signal Verwendung eines physischen Verbindungs-Connector beschreibt.</span><span class="sxs-lookup"><span data-stu-id="21274-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="21274-130">Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-131">**Connector Type**</span><span class="sxs-lookup"><span data-stu-id="21274-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-132">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="21274-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21274-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-134">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Connector Type"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9- \| slottyp")</span><span class="sxs-lookup"><span data-stu-id="21274-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="21274-135">Array physischer Attribute des Connector, der von diesem Slot verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21274-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="21274-136">Dieser Wert stammt aus dem **Slot-Typmember** der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-137">Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="21274-138">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="21274-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21274-139">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21274-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21274-140">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21274-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="21274-141">**Männlich** (2)</span><span class="sxs-lookup"><span data-stu-id="21274-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="21274-142">**Weiblich** (3)</span><span class="sxs-lookup"><span data-stu-id="21274-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="21274-143">**Abgeschirmt** (4)</span><span class="sxs-lookup"><span data-stu-id="21274-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="21274-144">Nicht **gezitet** (5)</span><span class="sxs-lookup"><span data-stu-id="21274-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="21274-145">**SCSI (A) High-Density (50 Pins)** (6)</span><span class="sxs-lookup"><span data-stu-id="21274-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="21274-146">**SCSI (A) Low-Density (50 Pins)** (7)</span><span class="sxs-lookup"><span data-stu-id="21274-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="21274-147">**SCSI (P) High-Density (68 Pins)** (8)</span><span class="sxs-lookup"><span data-stu-id="21274-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="21274-148">**SCSI SCA-I (80 Pins)** (9)</span><span class="sxs-lookup"><span data-stu-id="21274-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="21274-149">**SCSI SCA-II (80 Pins)** (10)</span><span class="sxs-lookup"><span data-stu-id="21274-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="21274-150">**SCSI-Fibre Channel (DB-9, Kupfer)** (11)</span><span class="sxs-lookup"><span data-stu-id="21274-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="21274-151">**SCSI-Fibre Channel (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="21274-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="21274-152">**SCSI-Fibre Channel SCA-II (40 Pins)** (13)</span><span class="sxs-lookup"><span data-stu-id="21274-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="21274-153">**SCSI-Fibre Channel SCA-II (20 Pins)** (14)</span><span class="sxs-lookup"><span data-stu-id="21274-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="21274-154">**SCSI-Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="21274-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="21274-155">**ATA 3-1/2 Zoll (40 Pins)** (16)</span><span class="sxs-lookup"><span data-stu-id="21274-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="21274-156">**ATA 2-1/2 Zoll (44 Pins)** (17)</span><span class="sxs-lookup"><span data-stu-id="21274-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="21274-157">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="21274-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="21274-158">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="21274-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="21274-159">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="21274-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="21274-160">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="21274-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="21274-161">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="21274-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="21274-162">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="21274-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="21274-163">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="21274-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="21274-164">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="21274-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="21274-165">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="21274-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="21274-166">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="21274-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="21274-167">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="21274-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="21274-168">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="21274-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="21274-169">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="21274-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="21274-170">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="21274-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="21274-171">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="21274-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="21274-172">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="21274-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="21274-173">**UTP Kategorie 3** (34)</span><span class="sxs-lookup"><span data-stu-id="21274-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="21274-174">**UTP Kategorie 4** (35)</span><span class="sxs-lookup"><span data-stu-id="21274-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="21274-175">**UTP Kategorie 5** (36)</span><span class="sxs-lookup"><span data-stu-id="21274-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="21274-176">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="21274-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="21274-177">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="21274-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="21274-178">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="21274-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="21274-179">**Fiber MIC** (40)</span><span class="sxs-lookup"><span data-stu-id="21274-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="21274-180">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="21274-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="21274-181">**Apple-GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="21274-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="21274-182">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="21274-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="21274-183">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="21274-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="21274-184">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="21274-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="21274-185">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="21274-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="21274-186">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="21274-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="21274-187">**PCMCIA-Typ I** (48)</span><span class="sxs-lookup"><span data-stu-id="21274-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="21274-188">**PCMCIA-Typ II** (49)</span><span class="sxs-lookup"><span data-stu-id="21274-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="21274-189">**PCMCIA-Typ III** (50)</span><span class="sxs-lookup"><span data-stu-id="21274-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="21274-190">**ZV-Port** (51)</span><span class="sxs-lookup"><span data-stu-id="21274-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="21274-191">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="21274-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="21274-192">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="21274-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="21274-193">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="21274-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="21274-194">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="21274-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="21274-195">**HSSDC (6 Pins)** (56)</span><span class="sxs-lookup"><span data-stu-id="21274-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="21274-196">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="21274-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="21274-197">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="21274-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="21274-198">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="21274-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="21274-199">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="21274-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="21274-200">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="21274-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="21274-201">**Infrarot** (62)</span><span class="sxs-lookup"><span data-stu-id="21274-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="21274-202">**HP-HIL** (63)</span><span class="sxs-lookup"><span data-stu-id="21274-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="21274-203">**Access. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="21274-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="21274-204">**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="21274-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="21274-205">**Zentronik** (66)</span><span class="sxs-lookup"><span data-stu-id="21274-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="21274-206">**Mini-centronik** (67)</span><span class="sxs-lookup"><span data-stu-id="21274-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="21274-207">**Minicentronics Type-14** (68)</span><span class="sxs-lookup"><span data-stu-id="21274-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="21274-208">**Minicentronics Type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="21274-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="21274-209">**Minicentronics Type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="21274-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="21274-210">**Busmaus** (71)</span><span class="sxs-lookup"><span data-stu-id="21274-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="21274-211">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="21274-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="21274-212">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="21274-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="21274-213">**VME-Bus** (74)</span><span class="sxs-lookup"><span data-stu-id="21274-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="21274-214">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="21274-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="21274-215">**Proprietär** (76)</span><span class="sxs-lookup"><span data-stu-id="21274-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="21274-216">**Platzhalter für proprietäre Prozessorkarte** (77)</span><span class="sxs-lookup"><span data-stu-id="21274-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="21274-217">Geschützter **Speicherkarten Slot** (78)</span><span class="sxs-lookup"><span data-stu-id="21274-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="21274-218">**Eigener e/a-Riser-Slot** (79)</span><span class="sxs-lookup"><span data-stu-id="21274-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="21274-219">**PCI-66MHz** (80)</span><span class="sxs-lookup"><span data-stu-id="21274-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="21274-220">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="21274-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="21274-221">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="21274-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="21274-222">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="21274-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="21274-223">**PC-98-hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="21274-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="21274-224">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="21274-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="21274-225">**PC-98note** (86)</span><span class="sxs-lookup"><span data-stu-id="21274-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="21274-226">**PC-98full** (87)</span><span class="sxs-lookup"><span data-stu-id="21274-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="21274-227">**PCI-X** (88)</span><span class="sxs-lookup"><span data-stu-id="21274-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="21274-228">**SBus IEEE 1396-1993 32 Bit** (89)</span><span class="sxs-lookup"><span data-stu-id="21274-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="21274-229">**SBus IEEE 1396-1993 64 Bit** (90)</span><span class="sxs-lookup"><span data-stu-id="21274-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="21274-230">**MCA** (91)</span><span class="sxs-lookup"><span data-stu-id="21274-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="21274-231">**Gio** (92)</span><span class="sxs-lookup"><span data-stu-id="21274-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="21274-232">**XIO** (93)</span><span class="sxs-lookup"><span data-stu-id="21274-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="21274-233">**Hio** (94)</span><span class="sxs-lookup"><span data-stu-id="21274-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="21274-234">**Ngio** (95)</span><span class="sxs-lookup"><span data-stu-id="21274-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="21274-235">**PMC** (96)</span><span class="sxs-lookup"><span data-stu-id="21274-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="21274-236">**Zukünftige e/a-** Vorgänge (97)</span><span class="sxs-lookup"><span data-stu-id="21274-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="21274-237">**InfiniBand** (98)</span><span class="sxs-lookup"><span data-stu-id="21274-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="21274-238">**AGP8X** (99)</span><span class="sxs-lookup"><span data-stu-id="21274-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="21274-239">**PCI-E** (100)</span><span class="sxs-lookup"><span data-stu-id="21274-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21274-240">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="21274-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-243">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="21274-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="21274-244">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21274-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="21274-245">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften einer Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="21274-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="21274-246">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-247">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="21274-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-248">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21274-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21274-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-250">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| Current Usage")</span><span class="sxs-lookup"><span data-stu-id="21274-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="21274-251">Der Status der System Slot-Verwendung.</span><span class="sxs-lookup"><span data-stu-id="21274-251">Status of system slot use.</span></span>

<span data-ttu-id="21274-252">Dieser Wert stammt aus dem **aktuellen Verwendungs** Mitglied der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-253">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="21274-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="21274-254">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="21274-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21274-255">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21274-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21274-256">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="21274-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="21274-257">**Verfügbar** (3)</span><span class="sxs-lookup"><span data-stu-id="21274-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="21274-258">**In Gebrauch** (4)</span><span class="sxs-lookup"><span data-stu-id="21274-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21274-259">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21274-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-262">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="21274-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="21274-263">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21274-263">Description of the object.</span></span>

<span data-ttu-id="21274-264">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-265">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="21274-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-266">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21274-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-268">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9- \| Gerätenummer")</span><span class="sxs-lookup"><span data-stu-id="21274-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="21274-269">SMBIOS-Gerätenummer.</span><span class="sxs-lookup"><span data-stu-id="21274-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="21274-270">Dieser Wert stammt aus dem **Geräte-/funktionsnummermember** der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21274-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="21274-272">**Functionnumber**</span><span class="sxs-lookup"><span data-stu-id="21274-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21274-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-275">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 9- \| Funktions Nummer")</span><span class="sxs-lookup"><span data-stu-id="21274-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="21274-276">SMBIOS-Funktions Nummer.</span><span class="sxs-lookup"><span data-stu-id="21274-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="21274-277">Dieser Wert stammt aus dem **Geräte-/funktionsnummermember** der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21274-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="21274-279">**Erhöht**</span><span class="sxs-lookup"><span data-stu-id="21274-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-280">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="21274-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-282">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="21274-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="21274-283">Maximale Höhe einer Adapterkarte, die in den Slot – in Zoll eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="21274-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="21274-284">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="21274-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-286">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="21274-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="21274-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-288">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="21274-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="21274-289">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="21274-289">Date and time the object is installed.</span></span> <span data-ttu-id="21274-290">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="21274-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="21274-291">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-292">**Verlängert**</span><span class="sxs-lookup"><span data-stu-id="21274-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-293">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="21274-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-295">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="21274-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="21274-296">Maximale Länge einer Adapterkarte, die in den Slot – in Zoll eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="21274-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="21274-297">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-298">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="21274-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-301">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="21274-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="21274-302">Der Name der Organisation, die das physische Element erzeugt.</span><span class="sxs-lookup"><span data-stu-id="21274-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="21274-303">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-304">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="21274-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-305">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21274-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21274-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-307">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Slot \| 004,3 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="21274-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="21274-308">Maximale Busbreite von Adapterkarten, die in diesen Slot eingefügt werden können – in Bits.</span><span class="sxs-lookup"><span data-stu-id="21274-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="21274-309">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="21274-309">This can be one of the following values.</span></span>

<span data-ttu-id="21274-310">Dieser Wert stammt aus dem **Slot Data Bus Width** -Member der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-311">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="21274-312">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="21274-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="21274-313"><span id="8"></span>**8** (0)</span><span class="sxs-lookup"><span data-stu-id="21274-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="21274-314">Maximale Daten Breite (Bits): 8</span><span class="sxs-lookup"><span data-stu-id="21274-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="21274-315"><span id="16"></span>**16** (1)</span><span class="sxs-lookup"><span data-stu-id="21274-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="21274-316">Maximale Daten Breite (Bits): 16</span><span class="sxs-lookup"><span data-stu-id="21274-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="21274-317"><span id="32"></span>**32** (2)</span><span class="sxs-lookup"><span data-stu-id="21274-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="21274-318">Maximale Daten Breite (Bits): 32</span><span class="sxs-lookup"><span data-stu-id="21274-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="21274-319"><span id="64"></span>**64** (3)</span><span class="sxs-lookup"><span data-stu-id="21274-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21274-320">Maximale Daten Breite (Bits): 64</span><span class="sxs-lookup"><span data-stu-id="21274-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="21274-321"><span id="128"></span>**128** (4)</span><span class="sxs-lookup"><span data-stu-id="21274-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="21274-322">Maximale Daten Breite (Bits): 128</span><span class="sxs-lookup"><span data-stu-id="21274-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21274-323">**Modell**</span><span class="sxs-lookup"><span data-stu-id="21274-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-326">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="21274-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="21274-327">Der Name für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="21274-327">Name for the physical element.</span></span>

<span data-ttu-id="21274-328">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-329">**Name**</span><span class="sxs-lookup"><span data-stu-id="21274-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-332">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="21274-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="21274-333">Die Bezeichnung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="21274-333">Label for the object.</span></span> <span data-ttu-id="21274-334">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="21274-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="21274-335">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-336">**Number**</span><span class="sxs-lookup"><span data-stu-id="21274-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-337">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21274-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21274-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21274-339">Die physische Slot-Nummer, die als Index in eine systemslottabelle verwendet werden kann, unabhängig davon, ob der Slot physisch leer ist.</span><span class="sxs-lookup"><span data-stu-id="21274-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="21274-340">Dieser Wert stammt aus dem **Slot-ID** -Element der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-341">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="21274-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21274-345">Zusätzliche Daten (d. h. mehr als die Informationen zum Bestands Kennzeichen), mit denen ein physisches Element identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="21274-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="21274-346">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="21274-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="21274-347">Beachten Sie, dass diese Eigenschaft **null** ist, wenn nur Barcode Daten verfügbar sind und Sie eindeutig ist oder als Element Schlüssel verwendet werden kann. die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="21274-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="21274-348">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-349">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="21274-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-352">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="21274-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="21274-353">Teilenummer, die der Producer oder der Hersteller dem physischen Element zuweist.</span><span class="sxs-lookup"><span data-stu-id="21274-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="21274-354">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-355">**PMESignal**</span><span class="sxs-lookup"><span data-stu-id="21274-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-356">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21274-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21274-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-358">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 9- \| Slot-Merkmale 2")</span><span class="sxs-lookup"><span data-stu-id="21274-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="21274-359">**True** gibt an, dass das PCI-Bus-PME-Signal (Power Management-fähig) von diesem Slot unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="21274-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="21274-360">Dieser Wert stammt aus dem **Slot-Merkmal 2** -Member der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="21274-361">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="21274-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-362">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21274-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21274-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21274-364">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="21274-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="21274-365">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-366">**Zweck Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21274-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-369">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Slot**](cim-slot.md).**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="21274-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="21274-370">Frei Form Zeichenfolge, die beschreibt, wie dieser Slot physisch eindeutig ist und spezielle Hardwaretypen beinhalten kann.</span><span class="sxs-lookup"><span data-stu-id="21274-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="21274-371">Diese Eigenschaft hat nur die Bedeutung, wenn die entsprechende Eigenschaft **SpecialPurpose** den Wert **true** aufweist.</span><span class="sxs-lookup"><span data-stu-id="21274-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="21274-372">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-373">**Segmentgroupnumber**</span><span class="sxs-lookup"><span data-stu-id="21274-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-374">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21274-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-376">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| Segment Group Number")</span><span class="sxs-lookup"><span data-stu-id="21274-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="21274-377">SMBIOS-Segment Gruppennummer.</span><span class="sxs-lookup"><span data-stu-id="21274-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="21274-378">Dieser Wert stammt aus dem **Segment Gruppennummer** -Member der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21274-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="21274-380">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="21274-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-383">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="21274-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="21274-384">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="21274-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="21274-385">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-386">**Freigegeben**</span><span class="sxs-lookup"><span data-stu-id="21274-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-387">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21274-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21274-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-389">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 9- \| Slot-Merkmale 1")</span><span class="sxs-lookup"><span data-stu-id="21274-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="21274-390">Wenn der Wert **true** ist, verwenden zwei oder mehr Slots einen Speicherort auf dem Baseboard, z. b. einen freigegebenen PCI/EISA-Slot.</span><span class="sxs-lookup"><span data-stu-id="21274-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="21274-391">Dieser Wert stammt aus den **Slot-Merkmalen 1** in der Struktur der **System Slots** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="21274-392">**SKU**</span><span class="sxs-lookup"><span data-stu-id="21274-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-393">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-395">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="21274-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="21274-396">Stock Keeping Unit Number für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="21274-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="21274-397">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-398">**Slotbezeichnung**</span><span class="sxs-lookup"><span data-stu-id="21274-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-401">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| Slot-Bezeichnung")</span><span class="sxs-lookup"><span data-stu-id="21274-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="21274-402">SMBIOS-Zeichenfolge, die die System Slot-Bezeichnung des Slots auf der Hauptplatine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="21274-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="21274-403">Beispiel: "PCI-1"</span><span class="sxs-lookup"><span data-stu-id="21274-403">Example: "PCI-1"</span></span>

<span data-ttu-id="21274-404">Dieser Wert stammt aus dem **Slot-Benennungs** Mitglied der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="21274-405">**Specialzweck**</span><span class="sxs-lookup"><span data-stu-id="21274-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-406">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21274-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21274-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-408">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Slot**](cim-slot.md).**Zweck Beschreibung**")</span><span class="sxs-lookup"><span data-stu-id="21274-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="21274-409">**True** gibt an, dass dieser Slot physisch eindeutig ist und spezielle Hardwaretypen, z. b. einen Grafikprozessor Slot, beinhalten kann.</span><span class="sxs-lookup"><span data-stu-id="21274-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="21274-410">Wenn der Wert **true** ist, sollte " **zieldescription** " die Art der Eindeutigkeit oder den Zweck des Slots angeben.</span><span class="sxs-lookup"><span data-stu-id="21274-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="21274-411">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-412">**Status**</span><span class="sxs-lookup"><span data-stu-id="21274-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-413">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-415">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="21274-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="21274-416">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21274-416">Current status of the object.</span></span> <span data-ttu-id="21274-417">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="21274-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="21274-418">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="21274-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="21274-419">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="21274-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="21274-420">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="21274-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="21274-421">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="21274-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="21274-422">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="21274-423">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="21274-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="21274-424">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="21274-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="21274-425">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="21274-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21274-426">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="21274-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21274-427">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="21274-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="21274-428">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="21274-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="21274-429">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="21274-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="21274-430">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="21274-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="21274-431">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="21274-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="21274-432">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="21274-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="21274-433">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="21274-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="21274-434">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="21274-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="21274-435">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="21274-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21274-436">**Supportshotplug**</span><span class="sxs-lookup"><span data-stu-id="21274-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-437">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21274-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21274-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21274-439">**True** gibt an, dass der Slot das Hot-Plugging von Adapterkarten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21274-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="21274-440">Dieser Wert stammt aus dem **Slot-Merkmal 2** -Member der **System Slots** -Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-441">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-442">**Tag**</span><span class="sxs-lookup"><span data-stu-id="21274-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-443">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-445">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="21274-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="21274-446">Der von einer Instanz dieser Klasse dargestellte System Slot.</span><span class="sxs-lookup"><span data-stu-id="21274-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="21274-447">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="21274-448">Beispiel: "System Slot 1"</span><span class="sxs-lookup"><span data-stu-id="21274-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="21274-449">**Theritäts Bewertung**</span><span class="sxs-lookup"><span data-stu-id="21274-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-450">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21274-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21274-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-452">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Slot \| 004,11 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="21274-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="21274-453">Maximale thermische Unterschiede des Slots in Milliwatt.</span><span class="sxs-lookup"><span data-stu-id="21274-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="21274-454">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-455">**Vccmixedvoltagesupport**</span><span class="sxs-lookup"><span data-stu-id="21274-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-456">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="21274-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21274-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-458">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Slot \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="21274-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="21274-459">Array von enumerationsintegern, das die von diesem Slot unterstützte VCC-Spannung angibt.</span><span class="sxs-lookup"><span data-stu-id="21274-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="21274-460">Dieser Wert stammt aus den **Slot-Merkmalen 1** in der Struktur der **System Slots** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="21274-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="21274-461">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="21274-462">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="21274-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21274-463">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21274-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21274-464">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21274-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="21274-465">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="21274-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="21274-466">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="21274-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21274-467">**Version**</span><span class="sxs-lookup"><span data-stu-id="21274-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-468">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21274-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21274-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-470">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="21274-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="21274-471">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="21274-471">Version of the physical element.</span></span>

<span data-ttu-id="21274-472">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21274-473">**Vppmixedvoltagesupport**</span><span class="sxs-lookup"><span data-stu-id="21274-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21274-474">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="21274-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21274-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21274-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21274-476">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Slot \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="21274-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="21274-477">Array von enumerationsintegern, das die von diesem Slot unterstützte VPP-Spannung angibt.</span><span class="sxs-lookup"><span data-stu-id="21274-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="21274-478">Diese Eigenschaft wird vom [**CIM- \_ Slot**](cim-slot.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21274-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="21274-479">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="21274-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21274-480">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21274-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21274-481">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21274-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="21274-482">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="21274-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="21274-483">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="21274-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="21274-484">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="21274-484">**12V** (4)</span></span>


<span data-ttu-id="21274-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="21274-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="21274-486">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21274-486">Remarks</span></span>

<span data-ttu-id="21274-487">Die **Win32- \_ systemslotklasse** wird vom [**CIM- \_ Slot**](cim-slot.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="21274-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21274-488">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21274-488">Requirements</span></span>



| <span data-ttu-id="21274-489">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21274-489">Requirement</span></span> | <span data-ttu-id="21274-490">Wert</span><span class="sxs-lookup"><span data-stu-id="21274-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21274-491">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21274-491">Minimum supported client</span></span><br/> | <span data-ttu-id="21274-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21274-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21274-493">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21274-493">Minimum supported server</span></span><br/> | <span data-ttu-id="21274-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21274-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21274-495">Namespace</span><span class="sxs-lookup"><span data-stu-id="21274-495">Namespace</span></span><br/>                | <span data-ttu-id="21274-496">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="21274-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21274-497">MOF</span><span class="sxs-lookup"><span data-stu-id="21274-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21274-498"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="21274-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21274-499">DLL</span><span class="sxs-lookup"><span data-stu-id="21274-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21274-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21274-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21274-501">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21274-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21274-502">**CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="21274-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="21274-503">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="21274-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
