---
description: Stellt ein physisches Speichergerät dar, das sich auf einem Computersystem befindet und dem Betriebssystem zur Verfügung steht.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Win32_PhysicalMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483958"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="0885a-103">Win32 \_ PhysicalMemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="0885a-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="0885a-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ PhysicalMemory** stellt ein physisches Speichergerät dar, das sich auf einem Computersystem befindet und dem Betriebssystem zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="0885a-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="0885a-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0885a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0885a-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0885a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0885a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0885a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="0885a-108">Member</span><span class="sxs-lookup"><span data-stu-id="0885a-108">Members</span></span>

<span data-ttu-id="0885a-109">Die **Win32 \_ PhysicalMemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0885a-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="0885a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0885a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0885a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0885a-111">Properties</span></span>

<span data-ttu-id="0885a-112">Die **Win32 \_ PhysicalMemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0885a-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0885a-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0885a-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-116">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17- \| Attribute")</span><span class="sxs-lookup"><span data-stu-id="0885a-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-117">SMBIOS-Type 17: Attribute.</span><span class="sxs-lookup"><span data-stu-id="0885a-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="0885a-118">Stellt den Rang dar.</span><span class="sxs-lookup"><span data-stu-id="0885a-118">Represents the RANK.</span></span>

<span data-ttu-id="0885a-119">Dieser Wert stammt aus dem **Attributmember** der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0885a-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-121">**Banklabel**</span><span class="sxs-lookup"><span data-stu-id="0885a-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-124">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="0885a-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-125">Physisch Bezeichnung Bank, auf der sich der Speicher befindet.</span><span class="sxs-lookup"><span data-stu-id="0885a-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="0885a-126">Beispiele: "Bank 0", "Bank A"</span><span class="sxs-lookup"><span data-stu-id="0885a-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="0885a-127">Dieser Wert stammt aus dem **Bank Locator** -Member der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-128">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-129">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="0885a-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-130">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0885a-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-132">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,5 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (Bytes)</span><span class="sxs-lookup"><span data-stu-id="0885a-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-133">Gesamtkapazität des physischen Speichers – (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="0885a-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="0885a-134">Dieser Wert stammt aus der **Speichergeräte** Struktur in den SMBIOS-Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="0885a-135">Für SMBIOS-Versionen 2,1 bis 2,6 ergibt sich der Wert aus dem **size** -Member.</span><span class="sxs-lookup"><span data-stu-id="0885a-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="0885a-136">Für SMBIOS, Version 2.7 und höher, wird der Wert aus dem **erweiterten Größen** Element abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0885a-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="0885a-137">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="0885a-138">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="0885a-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0885a-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-142">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0885a-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-143">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0885a-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="0885a-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-145">**Konfigurations Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="0885a-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-148">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 17 \| konfigurierte Speicher Taktgeschwindigkeit")</span><span class="sxs-lookup"><span data-stu-id="0885a-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-149">Die konfigurierte Taktfrequenz des Speichergeräts in Megahertz (MHz) oder 0 (null), wenn die Geschwindigkeit unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="0885a-150">Dieser Wert stammt aus dem **konfigurierten speicherclock-Geschwindigkeits** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0885a-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-152">**Konfiguriert**</span><span class="sxs-lookup"><span data-stu-id="0885a-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-155">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| konfigurierte Spannung")</span><span class="sxs-lookup"><span data-stu-id="0885a-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-156">Konfigurierte Spannung für dieses Gerät (in Millivolt) oder 0 (null), wenn die Spannung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="0885a-157">Dieser Wert stammt aus dem **konfigurierten Spannungs** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0885a-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-159">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0885a-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-162">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0885a-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-163">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0885a-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0885a-164">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0885a-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="0885a-165">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="0885a-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0885a-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-169">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,8 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="0885a-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-170">Daten Breite des physischen Speichers – in Bits.</span><span class="sxs-lookup"><span data-stu-id="0885a-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="0885a-171">Eine Daten Breite von 0 (null) und eine Gesamtbreite von 8 (acht) gibt an, dass der Arbeitsspeicher ausschließlich zur Bereitstellung von Fehlerkorrektur Bits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0885a-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="0885a-172">Dieser Wert stammt aus dem **datenwidth** -Member der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-173">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-174">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0885a-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-177">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0885a-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-178">Die Beschreibung eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="0885a-178">Description of an object.</span></span>

<span data-ttu-id="0885a-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="0885a-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-183">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Device Locator")</span><span class="sxs-lookup"><span data-stu-id="0885a-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-184">Die Bezeichnung des Sockets oder der Verbindungs Platine, die den Arbeitsspeicher enthält.</span><span class="sxs-lookup"><span data-stu-id="0885a-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="0885a-185">Beispiel: "SIMM 3"</span><span class="sxs-lookup"><span data-stu-id="0885a-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="0885a-186">Dieser Wert stammt aus dem **geräterlocatormember** der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-187">**Formfaktor**</span><span class="sxs-lookup"><span data-stu-id="0885a-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-188">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0885a-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-190">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="0885a-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-191">Der Implementierungs Formfaktor für den Chip.</span><span class="sxs-lookup"><span data-stu-id="0885a-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="0885a-192">Dieser Wert stammt aus dem **Form Faktor** -Member der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-193">Diese Eigenschaft wird vom [**CIM- \_ Chip**](cim-chip.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="0885a-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="0885a-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-195">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="0885a-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-196">(1)</span><span class="sxs-lookup"><span data-stu-id="0885a-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-197">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0885a-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-198">(2)</span><span class="sxs-lookup"><span data-stu-id="0885a-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-199">Fen</span><span class="sxs-lookup"><span data-stu-id="0885a-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-200">(3)</span><span class="sxs-lookup"><span data-stu-id="0885a-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-201">DIP</span><span class="sxs-lookup"><span data-stu-id="0885a-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-202">(4)</span><span class="sxs-lookup"><span data-stu-id="0885a-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="0885a-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-204">(5)</span><span class="sxs-lookup"><span data-stu-id="0885a-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-205">Soj</span><span class="sxs-lookup"><span data-stu-id="0885a-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="0885a-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-207">Proprietär</span><span class="sxs-lookup"><span data-stu-id="0885a-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-208">(7)</span><span class="sxs-lookup"><span data-stu-id="0885a-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-209">SIMM</span><span class="sxs-lookup"><span data-stu-id="0885a-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-210">(8)</span><span class="sxs-lookup"><span data-stu-id="0885a-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-211">DIMM</span><span class="sxs-lookup"><span data-stu-id="0885a-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-212">(9)</span><span class="sxs-lookup"><span data-stu-id="0885a-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-213">Wahrheits Satz</span><span class="sxs-lookup"><span data-stu-id="0885a-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-214">(10)</span><span class="sxs-lookup"><span data-stu-id="0885a-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-215">Besetzten</span><span class="sxs-lookup"><span data-stu-id="0885a-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-216">(11)</span><span class="sxs-lookup"><span data-stu-id="0885a-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-217">RIMM</span><span class="sxs-lookup"><span data-stu-id="0885a-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-218">(12)</span><span class="sxs-lookup"><span data-stu-id="0885a-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-219">SODIMM</span><span class="sxs-lookup"><span data-stu-id="0885a-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-220">(13)</span><span class="sxs-lookup"><span data-stu-id="0885a-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-221">Srimm</span><span class="sxs-lookup"><span data-stu-id="0885a-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-222">(14)</span><span class="sxs-lookup"><span data-stu-id="0885a-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-223">Tenden</span><span class="sxs-lookup"><span data-stu-id="0885a-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-224">(15)</span><span class="sxs-lookup"><span data-stu-id="0885a-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-225">SSMP</span><span class="sxs-lookup"><span data-stu-id="0885a-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-226">(16)</span><span class="sxs-lookup"><span data-stu-id="0885a-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-227">QFP</span><span class="sxs-lookup"><span data-stu-id="0885a-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-228">(17)</span><span class="sxs-lookup"><span data-stu-id="0885a-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-229">TQFP</span><span class="sxs-lookup"><span data-stu-id="0885a-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-230">(18)</span><span class="sxs-lookup"><span data-stu-id="0885a-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-231">SOIC</span><span class="sxs-lookup"><span data-stu-id="0885a-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-232">(19)</span><span class="sxs-lookup"><span data-stu-id="0885a-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-233">LCC</span><span class="sxs-lookup"><span data-stu-id="0885a-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-234">(20)</span><span class="sxs-lookup"><span data-stu-id="0885a-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-235">PLCC</span><span class="sxs-lookup"><span data-stu-id="0885a-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-236">(21)</span><span class="sxs-lookup"><span data-stu-id="0885a-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-237">BGA</span><span class="sxs-lookup"><span data-stu-id="0885a-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-238">(22)</span><span class="sxs-lookup"><span data-stu-id="0885a-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-239">Fpbga</span><span class="sxs-lookup"><span data-stu-id="0885a-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="0885a-240">(23)</span><span class="sxs-lookup"><span data-stu-id="0885a-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-241">LGA</span><span class="sxs-lookup"><span data-stu-id="0885a-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0885a-242">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="0885a-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-243">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0885a-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0885a-245">**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere, aber entsprechende ersetzt werden kann, während das enthaltende Paket die Stromversorgung hat.</span><span class="sxs-lookup"><span data-stu-id="0885a-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="0885a-246">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="0885a-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="0885a-247">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="0885a-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="0885a-248">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0885a-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-250">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0885a-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-252">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="0885a-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-253">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0885a-253">Date and time the object is installed.</span></span> <span data-ttu-id="0885a-254">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0885a-255">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-256">**InterleaveDataDepth**</span><span class="sxs-lookup"><span data-stu-id="0885a-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0885a-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-259">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 20 \| verschachtelte Datentiefe")</span><span class="sxs-lookup"><span data-stu-id="0885a-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-260">Ganze 16-Bit-Ganzzahl ohne Vorzeichen: maximale Anzahl aufeinander folgender Daten Zeilen, auf die in einer einzelnen überlappenden Übertragung vom Arbeitsspeicher Gerät zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="0885a-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="0885a-261">Wenn der Wert 0 (null) ist, wird der Arbeitsspeicher nicht überlappt.</span><span class="sxs-lookup"><span data-stu-id="0885a-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-262">**Interleaveposition**</span><span class="sxs-lookup"><span data-stu-id="0885a-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-263">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-265">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="0885a-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-266">Die Position des physischen Speichers in einem Interleave.</span><span class="sxs-lookup"><span data-stu-id="0885a-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="0885a-267">Beispielsweise gibt der Wert "1" in einem 2:1-Interleave an, dass sich der Speicher an der "geraden" Position befindet.</span><span class="sxs-lookup"><span data-stu-id="0885a-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="0885a-268">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="0885a-269">0</span><span class="sxs-lookup"><span data-stu-id="0885a-269">0</span></span>
</dt> <dd>

<span data-ttu-id="0885a-270">Nicht Interleaved</span><span class="sxs-lookup"><span data-stu-id="0885a-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="0885a-271">1</span><span class="sxs-lookup"><span data-stu-id="0885a-271">1</span></span>
</dt> <dd>

<span data-ttu-id="0885a-272">Erste Position</span><span class="sxs-lookup"><span data-stu-id="0885a-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="0885a-273">2</span><span class="sxs-lookup"><span data-stu-id="0885a-273">2</span></span>
</dt> <dd>

<span data-ttu-id="0885a-274">Zweite Position</span><span class="sxs-lookup"><span data-stu-id="0885a-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0885a-275">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="0885a-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-278">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0885a-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-279">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="0885a-280">Dieser Wert stammt vom **Hersteller** Mitglied der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-281">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-282">**Maxspannung**</span><span class="sxs-lookup"><span data-stu-id="0885a-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-285">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 17 \| Maximale Spannung")</span><span class="sxs-lookup"><span data-stu-id="0885a-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-286">Die maximale Betriebsspannung für dieses Gerät (in Millivolt) oder 0 (null), wenn die Spannung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="0885a-287">Dieser Wert stammt aus dem **Maximum-Spannungs** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0885a-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-289">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="0885a-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-290">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0885a-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-292">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="0885a-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-293">Typ des physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="0885a-293">Type of physical memory.</span></span> <span data-ttu-id="0885a-294">Dies ist ein CIM-Wert, der dem SMBIOS-Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="0885a-295">Die Eigenschaft **smbiosmemorytype** enthält den unformatierten SMBIOS-Arbeitsspeichertyp.</span><span class="sxs-lookup"><span data-stu-id="0885a-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="0885a-296">Dieser Wert stammt aus dem **Speichertyp** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-297">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0885a-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0885a-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0885a-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0885a-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="0885a-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="0885a-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="0885a-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchroner DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="0885a-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="0885a-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache-DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="0885a-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="0885a-303"><span id="EDO"></span><span id="edo"></span>**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="0885a-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="0885a-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="0885a-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="0885a-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="0885a-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="0885a-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="0885a-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="0885a-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="0885a-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="0885a-308"><span id="ROM"></span><span id="rom"></span>**Rom** (10)</span><span class="sxs-lookup"><span data-stu-id="0885a-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="0885a-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="0885a-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="0885a-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="0885a-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="0885a-311"><span id="FEPROM"></span><span id="feprom"></span>**Feprom** (13)</span><span class="sxs-lookup"><span data-stu-id="0885a-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="0885a-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="0885a-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="0885a-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="0885a-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="0885a-314"><span id="3DRAM"></span><span id="3dram"></span>**3dram** (16)</span><span class="sxs-lookup"><span data-stu-id="0885a-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="0885a-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="0885a-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="0885a-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="0885a-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="0885a-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="0885a-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="0885a-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="0885a-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="0885a-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="0885a-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-320">DDR2 – ist möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0885a-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="0885a-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="0885a-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-322">DDR2 – FB-DIMM ist möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0885a-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-323">24</span><span class="sxs-lookup"><span data-stu-id="0885a-323">24</span></span>
</dt> <dd>

<span data-ttu-id="0885a-324">"DDR3 –" ist möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0885a-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-325">25</span><span class="sxs-lookup"><span data-stu-id="0885a-325">25</span></span>
</dt> <dd>

<span data-ttu-id="0885a-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="0885a-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="0885a-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span><span class="sxs-lookup"><span data-stu-id="0885a-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0885a-328">**Minspannung**</span><span class="sxs-lookup"><span data-stu-id="0885a-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-329">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-331">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 20 \| minimale Spannung")</span><span class="sxs-lookup"><span data-stu-id="0885a-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-332">Die minimale Betriebsspannung für dieses Gerät (in Millivolt) oder 0 (null), wenn die Spannung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="0885a-333">Dieser Wert stammt aus dem **minimalen Spannungs** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0885a-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-335">**Modell**</span><span class="sxs-lookup"><span data-stu-id="0885a-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-338">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0885a-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-339">Der Name für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="0885a-339">Name for the physical element.</span></span>

<span data-ttu-id="0885a-340">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-341">**Name**</span><span class="sxs-lookup"><span data-stu-id="0885a-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-344">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0885a-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-345">Die Bezeichnung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0885a-345">Label for the object.</span></span> <span data-ttu-id="0885a-346">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0885a-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0885a-347">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0885a-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0885a-351">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0885a-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="0885a-352">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0885a-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="0885a-353">Wenn nur Barcode Daten verfügbar und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** , und die Barcode Daten werden als Klassen Schlüssel in der Tag-Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="0885a-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="0885a-354">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-355">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0885a-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-358">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0885a-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-359">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="0885a-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="0885a-360">Dieser Wert stammt aus dem **Teil Nummern** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-361">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-362">**Positioninrow**</span><span class="sxs-lookup"><span data-stu-id="0885a-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-363">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-365">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="0885a-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-366">Die Position des physischen Speichers in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="0885a-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="0885a-367">Wenn z. b. 2 8-Bit-Speichergeräte zum bilden einer 16-Bit-Zeile benötigt werden, bedeutet der Wert 2 (zwei), dass dieser Speicher das zweite Gerät ist – 0 (null) ist ein ungültiger Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0885a-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="0885a-368">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-369">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="0885a-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-370">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0885a-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0885a-372">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="0885a-373">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-374">**Ab**</span><span class="sxs-lookup"><span data-stu-id="0885a-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-375">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0885a-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0885a-377">**True** gibt an, dass eine physische Komponente Wechsel Datenträger ist (wenn Sie so konzipiert ist, dass Sie in den physischen Container übernommen wird, in dem Sie normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird).</span><span class="sxs-lookup"><span data-stu-id="0885a-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="0885a-378">Eine Komponente kann weiterhin Wechsel Datenträger durchgeführt werden, wenn die Stromversorgung deaktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0885a-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="0885a-379">Wenn Power "on" sein kann und die Komponente entfernt wurde, ist das Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="0885a-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="0885a-380">Beispielsweise kann ein aktualisierbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0885a-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="0885a-381">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-382">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="0885a-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-383">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0885a-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0885a-385">**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0885a-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="0885a-386">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="0885a-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="0885a-387">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0885a-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="0885a-388">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="0885a-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="0885a-389">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-390">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0885a-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-393">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0885a-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-394">Vom Hersteller zugewiesene Nummer, um das physische Element zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0885a-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="0885a-395">Dieser Wert stammt aus dem **Seriennummern** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-396">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-397">**SKU**</span><span class="sxs-lookup"><span data-stu-id="0885a-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-398">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-400">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0885a-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-401">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="0885a-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="0885a-402">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-403">**Smbiosmemorytype**</span><span class="sxs-lookup"><span data-stu-id="0885a-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-404">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-406">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 17- \| \_ Arbeitsspeichertyp")</span><span class="sxs-lookup"><span data-stu-id="0885a-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-407">Der unformatierte SMBIOS-Arbeitsspeichertyp.</span><span class="sxs-lookup"><span data-stu-id="0885a-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="0885a-408">Der Wert der **MemoryType** -Eigenschaft ist ein CIM-Wert, der dem SMBIOS-Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0885a-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="0885a-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0885a-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0885a-410">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="0885a-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-411">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0885a-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-413">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="0885a-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-414">Geschwindigkeit des physischen Speichers – in Nanosekunden.</span><span class="sxs-lookup"><span data-stu-id="0885a-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="0885a-415">Dieser Wert stammt aus dem **Geschwindigkeits** Mitglied der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-416">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-417">**Status**</span><span class="sxs-lookup"><span data-stu-id="0885a-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-420">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0885a-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-421">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0885a-421">Current status of the object.</span></span> <span data-ttu-id="0885a-422">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0885a-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0885a-423">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="0885a-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0885a-424">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="0885a-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0885a-425">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0885a-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0885a-426">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0885a-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0885a-427">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0885a-428">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="0885a-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0885a-429">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0885a-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0885a-430">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0885a-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0885a-431">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0885a-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0885a-432">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0885a-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0885a-433">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0885a-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0885a-434">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0885a-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0885a-435">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="0885a-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0885a-436">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0885a-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0885a-437">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="0885a-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0885a-438">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="0885a-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0885a-439">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="0885a-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0885a-440">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="0885a-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0885a-441">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0885a-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-444">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0885a-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-445">Eindeutiger Bezeichner für das physische Speichergerät, das durch eine Instanz von **Win32 \_ PhysicalMemory** repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="0885a-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="0885a-446">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="0885a-447">Beispiel: "physischer Speicher 1"</span><span class="sxs-lookup"><span data-stu-id="0885a-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="0885a-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="0885a-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-449">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0885a-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-451">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,7 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="0885a-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-452">Gesamtbreite des physischen Speichers (in Bits), einschließlich der Check-oder Error-Korrektur Bits.</span><span class="sxs-lookup"><span data-stu-id="0885a-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="0885a-453">Wenn keine Fehlerkorrektur Bits vorhanden sind, sollte der Wert in dieser Eigenschaft mit den Angaben für die **DataWidth** -Eigenschaft identisch sein.</span><span class="sxs-lookup"><span data-stu-id="0885a-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="0885a-454">Dieser Wert stammt aus dem **Total Width** -Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0885a-455">Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0885a-456">**TypeDetail**</span><span class="sxs-lookup"><span data-stu-id="0885a-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-457">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0885a-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-459">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Type Details")</span><span class="sxs-lookup"><span data-stu-id="0885a-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="0885a-460">Typ des dargestellten physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="0885a-460">Type of physical memory represented.</span></span>

<span data-ttu-id="0885a-461">Dieser Wert stammt vom **typdetailmember** der **Speichergeräte** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="0885a-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="0885a-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (1)</span><span class="sxs-lookup"><span data-stu-id="0885a-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0885a-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (2)</span><span class="sxs-lookup"><span data-stu-id="0885a-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0885a-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (4)</span><span class="sxs-lookup"><span data-stu-id="0885a-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="0885a-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Schnell Auslagerung(** 8)</span><span class="sxs-lookup"><span data-stu-id="0885a-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="0885a-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Statische Spalte** (16)</span><span class="sxs-lookup"><span data-stu-id="0885a-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="0885a-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo statisch** (32)</span><span class="sxs-lookup"><span data-stu-id="0885a-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="0885a-468"><span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)</span><span class="sxs-lookup"><span data-stu-id="0885a-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="0885a-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchron** (128)</span><span class="sxs-lookup"><span data-stu-id="0885a-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="0885a-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span><span class="sxs-lookup"><span data-stu-id="0885a-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="0885a-471"><span id="EDO"></span><span id="edo"></span>**Edo** (512)</span><span class="sxs-lookup"><span data-stu-id="0885a-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="0885a-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Fenster DRAM** (1024)</span><span class="sxs-lookup"><span data-stu-id="0885a-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="0885a-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache-DRAM** (2048)</span><span class="sxs-lookup"><span data-stu-id="0885a-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="0885a-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Nicht flüchtig** (4096)</span><span class="sxs-lookup"><span data-stu-id="0885a-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="0885a-475">Nicht volatil</span><span class="sxs-lookup"><span data-stu-id="0885a-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0885a-476">**Version**</span><span class="sxs-lookup"><span data-stu-id="0885a-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0885a-477">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0885a-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0885a-478">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0885a-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0885a-479">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0885a-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0885a-480">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="0885a-480">Version of the physical element.</span></span>

<span data-ttu-id="0885a-481">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0885a-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0885a-482">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0885a-482">Remarks</span></span>

<span data-ttu-id="0885a-483">Die **Win32 \_ PhysicalMemory** -Klasse wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0885a-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0885a-484">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0885a-484">Examples</span></span>

<span data-ttu-id="0885a-485">Das PowerShell [-Beispiel Get-ComputerInfo-Query Computer Info from Local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ PhysicalMemory**, um Informationen über ein lokales oder Remote System anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0885a-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="0885a-486">Das PowerShell-Beispiel für [Server Berichte](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ PhysicalMemory**, um Server Informationen zu erfassen und in Word-Dokumenten zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0885a-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="0885a-487">Das folgende PowerShell-Beispielcode ruft Informationen zum physischen Speicher des lokalen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="0885a-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="0885a-488">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0885a-488">Requirements</span></span>



| <span data-ttu-id="0885a-489">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0885a-489">Requirement</span></span> | <span data-ttu-id="0885a-490">Wert</span><span class="sxs-lookup"><span data-stu-id="0885a-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0885a-491">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0885a-491">Minimum supported client</span></span><br/> | <span data-ttu-id="0885a-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0885a-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0885a-493">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0885a-493">Minimum supported server</span></span><br/> | <span data-ttu-id="0885a-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0885a-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0885a-495">Namespace</span><span class="sxs-lookup"><span data-stu-id="0885a-495">Namespace</span></span><br/>                | <span data-ttu-id="0885a-496">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0885a-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0885a-497">MOF</span><span class="sxs-lookup"><span data-stu-id="0885a-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0885a-498"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0885a-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0885a-499">DLL</span><span class="sxs-lookup"><span data-stu-id="0885a-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0885a-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0885a-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0885a-501">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0885a-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0885a-502">**CIM- \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="0885a-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="0885a-503">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="0885a-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
