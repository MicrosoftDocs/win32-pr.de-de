---
description: Die CIM \_ videobioselfigure-Klasse stellt die Software auf niedriger Ebene dar, die in nicht flüchtigen Speicher geladen wird und zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.
ms.assetid: f23d411f-4781-4727-abd1-61fe1a366bf0
ms.tgt_platform: multiple
title: CIM_VideoBIOSElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSElement
- CIM_VideoBIOSElement.BuildNumber
- CIM_VideoBIOSElement.Caption
- CIM_VideoBIOSElement.CodeSet
- CIM_VideoBIOSElement.Description
- CIM_VideoBIOSElement.IdentificationCode
- CIM_VideoBIOSElement.InstallDate
- CIM_VideoBIOSElement.IsShadowed
- CIM_VideoBIOSElement.LanguageEdition
- CIM_VideoBIOSElement.Manufacturer
- CIM_VideoBIOSElement.Name
- CIM_VideoBIOSElement.OtherTargetOS
- CIM_VideoBIOSElement.SerialNumber
- CIM_VideoBIOSElement.SoftwareElementID
- CIM_VideoBIOSElement.SoftwareElementState
- CIM_VideoBIOSElement.Status
- CIM_VideoBIOSElement.TargetOperatingSystem
- CIM_VideoBIOSElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d873b17f0bf0ea123d988d281c0cab728dd50f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958338"
---
# <a name="cim_videobioselement-class"></a><span data-ttu-id="01669-103">CIM- \_ videobioselements-Klasse</span><span class="sxs-lookup"><span data-stu-id="01669-103">CIM\_VideoBIOSElement class</span></span>

<span data-ttu-id="01669-104">Die **CIM \_ videobioselfigure** -Klasse stellt die Software auf niedriger Ebene dar, die in nicht flüchtigen Speicher geladen wird und zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01669-104">The **CIM\_VideoBIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01669-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="01669-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01669-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01669-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01669-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01669-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="01669-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="01669-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01669-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="01669-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{76148BF6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VideoBIOSElement : CIM_SoftwareElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  boolean  IsShadowed;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="01669-110">Member</span><span class="sxs-lookup"><span data-stu-id="01669-110">Members</span></span>

<span data-ttu-id="01669-111">Die **CIM \_ videobioselements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="01669-111">The **CIM\_VideoBIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="01669-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01669-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01669-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01669-113">Properties</span></span>

<span data-ttu-id="01669-114">Die **CIM \_ videobioselements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01669-114">The **CIM\_VideoBIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01669-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="01669-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="01669-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="01669-119">Interner Bezeichner für die Kompilierung dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="01669-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="01669-120">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="01669-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="01669-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="01669-125">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="01669-125">Short textual description of the object.</span></span>

<span data-ttu-id="01669-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-127">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="01669-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01669-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01669-131">Vom Softwareelement verwendeter Codesatz.</span><span class="sxs-lookup"><span data-stu-id="01669-131">Code set used by the software element.</span></span>

<span data-ttu-id="01669-132">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01669-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-136">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="01669-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="01669-137">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="01669-137">Textual description of the object.</span></span>

<span data-ttu-id="01669-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-139">**Identificationcode**</span><span class="sxs-lookup"><span data-stu-id="01669-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-142">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="01669-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="01669-143">Der Bezeichner des Herstellers für das Softwareelement, z. b. eine SKU (Stock-Keeping Unit, SKU) oder eine Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="01669-143">Manufacturer's identifier for the software element, such as a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="01669-144">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="01669-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="01669-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01669-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="01669-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="01669-149">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="01669-149">Date and time the object was installed.</span></span> <span data-ttu-id="01669-150">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="01669-150">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="01669-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-152">**Isshadowing**</span><span class="sxs-lookup"><span data-stu-id="01669-152">**IsShadowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-153">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="01669-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01669-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-155">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video-BIOS \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="01669-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="01669-156">**True** gibt an, dass das Video-BIOS schattiert wird.</span><span class="sxs-lookup"><span data-stu-id="01669-156">If **TRUE**, the video BIOS is shadowed.</span></span>

</dd> <dt>

<span data-ttu-id="01669-157">**Languageedition**</span><span class="sxs-lookup"><span data-stu-id="01669-157">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-160">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="01669-160">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="01669-161">Language Edition des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="01669-161">Language edition of the software element.</span></span> <span data-ttu-id="01669-162">Die in ISO 639 definierten Sprachcodes sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01669-162">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="01669-163">Wenn das Softwareelement eine mehrsprachige oder internationale Version eines Produkts darstellt, sollte die Zeichenfolge "mehrsprachig" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01669-163">When the software element represents a multilingual or international version of a product, the string "Multilingual" should be used.</span></span>

<span data-ttu-id="01669-164">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-164">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-165">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="01669-165">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-168">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="01669-168">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="01669-169">Hersteller des Software Elements diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-169">Manufacturer of the software element This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-170">**Name**</span><span class="sxs-lookup"><span data-stu-id="01669-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-173">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01669-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01669-174">Name, der zum Identifizieren des Software Elements verwendet wird, das diese Eigenschaft von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="01669-174">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-175">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="01669-175">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-178">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="01669-178">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="01669-179">Hersteller und Betriebs Systemtyp für ein Softwareelement, wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 hat ("Other").</span><span class="sxs-lookup"><span data-stu-id="01669-179">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="01669-180">Wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 aufweist, muss diese Eigenschaft einen Wert aufweisen, der nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="01669-180">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="01669-181">Für alle anderen **TargetOperatingSystem** -Werte ist diese Eigenschaft NULL.</span><span class="sxs-lookup"><span data-stu-id="01669-181">For all other **TargetOperatingSystem** values, this property is null.</span></span> <span data-ttu-id="01669-182">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-182">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="01669-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-186">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="01669-186">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="01669-187">Zugewiesene Seriennummer des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="01669-187">Assigned serial number of the software element.</span></span>

<span data-ttu-id="01669-188">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-188">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-189">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="01669-189">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-192">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01669-192">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01669-193">Der Bezeichner für das Softwareelement, das für die Verwendung in Verbindung mit anderen Schlüsseln entworfen wurde, um eine eindeutige Darstellung der [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01669-193">Identifier for the software element that is designed to be used in conjunction with other keys to create a unique representation of the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

<span data-ttu-id="01669-194">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-194">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01669-195">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="01669-195">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01669-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01669-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-198">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01669-198">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01669-199">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="01669-199">State of a software element.</span></span>

<span data-ttu-id="01669-200">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-200">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="01669-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="01669-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="01669-202">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01669-202">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="01669-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="01669-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="01669-204">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01669-204">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="01669-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="01669-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="01669-206">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01669-206">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="01669-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="01669-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01669-208">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="01669-208">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01669-209">**Status**</span><span class="sxs-lookup"><span data-stu-id="01669-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-212">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="01669-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="01669-213">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="01669-213">Current status of the object.</span></span> <span data-ttu-id="01669-214">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="01669-215">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="01669-215">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="01669-216">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="01669-216">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="01669-217">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="01669-217">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="01669-218">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="01669-218">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01669-219">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="01669-219">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="01669-220">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="01669-220">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="01669-221">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="01669-221">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="01669-222">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="01669-222">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="01669-223">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="01669-223">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="01669-224">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="01669-224">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="01669-225">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="01669-225">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="01669-226">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="01669-226">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="01669-227">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="01669-227">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01669-228">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="01669-228">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-229">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01669-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01669-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-231">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Komponenten Informationen \| 002,5 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**OSType**")</span><span class="sxs-lookup"><span data-stu-id="01669-231">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="01669-232">Betriebssystemumgebung.</span><span class="sxs-lookup"><span data-stu-id="01669-232">Operating system environment.</span></span> <span data-ttu-id="01669-233">Der Wert dieser Eigenschaft gewährleistet nicht die binäre Ausführung.</span><span class="sxs-lookup"><span data-stu-id="01669-233">The value of this property does not ensure binary execution.</span></span> <span data-ttu-id="01669-234">Die Version des Betriebssystems muss mithilfe der Überprüfung der Betriebssystemversion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="01669-234">The version of the operating system must be specified using the operating system version check.</span></span> <span data-ttu-id="01669-235">Außerdem ist die Architektur erforderlich, in der das Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01669-235">Also required is the architecture on which the operating system runs.</span></span> <span data-ttu-id="01669-236">Die Kombination dieser Konstrukte ermöglicht es dem Anbieter, die für ein bestimmtes Softwareelement erforderliche Betriebssystemebene eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="01669-236">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="01669-237">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-237">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01669-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="01669-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01669-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="01669-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="01669-240"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="01669-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="01669-241">Mac OS</span><span class="sxs-lookup"><span data-stu-id="01669-241">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="01669-242"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="01669-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01669-243">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="01669-243">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="01669-244"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="01669-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="01669-245"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="01669-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="01669-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="01669-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="01669-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="01669-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="01669-248">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="01669-248">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="01669-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="01669-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="01669-250">HP-UX</span><span class="sxs-lookup"><span data-stu-id="01669-250">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="01669-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="01669-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="01669-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="01669-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="01669-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="01669-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="01669-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="01669-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="01669-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="01669-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="01669-256">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="01669-256">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="01669-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="01669-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="01669-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="01669-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="01669-259">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="01669-259">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="01669-260"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="01669-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="01669-261">Windows 95</span><span class="sxs-lookup"><span data-stu-id="01669-261">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="01669-262"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="01669-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="01669-263">Windows 98</span><span class="sxs-lookup"><span data-stu-id="01669-263">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="01669-264"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="01669-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="01669-265">Windows NT</span><span class="sxs-lookup"><span data-stu-id="01669-265">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="01669-266"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="01669-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="01669-267">Windows CE</span><span class="sxs-lookup"><span data-stu-id="01669-267">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="01669-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="01669-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="01669-269">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="01669-269">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="01669-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="01669-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="01669-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="01669-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="01669-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="01669-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="01669-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="01669-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="01669-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="01669-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="01669-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="01669-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="01669-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="01669-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="01669-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="01669-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="01669-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="01669-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="01669-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="01669-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="01669-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="01669-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="01669-281"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="01669-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="01669-282">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="01669-282">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="01669-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="01669-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="01669-284">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="01669-284">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="01669-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="01669-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="01669-286">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="01669-286">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="01669-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="01669-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="01669-288">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="01669-288">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="01669-289"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="01669-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="01669-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="01669-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="01669-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="01669-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="01669-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="01669-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="01669-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="01669-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="01669-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="01669-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="01669-295">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="01669-295">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="01669-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="01669-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="01669-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="01669-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="01669-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="01669-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="01669-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="01669-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="01669-300">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="01669-300">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="01669-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="01669-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="01669-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="01669-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="01669-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="01669-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="01669-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="01669-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="01669-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="01669-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="01669-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="01669-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="01669-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="01669-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="01669-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="01669-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="01669-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="01669-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="01669-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="01669-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="01669-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="01669-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="01669-312">Palm OS</span><span class="sxs-lookup"><span data-stu-id="01669-312">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="01669-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="01669-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="01669-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="01669-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="01669-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="01669-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="01669-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="01669-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="01669-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="01669-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01669-318">**Version**</span><span class="sxs-lookup"><span data-stu-id="01669-318">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01669-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="01669-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01669-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01669-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01669-321">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="01669-321">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="01669-322">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="01669-322">Version of the operation.</span></span>

<span data-ttu-id="01669-323">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="01669-323">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="01669-324"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="01669-324"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="01669-325"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="01669-325"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="01669-326">Diese Eigenschaft wird von der [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="01669-326">This property is inherited from the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01669-327">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01669-327">Remarks</span></span>

<span data-ttu-id="01669-328">Die **CIM \_ videobioselement** -Klasse wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="01669-328">The **CIM\_VideoBIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="01669-329">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="01669-329">WMI does not implement this class.</span></span>

<span data-ttu-id="01669-330">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="01669-330">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01669-331">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="01669-331">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01669-332">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01669-332">Requirements</span></span>



| <span data-ttu-id="01669-333">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01669-333">Requirement</span></span> | <span data-ttu-id="01669-334">Wert</span><span class="sxs-lookup"><span data-stu-id="01669-334">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01669-335">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01669-335">Minimum supported client</span></span><br/> | <span data-ttu-id="01669-336">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01669-336">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01669-337">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01669-337">Minimum supported server</span></span><br/> | <span data-ttu-id="01669-338">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01669-338">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01669-339">Namespace</span><span class="sxs-lookup"><span data-stu-id="01669-339">Namespace</span></span><br/>                | <span data-ttu-id="01669-340">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="01669-340">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01669-341">MOF</span><span class="sxs-lookup"><span data-stu-id="01669-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01669-342"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="01669-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01669-343">DLL</span><span class="sxs-lookup"><span data-stu-id="01669-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01669-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01669-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01669-345">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01669-345">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01669-346">**CIM- \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="01669-346">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

