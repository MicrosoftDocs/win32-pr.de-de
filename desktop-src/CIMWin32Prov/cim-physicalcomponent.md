---
description: Die CIM \_ physicalcomponent-Klasse stellt eine Komponente auf niedriger Ebene oder eine grundlegende Komponente innerhalb eines Pakets dar. Ein physisches Element, bei dem es sich nicht um einen Link, einen Connector oder ein Paket handelt, ist ein Nachfolger (oder Member) dieser Klasse.
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: CIM_PhysicalComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483523"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="261f5-104">CIM \_ physicalcomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="261f5-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="261f5-105">Die **CIM \_ physicalcomponent** -Klasse stellt eine Komponente auf niedriger Ebene oder eine grundlegende Komponente innerhalb eines Pakets dar.</span><span class="sxs-lookup"><span data-stu-id="261f5-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="261f5-106">Ein physisches Element, bei dem es sich nicht um einen Link, einen Connector oder ein Paket handelt, ist ein Nachfolger (oder Member) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="261f5-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="261f5-107">Beispielsweise wäre das UART-Chipsatz auf einer internen Modem Karte eine Unterklasse (wenn zusätzliche Eigenschaften oder Zuordnungen definiert sind) oder eine Instanz von **CIM \_ physicalcomponent**.</span><span class="sxs-lookup"><span data-stu-id="261f5-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="261f5-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="261f5-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="261f5-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="261f5-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="261f5-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="261f5-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="261f5-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="261f5-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="261f5-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
};
```

## <a name="members"></a><span data-ttu-id="261f5-113">Member</span><span class="sxs-lookup"><span data-stu-id="261f5-113">Members</span></span>

<span data-ttu-id="261f5-114">Die **CIM \_ physicalcomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="261f5-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="261f5-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="261f5-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="261f5-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="261f5-116">Properties</span></span>

<span data-ttu-id="261f5-117">Die **CIM \_ physicalcomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="261f5-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="261f5-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="261f5-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="261f5-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="261f5-122">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="261f5-122">A short textual description of the object.</span></span>

<span data-ttu-id="261f5-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-124">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="261f5-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-127">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="261f5-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-128">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="261f5-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="261f5-129">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="261f5-130">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="261f5-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-134">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="261f5-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="261f5-135">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="261f5-135">A textual description of the object.</span></span>

<span data-ttu-id="261f5-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-137">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="261f5-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="261f5-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="261f5-140">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="261f5-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="261f5-141">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="261f5-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="261f5-142">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="261f5-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="261f5-143">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="261f5-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="261f5-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="261f5-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-145">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="261f5-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-147">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="261f5-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="261f5-148">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="261f5-148">Indicates when the object was installed.</span></span> <span data-ttu-id="261f5-149">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="261f5-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="261f5-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-151">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="261f5-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-154">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="261f5-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-155">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="261f5-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="261f5-156">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="261f5-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="261f5-157">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-158">**Modell**</span><span class="sxs-lookup"><span data-stu-id="261f5-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-161">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="261f5-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-162">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="261f5-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="261f5-163">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-164">**Name**</span><span class="sxs-lookup"><span data-stu-id="261f5-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-167">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="261f5-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="261f5-168">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="261f5-168">Label by which the object is known.</span></span> <span data-ttu-id="261f5-169">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="261f5-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="261f5-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="261f5-174">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="261f5-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="261f5-175">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="261f5-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="261f5-176">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="261f5-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="261f5-177">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-178">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="261f5-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-181">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="261f5-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-182">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="261f5-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="261f5-183">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-184">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="261f5-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-185">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="261f5-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="261f5-187">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="261f5-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="261f5-188">Andernfalls ist Sie zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="261f5-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="261f5-189">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-190">**Ab**</span><span class="sxs-lookup"><span data-stu-id="261f5-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-191">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="261f5-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="261f5-193">**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="261f5-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="261f5-194">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="261f5-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="261f5-195">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="261f5-196">Beispielsweise kann ein erweiterbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="261f5-197">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="261f5-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-198">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="261f5-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="261f5-200">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="261f5-201">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="261f5-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="261f5-202">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="261f5-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="261f5-203">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="261f5-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="261f5-204">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="261f5-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-207">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="261f5-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-208">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="261f5-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="261f5-209">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-210">**SKU**</span><span class="sxs-lookup"><span data-stu-id="261f5-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-213">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="261f5-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-214">Die Stock Keeping Unit-Nummer für dieses physische Element.</span><span class="sxs-lookup"><span data-stu-id="261f5-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="261f5-215">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-216">**Status**</span><span class="sxs-lookup"><span data-stu-id="261f5-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-219">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="261f5-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="261f5-220">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="261f5-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="261f5-221">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="261f5-222">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="261f5-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="261f5-223">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="261f5-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="261f5-224">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="261f5-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="261f5-225">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="261f5-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="261f5-226">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="261f5-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="261f5-227">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="261f5-228">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="261f5-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="261f5-229">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="261f5-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="261f5-230">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="261f5-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="261f5-231">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="261f5-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="261f5-232">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="261f5-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="261f5-233">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="261f5-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="261f5-234">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="261f5-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="261f5-235">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="261f5-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="261f5-236">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="261f5-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="261f5-237">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="261f5-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="261f5-238">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="261f5-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="261f5-239">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="261f5-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="261f5-240">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="261f5-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="261f5-241">**Tag**</span><span class="sxs-lookup"><span data-stu-id="261f5-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-244">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="261f5-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-245">Identifiziert das physische Element eindeutig und fungiert als Schlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="261f5-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="261f5-246">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="261f5-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="261f5-247">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="261f5-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="261f5-248">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="261f5-249">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="261f5-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="261f5-250">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="261f5-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="261f5-251">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="261f5-252">**Version**</span><span class="sxs-lookup"><span data-stu-id="261f5-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261f5-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="261f5-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261f5-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="261f5-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261f5-255">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="261f5-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="261f5-256">Gibt die Version des physischen Elements an.</span><span class="sxs-lookup"><span data-stu-id="261f5-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="261f5-257">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="261f5-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="261f5-258">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="261f5-258">Remarks</span></span>

<span data-ttu-id="261f5-259">Die **CIM \_ physicalcomponent** -Klasse wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="261f5-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="261f5-260">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="261f5-260">WMI does not implement this class.</span></span> <span data-ttu-id="261f5-261">Informationen zu WMI-Klassen, die von **CIM \_ physicalcomponent** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="261f5-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="261f5-262">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="261f5-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="261f5-263">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="261f5-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="261f5-264">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="261f5-264">Requirements</span></span>



| <span data-ttu-id="261f5-265">Anforderung</span><span class="sxs-lookup"><span data-stu-id="261f5-265">Requirement</span></span> | <span data-ttu-id="261f5-266">Wert</span><span class="sxs-lookup"><span data-stu-id="261f5-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="261f5-267">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="261f5-267">Minimum supported client</span></span><br/> | <span data-ttu-id="261f5-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="261f5-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="261f5-269">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="261f5-269">Minimum supported server</span></span><br/> | <span data-ttu-id="261f5-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="261f5-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="261f5-271">Namespace</span><span class="sxs-lookup"><span data-stu-id="261f5-271">Namespace</span></span><br/>                | <span data-ttu-id="261f5-272">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="261f5-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="261f5-273">MOF</span><span class="sxs-lookup"><span data-stu-id="261f5-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="261f5-274"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="261f5-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="261f5-275">DLL</span><span class="sxs-lookup"><span data-stu-id="261f5-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="261f5-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="261f5-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="261f5-277">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="261f5-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261f5-278">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="261f5-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

