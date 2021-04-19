---
description: Die CIM- \_ Softwarefeature-Klasse stellt eine bestimmte Funktion oder Funktion eines Produkts oder Anwendungs Systems dar.
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: CIM_SoftwareFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342745"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="77cb1-103">CIM- \_ Softwarefeature-Klasse</span><span class="sxs-lookup"><span data-stu-id="77cb1-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="77cb1-104">Die **CIM- \_ Softwarefeature** -Klasse stellt eine bestimmte Funktion oder Funktion eines Produkts oder Anwendungs Systems dar.</span><span class="sxs-lookup"><span data-stu-id="77cb1-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="77cb1-105">Diese Klasse reflektiert eine Ebene der Granularität, die für einen Benutzer eines Produkts anstelle der Einheiten, die die Erstellung oder Verpackung des Produkts widerspiegeln (aufgezeichnet mithilfe einer CIM- [**\_ Softwareelement**](cim-softwareelement.md) -Klasse), sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="77cb1-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="77cb1-106">Wenn eine Software Funktion auf mehreren Plattformen oder Betriebssystemen vorhanden sein kann, handelt es sich bei der Software Funktion um eine Sammlung von Software Elementen für die unterschiedlichen Plattformen.</span><span class="sxs-lookup"><span data-stu-id="77cb1-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="77cb1-107">In diesem Fall sind die Benutzer des Modells in der Regel an einer Untersammlung der Software Elemente interessiert, die für eine bestimmte Plattform erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="77cb1-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="77cb1-108">Da Features über Produkte übermittelt werden, werden Software Features immer im Kontext einer CIM- [**\_ Produkt**](cim-product.md) Klasse definiert, die die [**CIM- \_ productsoftwarefeatures**](cim-productsoftwarefeatures.md) -Zuordnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="77cb1-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="77cb1-109">Optional können Software Features von einem oder mehreren Produkten mithilfe der [**CIM \_ applicationsystemsoftwarefeature-Zuordnung**](cim-applicationsystemsoftwarefeature.md) in Anwendungssysteme organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="77cb1-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77cb1-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="77cb1-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="77cb1-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="77cb1-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="77cb1-112">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="77cb1-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="77cb1-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="77cb1-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="77cb1-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="77cb1-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="77cb1-115">Member</span><span class="sxs-lookup"><span data-stu-id="77cb1-115">Members</span></span>

<span data-ttu-id="77cb1-116">Die **CIM- \_ Softwarefeature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="77cb1-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="77cb1-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77cb1-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77cb1-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77cb1-118">Properties</span></span>

<span data-ttu-id="77cb1-119">Die **CIM- \_ Softwarefeature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="77cb1-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77cb1-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="77cb1-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-123">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="77cb1-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-124">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="77cb1-124">Short textual description of the object.</span></span>

<span data-ttu-id="77cb1-125">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="77cb1-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77cb1-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-129">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="77cb1-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-130">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="77cb1-130">Textual description of the object.</span></span>

<span data-ttu-id="77cb1-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="77cb1-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="77cb1-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-135">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Identifyingnumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="77cb1-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-136">Produktidentifizierung, z. b. eine Seriennummer auf Software oder eine Zahl auf einem Hardware Chip.</span><span class="sxs-lookup"><span data-stu-id="77cb1-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="77cb1-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="77cb1-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="77cb1-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-141">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="77cb1-141">Date and time the object was installed.</span></span> <span data-ttu-id="77cb1-142">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="77cb1-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="77cb1-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="77cb1-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="77cb1-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-147">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="77cb1-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-148">Die Bezeichnung, mit der das Objekt außerhalb des Datenverarbeitungssystems bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="77cb1-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="77cb1-149">Die Bezeichnung ist ein lesbarer Name, der das Element im Kontext des Namespace des Elements eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="77cb1-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="77cb1-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="77cb1-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="77cb1-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-154">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="77cb1-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-155">Häufig verwendeter Produktname.</span><span class="sxs-lookup"><span data-stu-id="77cb1-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="77cb1-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-159">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="77cb1-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-160">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="77cb1-160">Current status of the object.</span></span>

<span data-ttu-id="77cb1-161">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="77cb1-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="77cb1-162">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="77cb1-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="77cb1-163">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="77cb1-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="77cb1-164">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="77cb1-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="77cb1-165">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="77cb1-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="77cb1-166">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="77cb1-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="77cb1-167">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="77cb1-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="77cb1-168">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="77cb1-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="77cb1-169">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="77cb1-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="77cb1-170">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="77cb1-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="77cb1-171">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="77cb1-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="77cb1-172">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="77cb1-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="77cb1-173">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="77cb1-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="77cb1-174">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="77cb1-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="77cb1-175">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="77cb1-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-178">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Vendor**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="77cb1-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-179">Der Name des Lieferanten des Produkts, der der **Vendor** -Eigenschaft im Product-Objekt des DMTF-Lösungs Austausch Standards entspricht.</span><span class="sxs-lookup"><span data-stu-id="77cb1-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="77cb1-180">**Version**</span><span class="sxs-lookup"><span data-stu-id="77cb1-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cb1-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="77cb1-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="77cb1-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cb1-183">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="77cb1-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="77cb1-184">Produkt Versionsinformationen, die der **Version** -Eigenschaft im Product-Objekt des DMTF-Lösungs Austausch Standards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="77cb1-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77cb1-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77cb1-185">Remarks</span></span>

<span data-ttu-id="77cb1-186">Die **CIM- \_ Softwarefeature** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="77cb1-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="77cb1-187">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="77cb1-187">WMI does not implement this class.</span></span> <span data-ttu-id="77cb1-188">Informationen zu WMI-Klassen, die von **CIM \_ Software Feature** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="77cb1-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="77cb1-189">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="77cb1-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="77cb1-190">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="77cb1-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="77cb1-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77cb1-191">Requirements</span></span>



| <span data-ttu-id="77cb1-192">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77cb1-192">Requirement</span></span> | <span data-ttu-id="77cb1-193">Wert</span><span class="sxs-lookup"><span data-stu-id="77cb1-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77cb1-194">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77cb1-194">Minimum supported client</span></span><br/> | <span data-ttu-id="77cb1-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77cb1-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77cb1-196">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77cb1-196">Minimum supported server</span></span><br/> | <span data-ttu-id="77cb1-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77cb1-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77cb1-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="77cb1-198">Namespace</span></span><br/>                | <span data-ttu-id="77cb1-199">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="77cb1-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77cb1-200">MOF</span><span class="sxs-lookup"><span data-stu-id="77cb1-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77cb1-201"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="77cb1-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77cb1-202">DLL</span><span class="sxs-lookup"><span data-stu-id="77cb1-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77cb1-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77cb1-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77cb1-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77cb1-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77cb1-205">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="77cb1-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

