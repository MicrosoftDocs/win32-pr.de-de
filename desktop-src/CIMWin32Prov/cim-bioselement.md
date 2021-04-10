---
description: Die CIM \_ bioselfigure-Klasse stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems verwendet wird.
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: CIM_BIOSElement-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041476"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="c84d3-103">CIM_BIOSElement-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="c84d3-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c84d3-104">Die **CIM \_ bioselfigure** -Klasse stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c84d3-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c84d3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c84d3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c84d3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c84d3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c84d3-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c84d3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c84d3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c84d3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84d3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c84d3-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="c84d3-110">Member</span><span class="sxs-lookup"><span data-stu-id="c84d3-110">Members</span></span>

<span data-ttu-id="c84d3-111">Die CIM-Klasse " **\_ bioselements** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c84d3-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c84d3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c84d3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c84d3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c84d3-113">Properties</span></span>

<span data-ttu-id="c84d3-114">Die CIM-Klasse " **\_ bioselements** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c84d3-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c84d3-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="c84d3-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-119">Interner Bezeichner für die Kompilierung dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="c84d3-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="c84d3-120">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c84d3-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c84d3-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-125">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c84d3-125">A short textual description of the object.</span></span>

<span data-ttu-id="c84d3-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-127">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="c84d3-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c84d3-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-131">Vom Softwareelement verwendeter Codesatz.</span><span class="sxs-lookup"><span data-stu-id="c84d3-131">Code set used by the software element.</span></span>

<span data-ttu-id="c84d3-132">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c84d3-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-136">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c84d3-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-137">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c84d3-137">A textual description of the object.</span></span>

<span data-ttu-id="c84d3-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-139">**Identificationcode**</span><span class="sxs-lookup"><span data-stu-id="c84d3-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-142">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-143">Der Bezeichner des Herstellers für das Softwareelement, häufig eine Stock Keeping Unit (SKU) oder eine Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="c84d3-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="c84d3-144">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c84d3-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c84d3-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-149">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c84d3-149">Indicates when the object was installed.</span></span> <span data-ttu-id="c84d3-150">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c84d3-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c84d3-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-152">**Languageedition**</span><span class="sxs-lookup"><span data-stu-id="c84d3-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-155">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-156">Language Edition des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="c84d3-156">Language edition of the software element.</span></span> <span data-ttu-id="c84d3-157">Die in ISO 639 definierten Sprachcodes sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c84d3-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="c84d3-158">Wenn das Softwareelement mehrsprachige oder internationale Versionen eines Produkts darstellt, sollte die Zeichenfolge "mehrsprachig" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c84d3-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="c84d3-159">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-160">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c84d3-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-163">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hersteller"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-164">Der Hersteller des BIOS.</span><span class="sxs-lookup"><span data-stu-id="c84d3-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-165">**Name**</span><span class="sxs-lookup"><span data-stu-id="c84d3-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-168">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c84d3-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-169">Der Name, der zum Identifizieren dieses Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c84d3-169">The name used to identify this software element</span></span>

<span data-ttu-id="c84d3-170">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-171">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="c84d3-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-174">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="c84d3-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-175">Hersteller und Betriebs Systemtyp für ein Softwareelement, wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 hat ("Other").</span><span class="sxs-lookup"><span data-stu-id="c84d3-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="c84d3-176">Wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 aufweist, muss diese Eigenschaft einen Wert aufweisen, der nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="c84d3-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="c84d3-177">Für alle anderen **TargetOperatingSystem** -Werte ist diese Eigenschaft NULL.</span><span class="sxs-lookup"><span data-stu-id="c84d3-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="c84d3-178">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-179">**Primarybios**</span><span class="sxs-lookup"><span data-stu-id="c84d3-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c84d3-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-182">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-183">**True** gibt an, dass dies das primäre BIOS des Computer Systems ist.</span><span class="sxs-lookup"><span data-stu-id="c84d3-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-184">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c84d3-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-187">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-188">Seriennummer des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="c84d3-188">Serial number of the software element.</span></span>

<span data-ttu-id="c84d3-189">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-190">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="c84d3-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-193">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c84d3-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-194">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="c84d3-194">Identifier for the software element.</span></span> <span data-ttu-id="c84d3-195">Es ist für die Verwendung in Verbindung mit anderen Schlüsseln konzipiert, um eine eindeutige Darstellung dieses [**CIM- \_ Softwareelement**](cim-softwareelement.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c84d3-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="c84d3-196">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84d3-197">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="c84d3-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c84d3-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-200">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c84d3-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-201">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="c84d3-201">State of a software element.</span></span>

<span data-ttu-id="c84d3-202">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="c84d3-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="c84d3-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-204">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c84d3-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="c84d3-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="c84d3-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-206">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c84d3-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="c84d3-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="c84d3-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-208">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c84d3-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c84d3-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="c84d3-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-210">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c84d3-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c84d3-211">**Status**</span><span class="sxs-lookup"><span data-stu-id="c84d3-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-214">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c84d3-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-215">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="c84d3-216">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c84d3-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c84d3-217">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c84d3-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c84d3-218">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c84d3-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c84d3-219">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c84d3-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c84d3-220">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c84d3-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c84d3-221">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c84d3-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c84d3-222">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c84d3-223">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c84d3-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c84d3-224">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c84d3-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c84d3-225">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c84d3-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c84d3-226">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c84d3-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c84d3-227">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c84d3-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c84d3-228">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c84d3-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c84d3-229">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c84d3-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c84d3-230">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c84d3-231">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c84d3-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c84d3-232">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c84d3-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c84d3-233">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c84d3-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c84d3-234">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c84d3-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c84d3-235">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c84d3-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c84d3-236">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="c84d3-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c84d3-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-239">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Komponenten Informationen \| 002,5 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**OSType**")</span><span class="sxs-lookup"><span data-stu-id="c84d3-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-240">Betriebssystemumgebung.</span><span class="sxs-lookup"><span data-stu-id="c84d3-240">Operating system environment.</span></span> <span data-ttu-id="c84d3-241">Der Wert dieser Eigenschaft gewährleistet nicht die binäre executabilität, es sind weitere Informationen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c84d3-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="c84d3-242">Die Betriebssystemversion muss mithilfe der Überprüfung der Betriebssystemversion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c84d3-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="c84d3-243">Außerdem ist die Architektur, in der das Betriebssystem ausgeführt wird, erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c84d3-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="c84d3-244">Die Kombination dieser Konstrukte ermöglicht es dem Anbieter, die für ein bestimmtes Softwareelement erforderliche Betriebssystemebene eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c84d3-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="c84d3-245">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c84d3-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c84d3-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c84d3-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c84d3-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c84d3-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="c84d3-248"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="c84d3-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-249">Mac OS</span><span class="sxs-lookup"><span data-stu-id="c84d3-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="c84d3-250"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="c84d3-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-251">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="c84d3-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="c84d3-252"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="c84d3-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="c84d3-253"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="c84d3-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="c84d3-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="c84d3-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="c84d3-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="c84d3-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-256">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="c84d3-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="c84d3-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="c84d3-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="c84d3-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="c84d3-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="c84d3-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="c84d3-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="c84d3-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="c84d3-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="c84d3-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="c84d3-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="c84d3-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="c84d3-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="c84d3-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-264">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="c84d3-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="c84d3-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="c84d3-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="c84d3-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="c84d3-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-267">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="c84d3-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="c84d3-268"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="c84d3-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="c84d3-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="c84d3-270"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="c84d3-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c84d3-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="c84d3-272"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="c84d3-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c84d3-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="c84d3-274"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="c84d3-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="c84d3-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="c84d3-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="c84d3-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-277">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="c84d3-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="c84d3-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="c84d3-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="c84d3-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="c84d3-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="c84d3-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="c84d3-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="c84d3-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="c84d3-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="c84d3-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="c84d3-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="c84d3-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="c84d3-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="c84d3-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="c84d3-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="c84d3-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="c84d3-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="c84d3-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="c84d3-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="c84d3-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="c84d3-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="c84d3-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="c84d3-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="c84d3-289"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="c84d3-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-290">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="c84d3-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="c84d3-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="c84d3-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-292">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="c84d3-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="c84d3-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="c84d3-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-294">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="c84d3-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="c84d3-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="c84d3-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="c84d3-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="c84d3-297"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="c84d3-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="c84d3-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="c84d3-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="c84d3-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="c84d3-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="c84d3-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="c84d3-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="c84d3-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="c84d3-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="c84d3-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="c84d3-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-303">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="c84d3-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="c84d3-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="c84d3-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="c84d3-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="c84d3-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="c84d3-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="c84d3-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="c84d3-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="c84d3-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="c84d3-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="c84d3-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="c84d3-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="c84d3-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="c84d3-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="c84d3-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="c84d3-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="c84d3-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="c84d3-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="c84d3-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="c84d3-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="c84d3-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="c84d3-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="c84d3-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="c84d3-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="c84d3-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="c84d3-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="c84d3-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="c84d3-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="c84d3-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="c84d3-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="c84d3-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="c84d3-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="c84d3-320">Palm OS</span><span class="sxs-lookup"><span data-stu-id="c84d3-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="c84d3-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="c84d3-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="c84d3-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="c84d3-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="c84d3-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="c84d3-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="c84d3-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="c84d3-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="c84d3-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="c84d3-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c84d3-326">**Version**</span><span class="sxs-lookup"><span data-stu-id="c84d3-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84d3-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c84d3-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c84d3-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84d3-329">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="c84d3-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c84d3-330">Die BIOS-Version.</span><span class="sxs-lookup"><span data-stu-id="c84d3-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c84d3-331">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c84d3-331">Remarks</span></span>

<span data-ttu-id="c84d3-332">Die **CIM- \_ bioselement** -Klasse wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c84d3-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="c84d3-333">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c84d3-333">WMI does not implement this class.</span></span> <span data-ttu-id="c84d3-334">Weitere Informationen zu Klassen, die von **CIM \_ bioselor** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c84d3-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c84d3-335">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c84d3-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c84d3-336">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c84d3-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84d3-337">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c84d3-337">Requirements</span></span>



| <span data-ttu-id="c84d3-338">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c84d3-338">Requirement</span></span> | <span data-ttu-id="c84d3-339">Wert</span><span class="sxs-lookup"><span data-stu-id="c84d3-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84d3-340">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c84d3-340">Minimum supported client</span></span><br/> | <span data-ttu-id="c84d3-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c84d3-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c84d3-342">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c84d3-342">Minimum supported server</span></span><br/> | <span data-ttu-id="c84d3-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c84d3-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c84d3-344">Namespace</span><span class="sxs-lookup"><span data-stu-id="c84d3-344">Namespace</span></span><br/>                | <span data-ttu-id="c84d3-345">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c84d3-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c84d3-346">MOF</span><span class="sxs-lookup"><span data-stu-id="c84d3-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c84d3-347"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c84d3-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c84d3-348">DLL</span><span class="sxs-lookup"><span data-stu-id="c84d3-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84d3-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84d3-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84d3-350">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c84d3-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84d3-351">**CIM- \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="c84d3-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

