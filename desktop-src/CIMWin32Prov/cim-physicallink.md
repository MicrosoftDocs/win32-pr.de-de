---
description: Die CIM \_ physicallink-Klasse stellt die Verkabelung physischer Elemente dar.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: CIM_PhysicalLink-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524011"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="dd94a-103">CIM \_ physicallink-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd94a-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="dd94a-104">Die **CIM \_ physicallink** -Klasse stellt die Verkabelung physischer Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="dd94a-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="dd94a-105">Beispielsweise sind serielle oder Ethernet-Kabel und Infrarot Verknüpfungen Unterklassen (wenn zusätzliche Eigenschaften oder Zuordnungen definiert sind) oder Instanzen von **CIM \_ physicallink**.</span><span class="sxs-lookup"><span data-stu-id="dd94a-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="dd94a-106">In der Regel werden die zahlreichen physischen Kabel innerhalb eines physischen Pakets oder Netzwerks nicht modelliert.</span><span class="sxs-lookup"><span data-stu-id="dd94a-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="dd94a-107">Wenn es sich bei den Kabeln oder Verknüpfungen jedoch um wichtige Komponenten oder markierte Ressourcen des Unternehmens handelt, können die Objekte mit dieser Klasse oder einer ihrer untergeordneten Klassen instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd94a-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dd94a-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dd94a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dd94a-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd94a-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dd94a-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd94a-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd94a-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd94a-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="dd94a-113">Member</span><span class="sxs-lookup"><span data-stu-id="dd94a-113">Members</span></span>

<span data-ttu-id="dd94a-114">Die **CIM \_ physicallink** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd94a-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="dd94a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd94a-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd94a-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd94a-116">Properties</span></span>

<span data-ttu-id="dd94a-117">Die **CIM \_ physicallink** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd94a-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd94a-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dd94a-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dd94a-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-122">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd94a-122">Short textual description of the object.</span></span>

<span data-ttu-id="dd94a-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-124">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="dd94a-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-127">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd94a-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-128">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd94a-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dd94a-129">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dd94a-130">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd94a-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-134">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dd94a-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-135">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd94a-135">Textual description of the object.</span></span>

<span data-ttu-id="dd94a-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dd94a-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd94a-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="dd94a-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-141">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd94a-141">Date and time the object was installed.</span></span> <span data-ttu-id="dd94a-142">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dd94a-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dd94a-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-144">**Länge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-145">Datentyp: **real64**</span><span class="sxs-lookup"><span data-stu-id="dd94a-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-147">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Füße")</span><span class="sxs-lookup"><span data-stu-id="dd94a-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-148">Die aktuelle Länge der physischen Verknüpfung in Fuß.</span><span class="sxs-lookup"><span data-stu-id="dd94a-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="dd94a-149">Bei einigen Verbindungen, insbesondere bei drahtlosen Technologien, ist diese Eigenschaft möglicherweise nicht anwendbar und sollte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-150">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="dd94a-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-153">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd94a-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-154">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="dd94a-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="dd94a-155">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="dd94a-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="dd94a-156">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="dd94a-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-158">Datentyp: **real64**</span><span class="sxs-lookup"><span data-stu-id="dd94a-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-160">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Füße")</span><span class="sxs-lookup"><span data-stu-id="dd94a-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-161">Maximale Länge der physischen Verknüpfung in Fuß.</span><span class="sxs-lookup"><span data-stu-id="dd94a-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-162">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="dd94a-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd94a-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-165">Medientyp, über den Übertragungssignale bestanden werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="dd94a-166">Zu den gängigen Netzwerk Medien zählen verdrehte Paare, koaxiale und Glasfaserkabel.</span><span class="sxs-lookup"><span data-stu-id="dd94a-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd94a-167">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd94a-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd94a-168">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dd94a-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="dd94a-169">**Cat1** (2)</span><span class="sxs-lookup"><span data-stu-id="dd94a-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="dd94a-170">**Cat2** (3)</span><span class="sxs-lookup"><span data-stu-id="dd94a-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="dd94a-171">**Cat3** (4)</span><span class="sxs-lookup"><span data-stu-id="dd94a-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="dd94a-172">**Cat4** (5)</span><span class="sxs-lookup"><span data-stu-id="dd94a-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="dd94a-173">**CAT5** (6)</span><span class="sxs-lookup"><span data-stu-id="dd94a-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="dd94a-174">**50-Ohm Koaxial** (7)</span><span class="sxs-lookup"><span data-stu-id="dd94a-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="dd94a-175">**75-Ohm Koaxial** (8)</span><span class="sxs-lookup"><span data-stu-id="dd94a-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="dd94a-176">**100-Ohm Koaxial** (9)</span><span class="sxs-lookup"><span data-stu-id="dd94a-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="dd94a-177">**Fiber-Optic** (10)</span><span class="sxs-lookup"><span data-stu-id="dd94a-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="dd94a-178">**UTP** (11)</span><span class="sxs-lookup"><span data-stu-id="dd94a-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="dd94a-179">**STP** (12)</span><span class="sxs-lookup"><span data-stu-id="dd94a-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="dd94a-180">**Menüband-Kabel** (13)</span><span class="sxs-lookup"><span data-stu-id="dd94a-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="dd94a-181">**Twinaxial** (14)</span><span class="sxs-lookup"><span data-stu-id="dd94a-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="dd94a-182">**Optische 9um** (15)</span><span class="sxs-lookup"><span data-stu-id="dd94a-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="dd94a-183">**Optische 50uM** (16)</span><span class="sxs-lookup"><span data-stu-id="dd94a-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="dd94a-184">**Optischer 62,5 um** (17)</span><span class="sxs-lookup"><span data-stu-id="dd94a-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd94a-185">**Modell**</span><span class="sxs-lookup"><span data-stu-id="dd94a-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-188">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dd94a-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-189">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="dd94a-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="dd94a-190">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-191">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd94a-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-194">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dd94a-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-195">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="dd94a-195">Label by which the object is known.</span></span> <span data-ttu-id="dd94a-196">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dd94a-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="dd94a-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-201">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="dd94a-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="dd94a-202">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="dd94a-203">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd94a-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="dd94a-204">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-205">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="dd94a-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-208">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd94a-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-209">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="dd94a-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="dd94a-210">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-211">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="dd94a-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-212">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd94a-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-214">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="dd94a-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="dd94a-215">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-216">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="dd94a-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-219">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dd94a-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-220">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="dd94a-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="dd94a-221">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-222">**SKU**</span><span class="sxs-lookup"><span data-stu-id="dd94a-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-225">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dd94a-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-226">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="dd94a-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="dd94a-227">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-228">**Status**</span><span class="sxs-lookup"><span data-stu-id="dd94a-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-231">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dd94a-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-232">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd94a-232">Current status of the object.</span></span>

<span data-ttu-id="dd94a-233">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dd94a-234">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="dd94a-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dd94a-235">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dd94a-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dd94a-236">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="dd94a-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd94a-237">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="dd94a-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd94a-238">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="dd94a-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dd94a-239">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="dd94a-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dd94a-240">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="dd94a-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dd94a-241">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="dd94a-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dd94a-242">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="dd94a-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dd94a-243">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="dd94a-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dd94a-244">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="dd94a-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dd94a-245">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="dd94a-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dd94a-246">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="dd94a-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd94a-247">**Tag**</span><span class="sxs-lookup"><span data-stu-id="dd94a-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-250">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd94a-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-251">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="dd94a-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="dd94a-252">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="dd94a-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="dd94a-253">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd94a-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="dd94a-254">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="dd94a-255">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dd94a-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="dd94a-256">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="dd94a-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="dd94a-257">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-258">**Version**</span><span class="sxs-lookup"><span data-stu-id="dd94a-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-259">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd94a-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-261">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dd94a-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-262">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="dd94a-262">Version of the physical element.</span></span>

<span data-ttu-id="dd94a-263">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd94a-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd94a-264">**Kabel**</span><span class="sxs-lookup"><span data-stu-id="dd94a-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd94a-265">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd94a-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd94a-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd94a-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd94a-267">**True** gibt an, dass die physische Verknüpfung ein Kabel ist.</span><span class="sxs-lookup"><span data-stu-id="dd94a-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="dd94a-268">Andernfalls handelt es sich um eine drahtlose Verbindung.</span><span class="sxs-lookup"><span data-stu-id="dd94a-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd94a-269">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd94a-269">Remarks</span></span>

<span data-ttu-id="dd94a-270">Die **CIM \_ physicallink** -Klasse wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dd94a-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="dd94a-271">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dd94a-271">WMI does not implement this class.</span></span>

<span data-ttu-id="dd94a-272">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dd94a-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dd94a-273">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dd94a-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd94a-274">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd94a-274">Requirements</span></span>



| <span data-ttu-id="dd94a-275">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd94a-275">Requirement</span></span> | <span data-ttu-id="dd94a-276">Wert</span><span class="sxs-lookup"><span data-stu-id="dd94a-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd94a-277">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd94a-277">Minimum supported client</span></span><br/> | <span data-ttu-id="dd94a-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd94a-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd94a-279">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd94a-279">Minimum supported server</span></span><br/> | <span data-ttu-id="dd94a-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd94a-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd94a-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd94a-281">Namespace</span></span><br/>                | <span data-ttu-id="dd94a-282">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dd94a-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd94a-283">MOF</span><span class="sxs-lookup"><span data-stu-id="dd94a-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd94a-284"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd94a-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd94a-285">DLL</span><span class="sxs-lookup"><span data-stu-id="dd94a-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd94a-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd94a-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd94a-287">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd94a-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd94a-288">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="dd94a-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

