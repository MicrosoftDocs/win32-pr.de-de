---
description: Die CIM \_ physicalframe-Klasse ist eine übergeordnete Klasse von Rack, Chassis und anderen Frame Gehäusen, die in Erweiterungs Klassen definiert sind.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: CIM_PhysicalFrame-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127381"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="c59f9-103">CIM \_ physicalframe-Klasse</span><span class="sxs-lookup"><span data-stu-id="c59f9-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="c59f9-104">Die **CIM \_ physicalframe** -Klasse ist eine übergeordnete Klasse von Rack, Chassis und anderen Frame Gehäusen, die in Erweiterungs Klassen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c59f9-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="c59f9-105">In dieser übergeordneten Klasse sind Eigenschaften wie **visiblewecker** und **audiblealarm** sowie Daten, die sich auf Sicherheitsverletzungen beziehen, enthalten.</span><span class="sxs-lookup"><span data-stu-id="c59f9-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c59f9-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c59f9-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c59f9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c59f9-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c59f9-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c59f9-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c59f9-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59f9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c59f9-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="c59f9-111">Member</span><span class="sxs-lookup"><span data-stu-id="c59f9-111">Members</span></span>

<span data-ttu-id="c59f9-112">Die **CIM \_ physicalframe** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c59f9-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="c59f9-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="c59f9-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c59f9-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c59f9-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c59f9-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="c59f9-115">Methods</span></span>

<span data-ttu-id="c59f9-116">Die **CIM \_ physicalframe** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="c59f9-117">Methode</span><span class="sxs-lookup"><span data-stu-id="c59f9-117">Method</span></span>                                                                 | <span data-ttu-id="c59f9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c59f9-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c59f9-119">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="c59f9-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="c59f9-120">Überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c59f9-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="c59f9-121">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c59f9-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c59f9-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c59f9-122">Properties</span></span>

<span data-ttu-id="c59f9-123">Die **CIM \_ physicalframe** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c59f9-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c59f9-124">**Audiblealarm**</span><span class="sxs-lookup"><span data-stu-id="c59f9-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-125">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-127">**True** gibt an, dass der Frame mit einem hörbaren Alarm ausgestattet ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="c59f9-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-131">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ physicalframe**.**Securityverletzungs**")</span><span class="sxs-lookup"><span data-stu-id="c59f9-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-132">Eine frei Form Zeichenfolge, die weitere Informationen bereitstellt, wenn die **securityverletzungs** -Eigenschaft angibt, dass eine Sicherheitsverletzung oder ein anderes Sicherheits bezogenes Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-133">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="c59f9-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-136">Eine frei Form Zeichenfolge, die Informationen darüber enthält, wie die verschiedenen Kabel mit dem Frame verbunden und gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="c59f9-137">Dank vieler Netzwerk-, Speicher-und Netzkabel kann die Kabel Verwaltung ein komplexes und anspruchsvolles Unterfangen sein.</span><span class="sxs-lookup"><span data-stu-id="c59f9-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="c59f9-138">Diese Zeichen folgen Eigenschaft enthält Informationen, um die Assembly und den Dienst des Frames zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c59f9-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c59f9-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-142">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c59f9-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-143">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c59f9-143">Short textual description of the object.</span></span>

<span data-ttu-id="c59f9-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-145">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c59f9-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-148">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c59f9-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-149">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c59f9-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c59f9-150">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c59f9-151">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-152">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="c59f9-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-153">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="c59f9-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-155">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="c59f9-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-156">Die Tiefe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="c59f9-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="c59f9-157">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c59f9-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-161">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c59f9-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-162">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c59f9-162">Textual description of the object.</span></span>

<span data-ttu-id="c59f9-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-164">**Height**</span><span class="sxs-lookup"><span data-stu-id="c59f9-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-165">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="c59f9-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-167">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="c59f9-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-168">Höhe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="c59f9-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="c59f9-169">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-170">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="c59f9-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-171">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-173">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="c59f9-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="c59f9-174">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="c59f9-175">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="c59f9-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="c59f9-176">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="c59f9-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="c59f9-177">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c59f9-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-179">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c59f9-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-181">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c59f9-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-182">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c59f9-182">Date and time the object was installed.</span></span> <span data-ttu-id="c59f9-183">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c59f9-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-185">**Sperre vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c59f9-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-186">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-188">**True** gibt an, dass der Frame durch eine Sperre geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="c59f9-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-189">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c59f9-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-192">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c59f9-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-193">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="c59f9-194">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="c59f9-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="c59f9-195">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-196">**Modell**</span><span class="sxs-lookup"><span data-stu-id="c59f9-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-199">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c59f9-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-200">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="c59f9-201">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-202">**Name**</span><span class="sxs-lookup"><span data-stu-id="c59f9-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-205">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c59f9-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-206">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c59f9-206">Label by which the object is known.</span></span> <span data-ttu-id="c59f9-207">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c59f9-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c59f9-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-212">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c59f9-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="c59f9-213">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="c59f9-214">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="c59f9-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="c59f9-215">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-216">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="c59f9-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-219">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c59f9-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-220">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="c59f9-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="c59f9-221">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-222">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="c59f9-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-223">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-225">**True** gibt an, dass das physische Element eingeschaltet ist. Andernfalls ist Sie zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c59f9-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="c59f9-226">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-227">**Ab**</span><span class="sxs-lookup"><span data-stu-id="c59f9-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-228">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-230">**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c59f9-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="c59f9-231">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c59f9-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="c59f9-232">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="c59f9-233">Beispielsweise kann ein erweiterbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="c59f9-234">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-235">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="c59f9-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-236">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-238">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="c59f9-239">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="c59f9-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="c59f9-240">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c59f9-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="c59f9-241">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="c59f9-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="c59f9-242">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-243">**Security-Verletzung**</span><span class="sxs-lookup"><span data-stu-id="c59f9-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c59f9-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-246">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physischer DMTF- \| Container Global Table \| 002,12 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ physicalframe**.**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="c59f9-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-247">Gibt an, ob ein physischer Verstoß gegen den Frame versucht wurde, jedoch nicht erfolgreich war oder ob versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="c59f9-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c59f9-248">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c59f9-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c59f9-249">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c59f9-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="c59f9-250">**Keine Verletzung** (3)</span><span class="sxs-lookup"><span data-stu-id="c59f9-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="c59f9-251">**Versuchte Sicherheitsverletzung** (4)</span><span class="sxs-lookup"><span data-stu-id="c59f9-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="c59f9-252">**Verletzung erfolgreich** (5)</span><span class="sxs-lookup"><span data-stu-id="c59f9-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c59f9-253">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c59f9-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-256">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c59f9-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-257">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c59f9-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="c59f9-258">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-259">**Service Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="c59f9-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-260">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c59f9-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-262">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ physicalframe**.**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="c59f9-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-263">Freiform-Zeichen folgen, die ausführliche Erläuterungen zu Einträgen im **ServicePhilosophy** -Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c59f9-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="c59f9-264">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **ServicePhilosophy** -Array, das sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="c59f9-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="c59f9-265">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="c59f9-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-266">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c59f9-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-268">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ physicalframe**.**Service Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="c59f9-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-269">Gibt an, ob der Frame vom oberen Rand, von der Vorderseite, von hinten oder von der Seite bedient wird. und ob Schiebe Fächer oder Wechsel Seiten vorhanden sind, und ob der Frame beweglich ist (z. b. über Walzen).</span><span class="sxs-lookup"><span data-stu-id="c59f9-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c59f9-270">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c59f9-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c59f9-271">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c59f9-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="c59f9-272">**Dienst von oben** (2)</span><span class="sxs-lookup"><span data-stu-id="c59f9-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="c59f9-273">**Dienst von Front** (3)</span><span class="sxs-lookup"><span data-stu-id="c59f9-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="c59f9-274">**Dienst von hinten** (4)</span><span class="sxs-lookup"><span data-stu-id="c59f9-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="c59f9-275">**Dienst von Seite** (5)</span><span class="sxs-lookup"><span data-stu-id="c59f9-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="c59f9-276">**Gleitende Tabletts** (6)</span><span class="sxs-lookup"><span data-stu-id="c59f9-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="c59f9-277">Wechsel **Seiten** (7)</span><span class="sxs-lookup"><span data-stu-id="c59f9-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="c59f9-278">**Verschiebbare** (8)</span><span class="sxs-lookup"><span data-stu-id="c59f9-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c59f9-279">**SKU**</span><span class="sxs-lookup"><span data-stu-id="c59f9-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-282">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c59f9-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-283">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="c59f9-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="c59f9-284">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-285">**Status**</span><span class="sxs-lookup"><span data-stu-id="c59f9-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-288">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c59f9-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-289">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c59f9-289">Current status of the object.</span></span>

<span data-ttu-id="c59f9-290">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c59f9-291">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c59f9-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c59f9-292">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c59f9-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c59f9-293">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c59f9-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c59f9-294">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c59f9-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c59f9-295">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c59f9-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c59f9-296">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c59f9-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c59f9-297">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c59f9-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c59f9-298">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c59f9-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c59f9-299">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c59f9-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c59f9-300">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c59f9-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c59f9-301">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c59f9-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c59f9-302">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c59f9-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c59f9-303">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c59f9-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c59f9-304">**Tag**</span><span class="sxs-lookup"><span data-stu-id="c59f9-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-307">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c59f9-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-308">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="c59f9-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="c59f9-309">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="c59f9-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="c59f9-310">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware/Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c59f9-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="c59f9-311">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="c59f9-312">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c59f9-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="c59f9-313">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c59f9-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="c59f9-314">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-315">**Version**</span><span class="sxs-lookup"><span data-stu-id="c59f9-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c59f9-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-318">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c59f9-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-319">Eine Zeichenfolge, die die Version des physischen Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="c59f9-320">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-321">**Visiblealarm**</span><span class="sxs-lookup"><span data-stu-id="c59f9-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-322">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-324">**True** gibt an, dass die Ausrüstung einen sichtbaren Alarm enthält.</span><span class="sxs-lookup"><span data-stu-id="c59f9-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-325">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c59f9-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-326">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="c59f9-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-328">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="c59f9-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-329">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="c59f9-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="c59f9-330">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59f9-331">**Width**</span><span class="sxs-lookup"><span data-stu-id="c59f9-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f9-332">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="c59f9-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c59f9-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f9-334">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="c59f9-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c59f9-335">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="c59f9-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="c59f9-336">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c59f9-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c59f9-337">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59f9-337">Remarks</span></span>

<span data-ttu-id="c59f9-338">Die **CIM \_ physicalframe** -Klasse wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c59f9-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="c59f9-339">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c59f9-339">WMI does not implement this class.</span></span> <span data-ttu-id="c59f9-340">Informationen zu WMI-Klassen, die von **CIM \_ physicalframe** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c59f9-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c59f9-341">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c59f9-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c59f9-342">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c59f9-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59f9-343">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c59f9-343">Requirements</span></span>



| <span data-ttu-id="c59f9-344">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c59f9-344">Requirement</span></span> | <span data-ttu-id="c59f9-345">Wert</span><span class="sxs-lookup"><span data-stu-id="c59f9-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c59f9-346">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c59f9-346">Minimum supported client</span></span><br/> | <span data-ttu-id="c59f9-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c59f9-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c59f9-348">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c59f9-348">Minimum supported server</span></span><br/> | <span data-ttu-id="c59f9-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c59f9-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c59f9-350">Namespace</span><span class="sxs-lookup"><span data-stu-id="c59f9-350">Namespace</span></span><br/>                | <span data-ttu-id="c59f9-351">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c59f9-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c59f9-352">MOF</span><span class="sxs-lookup"><span data-stu-id="c59f9-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c59f9-353"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c59f9-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c59f9-354">DLL</span><span class="sxs-lookup"><span data-stu-id="c59f9-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c59f9-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c59f9-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59f9-356">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c59f9-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59f9-357">**CIM- \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="c59f9-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

