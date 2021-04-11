---
description: Stellt ein Baseboard dar, das auch als "Motherboard" oder "System Board" bezeichnet wird.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Win32_BaseBoard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041516"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="a107f-103">Win32- \_ Baseboard-Klasse</span><span class="sxs-lookup"><span data-stu-id="a107f-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="a107f-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für das **Win32- \_ Baseboard** stellt ein Baseboard dar, das auch als "Motherboard" oder "System Board" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a107f-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="a107f-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a107f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a107f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a107f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="a107f-107">Member</span><span class="sxs-lookup"><span data-stu-id="a107f-107">Members</span></span>

<span data-ttu-id="a107f-108">Die **Win32- \_ Baseboard** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a107f-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="a107f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a107f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a107f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a107f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a107f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a107f-111">Methods</span></span>

<span data-ttu-id="a107f-112">Die **Win32- \_ Baseboard** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a107f-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="a107f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="a107f-113">Method</span></span>           | <span data-ttu-id="a107f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a107f-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="a107f-115">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="a107f-115">**IsCompatible**</span></span> | <span data-ttu-id="a107f-116">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a107f-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a107f-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a107f-117">Properties</span></span>

<span data-ttu-id="a107f-118">Die **Win32- \_ Baseboard** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a107f-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a107f-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a107f-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a107f-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-123">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a107f-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="a107f-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-125">**ConfigOptions**</span><span class="sxs-lookup"><span data-stu-id="a107f-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-126">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a107f-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a107f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 12- \| Konfigurationsoptionen Zeichen folgen")</span><span class="sxs-lookup"><span data-stu-id="a107f-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-129">Ein Array, das die Konfiguration der Springer und Switches auf dem Baseboard darstellt.</span><span class="sxs-lookup"><span data-stu-id="a107f-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="a107f-130">Beispiel: "JP2:1-2 Cache size is 256 k, 2-3 Cache size is 512K, SW1-1: Close to off on Board Video"</span><span class="sxs-lookup"><span data-stu-id="a107f-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="a107f-131">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a107f-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-134">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a107f-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-135">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a107f-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a107f-136">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a107f-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="a107f-137">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-138">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="a107f-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-139">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="a107f-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-141">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="a107f-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-142">Die Tiefe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="a107f-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="a107f-143">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a107f-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-147">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a107f-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-148">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a107f-148">Description of the object.</span></span>

<span data-ttu-id="a107f-149">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-150">**Height**</span><span class="sxs-lookup"><span data-stu-id="a107f-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-151">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="a107f-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-153">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="a107f-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-154">Höhe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="a107f-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="a107f-155">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-156">**Hostingboard**</span><span class="sxs-lookup"><span data-stu-id="a107f-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-157">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-159">**True** gibt an, dass es sich bei der Karte um eine Platine oder ein Baseboard in einem Chassis handelt.</span><span class="sxs-lookup"><span data-stu-id="a107f-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="a107f-160">Diese Eigenschaft wird von der [**CIM- \_ Karte**](cim-card.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-161">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="a107f-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-162">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-164">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="a107f-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="a107f-165">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn es möglich ist, das Element durch ein physisch anderes, aber gleichwertiges Element zu ersetzen, während das enthaltende Paket darauf angewendet wird, während es aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="a107f-166">Beispielsweise ist ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wurde, wechselseitig austauschbar.</span><span class="sxs-lookup"><span data-stu-id="a107f-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="a107f-167">Alle Pakete, die sich im laufenden Betrieb austauschen lassen, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="a107f-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="a107f-168">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a107f-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-170">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a107f-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-172">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a107f-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-173">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a107f-173">Date and time the object was installed.</span></span> <span data-ttu-id="a107f-174">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a107f-175">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-176">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="a107f-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-179">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a107f-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-180">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="a107f-181">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-182">**Modell**</span><span class="sxs-lookup"><span data-stu-id="a107f-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-185">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a107f-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-186">Der Name, mit dem das physische Element bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="a107f-187">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-188">**Name**</span><span class="sxs-lookup"><span data-stu-id="a107f-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-191">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a107f-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-192">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-192">Label by which the object is known.</span></span> <span data-ttu-id="a107f-193">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a107f-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a107f-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a107f-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-198">Erfasst zusätzliche Daten, über die Informationen zu Asset-Tags hinaus, die verwendet werden können, um ein physisches Element zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a107f-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a107f-199">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="a107f-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="a107f-200">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar und eindeutig sind oder als Element Schlüssel verwendet werden können, ist der Eigenschafts Wert **null** , und die Barcode Daten werden als Klassen Schlüssel in der Tag-Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="a107f-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="a107f-201">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-202">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="a107f-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-205">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a107f-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-206">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="a107f-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="a107f-207">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-208">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="a107f-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-209">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-211">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="a107f-212">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-213">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="a107f-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-216">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 2 \| Product")</span><span class="sxs-lookup"><span data-stu-id="a107f-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-217">Die vom Hersteller definierte Baseboard-Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="a107f-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="a107f-218">**Ab**</span><span class="sxs-lookup"><span data-stu-id="a107f-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-221">**True** gibt an, dass ein Paket entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a107f-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="a107f-222">Ein physisches Paket ist austauschbar, wenn es so konzipiert ist, dass es in den physischen Container übernommen wird, in dem es normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="a107f-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="a107f-223">Ein Paket kann weiterhin entfernt werden, wenn die Stromversorgung zum Durchführen des Entfernens deaktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a107f-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="a107f-224">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="a107f-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="a107f-225">Beispielsweise ist ein zusätzlicher Akku in einem Laptop austauschbar, ebenso wie ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a107f-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="a107f-226">Der letztere kann jedoch auch mit einem ausgetauschten Verhalten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="a107f-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="a107f-227">Die Anzeige eines Laptops kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil.</span><span class="sxs-lookup"><span data-stu-id="a107f-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="a107f-228">Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="a107f-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="a107f-229">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-230">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="a107f-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-233">**True** gibt an, dass ein Paket ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a107f-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="a107f-234">Ein physisches Paket ist austauschbar, wenn es möglich ist, das Element durch ein physisch anderes zu ersetzen (FRU oder Upgrade).</span><span class="sxs-lookup"><span data-stu-id="a107f-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="a107f-235">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="a107f-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="a107f-236">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a107f-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="a107f-237">Ein weiteres Beispiel ist ein Stromversorgung-Paket, das auf gleitenden Schienen eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="a107f-238">Alle Wechsel Pakete sind von Natur aus austauschbar.</span><span class="sxs-lookup"><span data-stu-id="a107f-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="a107f-239">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-240">**"Requirements mentsdescription"**</span><span class="sxs-lookup"><span data-stu-id="a107f-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-243">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Karte**](cim-card.md).**Specialrequirements**")</span><span class="sxs-lookup"><span data-stu-id="a107f-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-244">Frei Form Zeichenfolge, die beschreibt, wie diese Karte physisch von anderen Karten eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="a107f-245">Die-Eigenschaft hat nur Bedeutung, wenn die entsprechende boolesche Eigenschaft **specialrequirements** auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="a107f-246">Diese Eigenschaft wird von der [**CIM- \_ Karte**](cim-card.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-247">**Requirements-Daughterboard**</span><span class="sxs-lookup"><span data-stu-id="a107f-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-248">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-250">**True** gibt an, dass mindestens eine Daughterboard-oder eine Zusatzkarte erforderlich ist, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a107f-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="a107f-251">Diese Eigenschaft wird von der [**CIM- \_ Karte**](cim-card.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-252">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a107f-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-255">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a107f-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-256">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a107f-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="a107f-257">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-258">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a107f-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-259">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-261">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a107f-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-262">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="a107f-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="a107f-263">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-264">**Slotlayout**</span><span class="sxs-lookup"><span data-stu-id="a107f-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-265">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a107f-267">Eine frei Form Zeichenfolge, die die slotposition, die typische Verwendung, die Einschränkungen, den individuellen Platz Abstand oder andere relevante Informationen für die Slots auf einer Karte beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a107f-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="a107f-268">Diese Eigenschaft wird von der [**CIM- \_ Karte**](cim-card.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-269">**Specialrequirements**</span><span class="sxs-lookup"><span data-stu-id="a107f-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-270">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-272">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Karte**](cim-card.md).**"Requirements mentsdescription**")</span><span class="sxs-lookup"><span data-stu-id="a107f-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-273">Wenn der Wert **true** ist, ist diese Karte physisch eindeutig von anderen Karten desselben Typs und erfordert daher einen speziellen Slot.</span><span class="sxs-lookup"><span data-stu-id="a107f-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="a107f-274">Beispielsweise erfordert eine doppelte Karte zwei Slots.</span><span class="sxs-lookup"><span data-stu-id="a107f-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="a107f-275">Ein weiteres Beispiel ist, wo eine bestimmte Karte für dieselbe allgemeine Funktion verwendet werden kann wie andere Karten, erfordert jedoch einen sonderslot (z. b. Extra Long), während die anderen Karten in einem beliebigen verfügbaren Slot abgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="a107f-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="a107f-276">Wenn diese Eigenschaft auf " **true**" festgelegt ist, sollte die zugehörige Eigenschaft "Requirements **mentsdescription**" die Art der Eindeutigkeit oder des Zwecks der Karte angeben.</span><span class="sxs-lookup"><span data-stu-id="a107f-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="a107f-277">Diese Eigenschaft wird von der [**CIM- \_ Karte**](cim-card.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-278">**Status**</span><span class="sxs-lookup"><span data-stu-id="a107f-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-281">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a107f-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-282">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a107f-282">Current status of the object.</span></span> <span data-ttu-id="a107f-283">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a107f-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a107f-284">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="a107f-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a107f-285">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="a107f-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a107f-286">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a107f-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a107f-287">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a107f-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a107f-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a107f-289">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a107f-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a107f-290">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a107f-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a107f-291">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a107f-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a107f-292">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a107f-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a107f-293">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a107f-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a107f-294">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a107f-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a107f-295">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a107f-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a107f-296">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a107f-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a107f-297">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a107f-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a107f-298">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a107f-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a107f-299">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a107f-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a107f-300">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a107f-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a107f-301">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a107f-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a107f-302">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a107f-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-305">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a107f-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-306">Eindeutiger Bezeichner des Baseboards des Systems.</span><span class="sxs-lookup"><span data-stu-id="a107f-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="a107f-307">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="a107f-308">Beispiel: "Base Board"</span><span class="sxs-lookup"><span data-stu-id="a107f-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="a107f-309">**Version**</span><span class="sxs-lookup"><span data-stu-id="a107f-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a107f-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-312">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a107f-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a107f-313">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="a107f-313">Version of the physical element.</span></span>

<span data-ttu-id="a107f-314">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-315">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a107f-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-316">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="a107f-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-318">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="a107f-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-319">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="a107f-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="a107f-320">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a107f-321">**Width**</span><span class="sxs-lookup"><span data-stu-id="a107f-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a107f-322">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="a107f-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a107f-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a107f-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a107f-324">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="a107f-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="a107f-325">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="a107f-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="a107f-326">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a107f-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a107f-327">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a107f-327">Remarks</span></span>

<span data-ttu-id="a107f-328">Die **Win32- \_ Baseboard** -Klasse wird von der [**CIM- \_ Karte**](cim-card.md) abgeleitet, die von [**CIM \_ physicalpackage**](cim-physicalelement.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="a107f-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a107f-329">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a107f-329">Examples</span></span>

<span data-ttu-id="a107f-330">Im Beispiel [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) perl werden Informationen zum Computer-Baseboard zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a107f-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="a107f-331">Das PowerShell-Beispiel " [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) " gibt Informationen zum Computer-Baseboard zurück.</span><span class="sxs-lookup"><span data-stu-id="a107f-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="a107f-332">Im folgenden VBScript-Beispiel werden auch Informationen zum Computer-Baseboard zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a107f-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="a107f-333">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a107f-333">Requirements</span></span>



| <span data-ttu-id="a107f-334">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a107f-334">Requirement</span></span> | <span data-ttu-id="a107f-335">Wert</span><span class="sxs-lookup"><span data-stu-id="a107f-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a107f-336">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a107f-336">Minimum supported client</span></span><br/> | <span data-ttu-id="a107f-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a107f-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a107f-338">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a107f-338">Minimum supported server</span></span><br/> | <span data-ttu-id="a107f-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a107f-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a107f-340">MOF</span><span class="sxs-lookup"><span data-stu-id="a107f-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a107f-341"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a107f-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a107f-342">DLL</span><span class="sxs-lookup"><span data-stu-id="a107f-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a107f-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a107f-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a107f-344">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a107f-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a107f-345">**CIM- \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="a107f-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="a107f-346">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a107f-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

