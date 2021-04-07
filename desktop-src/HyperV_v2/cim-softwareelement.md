---
description: Stellt einen einzeln verwaltbaren oder bereitstell baren Teil eines CIM- \_ Softwarefeature dar.
ms.assetid: 96affc55-b001-4122-b883-3610bf95a786
title: CIM_SoftwareElement-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.Version
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.LanguageEdition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1d11b428e9a17819f850ce210e6854e4f1d17e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758419"
---
# <a name="cim_softwareelement-class-hyper-v-management"></a><span data-ttu-id="9008f-103">CIM_SoftwareElement-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="9008f-103">CIM_SoftwareElement class (Hyper-V management)</span></span>

<span data-ttu-id="9008f-104">Stellt einen einzeln verwaltbaren oder bereitstell baren Teil eines **CIM- \_ Softwarefeature** dar.</span><span class="sxs-lookup"><span data-stu-id="9008f-104">Represents an individually manageable or deployable part of a **CIM\_SoftwareFeature**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9008f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9008f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Application::DeploymentModel"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string Name;
  string Version;
  uint16 SoftwareElementState;
  string SoftwareElementID;
  uint16 TargetOperatingSystem;
  string OtherTargetOS;
  string Manufacturer;
  string BuildNumber;
  string SerialNumber;
  string CodeSet;
  string IdentificationCode;
  string LanguageEdition;
};
```

## <a name="members"></a><span data-ttu-id="9008f-106">Member</span><span class="sxs-lookup"><span data-stu-id="9008f-106">Members</span></span>

<span data-ttu-id="9008f-107">Die **CIM- \_ Softwareelement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9008f-107">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="9008f-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9008f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9008f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9008f-109">Properties</span></span>

<span data-ttu-id="9008f-110">Die **CIM- \_ Softwareelement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9008f-110">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9008f-111">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="9008f-111">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-114">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="9008f-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-115">Der interne Bezeichner für die Kompilierung des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="9008f-115">The internal identifier for the compilation of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-116">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="9008f-116">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9008f-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9008f-120">Die Zeichencodierung, die vom Softwareelement verwendet wird, z. b. UTF-8 und ISO8859-1.</span><span class="sxs-lookup"><span data-stu-id="9008f-120">The character encoding used by the software element, such as UTF-8 and ISO8859-1.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-121">**Identificationcode**</span><span class="sxs-lookup"><span data-stu-id="9008f-121">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| subkomponentensoftware \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="9008f-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-125">Der Hersteller Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="9008f-125">The manufacturer identifier for the software element.</span></span> <span data-ttu-id="9008f-126">Dies ist oft eine Stock Keeping Unit (SKU) oder eine Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="9008f-126">This is often a stock keeping unit (SKU) or a part number.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-127">**Languageedition**</span><span class="sxs-lookup"><span data-stu-id="9008f-127">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| subkomponentensoftware \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="9008f-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-131">Die Language Edition des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="9008f-131">The language edition of the software element.</span></span> <span data-ttu-id="9008f-132">Die im ISO 639-Standard definierten Sprachcodes sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9008f-132">The language codes defined in the ISO 639 standard should be used.</span></span> <span data-ttu-id="9008f-133">Wenn das Element eine mehrsprachige oder internationale Version darstellt, sollte die Zeichenfolge "mehrsprachig" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9008f-133">If the element represents a multi-lingual or international version, the string "Multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-134">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="9008f-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-137">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| subkomponentensoftware \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="9008f-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-138">Der Hersteller des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="9008f-138">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="9008f-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-142">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9008f-142">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9008f-143">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9008f-143">The name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-144">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="9008f-144">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-147">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="9008f-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-148">Hersteller und Betriebs Systemtyp, wenn die Eigenschaft **TargetOperatingSystem** auf **other** ("1") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9008f-148">The manufacturer and operating system type when the **TargetOperatingSystem** property is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="9008f-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="9008f-149">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-152">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="9008f-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-153">Die zugewiesene Seriennummer des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="9008f-153">The assigned serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-154">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9008f-154">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-157">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9008f-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9008f-158">Ein Bezeichner für das Softwareelement, das zusammen mit anderen Schlüsseln verwendet werden soll, um das Element eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9008f-158">An identifier for the software element to use in conjunction with other keys to create a uniquely identify the element.</span></span>

</dd> <dt>

<span data-ttu-id="9008f-159">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9008f-159">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-160">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9008f-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-162">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9008f-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9008f-163">Der Lebenszyklus Status des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="9008f-163">The life cycle state of the software element.</span></span>

<span data-ttu-id="9008f-164">\- Ein Softwareelement im bereitstell baren Zustand beschreibt die Details, die für die erfolgreiche Verteilung erforderlich sind, sowie die Details (Prüfungen und Aktionen), die erforderlich sind, um Sie in den installierbare-Zustand zu verschieben (d. h. der nächste Zustand).</span><span class="sxs-lookup"><span data-stu-id="9008f-164">\- A SoftwareElement in the deployable state describes the details necessary to successfully distribute it and the details (Checks and Actions) required to move it to the installable state (i.e, the next state).</span></span>

<span data-ttu-id="9008f-165">\- Ein Softwareelement im installierbare-Zustand beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Überprüfungen und Aktionen), die zum Erstellen eines Elements im Zustand der ausführbaren Datei (d. h. des nächsten Zustands) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9008f-165">\- A SoftwareElement in the installable state describes the details necessary to successfully install it and the details (Checks and Actions) required to create an element in the executable state (i.e., the next state).</span></span>

<span data-ttu-id="9008f-166">\- Ein Softwareelement im Zustand "ausführbare Datei" beschreibt die für den erfolgreichen Start erforderlichen Details und die Details (Überprüfungen und Aktionen), die erforderlich sind, um es in den Ausführungs Status (d. h. den nächsten Status) zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9008f-166">\- A SoftwareElement in the executable state describes the details necessary to successfully start it and the details (Checks and Actions) required to move it to the running state (i.e., the next state).</span></span>

<span data-ttu-id="9008f-167">\- Ein Softwareelement im Zustand "wird ausgeführt" beschreibt die Details, die zum Verwalten des gestarteten Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9008f-167">\- A SoftwareElement in the running state describes the details necessary to manage the started element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9008f-168">**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="9008f-168">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9008f-169">**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="9008f-169">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9008f-170">**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="9008f-170">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9008f-171">Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="9008f-171">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9008f-172">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9008f-172">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9008f-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-175">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| subkomponentensoftware \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem)".**OSType**")</span><span class="sxs-lookup"><span data-stu-id="9008f-175">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-176">Das Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="9008f-176">The operating system of the software element.</span></span> <span data-ttu-id="9008f-177">Der Wert dieser Eigenschaft stellt nicht sicher, dass es sich um eine binäre ausführbare Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="9008f-177">The value of this property does not ensure that it is binary executable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9008f-178">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9008f-178">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9008f-179">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9008f-179">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9008f-180">**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="9008f-180">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9008f-181">**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="9008f-181">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9008f-182">**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="9008f-182">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9008f-183">**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="9008f-183">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Tru64_UNIX"></span><span id="tru64_unix"></span><span id="TRU64_UNIX"></span>

<span data-ttu-id="9008f-184">**Tru64 UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="9008f-184">**Tru64 UNIX** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9008f-185">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="9008f-185">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9008f-186">**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="9008f-186">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9008f-187">**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="9008f-187">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9008f-188">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="9008f-188">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9008f-189">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="9008f-189">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9008f-190">**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="9008f-190">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9008f-191">**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="9008f-191">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9008f-192">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="9008f-192">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9008f-193">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="9008f-193">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9008f-194">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="9008f-194">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9008f-195">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="9008f-195">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9008f-196">**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="9008f-196">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9008f-197">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="9008f-197">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9008f-198">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="9008f-198">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9008f-199">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="9008f-199">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9008f-200">**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="9008f-200">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9008f-201">**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="9008f-201">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9008f-202">**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="9008f-202">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9008f-203">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="9008f-203">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9008f-204">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="9008f-204">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9008f-205">**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="9008f-205">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9008f-206">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="9008f-206">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9008f-207">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="9008f-207">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9008f-208">**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="9008f-208">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9008f-209">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="9008f-209">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9008f-210">**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="9008f-210">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OS"></span><span id="hp_nonstop_os"></span><span id="HP_NONSTOP_OS"></span>

<span data-ttu-id="9008f-211">**HP-nonstop-Betriebssystem** (33)</span><span class="sxs-lookup"><span data-stu-id="9008f-211">**HP NonStop OS** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OSS"></span><span id="hp_nonstop_oss"></span><span id="HP_NONSTOP_OSS"></span>

<span data-ttu-id="9008f-212">**HP nonstop OSS** (34)</span><span class="sxs-lookup"><span data-stu-id="9008f-212">**HP NonStop OSS** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9008f-213">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="9008f-213">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9008f-214">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="9008f-214">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9008f-215">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="9008f-215">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9008f-216">**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="9008f-216">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM"></span><span id="vm"></span>

<span data-ttu-id="9008f-217">**VM** (39)</span><span class="sxs-lookup"><span data-stu-id="9008f-217">**VM** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9008f-218">**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="9008f-218">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9008f-219">**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="9008f-219">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9008f-220">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="9008f-220">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9008f-221">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="9008f-221">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9008f-222">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="9008f-222">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9008f-223">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="9008f-223">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9008f-224">**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="9008f-224">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9008f-225">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="9008f-225">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9008f-226">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="9008f-226">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9008f-227">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="9008f-227">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9008f-228">**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="9008f-228">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9008f-229">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="9008f-229">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9008f-230">**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="9008f-230">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9008f-231">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="9008f-231">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9008f-232">**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="9008f-232">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9008f-233">**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="9008f-233">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9008f-234">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="9008f-234">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9008f-235">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="9008f-235">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9008f-236">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="9008f-236">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9008f-237">**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="9008f-237">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="9008f-238">**Betriebssystem/390** (60)</span><span class="sxs-lookup"><span data-stu-id="9008f-238">**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9008f-239">**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="9008f-239">**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9008f-240">**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="9008f-240">**TPF** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows__R__Me"></span><span id="windows__r__me"></span><span id="WINDOWS__R__ME"></span>

<span data-ttu-id="9008f-241">**Windows (R) Me** (63)</span><span class="sxs-lookup"><span data-stu-id="9008f-241">**Windows (R) Me** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Caldera_Open_UNIX"></span><span id="caldera_open_unix"></span><span id="CALDERA_OPEN_UNIX"></span>

<span data-ttu-id="9008f-242">" **Caldera Open Unix** (64)"</span><span class="sxs-lookup"><span data-stu-id="9008f-242">**Caldera Open UNIX** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenBSD"></span><span id="openbsd"></span><span id="OPENBSD"></span>

<span data-ttu-id="9008f-243">**OpenBSD** (65)</span><span class="sxs-lookup"><span data-stu-id="9008f-243">**OpenBSD** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9008f-244">**Nicht zutreffend** (66)</span><span class="sxs-lookup"><span data-stu-id="9008f-244">**Not Applicable** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP"></span><span id="windows_xp"></span><span id="WINDOWS_XP"></span>

<span data-ttu-id="9008f-245">**Windows XP** (67)</span><span class="sxs-lookup"><span data-stu-id="9008f-245">**Windows XP** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="z_OS"></span><span id="z_os"></span><span id="Z_OS"></span>

<span data-ttu-id="9008f-246">**z/OS** (68)</span><span class="sxs-lookup"><span data-stu-id="9008f-246">**z/OS** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003"></span><span id="microsoft_windows_server_2003"></span><span id="MICROSOFT_WINDOWS_SERVER_2003"></span>

<span data-ttu-id="9008f-247">**Microsoft Windows Server 2003** (69)</span><span class="sxs-lookup"><span data-stu-id="9008f-247">**Microsoft Windows Server 2003** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003_64-Bit"></span><span id="microsoft_windows_server_2003_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2003_64-BIT"></span>

<span data-ttu-id="9008f-248">**Microsoft Windows Server 2003 64-Bit** (70)</span><span class="sxs-lookup"><span data-stu-id="9008f-248">**Microsoft Windows Server 2003 64-Bit** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP_64-Bit"></span><span id="windows_xp_64-bit"></span><span id="WINDOWS_XP_64-BIT"></span>

<span data-ttu-id="9008f-249">**Windows XP 64 Bit** (71)</span><span class="sxs-lookup"><span data-stu-id="9008f-249">**Windows XP 64-Bit** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP_Embedded"></span><span id="windows_xp_embedded"></span><span id="WINDOWS_XP_EMBEDDED"></span>

<span data-ttu-id="9008f-250">**Windows XP Embedded** (72)</span><span class="sxs-lookup"><span data-stu-id="9008f-250">**Windows XP Embedded** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Vista"></span><span id="windows_vista"></span><span id="WINDOWS_VISTA"></span>

<span data-ttu-id="9008f-251">**Windows Vista** (73)</span><span class="sxs-lookup"><span data-stu-id="9008f-251">**Windows Vista** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Vista_64-Bit"></span><span id="windows_vista_64-bit"></span><span id="WINDOWS_VISTA_64-BIT"></span>

<span data-ttu-id="9008f-252">**Windows Vista 64 Bit** (74)</span><span class="sxs-lookup"><span data-stu-id="9008f-252">**Windows Vista 64-Bit** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Embedded_for_Point_of_Service"></span><span id="windows_embedded_for_point_of_service"></span><span id="WINDOWS_EMBEDDED_FOR_POINT_OF_SERVICE"></span>

<span data-ttu-id="9008f-253">**Windows Embedded für Point of Service** (75)</span><span class="sxs-lookup"><span data-stu-id="9008f-253">**Windows Embedded for Point of Service** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008"></span><span id="microsoft_windows_server_2008"></span><span id="MICROSOFT_WINDOWS_SERVER_2008"></span>

<span data-ttu-id="9008f-254">**Microsoft Windows Server 2008** (76)</span><span class="sxs-lookup"><span data-stu-id="9008f-254">**Microsoft Windows Server 2008** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_64-Bit"></span><span id="microsoft_windows_server_2008_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_64-BIT"></span>

<span data-ttu-id="9008f-255">**Microsoft Windows Server 2008 64-Bit** (77)</span><span class="sxs-lookup"><span data-stu-id="9008f-255">**Microsoft Windows Server 2008 64-Bit** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD_64-Bit"></span><span id="freebsd_64-bit"></span><span id="FREEBSD_64-BIT"></span>

<span data-ttu-id="9008f-256">**FreeBSD 64-Bit** (78)</span><span class="sxs-lookup"><span data-stu-id="9008f-256">**FreeBSD 64-Bit** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux"></span><span id="redhat_enterprise_linux"></span><span id="REDHAT_ENTERPRISE_LINUX"></span>

<span data-ttu-id="9008f-257">**RedHat Enterprise Linux** (79)</span><span class="sxs-lookup"><span data-stu-id="9008f-257">**RedHat Enterprise Linux** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux_64-Bit"></span><span id="redhat_enterprise_linux_64-bit"></span><span id="REDHAT_ENTERPRISE_LINUX_64-BIT"></span>

<span data-ttu-id="9008f-258">**RedHat Enterprise Linux 64-Bit** (80)</span><span class="sxs-lookup"><span data-stu-id="9008f-258">**RedHat Enterprise Linux 64-Bit** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris_64-Bit"></span><span id="solaris_64-bit"></span><span id="SOLARIS_64-BIT"></span>

<span data-ttu-id="9008f-259">**Solaris 64 Bit** (81)</span><span class="sxs-lookup"><span data-stu-id="9008f-259">**Solaris 64-Bit** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="SUSE"></span><span id="suse"></span>

<span data-ttu-id="9008f-260">**SUSE** (82)</span><span class="sxs-lookup"><span data-stu-id="9008f-260">**SUSE** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="SUSE_64-Bit"></span><span id="suse_64-bit"></span><span id="SUSE_64-BIT"></span>

<span data-ttu-id="9008f-261">**SUSE 64-Bit** (83)</span><span class="sxs-lookup"><span data-stu-id="9008f-261">**SUSE 64-Bit** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="SLES"></span><span id="sles"></span>

<span data-ttu-id="9008f-262">**SLES** (84)</span><span class="sxs-lookup"><span data-stu-id="9008f-262">**SLES** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="SLES_64-Bit"></span><span id="sles_64-bit"></span><span id="SLES_64-BIT"></span>

<span data-ttu-id="9008f-263">**SLES 64-Bit** (85)</span><span class="sxs-lookup"><span data-stu-id="9008f-263">**SLES 64-Bit** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Novell_OES"></span><span id="novell_oes"></span><span id="NOVELL_OES"></span>

<span data-ttu-id="9008f-264">**Novell-OES** (86)</span><span class="sxs-lookup"><span data-stu-id="9008f-264">**Novell OES** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Novell_Linux_Desktop"></span><span id="novell_linux_desktop"></span><span id="NOVELL_LINUX_DESKTOP"></span>

<span data-ttu-id="9008f-265">**Novell Linux-Desktop** (87)</span><span class="sxs-lookup"><span data-stu-id="9008f-265">**Novell Linux Desktop** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Sun_Java_Desktop_System"></span><span id="sun_java_desktop_system"></span><span id="SUN_JAVA_DESKTOP_SYSTEM"></span>

<span data-ttu-id="9008f-266">**Sun Java Desktop System** (88)</span><span class="sxs-lookup"><span data-stu-id="9008f-266">**Sun Java Desktop System** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Mandriva"></span><span id="mandriva"></span><span id="MANDRIVA"></span>

<span data-ttu-id="9008f-267">**Mandriva** (89)</span><span class="sxs-lookup"><span data-stu-id="9008f-267">**Mandriva** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Mandriva_64-Bit"></span><span id="mandriva_64-bit"></span><span id="MANDRIVA_64-BIT"></span>

<span data-ttu-id="9008f-268">**Mandriva 64 Bit** (90)</span><span class="sxs-lookup"><span data-stu-id="9008f-268">**Mandriva 64-Bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboLinux"></span><span id="turbolinux"></span><span id="TURBOLINUX"></span>

<span data-ttu-id="9008f-269">**Turbolinux** (91)</span><span class="sxs-lookup"><span data-stu-id="9008f-269">**TurboLinux** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboLinux_64-Bit"></span><span id="turbolinux_64-bit"></span><span id="TURBOLINUX_64-BIT"></span>

<span data-ttu-id="9008f-270">**Turbolinux 64 Bit** (92)</span><span class="sxs-lookup"><span data-stu-id="9008f-270">**TurboLinux 64-Bit** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Ubuntu"></span><span id="ubuntu"></span><span id="UBUNTU"></span>

<span data-ttu-id="9008f-271">**Ubuntu** (93)</span><span class="sxs-lookup"><span data-stu-id="9008f-271">**Ubuntu** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Ubuntu_64-Bit"></span><span id="ubuntu_64-bit"></span><span id="UBUNTU_64-BIT"></span>

<span data-ttu-id="9008f-272">**Ubuntu 64-Bit** (94)</span><span class="sxs-lookup"><span data-stu-id="9008f-272">**Ubuntu 64-Bit** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Debian"></span><span id="debian"></span><span id="DEBIAN"></span>

<span data-ttu-id="9008f-273">**Debian** (95)</span><span class="sxs-lookup"><span data-stu-id="9008f-273">**Debian** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Debian_64-Bit"></span><span id="debian_64-bit"></span><span id="DEBIAN_64-BIT"></span>

<span data-ttu-id="9008f-274">**Debian 64-Bit** (96)</span><span class="sxs-lookup"><span data-stu-id="9008f-274">**Debian 64-Bit** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x"></span><span id="linux_2.4.x"></span><span id="LINUX_2.4.X"></span>

<span data-ttu-id="9008f-275">**Linux 2.4. x** (97)</span><span class="sxs-lookup"><span data-stu-id="9008f-275">**Linux 2.4.x** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x_64-Bit"></span><span id="linux_2.4.x_64-bit"></span><span id="LINUX_2.4.X_64-BIT"></span>

<span data-ttu-id="9008f-276">**Linux 2.4. x 64 Bit** (98)</span><span class="sxs-lookup"><span data-stu-id="9008f-276">**Linux 2.4.x 64-Bit** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x"></span><span id="linux_2.6.x"></span><span id="LINUX_2.6.X"></span>

<span data-ttu-id="9008f-277">**Linux 2.6. x** (99)</span><span class="sxs-lookup"><span data-stu-id="9008f-277">**Linux 2.6.x** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x_64-Bit"></span><span id="linux_2.6.x_64-bit"></span><span id="LINUX_2.6.X_64-BIT"></span>

<span data-ttu-id="9008f-278">**Linux 2.6. x 64 Bit** (100)</span><span class="sxs-lookup"><span data-stu-id="9008f-278">**Linux 2.6.x 64-Bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_64-Bit"></span><span id="linux_64-bit"></span><span id="LINUX_64-BIT"></span>

<span data-ttu-id="9008f-279">**Linux 64-Bit** (101)</span><span class="sxs-lookup"><span data-stu-id="9008f-279">**Linux 64-Bit** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_64-Bit"></span><span id="other_64-bit"></span><span id="OTHER_64-BIT"></span>

<span data-ttu-id="9008f-280">**Sonstige 64-Bit-** Version (102)</span><span class="sxs-lookup"><span data-stu-id="9008f-280">**Other 64-Bit** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_R2"></span><span id="microsoft_windows_server_2008_r2"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_R2"></span>

<span data-ttu-id="9008f-281">**Microsoft Windows Server 2008 R2** (103)</span><span class="sxs-lookup"><span data-stu-id="9008f-281">**Microsoft Windows Server 2008 R2** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="VMware_ESXi"></span><span id="vmware_esxi"></span><span id="VMWARE_ESXI"></span>

<span data-ttu-id="9008f-282">**VMware ESXi** (104)</span><span class="sxs-lookup"><span data-stu-id="9008f-282">**VMware ESXi** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_7"></span><span id="microsoft_windows_7"></span><span id="MICROSOFT_WINDOWS_7"></span>

<span data-ttu-id="9008f-283">**Microsoft Windows 7** (105)</span><span class="sxs-lookup"><span data-stu-id="9008f-283">**Microsoft Windows 7** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="CentOS_32-bit"></span><span id="centos_32-bit"></span><span id="CENTOS_32-BIT"></span>

<span data-ttu-id="9008f-284">**CentOS 32 Bit** (106)</span><span class="sxs-lookup"><span data-stu-id="9008f-284">**CentOS 32-bit** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="CentOS_64-bit"></span><span id="centos_64-bit"></span><span id="CENTOS_64-BIT"></span>

<span data-ttu-id="9008f-285">**CentOS 64 Bit** (107)</span><span class="sxs-lookup"><span data-stu-id="9008f-285">**CentOS 64-bit** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_32-bit"></span><span id="oracle_enterprise_linux_32-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_32-BIT"></span>

<span data-ttu-id="9008f-286">**Oracle Enterprise Linux 32-Bit** (108)</span><span class="sxs-lookup"><span data-stu-id="9008f-286">**Oracle Enterprise Linux 32-bit** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_64-bit"></span><span id="oracle_enterprise_linux_64-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_64-BIT"></span>

<span data-ttu-id="9008f-287">**Oracle Enterprise Linux 64-Bit** (109)</span><span class="sxs-lookup"><span data-stu-id="9008f-287">**Oracle Enterprise Linux 64-bit** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="eComStation_32-bitx"></span><span id="ecomstation_32-bitx"></span><span id="ECOMSTATION_32-BITX"></span>

<span data-ttu-id="9008f-288">**eComStation 32-bitx** (110)</span><span class="sxs-lookup"><span data-stu-id="9008f-288">**eComStation 32-bitx** (110)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9008f-289">**Version**</span><span class="sxs-lookup"><span data-stu-id="9008f-289">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9008f-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9008f-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9008f-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9008f-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9008f-292">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| subkomponentensoftware \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="9008f-292">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software \|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="9008f-293">Die Softwareversion im Format *<Major>* . *<Minor>\*\*<Revision>*</span><span class="sxs-lookup"><span data-stu-id="9008f-293">The software version in the format *<Major>*.*<Minor>*.*<Revision>*</span></span> <span data-ttu-id="9008f-294">oder *<Major>* . *<Minor><letter><revision>* .</span><span class="sxs-lookup"><span data-stu-id="9008f-294">or *<Major>*.*<Minor><letter><revision>*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9008f-295">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9008f-295">Requirements</span></span>



| <span data-ttu-id="9008f-296">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9008f-296">Requirement</span></span> | <span data-ttu-id="9008f-297">Wert</span><span class="sxs-lookup"><span data-stu-id="9008f-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9008f-298">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9008f-298">Minimum supported client</span></span><br/> | <span data-ttu-id="9008f-299">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9008f-299">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9008f-300">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9008f-300">Minimum supported server</span></span><br/> | <span data-ttu-id="9008f-301">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9008f-301">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9008f-302">Namespace</span><span class="sxs-lookup"><span data-stu-id="9008f-302">Namespace</span></span><br/>                | <span data-ttu-id="9008f-303">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9008f-303">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9008f-304">MOF</span><span class="sxs-lookup"><span data-stu-id="9008f-304">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9008f-305"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9008f-305"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9008f-306">DLL</span><span class="sxs-lookup"><span data-stu-id="9008f-306">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9008f-307"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9008f-307"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9008f-308">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9008f-308">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9008f-309">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="9008f-309">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

