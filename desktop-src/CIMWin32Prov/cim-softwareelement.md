---
description: Die CIM- \_ Softwareelement-Klasse zerlegt ein CIM- \_ Softwarefeature-Objekt in einen Satz individuell verwaltbarer oder bereitstell barer Teile für eine bestimmte Plattform.
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: CIM_SoftwareElement-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126932"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="07797-103">CIM_SoftwareElement-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="07797-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="07797-104">Die **CIM- \_ Softwareelement** -Klasse zerlegt ein [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Objekt in einen Satz individuell verwaltbarer oder bereitstell barer Teile für eine bestimmte Plattform.</span><span class="sxs-lookup"><span data-stu-id="07797-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="07797-105">Die Plattform eines Software Elements wird durch die zugrunde liegende Hardwarearchitektur und das Betriebssystem eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="07797-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="07797-106">Um die Details zu verstehen, wie die Funktionalität eines bestimmten Software Features auf einer bestimmten Plattform bereitgestellt wird, werden die **CIM- \_ Softwareelement** -Objekte, auf die von [**CIM \_ softwarefeaturesoftwareelements**](cim-softwarefeaturesoftwareelements.md) -Zuordnungen verwiesen wird, basierend auf der **TargetOperatingSystem** -Eigenschaft in Zusammenhang losen Sets organisiert.</span><span class="sxs-lookup"><span data-stu-id="07797-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="07797-107">Ein **CIM \_ Softwareelement** -Objekt erfasst die Verwaltungs Details eines Teils oder einer Komponente in einem von vier Zuständen, die von der **SoftwareElementState** -Eigenschaft gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="07797-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07797-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07797-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="07797-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="07797-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="07797-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07797-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="07797-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="07797-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07797-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="07797-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
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

## <a name="members"></a><span data-ttu-id="07797-113">Member</span><span class="sxs-lookup"><span data-stu-id="07797-113">Members</span></span>

<span data-ttu-id="07797-114">Die **CIM- \_ Softwareelement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="07797-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="07797-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07797-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07797-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07797-116">Properties</span></span>

<span data-ttu-id="07797-117">Die **CIM- \_ Softwareelement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07797-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07797-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="07797-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="07797-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="07797-122">Interner Bezeichner für die Kompilierung dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="07797-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="07797-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="07797-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-126">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="07797-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="07797-127">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="07797-127">Short textual description of the object.</span></span>

<span data-ttu-id="07797-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07797-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07797-129">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="07797-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-132">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="07797-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="07797-133">Vom Softwareelement verwendeter Codesatz.</span><span class="sxs-lookup"><span data-stu-id="07797-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="07797-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07797-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-137">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="07797-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="07797-138">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="07797-138">Textual description of the object.</span></span>

<span data-ttu-id="07797-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07797-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07797-140">**Identificationcode**</span><span class="sxs-lookup"><span data-stu-id="07797-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-143">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="07797-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="07797-144">Der Bezeichner des Herstellers für das Softwareelement, häufig eine Stock Keeping Unit (SKU) oder eine Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="07797-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="07797-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07797-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="07797-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07797-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="07797-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="07797-149">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="07797-149">Date and time the object was installed.</span></span> <span data-ttu-id="07797-150">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="07797-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="07797-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07797-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07797-152">**Languageedition**</span><span class="sxs-lookup"><span data-stu-id="07797-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-155">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="07797-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="07797-156">Language Edition des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="07797-156">Language edition of the software element.</span></span> <span data-ttu-id="07797-157">Die in ISO 639 definierten Sprachcodes sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07797-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="07797-158">Wenn das Softwareelement mehrsprachige oder internationale Versionen eines Produkts darstellt, sollte die Zeichenfolge "mehrsprachig" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07797-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="07797-159">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="07797-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="07797-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="07797-163">Hersteller des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="07797-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="07797-164">**Name**</span><span class="sxs-lookup"><span data-stu-id="07797-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-167">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="07797-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="07797-168">Name, der zum Identifizieren des Software Elements verwendet wird, das diese Eigenschaft von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="07797-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07797-169">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="07797-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="07797-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="07797-173">Hersteller und Betriebs Systemtyp für ein Softwareelement, wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 hat ("Other").</span><span class="sxs-lookup"><span data-stu-id="07797-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="07797-174">Wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 aufweist, muss diese Eigenschaft einen Wert aufweisen, der nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="07797-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="07797-175">Für alle anderen **TargetOperatingSystem** -Werte ist diese Eigenschaft NULL.</span><span class="sxs-lookup"><span data-stu-id="07797-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="07797-176">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="07797-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-179">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="07797-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="07797-180">Seriennummer des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="07797-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="07797-181">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="07797-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-184">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="07797-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="07797-185">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="07797-185">Identifier for the software element.</span></span> <span data-ttu-id="07797-186">Es ist für die Verwendung in Verbindung mit anderen Schlüsseln konzipiert, um eine eindeutige Darstellung dieses **CIM- \_ Softwareelement** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07797-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="07797-187">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="07797-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-188">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07797-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07797-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-190">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07797-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07797-191">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="07797-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="07797-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="07797-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="07797-193">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07797-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="07797-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="07797-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="07797-195">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07797-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="07797-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="07797-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="07797-197">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07797-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="07797-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="07797-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07797-199">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="07797-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07797-200">**Status**</span><span class="sxs-lookup"><span data-stu-id="07797-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-203">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="07797-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="07797-204">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="07797-204">Current status of the object.</span></span>

<span data-ttu-id="07797-205">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07797-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="07797-206">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="07797-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="07797-207">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="07797-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="07797-208">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="07797-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07797-209">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="07797-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07797-210">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="07797-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="07797-211">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="07797-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="07797-212">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="07797-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="07797-213">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="07797-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="07797-214">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="07797-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="07797-215">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="07797-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="07797-216">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="07797-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="07797-217">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="07797-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="07797-218">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="07797-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07797-219">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="07797-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-220">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07797-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07797-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-222">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Komponenten Informationen \| 002,5 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**OSType**")</span><span class="sxs-lookup"><span data-stu-id="07797-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="07797-223">Betriebssystemumgebung.</span><span class="sxs-lookup"><span data-stu-id="07797-223">Operating system environment.</span></span> <span data-ttu-id="07797-224">Der Wert dieser Eigenschaft gewährleistet nicht die binäre executabilität, es sind weitere Informationen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07797-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="07797-225">Die Betriebssystemversion muss mithilfe der Überprüfung der Betriebssystemversion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="07797-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="07797-226">Außerdem ist die Architektur, in der das Betriebssystem ausgeführt wird, erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07797-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="07797-227">Die Kombination dieser Konstrukte ermöglicht es dem Anbieter, die für ein bestimmtes Softwareelement erforderliche Betriebssystemebene eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="07797-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07797-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="07797-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07797-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="07797-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="07797-230"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="07797-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="07797-231">Mac OS</span><span class="sxs-lookup"><span data-stu-id="07797-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="07797-232"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="07797-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07797-233">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="07797-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="07797-234"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="07797-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="07797-235"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="07797-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="07797-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="07797-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="07797-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="07797-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="07797-238">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="07797-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="07797-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="07797-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="07797-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="07797-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="07797-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="07797-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="07797-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="07797-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="07797-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="07797-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="07797-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="07797-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="07797-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="07797-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="07797-246">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="07797-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="07797-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="07797-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="07797-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="07797-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="07797-249">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="07797-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="07797-250"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="07797-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="07797-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="07797-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="07797-252"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="07797-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="07797-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="07797-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="07797-254"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="07797-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="07797-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="07797-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="07797-256"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="07797-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="07797-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="07797-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="07797-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="07797-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="07797-259">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="07797-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="07797-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="07797-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="07797-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="07797-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="07797-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="07797-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="07797-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="07797-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="07797-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="07797-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="07797-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="07797-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="07797-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="07797-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="07797-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="07797-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="07797-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="07797-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="07797-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="07797-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="07797-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="07797-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="07797-271"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="07797-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="07797-272">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="07797-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="07797-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="07797-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="07797-274">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="07797-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="07797-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="07797-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="07797-276">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="07797-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="07797-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="07797-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="07797-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="07797-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="07797-279"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="07797-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="07797-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="07797-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="07797-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="07797-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="07797-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="07797-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="07797-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="07797-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="07797-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="07797-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="07797-285">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="07797-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="07797-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="07797-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="07797-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="07797-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="07797-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="07797-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="07797-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="07797-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="07797-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="07797-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="07797-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="07797-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="07797-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="07797-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="07797-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="07797-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="07797-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="07797-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="07797-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="07797-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="07797-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="07797-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="07797-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="07797-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="07797-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="07797-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="07797-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="07797-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="07797-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="07797-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="07797-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="07797-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="07797-302">Palm OS</span><span class="sxs-lookup"><span data-stu-id="07797-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="07797-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="07797-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="07797-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="07797-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="07797-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="07797-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="07797-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="07797-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="07797-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="07797-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07797-308">**Version**</span><span class="sxs-lookup"><span data-stu-id="07797-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07797-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07797-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07797-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07797-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07797-311">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="07797-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="07797-312">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="07797-312">Version of the operation.</span></span>

<span data-ttu-id="07797-313">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="07797-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="07797-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="07797-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="07797-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="07797-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07797-316">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07797-316">Remarks</span></span>

<span data-ttu-id="07797-317">Die **CIM- \_ Softwareelement** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="07797-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="07797-318">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="07797-318">WMI does not implement this class.</span></span> <span data-ttu-id="07797-319">Informationen zu WMI-Klassen, die von **CIM \_ Softwareelement** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="07797-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="07797-320">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="07797-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="07797-321">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="07797-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="07797-322">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07797-322">Requirements</span></span>



| <span data-ttu-id="07797-323">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07797-323">Requirement</span></span> | <span data-ttu-id="07797-324">Wert</span><span class="sxs-lookup"><span data-stu-id="07797-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07797-325">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07797-325">Minimum supported client</span></span><br/> | <span data-ttu-id="07797-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07797-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07797-327">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07797-327">Minimum supported server</span></span><br/> | <span data-ttu-id="07797-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07797-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07797-329">Namespace</span><span class="sxs-lookup"><span data-stu-id="07797-329">Namespace</span></span><br/>                | <span data-ttu-id="07797-330">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07797-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07797-331">MOF</span><span class="sxs-lookup"><span data-stu-id="07797-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07797-332"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="07797-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07797-333">DLL</span><span class="sxs-lookup"><span data-stu-id="07797-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07797-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07797-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07797-335">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07797-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07797-336">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="07797-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

