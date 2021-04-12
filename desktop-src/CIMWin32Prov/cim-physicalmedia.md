---
description: Die CIM \_ physicalmedia-Klasse stellt Typen von Dokumentation und Speichermedium (z. b. Bänder, CD-ROMs usw.) dar.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: CIM_PhysicalMedia-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104219020"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="599c5-103">CIM \_ physicalmedia-Klasse</span><span class="sxs-lookup"><span data-stu-id="599c5-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="599c5-104">Die **CIM \_ physicalmedia** -Klasse stellt Typen von Dokumentation und Speichermedium (z. b. Bänder, CD-ROMs usw.) dar.</span><span class="sxs-lookup"><span data-stu-id="599c5-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="599c5-105">Diese Klasse wird in der Regel zum Suchen und Verwalten von Wechselmedien (im Gegensatz zu Medien, die mit dem Medien Zugriffsgerät versiegelt sind, als ein einzelnes Paket, z. b. Festplatten)</span><span class="sxs-lookup"><span data-stu-id="599c5-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="599c5-106">Versiegelte Medien können jedoch auch mit dieser Klasse modelliert werden, wenn das Medium mithilfe der [**CIM \_ packagedcomponent**](cim-packagedcomponent.md) -Beziehung dem physischen Paket zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="599c5-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="599c5-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="599c5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="599c5-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="599c5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="599c5-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="599c5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="599c5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="599c5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
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
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="599c5-112">Member</span><span class="sxs-lookup"><span data-stu-id="599c5-112">Members</span></span>

<span data-ttu-id="599c5-113">Die **CIM \_ physicalmedia** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="599c5-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="599c5-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="599c5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="599c5-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="599c5-115">Properties</span></span>

<span data-ttu-id="599c5-116">Die **CIM \_ physicalmedia** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="599c5-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="599c5-117">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="599c5-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-118">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="599c5-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-120">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="599c5-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-121">Anzahl von Bytes, die von einem Medium gelesen oder geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="599c5-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="599c5-122">Diese Eigenschaft ist nicht auf die Festplatten Kopie (Dokumentation) oder das Reinigungsmedium anwendbar.</span><span class="sxs-lookup"><span data-stu-id="599c5-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="599c5-123">Die Datenkomprimierung sollte nicht angenommen werden, da Sie den Wert in dieser Eigenschaft erhöhen würde.</span><span class="sxs-lookup"><span data-stu-id="599c5-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="599c5-124">Bei Bändern sollte davon ausgegangen werden, dass keine Datei Markierungen oder Leerraum Bereiche auf den Medien aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="599c5-125">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="599c5-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="599c5-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="599c5-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-130">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="599c5-130">Short textual description of the object.</span></span>

<span data-ttu-id="599c5-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-132">**Cleanermedia**</span><span class="sxs-lookup"><span data-stu-id="599c5-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-135">**True** gibt an, dass die physischen Medien zu Reinigungszwecken und nicht als Datenspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="599c5-136">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="599c5-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-139">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="599c5-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-140">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="599c5-141">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="599c5-142">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="599c5-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-146">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="599c5-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-147">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="599c5-147">Textual description of the object.</span></span>

<span data-ttu-id="599c5-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-149">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="599c5-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-150">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-152">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="599c5-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="599c5-153">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="599c5-154">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="599c5-155">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="599c5-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="599c5-156">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="599c5-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-158">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="599c5-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-160">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="599c5-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-161">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="599c5-161">Date and time the object was installed.</span></span> <span data-ttu-id="599c5-162">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="599c5-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-164">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="599c5-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-167">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="599c5-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-168">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="599c5-169">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="599c5-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="599c5-170">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="599c5-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-174">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ physicalmedia**".**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="599c5-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-175">Weitere Details im Zusammenhang mit der **mediaType** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="599c5-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="599c5-176">Wenn z. b. Value 3 ("QIC Cartridge") angegeben wird, gibt diese Eigenschaft an, ob das Band breit oder 1/4 Zoll ist, vorformatiert, mit einem Wert kompatibel ist usw.</span><span class="sxs-lookup"><span data-stu-id="599c5-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="599c5-177">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="599c5-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="599c5-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-180">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ physicalmedia**".**Mediadeabo**")</span><span class="sxs-lookup"><span data-stu-id="599c5-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-181">Typ des physischen Mediums.</span><span class="sxs-lookup"><span data-stu-id="599c5-181">Type of physical media.</span></span> <span data-ttu-id="599c5-182">Die **mediadedie** -Eigenschaft bietet eine explizite Definition des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="599c5-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="599c5-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="599c5-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="599c5-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="599c5-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="599c5-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Band-Cartridge** (2)</span><span class="sxs-lookup"><span data-stu-id="599c5-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="599c5-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC-Cartridge** (3)</span><span class="sxs-lookup"><span data-stu-id="599c5-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="599c5-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT-Cartridge** (4)</span><span class="sxs-lookup"><span data-stu-id="599c5-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="599c5-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF-Cartridge** (5)</span><span class="sxs-lookup"><span data-stu-id="599c5-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="599c5-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT-Cartridge** (6)</span><span class="sxs-lookup"><span data-stu-id="599c5-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="599c5-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8-mm-bandcartridge** (7)</span><span class="sxs-lookup"><span data-stu-id="599c5-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="599c5-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19-mm-bandcartridge** (8)</span><span class="sxs-lookup"><span data-stu-id="599c5-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="599c5-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT-Cartridge** (9)</span><span class="sxs-lookup"><span data-stu-id="599c5-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="599c5-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Halbzoll-Magnet bandcartridge** (10)</span><span class="sxs-lookup"><span data-stu-id="599c5-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="599c5-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Patronen** Datenträger (11)</span><span class="sxs-lookup"><span data-stu-id="599c5-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="599c5-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Jaz** -Datenträger (12)</span><span class="sxs-lookup"><span data-stu-id="599c5-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="599c5-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP-Festplatte** (13)</span><span class="sxs-lookup"><span data-stu-id="599c5-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="599c5-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Syquest** -Datenträger (14)</span><span class="sxs-lookup"><span data-stu-id="599c5-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="599c5-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>Wechsel Datenträger von **Winchester** (15)</span><span class="sxs-lookup"><span data-stu-id="599c5-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="599c5-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="599c5-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="599c5-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="599c5-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="599c5-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="599c5-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="599c5-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD-Recordable** (19)</span><span class="sxs-lookup"><span data-stu-id="599c5-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="599c5-203"><span id="WORM"></span><span id="worm"></span>**Wurm** (20)</span><span class="sxs-lookup"><span data-stu-id="599c5-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="599c5-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span><span class="sxs-lookup"><span data-stu-id="599c5-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="599c5-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="599c5-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="599c5-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)</span><span class="sxs-lookup"><span data-stu-id="599c5-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="599c5-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="599c5-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="599c5-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="599c5-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="599c5-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span><span class="sxs-lookup"><span data-stu-id="599c5-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="599c5-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**MPEG** (27)</span><span class="sxs-lookup"><span data-stu-id="599c5-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="599c5-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Diskette/Diskette** (28)</span><span class="sxs-lookup"><span data-stu-id="599c5-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-212">Diskette</span><span class="sxs-lookup"><span data-stu-id="599c5-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="599c5-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Festplatte** (29)</span><span class="sxs-lookup"><span data-stu-id="599c5-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="599c5-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Speicherkarte** (30)</span><span class="sxs-lookup"><span data-stu-id="599c5-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="599c5-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Harte Kopie** (31)</span><span class="sxs-lookup"><span data-stu-id="599c5-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="599c5-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik** -Datenträger (32)</span><span class="sxs-lookup"><span data-stu-id="599c5-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="599c5-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="599c5-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="599c5-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="599c5-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="599c5-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="599c5-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="599c5-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD-Recordable** (36)</span><span class="sxs-lookup"><span data-stu-id="599c5-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="599c5-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="599c5-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="599c5-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audiodaten** (38)</span><span class="sxs-lookup"><span data-stu-id="599c5-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="599c5-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="599c5-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="599c5-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="599c5-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="599c5-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="599c5-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="599c5-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="599c5-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="599c5-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>" **Magneto-Optical Rewrite able** " (43)</span><span class="sxs-lookup"><span data-stu-id="599c5-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="599c5-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Ein-optischer-Schreibvorgang einmal** (44)</span><span class="sxs-lookup"><span data-stu-id="599c5-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="599c5-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>" **Magneto-Optical Rewrite able" (LIMDOW)** (45)</span><span class="sxs-lookup"><span data-stu-id="599c5-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="599c5-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Änderung einmal schreiben** (46)</span><span class="sxs-lookup"><span data-stu-id="599c5-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="599c5-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Neuschreibbarkeit von Phasen Änderungen** (47)</span><span class="sxs-lookup"><span data-stu-id="599c5-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="599c5-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phasenänderung Dual reschreibbar** (48)</span><span class="sxs-lookup"><span data-stu-id="599c5-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="599c5-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablativer Schreibvorgang einmal** (49)</span><span class="sxs-lookup"><span data-stu-id="599c5-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="599c5-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near-Feld Aufzeichnung** (50)</span><span class="sxs-lookup"><span data-stu-id="599c5-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="599c5-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQIC** (51)</span><span class="sxs-lookup"><span data-stu-id="599c5-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="599c5-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span><span class="sxs-lookup"><span data-stu-id="599c5-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="599c5-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm-Metal-Partikel** (53)</span><span class="sxs-lookup"><span data-stu-id="599c5-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="599c5-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal verdampate** (54)</span><span class="sxs-lookup"><span data-stu-id="599c5-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="599c5-239"><span id="NCTP"></span><span id="nctp"></span>**Nctp** (55)</span><span class="sxs-lookup"><span data-stu-id="599c5-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="599c5-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO ultrum** (56)</span><span class="sxs-lookup"><span data-stu-id="599c5-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="599c5-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO-Accelis** (57)</span><span class="sxs-lookup"><span data-stu-id="599c5-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="599c5-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Nachverfolgung des Bands** (58)</span><span class="sxs-lookup"><span data-stu-id="599c5-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-243">9: Nachverfolgung des Bands</span><span class="sxs-lookup"><span data-stu-id="599c5-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="599c5-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Nachverfolgung des Bands** (59)</span><span class="sxs-lookup"><span data-stu-id="599c5-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-245">18. Nachverfolgen des Bands</span><span class="sxs-lookup"><span data-stu-id="599c5-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="599c5-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36-Track-Band** (60)</span><span class="sxs-lookup"><span data-stu-id="599c5-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-247">36-Band Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="599c5-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="599c5-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span><span class="sxs-lookup"><span data-stu-id="599c5-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="599c5-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span><span class="sxs-lookup"><span data-stu-id="599c5-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="599c5-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2-Band** (63)</span><span class="sxs-lookup"><span data-stu-id="599c5-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="599c5-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape-DST Small** (64)</span><span class="sxs-lookup"><span data-stu-id="599c5-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-252">Band-DST Klein</span><span class="sxs-lookup"><span data-stu-id="599c5-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="599c5-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Band-DST-Mittel** (65)</span><span class="sxs-lookup"><span data-stu-id="599c5-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-254">Band-DST-Medium</span><span class="sxs-lookup"><span data-stu-id="599c5-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="599c5-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Band-DST groß** (66)</span><span class="sxs-lookup"><span data-stu-id="599c5-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="599c5-256">Band-DST groß</span><span class="sxs-lookup"><span data-stu-id="599c5-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="599c5-257">**Modell**</span><span class="sxs-lookup"><span data-stu-id="599c5-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-260">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="599c5-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-261">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="599c5-262">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-263">**Name**</span><span class="sxs-lookup"><span data-stu-id="599c5-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-266">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="599c5-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-267">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-267">Label by which the object is known.</span></span> <span data-ttu-id="599c5-268">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="599c5-269">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="599c5-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-273">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="599c5-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="599c5-274">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="599c5-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="599c5-275">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="599c5-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="599c5-276">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-277">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="599c5-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-280">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="599c5-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-281">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="599c5-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="599c5-282">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-283">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="599c5-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-284">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-286">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="599c5-287">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-288">**Ab**</span><span class="sxs-lookup"><span data-stu-id="599c5-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-289">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-291">**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="599c5-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="599c5-292">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="599c5-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="599c5-293">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="599c5-294">Beispielsweise kann ein nicht Abzieh barer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="599c5-295">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-296">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="599c5-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-297">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-299">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="599c5-300">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="599c5-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="599c5-301">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="599c5-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="599c5-302">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="599c5-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="599c5-303">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-304">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="599c5-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-307">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="599c5-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-308">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="599c5-309">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-310">**SKU**</span><span class="sxs-lookup"><span data-stu-id="599c5-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-313">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="599c5-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-314">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="599c5-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="599c5-315">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-316">**Status**</span><span class="sxs-lookup"><span data-stu-id="599c5-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-319">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="599c5-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="599c5-320">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="599c5-320">Current status of the object.</span></span>

<span data-ttu-id="599c5-321">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="599c5-322">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="599c5-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="599c5-323">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="599c5-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="599c5-324">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="599c5-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="599c5-325">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="599c5-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="599c5-326">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="599c5-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="599c5-327">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="599c5-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="599c5-328">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="599c5-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="599c5-329">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="599c5-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="599c5-330">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="599c5-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="599c5-331">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="599c5-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="599c5-332">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="599c5-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="599c5-333">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="599c5-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="599c5-334">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="599c5-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="599c5-335">**Tag**</span><span class="sxs-lookup"><span data-stu-id="599c5-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-338">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="599c5-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-339">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="599c5-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="599c5-340">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="599c5-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="599c5-341">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="599c5-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="599c5-342">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="599c5-343">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="599c5-344">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="599c5-345">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-346">**Version**</span><span class="sxs-lookup"><span data-stu-id="599c5-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="599c5-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599c5-349">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="599c5-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="599c5-350">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="599c5-350">Version of the physical element.</span></span>

<span data-ttu-id="599c5-351">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="599c5-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="599c5-352">**Schreibgeschützten Ton**</span><span class="sxs-lookup"><span data-stu-id="599c5-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599c5-353">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="599c5-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="599c5-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599c5-355">**True** gibt an, dass das Medium zurzeit durch einen physischen Mechanismus, z. b. eine Registerkarte schützen auf einer Diskette, geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="599c5-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="599c5-356">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="599c5-356">Remarks</span></span>

<span data-ttu-id="599c5-357">Die **CIM \_ physicalmedia** -Klasse wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="599c5-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="599c5-358">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="599c5-358">WMI does not implement this class.</span></span>

<span data-ttu-id="599c5-359">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="599c5-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="599c5-360">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="599c5-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="599c5-361">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="599c5-361">Requirements</span></span>



| <span data-ttu-id="599c5-362">Anforderung</span><span class="sxs-lookup"><span data-stu-id="599c5-362">Requirement</span></span> | <span data-ttu-id="599c5-363">Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="599c5-364">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="599c5-364">Minimum supported client</span></span><br/> | <span data-ttu-id="599c5-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="599c5-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="599c5-366">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="599c5-366">Minimum supported server</span></span><br/> | <span data-ttu-id="599c5-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="599c5-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="599c5-368">Namespace</span><span class="sxs-lookup"><span data-stu-id="599c5-368">Namespace</span></span><br/>                | <span data-ttu-id="599c5-369">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="599c5-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="599c5-370">MOF</span><span class="sxs-lookup"><span data-stu-id="599c5-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="599c5-371"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="599c5-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="599c5-372">DLL</span><span class="sxs-lookup"><span data-stu-id="599c5-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599c5-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599c5-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="599c5-374">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="599c5-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599c5-375">**CIM- \_ physicalcomponent**</span><span class="sxs-lookup"><span data-stu-id="599c5-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

