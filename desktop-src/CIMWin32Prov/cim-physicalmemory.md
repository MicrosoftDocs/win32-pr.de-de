---
description: Die CIM \_ PhysicalMemory-Klasse stellt Speichergeräte auf niedriger Ebene dar, wie z. b. Simms, DIMMs, Rohdaten Speicher-Chips usw.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: CIM_PhysicalMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861535"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="9af1a-103">CIM \_ PhysicalMemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="9af1a-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="9af1a-104">Die **CIM \_ PhysicalMemory** -Klasse stellt Speichergeräte auf niedriger Ebene dar, wie z. b. Simms, DIMMs, Rohdaten Speicher-Chips usw.</span><span class="sxs-lookup"><span data-stu-id="9af1a-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9af1a-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9af1a-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9af1a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9af1a-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9af1a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9af1a-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af1a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9af1a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
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
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="9af1a-110">Member</span><span class="sxs-lookup"><span data-stu-id="9af1a-110">Members</span></span>

<span data-ttu-id="9af1a-111">Die **CIM \_ PhysicalMemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9af1a-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="9af1a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9af1a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9af1a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9af1a-113">Properties</span></span>

<span data-ttu-id="9af1a-114">Die **CIM \_ PhysicalMemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9af1a-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9af1a-115">**Banklabel**</span><span class="sxs-lookup"><span data-stu-id="9af1a-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-119">Bezeichnung Bank, in der sich der Arbeitsspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="9af1a-120">Beispiel: "Bank 0" oder "Bank A".</span><span class="sxs-lookup"><span data-stu-id="9af1a-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-121">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="9af1a-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-122">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9af1a-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-124">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (Bytes)</span><span class="sxs-lookup"><span data-stu-id="9af1a-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-125">Gesamtkapazität des physischen Speichers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9af1a-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="9af1a-126">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9af1a-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-127">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9af1a-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9af1a-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-131">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9af1a-131">Short textual description of the object.</span></span>

<span data-ttu-id="9af1a-132">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-133">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9af1a-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-136">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9af1a-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-137">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9af1a-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9af1a-138">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9af1a-139">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="9af1a-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af1a-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-144">Daten Breite des physischen Speichers in Bits.</span><span class="sxs-lookup"><span data-stu-id="9af1a-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="9af1a-145">Eine Daten Breite von 0 (null) und eine Gesamtbreite von 8 gibt an, dass der Arbeitsspeicher ausschließlich zur Bereitstellung von Fehlerkorrektur Bits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9af1a-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9af1a-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-149">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9af1a-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-150">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9af1a-150">Textual description of the object.</span></span>

<span data-ttu-id="9af1a-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-152">**Formfaktor**</span><span class="sxs-lookup"><span data-stu-id="9af1a-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af1a-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-155">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-156">Der Implementierungs Formfaktor für den Chip.</span><span class="sxs-lookup"><span data-stu-id="9af1a-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="9af1a-157">Beispielsweise können Werte wie z. b. SIMM, SPOP oder PGA angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="9af1a-158">Diese Eigenschaft wird vom [**CIM- \_ Chip**](cim-chip.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="9af1a-159">0</span><span class="sxs-lookup"><span data-stu-id="9af1a-159">0</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-160">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="9af1a-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-161">1</span><span class="sxs-lookup"><span data-stu-id="9af1a-161">1</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-162">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="9af1a-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-163">2</span><span class="sxs-lookup"><span data-stu-id="9af1a-163">2</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-164">Fen</span><span class="sxs-lookup"><span data-stu-id="9af1a-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-165">3</span><span class="sxs-lookup"><span data-stu-id="9af1a-165">3</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-166">DIP</span><span class="sxs-lookup"><span data-stu-id="9af1a-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-167">4</span><span class="sxs-lookup"><span data-stu-id="9af1a-167">4</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="9af1a-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-169">5</span><span class="sxs-lookup"><span data-stu-id="9af1a-169">5</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-170">Soj</span><span class="sxs-lookup"><span data-stu-id="9af1a-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-171">6</span><span class="sxs-lookup"><span data-stu-id="9af1a-171">6</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-172">Proprietär</span><span class="sxs-lookup"><span data-stu-id="9af1a-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-173">7</span><span class="sxs-lookup"><span data-stu-id="9af1a-173">7</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-174">SIMM</span><span class="sxs-lookup"><span data-stu-id="9af1a-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-175">8</span><span class="sxs-lookup"><span data-stu-id="9af1a-175">8</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-176">DIMM</span><span class="sxs-lookup"><span data-stu-id="9af1a-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-177">9</span><span class="sxs-lookup"><span data-stu-id="9af1a-177">9</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-178">Wahrheits Satz</span><span class="sxs-lookup"><span data-stu-id="9af1a-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-179">10</span><span class="sxs-lookup"><span data-stu-id="9af1a-179">10</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-180">Besetzten</span><span class="sxs-lookup"><span data-stu-id="9af1a-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-181">11</span><span class="sxs-lookup"><span data-stu-id="9af1a-181">11</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-182">RIMM</span><span class="sxs-lookup"><span data-stu-id="9af1a-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-183">12</span><span class="sxs-lookup"><span data-stu-id="9af1a-183">12</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-184">SODIMM</span><span class="sxs-lookup"><span data-stu-id="9af1a-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-185">13</span><span class="sxs-lookup"><span data-stu-id="9af1a-185">13</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-186">Srimm</span><span class="sxs-lookup"><span data-stu-id="9af1a-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-187">14</span><span class="sxs-lookup"><span data-stu-id="9af1a-187">14</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-188">Tenden</span><span class="sxs-lookup"><span data-stu-id="9af1a-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-189">15</span><span class="sxs-lookup"><span data-stu-id="9af1a-189">15</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-190">SSMP</span><span class="sxs-lookup"><span data-stu-id="9af1a-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-191">16</span><span class="sxs-lookup"><span data-stu-id="9af1a-191">16</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-192">QFP</span><span class="sxs-lookup"><span data-stu-id="9af1a-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-193">17</span><span class="sxs-lookup"><span data-stu-id="9af1a-193">17</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-194">TQFP</span><span class="sxs-lookup"><span data-stu-id="9af1a-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-195">18</span><span class="sxs-lookup"><span data-stu-id="9af1a-195">18</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-196">SOIC</span><span class="sxs-lookup"><span data-stu-id="9af1a-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-197">19</span><span class="sxs-lookup"><span data-stu-id="9af1a-197">19</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-198">LCC</span><span class="sxs-lookup"><span data-stu-id="9af1a-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-199">20</span><span class="sxs-lookup"><span data-stu-id="9af1a-199">20</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-200">PLCC</span><span class="sxs-lookup"><span data-stu-id="9af1a-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-201">21</span><span class="sxs-lookup"><span data-stu-id="9af1a-201">21</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-202">BGA</span><span class="sxs-lookup"><span data-stu-id="9af1a-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-203">22</span><span class="sxs-lookup"><span data-stu-id="9af1a-203">22</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-204">Fpbga</span><span class="sxs-lookup"><span data-stu-id="9af1a-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-205">23</span><span class="sxs-lookup"><span data-stu-id="9af1a-205">23</span></span>
</dt> <dd>

<span data-ttu-id="9af1a-206">LGA</span><span class="sxs-lookup"><span data-stu-id="9af1a-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9af1a-207">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="9af1a-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-208">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9af1a-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-210">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="9af1a-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="9af1a-211">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="9af1a-212">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="9af1a-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="9af1a-213">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="9af1a-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="9af1a-214">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9af1a-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-216">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9af1a-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-218">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-219">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9af1a-219">Date and time the object was installed.</span></span> <span data-ttu-id="9af1a-220">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9af1a-221">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-222">**Interleaveposition**</span><span class="sxs-lookup"><span data-stu-id="9af1a-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-223">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9af1a-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-225">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-226">Die Position des physischen Speichers in einem Interleave.</span><span class="sxs-lookup"><span data-stu-id="9af1a-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="9af1a-227">Der Wert 0 gibt eine nicht überlappte an, 1 gibt die erste Position an, 2 gibt die zweite Position an usw.</span><span class="sxs-lookup"><span data-stu-id="9af1a-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="9af1a-228">Beispielsweise gibt der Wert 1 in einem 2:1-Interleave an, dass sich der Speicher in der geraden Position befindet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-229">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="9af1a-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-232">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9af1a-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-233">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="9af1a-234">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="9af1a-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="9af1a-235">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-236">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="9af1a-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af1a-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-239">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-240">Typ des physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="9af1a-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9af1a-241">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9af1a-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9af1a-242">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9af1a-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="9af1a-243">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="9af1a-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="9af1a-244">**Synchroner DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="9af1a-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="9af1a-245">**Cache-DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="9af1a-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="9af1a-246">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="9af1a-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="9af1a-247">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="9af1a-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="9af1a-248">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="9af1a-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="9af1a-249">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="9af1a-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="9af1a-250">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="9af1a-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="9af1a-251">**Rom** (10)</span><span class="sxs-lookup"><span data-stu-id="9af1a-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="9af1a-252">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="9af1a-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="9af1a-253">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="9af1a-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="9af1a-254">**Feprom** (13)</span><span class="sxs-lookup"><span data-stu-id="9af1a-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="9af1a-255">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="9af1a-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="9af1a-256">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="9af1a-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="9af1a-257">**3dram** (16)</span><span class="sxs-lookup"><span data-stu-id="9af1a-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="9af1a-258">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="9af1a-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="9af1a-259">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="9af1a-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="9af1a-260">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="9af1a-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="9af1a-261">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="9af1a-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="9af1a-262">**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="9af1a-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="9af1a-263">**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="9af1a-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9af1a-264">**Modell**</span><span class="sxs-lookup"><span data-stu-id="9af1a-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-265">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-267">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9af1a-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-268">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="9af1a-269">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-270">**Name**</span><span class="sxs-lookup"><span data-stu-id="9af1a-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-273">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9af1a-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-274">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-274">Label by which the object is known.</span></span> <span data-ttu-id="9af1a-275">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9af1a-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9af1a-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-280">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9af1a-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="9af1a-281">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="9af1a-282">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="9af1a-283">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-284">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="9af1a-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-287">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9af1a-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-288">Die Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="9af1a-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="9af1a-289">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-290">**Positioninrow**</span><span class="sxs-lookup"><span data-stu-id="9af1a-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-291">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9af1a-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-293">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-294">Die Position des physischen Speichers in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="9af1a-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="9af1a-295">Wenn z. b. 2 8-Bit-Speichergeräte zum bilden einer 16-Bit-Zeile benötigt werden, gibt der Wert 2 an, dass der Arbeitsspeicher das zweite Gerät ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="9af1a-296">Der Wert 0 (null) ist ein ungültiger Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9af1a-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-297">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="9af1a-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-298">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9af1a-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-300">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="9af1a-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="9af1a-301">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-302">**Ab**</span><span class="sxs-lookup"><span data-stu-id="9af1a-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-303">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9af1a-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-305">**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="9af1a-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="9af1a-306">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9af1a-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="9af1a-307">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="9af1a-308">Beispielsweise kann ein nicht Abzieh barer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="9af1a-309">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-310">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="9af1a-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-311">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9af1a-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-313">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="9af1a-314">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="9af1a-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="9af1a-315">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="9af1a-316">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="9af1a-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="9af1a-317">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-318">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="9af1a-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-321">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9af1a-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-322">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9af1a-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="9af1a-323">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-324">**SKU**</span><span class="sxs-lookup"><span data-stu-id="9af1a-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-327">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9af1a-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-328">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="9af1a-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="9af1a-329">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-330">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="9af1a-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-331">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9af1a-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-333">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="9af1a-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-334">Geschwindigkeit des physischen Speichers in Nanosekunden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-335">**Status**</span><span class="sxs-lookup"><span data-stu-id="9af1a-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-338">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9af1a-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-339">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9af1a-339">Current status of the object.</span></span> <span data-ttu-id="9af1a-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9af1a-341">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="9af1a-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9af1a-342">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9af1a-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9af1a-343">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9af1a-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9af1a-344">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9af1a-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9af1a-345">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9af1a-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9af1a-346">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9af1a-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9af1a-347">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9af1a-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9af1a-348">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9af1a-349">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9af1a-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9af1a-350">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9af1a-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9af1a-351">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9af1a-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9af1a-352">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9af1a-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9af1a-353">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9af1a-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9af1a-354">**Tag**</span><span class="sxs-lookup"><span data-stu-id="9af1a-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-357">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9af1a-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-358">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="9af1a-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="9af1a-359">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="9af1a-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="9af1a-360">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9af1a-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="9af1a-361">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="9af1a-362">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9af1a-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="9af1a-363">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="9af1a-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="9af1a-364">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="9af1a-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-366">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af1a-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-368">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="9af1a-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-369">Gesamtbreite des physischen Speichers (in Bits), einschließlich der Check-oder Error-Korrektur Bits.</span><span class="sxs-lookup"><span data-stu-id="9af1a-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="9af1a-370">Wenn keine Fehlerkorrektur Bits vorhanden sind, sollte der Wert in dieser Eigenschaft mit dem für die **DataWidth** -Eigenschaft angegebenen Wert identisch sein.</span><span class="sxs-lookup"><span data-stu-id="9af1a-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="9af1a-371">**Version**</span><span class="sxs-lookup"><span data-stu-id="9af1a-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af1a-372">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9af1a-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9af1a-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af1a-374">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9af1a-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9af1a-375">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="9af1a-375">Version of the physical element.</span></span>

<span data-ttu-id="9af1a-376">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9af1a-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9af1a-377">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9af1a-377">Remarks</span></span>

<span data-ttu-id="9af1a-378">Die **CIM \_ PhysicalMemory** -Klasse wird vom [**CIM- \_ Chip**](cim-chip.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="9af1a-379">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9af1a-379">WMI does not implement this class.</span></span> <span data-ttu-id="9af1a-380">Informationen zu WMI-Klassen, die von **CIM \_ PhysicalMemory** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="9af1a-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9af1a-381">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9af1a-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9af1a-382">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9af1a-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af1a-383">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9af1a-383">Requirements</span></span>



| <span data-ttu-id="9af1a-384">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9af1a-384">Requirement</span></span> | <span data-ttu-id="9af1a-385">Wert</span><span class="sxs-lookup"><span data-stu-id="9af1a-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9af1a-386">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9af1a-386">Minimum supported client</span></span><br/> | <span data-ttu-id="9af1a-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9af1a-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9af1a-388">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9af1a-388">Minimum supported server</span></span><br/> | <span data-ttu-id="9af1a-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9af1a-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9af1a-390">Namespace</span><span class="sxs-lookup"><span data-stu-id="9af1a-390">Namespace</span></span><br/>                | <span data-ttu-id="9af1a-391">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9af1a-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9af1a-392">MOF</span><span class="sxs-lookup"><span data-stu-id="9af1a-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9af1a-393"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9af1a-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9af1a-394">DLL</span><span class="sxs-lookup"><span data-stu-id="9af1a-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af1a-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af1a-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af1a-396">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9af1a-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af1a-397">**CIM- \_ Chip**</span><span class="sxs-lookup"><span data-stu-id="9af1a-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 

