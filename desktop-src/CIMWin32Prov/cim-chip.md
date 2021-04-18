---
description: Die CIM \_ -Chip Klasse stellt den Typ der integrierten Verbindungs Hardware dar, einschließlich ASICs, Prozessoren, Speicherchips usw.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: CIM_Chip-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483550"
---
# <a name="cim_chip-class"></a><span data-ttu-id="f3f12-103">CIM- \_ Chip Klasse</span><span class="sxs-lookup"><span data-stu-id="f3f12-103">CIM\_Chip class</span></span>

<span data-ttu-id="f3f12-104">Die **CIM- \_ Chip** Klasse stellt den Typ der integrierten Verbindungs Hardware dar, einschließlich ASICs, Prozessoren, Speicherchips usw.</span><span class="sxs-lookup"><span data-stu-id="f3f12-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3f12-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f3f12-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f3f12-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f3f12-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f3f12-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f3f12-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f3f12-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f12-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3f12-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="f3f12-110">Member</span><span class="sxs-lookup"><span data-stu-id="f3f12-110">Members</span></span>

<span data-ttu-id="f3f12-111">Die **CIM- \_ Chip** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f3f12-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="f3f12-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3f12-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3f12-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3f12-113">Properties</span></span>

<span data-ttu-id="f3f12-114">Die **CIM- \_ Chip** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3f12-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3f12-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f3f12-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f3f12-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f3f12-119">A short textual description of the object.</span></span>

<span data-ttu-id="f3f12-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-121">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f3f12-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-124">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f3f12-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-125">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3f12-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f3f12-126">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f3f12-127">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3f12-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-131">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f3f12-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-132">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f3f12-132">A textual description of the object.</span></span>

<span data-ttu-id="f3f12-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-134">**Formfaktor**</span><span class="sxs-lookup"><span data-stu-id="f3f12-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3f12-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-137">Der Implementierungs Formfaktor für den Chip.</span><span class="sxs-lookup"><span data-stu-id="f3f12-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="f3f12-138">Die folgenden Werte können angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3f12-139">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f3f12-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f3f12-140">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f3f12-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="f3f12-141">**SIP** (2)</span><span class="sxs-lookup"><span data-stu-id="f3f12-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="f3f12-142">**DIP** (3)</span><span class="sxs-lookup"><span data-stu-id="f3f12-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="f3f12-143">**ZIP** (4)</span><span class="sxs-lookup"><span data-stu-id="f3f12-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="f3f12-144">**SOJ** (5)</span><span class="sxs-lookup"><span data-stu-id="f3f12-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="f3f12-145">**Proprietär** (6)</span><span class="sxs-lookup"><span data-stu-id="f3f12-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="f3f12-146">**SIMM** (7)</span><span class="sxs-lookup"><span data-stu-id="f3f12-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="f3f12-147">**DIMM** (8)</span><span class="sxs-lookup"><span data-stu-id="f3f12-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="f3f12-148">**Wahrheits** Satz (9)</span><span class="sxs-lookup"><span data-stu-id="f3f12-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="f3f12-149">**PGA** (10)</span><span class="sxs-lookup"><span data-stu-id="f3f12-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="f3f12-150">**RIMM** (11)</span><span class="sxs-lookup"><span data-stu-id="f3f12-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="f3f12-151">**SODIMM** (12)</span><span class="sxs-lookup"><span data-stu-id="f3f12-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="f3f12-152">**Srimm** (13)</span><span class="sxs-lookup"><span data-stu-id="f3f12-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="f3f12-153">**SMD** (14)</span><span class="sxs-lookup"><span data-stu-id="f3f12-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="f3f12-154">**SSMP** (15)</span><span class="sxs-lookup"><span data-stu-id="f3f12-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="f3f12-155">**QFP** (16)</span><span class="sxs-lookup"><span data-stu-id="f3f12-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="f3f12-156">**TQFP** (17)</span><span class="sxs-lookup"><span data-stu-id="f3f12-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="f3f12-157">**SOIC** (18)</span><span class="sxs-lookup"><span data-stu-id="f3f12-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="f3f12-158">**LCC** (19)</span><span class="sxs-lookup"><span data-stu-id="f3f12-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="f3f12-159">**PLCC** (20)</span><span class="sxs-lookup"><span data-stu-id="f3f12-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="f3f12-160">**BGA** (21)</span><span class="sxs-lookup"><span data-stu-id="f3f12-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="f3f12-161">**Fpbga** (22)</span><span class="sxs-lookup"><span data-stu-id="f3f12-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="f3f12-162">**LGA** (23)</span><span class="sxs-lookup"><span data-stu-id="f3f12-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="f3f12-163">**FB-DIMM** (24)</span><span class="sxs-lookup"><span data-stu-id="f3f12-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3f12-164">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="f3f12-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-165">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f3f12-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-167">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3f12-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f3f12-168">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="f3f12-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f3f12-169">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="f3f12-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f3f12-170">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="f3f12-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f3f12-171">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3f12-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-173">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3f12-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-175">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f3f12-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-176">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f3f12-176">Indicates when the object was installed.</span></span> <span data-ttu-id="f3f12-177">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3f12-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f3f12-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-179">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="f3f12-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-182">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f3f12-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-183">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="f3f12-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="f3f12-184">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f3f12-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f3f12-185">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-186">**Modell**</span><span class="sxs-lookup"><span data-stu-id="f3f12-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-189">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f3f12-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-190">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f3f12-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f3f12-191">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-192">**Name**</span><span class="sxs-lookup"><span data-stu-id="f3f12-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-195">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f3f12-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-196">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f3f12-196">Label by which the object is known.</span></span> <span data-ttu-id="f3f12-197">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f3f12-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f3f12-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-202">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f3f12-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="f3f12-203">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="f3f12-204">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3f12-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="f3f12-205">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-206">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="f3f12-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-209">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f3f12-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-210">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="f3f12-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="f3f12-211">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-212">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="f3f12-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-213">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f3f12-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-215">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="f3f12-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="f3f12-216">Andernfalls ist Sie zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f3f12-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="f3f12-217">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-218">**Ab**</span><span class="sxs-lookup"><span data-stu-id="f3f12-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f3f12-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-221">**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="f3f12-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f3f12-222">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f3f12-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="f3f12-223">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f3f12-224">Beispielsweise kann ein erweiterbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="f3f12-225">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-226">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="f3f12-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-227">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f3f12-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-229">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f3f12-230">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="f3f12-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f3f12-231">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f3f12-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f3f12-232">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="f3f12-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f3f12-233">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-234">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f3f12-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-237">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f3f12-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-238">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f3f12-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="f3f12-239">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-240">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f3f12-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-243">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f3f12-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-244">Die Stock Keeping Unit-Nummer für dieses physische Element.</span><span class="sxs-lookup"><span data-stu-id="f3f12-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="f3f12-245">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-246">**Status**</span><span class="sxs-lookup"><span data-stu-id="f3f12-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-249">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f3f12-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-250">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="f3f12-251">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f3f12-252">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3f12-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f3f12-253">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="f3f12-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f3f12-254">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3f12-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f3f12-255">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f3f12-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f3f12-256">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f3f12-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f3f12-257">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f3f12-258">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f3f12-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f3f12-259">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f3f12-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f3f12-260">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f3f12-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f3f12-261">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f3f12-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3f12-262">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f3f12-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f3f12-263">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f3f12-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f3f12-264">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f3f12-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f3f12-265">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f3f12-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f3f12-266">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f3f12-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f3f12-267">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f3f12-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f3f12-268">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f3f12-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f3f12-269">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f3f12-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f3f12-270">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f3f12-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3f12-271">**Tag**</span><span class="sxs-lookup"><span data-stu-id="f3f12-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-274">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f3f12-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-275">Identifiziert das physische Element eindeutig und fungiert als Schlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="f3f12-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f3f12-276">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="f3f12-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f3f12-277">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f3f12-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f3f12-278">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f3f12-279">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f3f12-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f3f12-280">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f3f12-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f3f12-281">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f12-282">**Version**</span><span class="sxs-lookup"><span data-stu-id="f3f12-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3f12-283">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3f12-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f12-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f12-285">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f3f12-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3f12-286">Gibt die Version des physischen Elements an.</span><span class="sxs-lookup"><span data-stu-id="f3f12-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="f3f12-287">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f3f12-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3f12-288">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3f12-288">Remarks</span></span>

<span data-ttu-id="f3f12-289">Die **CIM- \_ Chip** Klasse wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f3f12-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="f3f12-290">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f3f12-290">WMI does not implement this class.</span></span> <span data-ttu-id="f3f12-291">Weitere Informationen zu Klassen, die vom **CIM- \_ Chip** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f12-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f3f12-292">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f3f12-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f3f12-293">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f3f12-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f12-294">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3f12-294">Requirements</span></span>



| <span data-ttu-id="f3f12-295">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3f12-295">Requirement</span></span> | <span data-ttu-id="f3f12-296">Wert</span><span class="sxs-lookup"><span data-stu-id="f3f12-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f12-297">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3f12-297">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f12-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3f12-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3f12-299">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3f12-299">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f12-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3f12-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3f12-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3f12-301">Namespace</span></span><br/>                | <span data-ttu-id="f3f12-302">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3f12-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3f12-303">MOF</span><span class="sxs-lookup"><span data-stu-id="f3f12-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3f12-304"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f3f12-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3f12-305">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f12-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f12-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f12-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3f12-307">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3f12-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f12-308">**CIM- \_ physicalcomponent**</span><span class="sxs-lookup"><span data-stu-id="f3f12-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

