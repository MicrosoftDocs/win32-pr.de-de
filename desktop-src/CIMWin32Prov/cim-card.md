---
description: Die CIM- \_ Karten Klasse stellt einen Typ von physischem Container dar, der an eine andere Karte oder ein hostingboard angeschlossen werden kann oder selbst ein hostingboard/-Motherboard in einem Chassis ist.
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: CIM_Card-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339694"
---
# <a name="cim_card-class"></a><span data-ttu-id="d8ed7-103">CIM- \_ Karten Klasse</span><span class="sxs-lookup"><span data-stu-id="d8ed7-103">CIM\_Card class</span></span>

<span data-ttu-id="d8ed7-104">Die **CIM- \_ Karten** Klasse stellt einen Typ von physischem Container dar, der an eine andere Karte oder ein hostingboard angeschlossen werden kann oder selbst ein hostingboard/-Motherboard in einem Chassis ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="d8ed7-105">Diese Klasse enthält alle Pakete, die Signale ausführen können und einen Bereitstellungs Punkt für physische Komponenten bereitstellen, wie z. b. Chips oder andere physische Pakete, wie z. b. andere Karten.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8ed7-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d8ed7-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d8ed7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d8ed7-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d8ed7-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ed7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8ed7-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="d8ed7-111">Member</span><span class="sxs-lookup"><span data-stu-id="d8ed7-111">Members</span></span>

<span data-ttu-id="d8ed7-112">Die **CIM- \_ Karten** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8ed7-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="d8ed7-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8ed7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="d8ed7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8ed7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d8ed7-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8ed7-115">Methods</span></span>

<span data-ttu-id="d8ed7-116">Die **CIM- \_ Karten** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="d8ed7-117">Methode</span><span class="sxs-lookup"><span data-stu-id="d8ed7-117">Method</span></span>                                                        | <span data-ttu-id="d8ed7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8ed7-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8ed7-119">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="d8ed7-120">Überprüft, ob das physische Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="d8ed7-121">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d8ed7-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8ed7-122">Properties</span></span>

<span data-ttu-id="d8ed7-123">Die **CIM- \_ Karten** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8ed7-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-127">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-128">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-128">A short textual description of the object.</span></span>

<span data-ttu-id="d8ed7-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-130">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-133">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-134">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d8ed7-135">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d8ed7-136">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-137">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-138">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-140">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-141">Die Tiefe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="d8ed7-142">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-146">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-147">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-147">A textual description of the object.</span></span>

<span data-ttu-id="d8ed7-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-150">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-152">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-153">Höhe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="d8ed7-154">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-155">**Hostingboard**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-156">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-158">Wenn der Wert **true** ist, ist diese Karte eine Platine oder, generisch, ein Baseboard in einem Gehäuse.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-159">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-160">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-162">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="d8ed7-163">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="d8ed7-164">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="d8ed7-165">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="d8ed7-166">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-168">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-170">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-171">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-171">Indicates when the object was installed.</span></span> <span data-ttu-id="d8ed7-172">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d8ed7-173">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-174">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-177">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-178">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="d8ed7-179">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d8ed7-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="d8ed7-180">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-181">**Modell**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-184">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-185">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="d8ed7-186">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-187">**Name**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-190">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-191">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-191">Label by which the object is known.</span></span> <span data-ttu-id="d8ed7-192">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d8ed7-193">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-197">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="d8ed7-198">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="d8ed7-199">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="d8ed7-200">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-201">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-204">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-205">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="d8ed7-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="d8ed7-206">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-207">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-208">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-210">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="d8ed7-211">Andernfalls ist Sie zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="d8ed7-212">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-213">**Ab**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-214">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-216">**True** gibt an, dass das Paket in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="d8ed7-217">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="d8ed7-218">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="d8ed7-219">Beispielsweise kann ein erweiterbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="d8ed7-220">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-221">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-222">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-224">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="d8ed7-225">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="d8ed7-226">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="d8ed7-227">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="d8ed7-228">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-229">**"Requirements mentsdescription"**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-232">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Karte**.**Specialrequirements**")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-233">Eine frei Form Zeichenfolge, die beschreibt, wie die Karte physisch von anderen Karten eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="d8ed7-234">Diese Eigenschaft hat nur Bedeutung, wenn die entsprechende boolesche Eigenschaft **specialrequirements** auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-235">**Requirements-Daughterboard**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-236">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-238">Wenn **true**, ist mindestens eine Daughterboard-oder eine Zusatzkarte erforderlich, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-239">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-242">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-243">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d8ed7-244">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-245">**SKU**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-248">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-249">Die Stock Keeping Unit-Nummer für dieses physische Element.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="d8ed7-250">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-251">**Slotlayout**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-254">Frei Form Zeichenfolge, die die slotpositionierung, die typische Verwendung, Einschränkungen, einzelne Slot-Abstände oder andere relevante Informationen für die Slots auf einer Karte beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-255">**Specialrequirements**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-256">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-258">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Karte**.**"Requirements mentsdescription**")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-259">**True** gibt an, dass die Karte physisch von anderen Karten desselben Typs eindeutig ist und daher einen speziellen Slot erfordert.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="d8ed7-260">Beispielsweise erfordert eine doppelte Karte zwei Slots.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="d8ed7-261">Ein weiteres Beispiel ist eine bestimmte Karte, die für dieselbe allgemeine Funktion verwendet werden kann wie andere Karten, erfordert jedoch einen sonderslot (z. b. "Extra Long"); andere Karten können dagegen in einem beliebigen verfügbaren Slot abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="d8ed7-262">**True** gibt an, dass die entsprechende Eigenschaft "Requirements **mentsdescription** " die Art der Eindeutigkeit oder des Zwecks der Karte angeben soll.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-263">**Status**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-266">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-267">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="d8ed7-268">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d8ed7-269">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d8ed7-270">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="d8ed7-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d8ed7-271">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d8ed7-272">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d8ed7-273">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d8ed7-274">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d8ed7-275">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="d8ed7-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d8ed7-276">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d8ed7-277">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d8ed7-278">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8ed7-279">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d8ed7-280">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d8ed7-281">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d8ed7-282">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d8ed7-283">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d8ed7-284">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d8ed7-285">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d8ed7-286">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d8ed7-287">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8ed7-288">**Tag**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-291">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-292">Identifiziert das physische Element eindeutig und fungiert als Schlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="d8ed7-293">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="d8ed7-294">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="d8ed7-295">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="d8ed7-296">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="d8ed7-297">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="d8ed7-298">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-299">**Version**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-302">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-303">Gibt die Version des physischen Elements an.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="d8ed7-304">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-305">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-306">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-308">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-309">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="d8ed7-310">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ed7-311">**Width**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ed7-312">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8ed7-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ed7-314">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="d8ed7-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d8ed7-315">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="d8ed7-316">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8ed7-317">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8ed7-317">Remarks</span></span>

<span data-ttu-id="d8ed7-318">Die **CIM- \_ Karten** Klasse wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="d8ed7-319">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-319">WMI does not implement this class.</span></span> <span data-ttu-id="d8ed7-320">Weitere Informationen über von der CIM- **\_ Karte** abgeleitete Klassen finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d8ed7-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d8ed7-321">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d8ed7-322">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8ed7-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ed7-323">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8ed7-323">Requirements</span></span>



| <span data-ttu-id="d8ed7-324">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8ed7-324">Requirement</span></span> | <span data-ttu-id="d8ed7-325">Wert</span><span class="sxs-lookup"><span data-stu-id="d8ed7-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ed7-326">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-326">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ed7-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8ed7-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8ed7-328">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8ed7-328">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ed7-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8ed7-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8ed7-330">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8ed7-330">Namespace</span></span><br/>                | <span data-ttu-id="d8ed7-331">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d8ed7-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8ed7-332">MOF</span><span class="sxs-lookup"><span data-stu-id="d8ed7-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8ed7-333"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d8ed7-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8ed7-334">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ed7-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ed7-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ed7-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ed7-336">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8ed7-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ed7-337">**CIM- \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="d8ed7-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

