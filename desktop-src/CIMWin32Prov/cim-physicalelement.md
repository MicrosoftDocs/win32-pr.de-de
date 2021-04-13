---
description: Die CIM \_ PhysicalElement-Unterklassen definieren jede Komponente eines Systems, das über eine eindeutige physische Identität verfügt. Instanzen dieser Klasse können in Bezug auf Bezeichnungen definiert werden, die physisch an das Objekt angefügt werden können.
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: CIM_PhysicalElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523120"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="2496b-104">CIM \_ PhysicalElement-Klasse</span><span class="sxs-lookup"><span data-stu-id="2496b-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="2496b-105">Die **CIM \_ PhysicalElement** -Unterklassen definieren jede Komponente eines Systems, das über eine eindeutige physische Identität verfügt.</span><span class="sxs-lookup"><span data-stu-id="2496b-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="2496b-106">Instanzen dieser Klasse können in Bezug auf Bezeichnungen definiert werden, die physisch an das Objekt angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="2496b-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="2496b-107">Alle Prozesse, Dateien und logischen Geräte werden nicht als physische Elemente betrachtet.</span><span class="sxs-lookup"><span data-stu-id="2496b-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="2496b-108">Beispielsweise ist es nicht möglich, eine Bezeichnung an ein Modem anzufügen. Es ist nur möglich, eine Bezeichnung an die Karte anzufügen, die das Modem implementiert.</span><span class="sxs-lookup"><span data-stu-id="2496b-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="2496b-109">Dieselbe Karte könnte auch einen LAN-Adapter implementieren.</span><span class="sxs-lookup"><span data-stu-id="2496b-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="2496b-110">Greifbare verwaltete Systemelemente (in der Regel Hardwareelemente) weisen eine physische Manifestation auf.</span><span class="sxs-lookup"><span data-stu-id="2496b-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="2496b-111">Ein verwaltetes System Element ist nicht notwendigerweise eine diskrete Komponente.</span><span class="sxs-lookup"><span data-stu-id="2496b-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="2496b-112">Beispielsweise ist es möglich, dass eine einzelne Karte (ein physischer Elementtyp) mehr als ein logisches Gerät hostet.</span><span class="sxs-lookup"><span data-stu-id="2496b-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="2496b-113">Die Karte wird durch ein einzelnes physisches Element dargestellt, das mehreren logischen Geräten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2496b-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2496b-114">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2496b-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2496b-115">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2496b-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2496b-116">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2496b-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2496b-117">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2496b-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2496b-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="2496b-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
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
};
```

## <a name="members"></a><span data-ttu-id="2496b-119">Member</span><span class="sxs-lookup"><span data-stu-id="2496b-119">Members</span></span>

<span data-ttu-id="2496b-120">Die **CIM \_ PhysicalElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2496b-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="2496b-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2496b-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2496b-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2496b-122">Properties</span></span>

<span data-ttu-id="2496b-123">Die **CIM \_ PhysicalElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2496b-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2496b-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2496b-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-127">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2496b-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2496b-128">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2496b-128">A short textual description of the object.</span></span>

<span data-ttu-id="2496b-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2496b-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2496b-130">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="2496b-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-133">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2496b-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-134">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2496b-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2496b-135">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2496b-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2496b-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-139">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2496b-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2496b-140">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2496b-140">A textual description of the object.</span></span>

<span data-ttu-id="2496b-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2496b-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2496b-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2496b-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-143">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2496b-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="2496b-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2496b-146">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2496b-146">Indicates when the object was installed.</span></span> <span data-ttu-id="2496b-147">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2496b-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2496b-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2496b-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2496b-149">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="2496b-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-152">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2496b-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-153">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="2496b-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="2496b-154">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="2496b-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="2496b-155">**Modell**</span><span class="sxs-lookup"><span data-stu-id="2496b-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-158">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2496b-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-159">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2496b-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="2496b-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-163">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2496b-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2496b-164">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2496b-164">Label by which the object is known.</span></span> <span data-ttu-id="2496b-165">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2496b-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2496b-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2496b-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2496b-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2496b-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2496b-170">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2496b-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="2496b-171">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="2496b-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="2496b-172">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="2496b-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-173">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="2496b-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-176">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2496b-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-177">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="2496b-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-178">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="2496b-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-179">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2496b-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2496b-181">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="2496b-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="2496b-182">Andernfalls ist Sie zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2496b-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="2496b-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-186">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2496b-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-187">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2496b-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-188">**SKU**</span><span class="sxs-lookup"><span data-stu-id="2496b-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-191">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2496b-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-192">Die Stock Keeping Unit-Nummer für dieses physische Element.</span><span class="sxs-lookup"><span data-stu-id="2496b-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="2496b-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-196">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2496b-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2496b-197">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="2496b-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="2496b-198">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2496b-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2496b-199">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="2496b-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2496b-200">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="2496b-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2496b-201">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="2496b-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2496b-202">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="2496b-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2496b-203">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="2496b-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2496b-204">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2496b-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2496b-205">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="2496b-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2496b-206">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2496b-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2496b-207">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="2496b-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2496b-208">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="2496b-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2496b-209">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="2496b-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2496b-210">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2496b-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2496b-211">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="2496b-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2496b-212">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="2496b-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2496b-213">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="2496b-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2496b-214">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="2496b-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2496b-215">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="2496b-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2496b-216">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="2496b-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2496b-217">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="2496b-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2496b-218">**Tag**</span><span class="sxs-lookup"><span data-stu-id="2496b-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-221">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2496b-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-222">Identifiziert das physische Element eindeutig und fungiert als Schlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="2496b-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="2496b-223">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="2496b-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="2496b-224">Der Schlüssel für **CIM \_ PhysicalElement** wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2496b-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="2496b-225">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2496b-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="2496b-226">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2496b-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="2496b-227">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="2496b-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="2496b-228">**Version**</span><span class="sxs-lookup"><span data-stu-id="2496b-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2496b-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2496b-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2496b-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2496b-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2496b-231">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2496b-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2496b-232">Gibt die Version des physischen Elements an.</span><span class="sxs-lookup"><span data-stu-id="2496b-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2496b-233">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2496b-233">Remarks</span></span>

<span data-ttu-id="2496b-234">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2496b-234">WMI does not implement this class.</span></span> <span data-ttu-id="2496b-235">Informationen zu WMI-Klassen, die von **CIM \_ PhysicalElement** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2496b-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2496b-236">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2496b-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2496b-237">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2496b-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2496b-238">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2496b-238">Requirements</span></span>



| <span data-ttu-id="2496b-239">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2496b-239">Requirement</span></span> | <span data-ttu-id="2496b-240">Wert</span><span class="sxs-lookup"><span data-stu-id="2496b-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2496b-241">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2496b-241">Minimum supported client</span></span><br/> | <span data-ttu-id="2496b-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2496b-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2496b-243">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2496b-243">Minimum supported server</span></span><br/> | <span data-ttu-id="2496b-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2496b-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2496b-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="2496b-245">Namespace</span></span><br/>                | <span data-ttu-id="2496b-246">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2496b-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2496b-247">MOF</span><span class="sxs-lookup"><span data-stu-id="2496b-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2496b-248"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2496b-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2496b-249">DLL</span><span class="sxs-lookup"><span data-stu-id="2496b-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2496b-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2496b-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2496b-251">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2496b-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2496b-252">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="2496b-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

