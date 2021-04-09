---
description: Das Win32 \_ physicalmemoryarray-&\# 160; WMI-Klasse stellt Details zum physischen Arbeitsspeicher des Computer Systems dar. Dies schließt die Anzahl der Speichergeräte, die verfügbare Arbeitsspeicher Kapazität und den Arbeits Speichertyp&8212 ein, \# z. b. System-oder Videospeicher.
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryArray-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958608"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="37fba-104">Win32 \_ physicalmemoryarray-Klasse</span><span class="sxs-lookup"><span data-stu-id="37fba-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="37fba-105">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **\_ physicalmemoryarray** " von Win32 stellt Details zum physischen Arbeitsspeicher des Computer Systems dar.</span><span class="sxs-lookup"><span data-stu-id="37fba-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="37fba-106">Dies schließt die Anzahl der Speichergeräte, die verfügbare Arbeitsspeicher Kapazität und den Arbeits Speichertyp ein – z. b. System-oder Videospeicher.</span><span class="sxs-lookup"><span data-stu-id="37fba-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="37fba-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37fba-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="37fba-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="37fba-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="37fba-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="37fba-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="37fba-110">Member</span><span class="sxs-lookup"><span data-stu-id="37fba-110">Members</span></span>

<span data-ttu-id="37fba-111">Die **Win32 \_ physicalmemoryarray** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37fba-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="37fba-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="37fba-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="37fba-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37fba-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="37fba-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="37fba-114">Methods</span></span>

<span data-ttu-id="37fba-115">Die **Win32 \_ physicalmemoryarray** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="37fba-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="37fba-116">Methode</span><span class="sxs-lookup"><span data-stu-id="37fba-116">Method</span></span>           | <span data-ttu-id="37fba-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37fba-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="37fba-118">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="37fba-118">**IsCompatible**</span></span> | <span data-ttu-id="37fba-119">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="37fba-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="37fba-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37fba-120">Properties</span></span>

<span data-ttu-id="37fba-121">Die **Win32 \_ physicalmemoryarray** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37fba-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37fba-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="37fba-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-125">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="37fba-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-126">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="37fba-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="37fba-127">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-128">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="37fba-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-131">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="37fba-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-132">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37fba-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="37fba-133">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="37fba-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="37fba-134">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-135">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="37fba-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-136">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="37fba-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-138">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="37fba-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-139">Tiefe des physischen Pakets – in Zoll.</span><span class="sxs-lookup"><span data-stu-id="37fba-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="37fba-140">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37fba-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-144">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="37fba-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-145">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="37fba-145">Description of the object.</span></span>

<span data-ttu-id="37fba-146">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-147">**Height**</span><span class="sxs-lookup"><span data-stu-id="37fba-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-148">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="37fba-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-150">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="37fba-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-151">Höhe des physischen Pakets – in Zoll.</span><span class="sxs-lookup"><span data-stu-id="37fba-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="37fba-152">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-153">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="37fba-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-154">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="37fba-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37fba-156">**True** gibt an, dass ein physisches Paket im laufenden Betrieb ausgetauscht werden kann (wenn es möglich ist, das Element durch eine physisch abweichende, aber entsprechende zu ersetzen, während für das enthaltene Paket eine Stromversorgung angewendet wurde, ist "on").</span><span class="sxs-lookup"><span data-stu-id="37fba-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="37fba-157">Beispielsweise ist ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wurde, wechselseitig austauschbar.</span><span class="sxs-lookup"><span data-stu-id="37fba-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="37fba-158">Alle Pakete, die sich im laufenden Betrieb austauschen lassen, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="37fba-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="37fba-159">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="37fba-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-161">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="37fba-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-163">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="37fba-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-164">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="37fba-164">Date and time the object was installed.</span></span> <span data-ttu-id="37fba-165">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="37fba-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-167">**Location**</span><span class="sxs-lookup"><span data-stu-id="37fba-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37fba-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-170">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Location")</span><span class="sxs-lookup"><span data-stu-id="37fba-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-171">Der physische Speicherort des Speicherarrays.</span><span class="sxs-lookup"><span data-stu-id="37fba-171">Physical location of the memory array.</span></span>

<span data-ttu-id="37fba-172">Dieser Wert stammt aus dem **Location** -Member der **Array Struktur des physischen Speichers** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="37fba-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="37fba-173">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="37fba-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37fba-174">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="37fba-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37fba-175">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="37fba-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="37fba-176">**System Board oder Motherboard** (3)</span><span class="sxs-lookup"><span data-stu-id="37fba-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-177">**ISA-Add-on-Karte** (4)</span><span class="sxs-lookup"><span data-stu-id="37fba-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-178">**EISA-Add-on-Karte** (5)</span><span class="sxs-lookup"><span data-stu-id="37fba-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-179">**PCI-Add-on-Karte** (6)</span><span class="sxs-lookup"><span data-stu-id="37fba-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-180">**MCA-Add-on-Karte** (7)</span><span class="sxs-lookup"><span data-stu-id="37fba-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-181">**PCMCIA-Add-on-Karte** (8)</span><span class="sxs-lookup"><span data-stu-id="37fba-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-182">**Proprietäre Add-on-Karte** (9)</span><span class="sxs-lookup"><span data-stu-id="37fba-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="37fba-183">**NuBus** (10)</span><span class="sxs-lookup"><span data-stu-id="37fba-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-184">**PC-98/C20-Add-on-Karte** (11)</span><span class="sxs-lookup"><span data-stu-id="37fba-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-185">**PC-98/C24-Add-on-Karte** (12)</span><span class="sxs-lookup"><span data-stu-id="37fba-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-186">**PC-98/E-Add-on-Karte** (13)</span><span class="sxs-lookup"><span data-stu-id="37fba-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="37fba-187">**PC-98/Local Bus-Add-on-Karte** (14)</span><span class="sxs-lookup"><span data-stu-id="37fba-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37fba-188">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="37fba-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-191">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="37fba-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-192">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="37fba-193">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="37fba-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-195">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37fba-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-197">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ: 16 \| Maximale Kapazität")</span><span class="sxs-lookup"><span data-stu-id="37fba-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-198">Verwenden Sie stattdessen die **maxcapacityex** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="37fba-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="37fba-199">Dieser Wert stammt aus dem **Maximum Capacity** -Element der **Array Struktur des physischen Speichers** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="37fba-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="37fba-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Maximale Arbeitsspeicher Größe (in Bytes), die für dieses bestimmte Speicher Array installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="37fba-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="37fba-201">Wenn die Größe unbekannt ist, erhält die Eigenschaft den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="37fba-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-202">**Maxcapacityex**</span><span class="sxs-lookup"><span data-stu-id="37fba-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-203">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37fba-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-205">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 16 \| Erweiterte maximale Kapazität"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="37fba-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-206">Maximale Arbeitsspeicher Größe (in Kilobyte), die für dieses bestimmte Speicher Array installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="37fba-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="37fba-207">Wenn die Größe unbekannt ist, erhält die Eigenschaft den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="37fba-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="37fba-208">Dieser Wert stammt aus dem **erweiterten Maximum Capacity** -Element der **Array Struktur des physischen Speichers** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="37fba-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="37fba-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37fba-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="37fba-210">**Memorydevices**</span><span class="sxs-lookup"><span data-stu-id="37fba-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37fba-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-213">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 16 \| Anzahl von Speichergeräten")</span><span class="sxs-lookup"><span data-stu-id="37fba-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-214">Anzahl der physischen Slots oder Sockets, die in diesem Speicher Array verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="37fba-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="37fba-215">Dieser Wert stammt aus der **Anzahl der Speichergeräte** Elemente der Array Struktur des **physischen Speichers** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="37fba-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="37fba-216">**Memoryerrorkorrektur**</span><span class="sxs-lookup"><span data-stu-id="37fba-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-217">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37fba-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-219">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 16 Arbeits \| Speicherfehler Korrektur")</span><span class="sxs-lookup"><span data-stu-id="37fba-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-220">Der Typ der vom Speicher Array verwendeten Fehlerkorrektur.</span><span class="sxs-lookup"><span data-stu-id="37fba-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="37fba-221">Dieser Wert stammt aus dem **Speicherfehlerkorrektur** -Member der **Array Struktur des physischen Speichers** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="37fba-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="37fba-222">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="37fba-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37fba-223">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="37fba-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37fba-224">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="37fba-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="37fba-225">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="37fba-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="37fba-226">**Parität** (4)</span><span class="sxs-lookup"><span data-stu-id="37fba-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="37fba-227">**Single-Bit ECC** (5)</span><span class="sxs-lookup"><span data-stu-id="37fba-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="37fba-228">**Multi-Bit ECC** (6)</span><span class="sxs-lookup"><span data-stu-id="37fba-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="37fba-229">**CRC** (7)</span><span class="sxs-lookup"><span data-stu-id="37fba-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37fba-230">**Modell**</span><span class="sxs-lookup"><span data-stu-id="37fba-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-233">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="37fba-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-234">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="37fba-235">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-236">**Name**</span><span class="sxs-lookup"><span data-stu-id="37fba-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-239">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="37fba-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-240">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-240">Label by which the object is known.</span></span> <span data-ttu-id="37fba-241">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="37fba-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="37fba-242">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="37fba-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37fba-246">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="37fba-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="37fba-247">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="37fba-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="37fba-248">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** und die Barcode-Daten, die als Klassen Schlüssel verwendet werden, in der Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="37fba-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="37fba-249">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-250">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="37fba-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-253">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="37fba-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-254">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="37fba-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="37fba-255">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-256">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="37fba-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-257">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="37fba-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37fba-259">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="37fba-260">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-261">**Ab**</span><span class="sxs-lookup"><span data-stu-id="37fba-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-262">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="37fba-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37fba-264">**True** gibt an, dass ein physisches Paket entfernt werden kann (wenn es so konzipiert ist, dass es in den physischen Container übernommen wird, in dem es normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird).</span><span class="sxs-lookup"><span data-stu-id="37fba-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="37fba-265">Ein Paket kann weiterhin entfernt werden, wenn die Stromversorgung "Off" sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="37fba-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="37fba-266">Wenn Power "on" sein kann und das Paket entfernt werden kann, ist das Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="37fba-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="37fba-267">Beispielsweise ist ein zusätzlicher Akku in einem Laptop austauschbar, ebenso wie ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="37fba-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="37fba-268">Der letztere kann jedoch im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="37fba-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="37fba-269">Die Anzeige eines Laptops kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil.</span><span class="sxs-lookup"><span data-stu-id="37fba-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="37fba-270">Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="37fba-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="37fba-271">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-272">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="37fba-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-273">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="37fba-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37fba-275">**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37fba-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="37fba-276">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="37fba-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="37fba-277">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37fba-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="37fba-278">Ein weiteres Beispiel ist ein Stromversorgung-Paket, das auf gleitenden Schienen eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="37fba-279">Alle Wechsel Pakete sind von Natur aus austauschbar.</span><span class="sxs-lookup"><span data-stu-id="37fba-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="37fba-280">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-281">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="37fba-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-284">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="37fba-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-285">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="37fba-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="37fba-286">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-287">**SKU**</span><span class="sxs-lookup"><span data-stu-id="37fba-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-290">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="37fba-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-291">Stock Keeping Unit Number für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="37fba-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="37fba-292">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-293">**Status**</span><span class="sxs-lookup"><span data-stu-id="37fba-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-296">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="37fba-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-297">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="37fba-297">Current status of the object.</span></span> <span data-ttu-id="37fba-298">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="37fba-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="37fba-299">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="37fba-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="37fba-300">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="37fba-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="37fba-301">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="37fba-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="37fba-302">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="37fba-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="37fba-303">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="37fba-304">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="37fba-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="37fba-305">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="37fba-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="37fba-306">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="37fba-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37fba-307">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="37fba-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37fba-308">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="37fba-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="37fba-309">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="37fba-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="37fba-310">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="37fba-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="37fba-311">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="37fba-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="37fba-312">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="37fba-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="37fba-313">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="37fba-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="37fba-314">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="37fba-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="37fba-315">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="37fba-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="37fba-316">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="37fba-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37fba-317">**Tag**</span><span class="sxs-lookup"><span data-stu-id="37fba-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-320">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="37fba-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-321">Eindeutiger Bezeichner des physischen Speicherarrays.</span><span class="sxs-lookup"><span data-stu-id="37fba-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="37fba-322">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="37fba-323">Beispiel: "physikalischer Speicher Array 1"</span><span class="sxs-lookup"><span data-stu-id="37fba-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="37fba-324">**Verwenden Sie**</span><span class="sxs-lookup"><span data-stu-id="37fba-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-325">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37fba-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-327">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 16 \| verwenden")</span><span class="sxs-lookup"><span data-stu-id="37fba-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-328">Wie Arbeitsspeicher im Computersystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37fba-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="37fba-329">Dieser Wert stammt aus dem **use** -Member der **Array Struktur des physischen Speichers** in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="37fba-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="37fba-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="37fba-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37fba-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="37fba-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37fba-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="37fba-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="37fba-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System Arbeitsspeicher** (3)</span><span class="sxs-lookup"><span data-stu-id="37fba-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="37fba-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="37fba-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="37fba-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash Speicher** (5)</span><span class="sxs-lookup"><span data-stu-id="37fba-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="37fba-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Nicht flüchtiges RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="37fba-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="37fba-337">Nicht flüchtiges RAM</span><span class="sxs-lookup"><span data-stu-id="37fba-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="37fba-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache Speicher** (7)</span><span class="sxs-lookup"><span data-stu-id="37fba-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37fba-339">**Version**</span><span class="sxs-lookup"><span data-stu-id="37fba-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37fba-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-342">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="37fba-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37fba-343">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="37fba-343">Version of the physical element.</span></span>

<span data-ttu-id="37fba-344">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-345">**Weight**</span><span class="sxs-lookup"><span data-stu-id="37fba-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-346">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="37fba-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-348">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="37fba-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-349">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="37fba-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="37fba-350">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="37fba-351">**Width**</span><span class="sxs-lookup"><span data-stu-id="37fba-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37fba-352">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="37fba-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="37fba-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37fba-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37fba-354">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="37fba-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="37fba-355">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="37fba-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="37fba-356">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37fba-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37fba-357">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37fba-357">Remarks</span></span>

<span data-ttu-id="37fba-358">Die **Win32 \_ physicalmemoryarray** -Klasse wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="37fba-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="37fba-359">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37fba-359">Examples</span></span>

<span data-ttu-id="37fba-360">Im folgenden PowerShell-Beispiel wird die Anzahl der Arbeitsspeicher Slots und der auf einem Bereitstellungs Zielcomputer installierte Arbeitsspeicher abgerufen.</span><span class="sxs-lookup"><span data-stu-id="37fba-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="37fba-361">Im folgenden VBScript-Codebeispiel werden Informationen über den physischen Speicher zurückgegeben, der auf einem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="37fba-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="37fba-362">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37fba-362">Requirements</span></span>



| <span data-ttu-id="37fba-363">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37fba-363">Requirement</span></span> | <span data-ttu-id="37fba-364">Wert</span><span class="sxs-lookup"><span data-stu-id="37fba-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37fba-365">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37fba-365">Minimum supported client</span></span><br/> | <span data-ttu-id="37fba-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37fba-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37fba-367">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37fba-367">Minimum supported server</span></span><br/> | <span data-ttu-id="37fba-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37fba-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37fba-369">Namespace</span><span class="sxs-lookup"><span data-stu-id="37fba-369">Namespace</span></span><br/>                | <span data-ttu-id="37fba-370">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37fba-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37fba-371">MOF</span><span class="sxs-lookup"><span data-stu-id="37fba-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37fba-372"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37fba-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37fba-373">DLL</span><span class="sxs-lookup"><span data-stu-id="37fba-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37fba-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37fba-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fba-375">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37fba-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fba-376">**CIM- \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="37fba-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="37fba-377">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="37fba-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="37fba-378">**Win32 \_ memoryarraylocation**</span><span class="sxs-lookup"><span data-stu-id="37fba-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 
