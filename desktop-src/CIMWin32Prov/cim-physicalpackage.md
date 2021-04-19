---
description: Die CIM \_ physicalpackage-Klasse stellt physische Elemente dar, die andere Komponenten enthalten oder hosten. Beispiele hierfür sind ein Regal Gehäuse oder eine Adapterkarte.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: CIM_PhysicalPackage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339700"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="491b5-104">CIM \_ physicalpackage-Klasse</span><span class="sxs-lookup"><span data-stu-id="491b5-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="491b5-105">Die **CIM \_ physicalpackage** -Klasse stellt physische Elemente dar, die andere Komponenten enthalten oder hosten.</span><span class="sxs-lookup"><span data-stu-id="491b5-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="491b5-106">Beispiele hierfür sind ein Regal Gehäuse oder eine Adapterkarte.</span><span class="sxs-lookup"><span data-stu-id="491b5-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="491b5-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="491b5-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="491b5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="491b5-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="491b5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="491b5-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="491b5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="491b5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="491b5-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
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
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="491b5-112">Member</span><span class="sxs-lookup"><span data-stu-id="491b5-112">Members</span></span>

<span data-ttu-id="491b5-113">Die **CIM \_ physicalpackage** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="491b5-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="491b5-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="491b5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="491b5-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="491b5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="491b5-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="491b5-116">Methods</span></span>

<span data-ttu-id="491b5-117">Die **CIM \_ physicalpackage** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="491b5-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="491b5-118">Methode</span><span class="sxs-lookup"><span data-stu-id="491b5-118">Method</span></span>                                                                   | <span data-ttu-id="491b5-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="491b5-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="491b5-120">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="491b5-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="491b5-121">Überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="491b5-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="491b5-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="491b5-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="491b5-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="491b5-123">Properties</span></span>

<span data-ttu-id="491b5-124">Die **CIM \_ physicalpackage** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="491b5-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="491b5-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="491b5-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-128">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="491b5-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-129">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="491b5-129">Short textual description of the object.</span></span>

<span data-ttu-id="491b5-130">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-131">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="491b5-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-134">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="491b5-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-135">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="491b5-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="491b5-136">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="491b5-137">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-138">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="491b5-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-139">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="491b5-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-141">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="491b5-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-142">Die Tiefe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="491b5-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="491b5-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="491b5-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-146">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="491b5-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-147">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="491b5-147">Textual description of the object.</span></span>

<span data-ttu-id="491b5-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="491b5-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-150">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="491b5-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-152">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="491b5-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-153">Höhe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="491b5-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="491b5-154">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="491b5-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-155">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="491b5-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491b5-157">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="491b5-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="491b5-158">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="491b5-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="491b5-159">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="491b5-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="491b5-160">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="491b5-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="491b5-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="491b5-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-162">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="491b5-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-164">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="491b5-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-165">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="491b5-165">Date and time the object was installed.</span></span> <span data-ttu-id="491b5-166">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="491b5-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="491b5-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-168">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="491b5-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-171">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="491b5-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-172">Der Name der Organisation, die das physische Element erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="491b5-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="491b5-173">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="491b5-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="491b5-174">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-175">**Modell**</span><span class="sxs-lookup"><span data-stu-id="491b5-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-178">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="491b5-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-179">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="491b5-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="491b5-180">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-181">**Name**</span><span class="sxs-lookup"><span data-stu-id="491b5-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-184">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="491b5-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-185">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="491b5-185">Label by which the object is known.</span></span> <span data-ttu-id="491b5-186">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="491b5-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="491b5-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491b5-191">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="491b5-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="491b5-192">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="491b5-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="491b5-193">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="491b5-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="491b5-194">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-195">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="491b5-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-198">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="491b5-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-199">Die Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="491b5-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="491b5-200">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-201">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="491b5-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-202">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="491b5-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491b5-204">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="491b5-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="491b5-205">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-206">**Ab**</span><span class="sxs-lookup"><span data-stu-id="491b5-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-207">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="491b5-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491b5-209">**True** gibt an, dass das Paket in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="491b5-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="491b5-210">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="491b5-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="491b5-211">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="491b5-212">Beispielsweise kann ein erweiterbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="491b5-213">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="491b5-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-214">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="491b5-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491b5-216">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="491b5-217">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="491b5-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="491b5-218">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="491b5-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="491b5-219">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="491b5-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="491b5-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="491b5-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-223">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="491b5-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-224">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="491b5-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="491b5-225">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="491b5-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-229">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="491b5-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-230">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="491b5-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="491b5-231">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-232">**Status**</span><span class="sxs-lookup"><span data-stu-id="491b5-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-235">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="491b5-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-236">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="491b5-236">Current status of the object.</span></span>

<span data-ttu-id="491b5-237">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="491b5-238">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="491b5-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="491b5-239">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="491b5-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="491b5-240">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="491b5-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="491b5-241">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="491b5-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="491b5-242">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="491b5-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="491b5-243">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="491b5-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="491b5-244">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="491b5-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="491b5-245">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="491b5-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="491b5-246">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="491b5-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="491b5-247">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="491b5-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="491b5-248">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="491b5-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="491b5-249">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="491b5-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="491b5-250">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="491b5-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="491b5-251">**Tag**</span><span class="sxs-lookup"><span data-stu-id="491b5-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-254">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="491b5-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-255">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="491b5-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="491b5-256">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="491b5-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="491b5-257">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="491b5-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="491b5-258">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="491b5-259">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="491b5-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="491b5-260">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="491b5-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="491b5-261">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-262">**Version**</span><span class="sxs-lookup"><span data-stu-id="491b5-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="491b5-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-265">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="491b5-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="491b5-266">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="491b5-266">Version of the physical element.</span></span>

<span data-ttu-id="491b5-267">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="491b5-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491b5-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="491b5-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-269">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="491b5-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-271">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="491b5-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-272">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="491b5-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="491b5-273">**Width**</span><span class="sxs-lookup"><span data-stu-id="491b5-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491b5-274">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="491b5-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="491b5-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="491b5-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491b5-276">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="491b5-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="491b5-277">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="491b5-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="491b5-278">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="491b5-278">Remarks</span></span>

<span data-ttu-id="491b5-279">Die **CIM \_ physicalpackage** -Klasse wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="491b5-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="491b5-280">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="491b5-280">WMI does not implement this class.</span></span> <span data-ttu-id="491b5-281">Informationen zu WMI-Klassen, die von **CIM \_ physicalpackage** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="491b5-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="491b5-282">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="491b5-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="491b5-283">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="491b5-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="491b5-284">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="491b5-284">Requirements</span></span>



| <span data-ttu-id="491b5-285">Anforderung</span><span class="sxs-lookup"><span data-stu-id="491b5-285">Requirement</span></span> | <span data-ttu-id="491b5-286">Wert</span><span class="sxs-lookup"><span data-stu-id="491b5-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="491b5-287">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="491b5-287">Minimum supported client</span></span><br/> | <span data-ttu-id="491b5-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="491b5-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="491b5-289">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="491b5-289">Minimum supported server</span></span><br/> | <span data-ttu-id="491b5-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="491b5-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="491b5-291">Namespace</span><span class="sxs-lookup"><span data-stu-id="491b5-291">Namespace</span></span><br/>                | <span data-ttu-id="491b5-292">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="491b5-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="491b5-293">MOF</span><span class="sxs-lookup"><span data-stu-id="491b5-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="491b5-294"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="491b5-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="491b5-295">DLL</span><span class="sxs-lookup"><span data-stu-id="491b5-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="491b5-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="491b5-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491b5-297">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="491b5-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491b5-298">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="491b5-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

