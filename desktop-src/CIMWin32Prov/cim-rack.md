---
description: Die CIM- \_ Rack-Klasse stellt ein Gestell (ein physischer Frame oder Gehäuse) dar, in dem das Chassis gespeichert wird. In der Regel stellt ein Rack das Gehäuse dar. Alle funktionierenden Komponenten werden in das Chassis gepackt.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: CIM_Rack-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748233"
---
# <a name="cim_rack-class"></a><span data-ttu-id="41c2d-104">CIM- \_ Rack-Klasse</span><span class="sxs-lookup"><span data-stu-id="41c2d-104">CIM\_Rack class</span></span>

<span data-ttu-id="41c2d-105">Die **CIM- \_ Rack** -Klasse stellt ein Gestell (ein physischer Frame oder Gehäuse) dar, in dem das Chassis gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="41c2d-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="41c2d-106">In der Regel stellt ein Rack das Gehäuse dar. Alle funktionierenden Komponenten werden in das Chassis gepackt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41c2d-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="41c2d-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="41c2d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="41c2d-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41c2d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="41c2d-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="41c2d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c2d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="41c2d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
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
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="41c2d-112">Member</span><span class="sxs-lookup"><span data-stu-id="41c2d-112">Members</span></span>

<span data-ttu-id="41c2d-113">Die **CIM- \_ Rack** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="41c2d-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="41c2d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="41c2d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="41c2d-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41c2d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41c2d-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="41c2d-116">Methods</span></span>

<span data-ttu-id="41c2d-117">Die **CIM- \_ Rack** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="41c2d-118">Methode</span><span class="sxs-lookup"><span data-stu-id="41c2d-118">Method</span></span>                                                        | <span data-ttu-id="41c2d-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41c2d-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41c2d-120">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="41c2d-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="41c2d-121">Überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="41c2d-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="41c2d-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="41c2d-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41c2d-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41c2d-123">Properties</span></span>

<span data-ttu-id="41c2d-124">Die **CIM- \_ Rack** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41c2d-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41c2d-125">**Audiblealarm**</span><span class="sxs-lookup"><span data-stu-id="41c2d-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-128">**True** gibt an, dass der Frame mit einem hörbaren Alarm ausgestattet ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="41c2d-129">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-130">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="41c2d-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-133">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Securityverletzungs**")</span><span class="sxs-lookup"><span data-stu-id="41c2d-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-134">Eine frei Form Zeichenfolge, die Informationen bereitstellt, wenn die **securityverletzungs** -Eigenschaft angibt, dass eine Sicherheitsverletzung oder ein anderes Sicherheits bezogenes Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="41c2d-135">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-136">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="41c2d-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-139">Eine frei Form Zeichenfolge, die Informationen darüber enthält, wie die verschiedenen Kabel mit dem Frame verbunden und gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="41c2d-140">Dank vieler Netzwerk-, Speicher-und Netzkabel kann die Kabel Verwaltung ein komplexes und anspruchsvolles Unterfangen sein.</span><span class="sxs-lookup"><span data-stu-id="41c2d-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="41c2d-141">Diese Zeichen folgen Eigenschaft enthält Informationen, um die Assembly und den Dienst des Frames zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41c2d-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="41c2d-142">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="41c2d-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-146">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="41c2d-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-147">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="41c2d-147">Short textual description of the object.</span></span>

<span data-ttu-id="41c2d-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-149">**Countrybezeichnung**</span><span class="sxs-lookup"><span data-stu-id="41c2d-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-152">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Rack**".**TypeOfRack**")</span><span class="sxs-lookup"><span data-stu-id="41c2d-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-153">Das Land oder die Region, für das das Gestell entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="41c2d-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="41c2d-154">Code Zeichenfolgen für Länder oder Regionen sind gemäß ISO/IEC 3166 definiert.</span><span class="sxs-lookup"><span data-stu-id="41c2d-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="41c2d-155">Der Rack-Typ wird in der **TypeOfRack** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="41c2d-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-156">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="41c2d-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-159">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41c2d-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-160">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41c2d-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="41c2d-161">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="41c2d-162">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-163">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="41c2d-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-164">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="41c2d-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-166">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="41c2d-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-167">Die Tiefe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="41c2d-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="41c2d-168">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41c2d-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-172">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="41c2d-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-173">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="41c2d-173">Textual description of the object.</span></span>

<span data-ttu-id="41c2d-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-175">**Height**</span><span class="sxs-lookup"><span data-stu-id="41c2d-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-176">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="41c2d-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-178">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Height"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="41c2d-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-179">Die Höhe des physischen Pakets mithilfe der Maßeinheit "U".</span><span class="sxs-lookup"><span data-stu-id="41c2d-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="41c2d-180">Ein "U" ist eine Standard Maßeinheit für die Höhe eines Rasters oder einer Regal baren Komponente und ist gleich 1,75 Zoll oder 4,445 Zentimeter.</span><span class="sxs-lookup"><span data-stu-id="41c2d-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="41c2d-181">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-182">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="41c2d-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-183">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-185">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="41c2d-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="41c2d-186">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="41c2d-187">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="41c2d-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="41c2d-188">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="41c2d-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="41c2d-189">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41c2d-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-191">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="41c2d-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-193">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="41c2d-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-194">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="41c2d-194">Date and time the object was installed.</span></span> <span data-ttu-id="41c2d-195">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="41c2d-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-197">**Sperre vorhanden**</span><span class="sxs-lookup"><span data-stu-id="41c2d-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-198">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-200">**True** gibt an, dass der Frame durch eine Sperre geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="41c2d-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="41c2d-201">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-202">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="41c2d-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-205">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41c2d-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-206">Der Name der Organisation, die das physische Element erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="41c2d-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="41c2d-207">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="41c2d-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="41c2d-208">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-209">**Modell**</span><span class="sxs-lookup"><span data-stu-id="41c2d-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-212">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="41c2d-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-213">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="41c2d-214">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-215">**Name**</span><span class="sxs-lookup"><span data-stu-id="41c2d-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-218">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="41c2d-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-219">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-219">Label by which the object is known.</span></span> <span data-ttu-id="41c2d-220">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="41c2d-221">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="41c2d-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-225">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="41c2d-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="41c2d-226">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="41c2d-227">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="41c2d-228">Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="41c2d-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="41c2d-229">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="41c2d-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-232">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41c2d-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-233">Die Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="41c2d-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="41c2d-234">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-235">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="41c2d-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-236">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-238">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="41c2d-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="41c2d-239">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-240">**Ab**</span><span class="sxs-lookup"><span data-stu-id="41c2d-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-241">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-243">**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="41c2d-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="41c2d-244">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung "Off" lauten muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="41c2d-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="41c2d-245">Wenn die Stromversorgung "on" und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="41c2d-246">Beispielsweise ist ein zusätzlicher Akku in einem Laptop austauschbar, ebenso wie ein Laufwerk, das mithilfe von SCA-Connectors eingefügt wurde. der letztere kann jedoch im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="41c2d-247">Die Anzeige eines Laptops kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil.</span><span class="sxs-lookup"><span data-stu-id="41c2d-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="41c2d-248">Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="41c2d-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="41c2d-249">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-250">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="41c2d-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-251">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-253">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="41c2d-254">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="41c2d-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="41c2d-255">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="41c2d-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="41c2d-256">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="41c2d-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="41c2d-257">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-258">**Security-Verletzung**</span><span class="sxs-lookup"><span data-stu-id="41c2d-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-259">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c2d-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-261">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physischer DMTF- \| Container Global Table \| 002,12 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="41c2d-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-262">Gibt an, ob ein physischer Verstoß gegen den Frame versucht wurde, jedoch nicht erfolgreich war oder ob versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="41c2d-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="41c2d-263">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41c2d-264">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="41c2d-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c2d-265">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="41c2d-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="41c2d-266">**Keine Verletzung** (3)</span><span class="sxs-lookup"><span data-stu-id="41c2d-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="41c2d-267">**Versuchte Sicherheitsverletzung** (4)</span><span class="sxs-lookup"><span data-stu-id="41c2d-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="41c2d-268">**Verletzung erfolgreich** (5)</span><span class="sxs-lookup"><span data-stu-id="41c2d-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c2d-269">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="41c2d-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-272">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="41c2d-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-273">Vom Hersteller zugewiesene Nummer, die zum Identifizieren des Racks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41c2d-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="41c2d-274">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-275">**Service Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="41c2d-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-276">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41c2d-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-278">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="41c2d-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-279">Freiform-Zeichen folgen, die ausführliche Erläuterungen zu Einträgen im **ServicePhilosophy** -Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="41c2d-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="41c2d-280">Beachten Sie, dass jeder Eintrag des Arrays mit dem Eintrag in **ServicePhilosophy** verknüpft ist, der sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="41c2d-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="41c2d-281">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-282">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="41c2d-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-283">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="41c2d-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-285">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Service Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="41c2d-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-286">Gibt an, ob der Frame vom oberen Rand, von der Vorderseite, von hinten oder von der Seite bedient wird. und ob Schiebe Fächer oder Wechsel Seiten vorhanden sind, und ob der Frame beweglich ist (z. b. über Walzen).</span><span class="sxs-lookup"><span data-stu-id="41c2d-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="41c2d-287">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c2d-288">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="41c2d-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41c2d-289">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="41c2d-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="41c2d-290">**Dienst von oben** (2)</span><span class="sxs-lookup"><span data-stu-id="41c2d-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="41c2d-291">**Dienst von Front** (3)</span><span class="sxs-lookup"><span data-stu-id="41c2d-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="41c2d-292">**Dienst von hinten** (4)</span><span class="sxs-lookup"><span data-stu-id="41c2d-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="41c2d-293">**Dienst von Seite** (5)</span><span class="sxs-lookup"><span data-stu-id="41c2d-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="41c2d-294">**Gleitende Tabletts** (6)</span><span class="sxs-lookup"><span data-stu-id="41c2d-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="41c2d-295">Wechsel **Seiten** (7)</span><span class="sxs-lookup"><span data-stu-id="41c2d-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="41c2d-296">**Verschiebbare** (8)</span><span class="sxs-lookup"><span data-stu-id="41c2d-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c2d-297">**SKU**</span><span class="sxs-lookup"><span data-stu-id="41c2d-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-300">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="41c2d-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-301">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="41c2d-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="41c2d-302">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-303">**Status**</span><span class="sxs-lookup"><span data-stu-id="41c2d-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-306">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="41c2d-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-307">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="41c2d-307">Current status of the object.</span></span> <span data-ttu-id="41c2d-308">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="41c2d-309">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="41c2d-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="41c2d-310">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="41c2d-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="41c2d-311">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="41c2d-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41c2d-312">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="41c2d-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c2d-313">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="41c2d-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="41c2d-314">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="41c2d-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="41c2d-315">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="41c2d-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="41c2d-316">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="41c2d-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="41c2d-317">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="41c2d-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="41c2d-318">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="41c2d-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="41c2d-319">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="41c2d-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="41c2d-320">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="41c2d-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="41c2d-321">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="41c2d-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c2d-322">**Tag**</span><span class="sxs-lookup"><span data-stu-id="41c2d-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-325">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41c2d-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-326">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="41c2d-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="41c2d-327">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="41c2d-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="41c2d-328">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="41c2d-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="41c2d-329">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="41c2d-330">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="41c2d-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="41c2d-331">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="41c2d-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="41c2d-332">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-333">**TypeOfRack**</span><span class="sxs-lookup"><span data-stu-id="41c2d-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-334">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c2d-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-336">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Rack**".**Countrybezeichnung**")</span><span class="sxs-lookup"><span data-stu-id="41c2d-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-337">Der Typ des Racks.</span><span class="sxs-lookup"><span data-stu-id="41c2d-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c2d-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="41c2d-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="41c2d-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Zoll** (1)</span><span class="sxs-lookup"><span data-stu-id="41c2d-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="41c2d-340">Standard 19 Zoll</span><span class="sxs-lookup"><span data-stu-id="41c2d-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="41c2d-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span><span class="sxs-lookup"><span data-stu-id="41c2d-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="41c2d-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Geräte Regal** (3)</span><span class="sxs-lookup"><span data-stu-id="41c2d-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="41c2d-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Nicht Standard** (4)</span><span class="sxs-lookup"><span data-stu-id="41c2d-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c2d-344">**Version**</span><span class="sxs-lookup"><span data-stu-id="41c2d-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41c2d-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-347">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="41c2d-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-348">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="41c2d-348">Version of the physical element.</span></span>

<span data-ttu-id="41c2d-349">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-350">**Visiblealarm**</span><span class="sxs-lookup"><span data-stu-id="41c2d-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-351">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-353">**True** gibt an, dass die Ausrüstung einen sichtbaren Alarm enthält.</span><span class="sxs-lookup"><span data-stu-id="41c2d-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="41c2d-354">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-355">**Weight**</span><span class="sxs-lookup"><span data-stu-id="41c2d-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-356">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="41c2d-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-358">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="41c2d-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-359">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="41c2d-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="41c2d-360">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c2d-361">**Width**</span><span class="sxs-lookup"><span data-stu-id="41c2d-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c2d-362">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="41c2d-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41c2d-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c2d-364">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="41c2d-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="41c2d-365">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="41c2d-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="41c2d-366">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41c2d-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c2d-367">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41c2d-367">Remarks</span></span>

<span data-ttu-id="41c2d-368">Die **CIM- \_ Rack** -Klasse wird von [**CIM \_ physicalframe**](cim-physicalframe.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="41c2d-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="41c2d-369">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="41c2d-369">WMI does not implement this class.</span></span>

<span data-ttu-id="41c2d-370">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="41c2d-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="41c2d-371">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="41c2d-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c2d-372">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41c2d-372">Requirements</span></span>



| <span data-ttu-id="41c2d-373">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41c2d-373">Requirement</span></span> | <span data-ttu-id="41c2d-374">Wert</span><span class="sxs-lookup"><span data-stu-id="41c2d-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c2d-375">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41c2d-375">Minimum supported client</span></span><br/> | <span data-ttu-id="41c2d-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41c2d-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41c2d-377">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41c2d-377">Minimum supported server</span></span><br/> | <span data-ttu-id="41c2d-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41c2d-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41c2d-379">Namespace</span><span class="sxs-lookup"><span data-stu-id="41c2d-379">Namespace</span></span><br/>                | <span data-ttu-id="41c2d-380">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41c2d-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41c2d-381">MOF</span><span class="sxs-lookup"><span data-stu-id="41c2d-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41c2d-382"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="41c2d-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41c2d-383">DLL</span><span class="sxs-lookup"><span data-stu-id="41c2d-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c2d-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c2d-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c2d-385">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41c2d-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c2d-386">**CIM- \_ physicalframe**</span><span class="sxs-lookup"><span data-stu-id="41c2d-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

