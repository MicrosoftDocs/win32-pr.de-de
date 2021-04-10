---
description: Die CIM \_ softwareelementversioncheck-Klasse stellt einen Typ von Softwareelement dar, der in der Umgebung vorhanden sein muss.
ms.assetid: a1c0f0d5-2586-499c-bd82-bbb107570d81
ms.tgt_platform: multiple
title: CIM_SoftwareElementVersionCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck
- CIM_SoftwareElementVersionCheck.Caption
- CIM_SoftwareElementVersionCheck.CheckID
- CIM_SoftwareElementVersionCheck.CheckMode
- CIM_SoftwareElementVersionCheck.Description
- CIM_SoftwareElementVersionCheck.LowerSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Name
- CIM_SoftwareElementVersionCheck.SoftwareElementID
- CIM_SoftwareElementVersionCheck.SoftwareElementName
- CIM_SoftwareElementVersionCheck.SoftwareElementState
- CIM_SoftwareElementVersionCheck.SoftwareElementStateDesired
- CIM_SoftwareElementVersionCheck.TargetOperatingSystem
- CIM_SoftwareElementVersionCheck.TargetOperatingSystemDesired
- CIM_SoftwareElementVersionCheck.UpperSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb55a44a3aba9092567cdc91b668ba1b63e33174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214035"
---
# <a name="cim_softwareelementversioncheck-class"></a><span data-ttu-id="ff1f4-103">CIM- \_ softwareelementversioncheck-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff1f4-103">CIM\_SoftwareElementVersionCheck class</span></span>

<span data-ttu-id="ff1f4-104">Die **CIM \_ softwareelementversioncheck** -Klasse stellt einen Typ von Softwareelement dar, der in der Umgebung vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-104">The **CIM\_SoftwareElementVersionCheck** class represents a type of software element that must exist in the environment.</span></span> <span data-ttu-id="ff1f4-105">Diese Überprüfung kann für ein bestimmtes, maximales, maximales oder einen Bereich von Versionen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-105">This check can be for a specific, minimum, maximum, or a range of versions.</span></span> <span data-ttu-id="ff1f4-106">Um eine bestimmte Version anzugeben, müssen die unter-und die obere Version identisch sein.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-106">To specify a specific version, the lower and upper versions must be the same.</span></span> <span data-ttu-id="ff1f4-107">Geben Sie nur die niedrigere Version an, um eine Mindestversion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-107">To specify a minimum version, specify only the lower version.</span></span> <span data-ttu-id="ff1f4-108">Geben Sie nur die obere Version an, um eine maximale Version anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-108">To specify a maximum version, specify only the upper version.</span></span> <span data-ttu-id="ff1f4-109">Um einen Bereich anzugeben, müssen sowohl die obere als auch die niedrigere Version angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-109">To specify a range, both upper and lower versions must be specified.</span></span> <span data-ttu-id="ff1f4-110">Die Details der Überprüfungen werden mit den entsprechenden Details in einem [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Objekt verglichen, auf das von einer [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) -Zuordnung für das [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-110">Details of the checks are compared with the corresponding details found in a [**CIM\_SoftwareElement**](cim-softwareelement.md) object referenced by a [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object.</span></span> <span data-ttu-id="ff1f4-111">Mindestens ein **CIM- \_ Softwareelement** muss die Details der Bedingung erfüllen, damit die Überprüfung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-111">At least one **CIM\_SoftwareElement** needs to satisfy the details of the condition for the check to be satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff1f4-112">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff1f4-113">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff1f4-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff1f4-114">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ff1f4-115">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1f4-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff1f4-116">Syntax</span></span>

``` syntax
[UUID("{4D23FBD0-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareElementVersionCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  string  Description;
  string  LowerSoftwareElementVersion;
  string  Name;
  string  SoftwareElementID;
  string  SoftwareElementName;
  uint16  SoftwareElementState;
  uint16  SoftwareElementStateDesired;
  uint16  TargetOperatingSystem;
  uint16  TargetOperatingSystemDesired;
  string  UpperSoftwareElementVersion;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="ff1f4-117">Member</span><span class="sxs-lookup"><span data-stu-id="ff1f4-117">Members</span></span>

<span data-ttu-id="ff1f4-118">Die **CIM- \_ softwareelementversioncheck** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ff1f4-118">The **CIM\_SoftwareElementVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="ff1f4-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="ff1f4-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="ff1f4-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff1f4-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ff1f4-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="ff1f4-121">Methods</span></span>

<span data-ttu-id="ff1f4-122">Die **CIM- \_ softwareelementversioncheck** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-122">The **CIM\_SoftwareElementVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="ff1f4-123">Methode</span><span class="sxs-lookup"><span data-stu-id="ff1f4-123">Method</span></span>                                                                   | <span data-ttu-id="ff1f4-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff1f4-124">Description</span></span>                                                   |
|:-------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="ff1f4-125">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-125">**Invoke**</span></span>](invoke-method-in-class-cim-softwareelementversioncheck.md) | <span data-ttu-id="ff1f4-126">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-126">Takes a particular action.</span></span> <span data-ttu-id="ff1f4-127">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ff1f4-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff1f4-128">Properties</span></span>

<span data-ttu-id="ff1f4-129">Die **CIM- \_ softwareelementversioncheck** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-129">The **CIM\_SoftwareElementVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff1f4-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-133">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-133">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-134">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-134">Short textual description of the object.</span></span>

<span data-ttu-id="ff1f4-135">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-135">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-136">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-136">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-139">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-140">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-140">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="ff1f4-141">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-141">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-142">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-142">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff1f4-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-145">Wenn **true**, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist (wenn sich z. b. eine Datei auf einem System befindet, sollte die [**Aufruf**](invoke-method-in-class-cim-softwareelementversioncheck.md) Methode **true** zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="ff1f4-145">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="ff1f4-146">Wenn **false**, sollte die Bedingung nicht vorhanden sein (wenn sich z. b. eine Datei nicht auf einem System befindet, sollte die **Aufruf** Methode **false** zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="ff1f4-146">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="ff1f4-147">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-147">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-148">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-151">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-151">Description of the object.</span></span>

<span data-ttu-id="ff1f4-152">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-153">**Lowersoftwareelementversion**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-153">**LowerSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-156">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Softwareelement**](cim-softwareelement.md)".**Version**")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-156">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-157">Die minimale Version der Software Elemente, die geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-157">Minimum version of a software elements being checked.</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-161">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-162">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-162">Name used to identify the software element.</span></span>

<span data-ttu-id="ff1f4-163">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-163">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-164">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-164">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-167">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-168">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-168">Identifier for the software element.</span></span>

<span data-ttu-id="ff1f4-169">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-169">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-170">**Softwareelementname**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-170">**SoftwareElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-173">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Softwareelement**](cim-softwareelement.md)".**Name**")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-173">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-174">Der Name des Software Elements, das geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-174">Name of the software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-175">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-175">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-176">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-178">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-179">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-179">State of a software element.</span></span>

<span data-ttu-id="ff1f4-180">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-180">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ff1f4-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-182">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-182">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ff1f4-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-184">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-184">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ff1f4-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-186">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-186">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ff1f4-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-188">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-188">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ff1f4-189">**Softwareelementstateerwünscht**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-189">**SoftwareElementStateDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-192">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Softwareelement**](cim-softwareelement.md)".**SoftwareElementState**")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-192">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-193">Status des zu überprüfenden Software Elements.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-193">State of the software element being checked.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ff1f4-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-195">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-195">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ff1f4-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-197">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-197">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ff1f4-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-199">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-199">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ff1f4-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-201">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-201">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ff1f4-202">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-202">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-203">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-205">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-206">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-206">Target operating system of the software element.</span></span>

<span data-ttu-id="ff1f4-207">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-207">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ff1f4-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ff1f4-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ff1f4-210"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-211">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ff1f4-211">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ff1f4-212"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-213">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="ff1f4-213">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ff1f4-214"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ff1f4-215"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ff1f4-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ff1f4-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-218">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="ff1f4-218">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ff1f4-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-220">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ff1f4-220">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ff1f4-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ff1f4-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ff1f4-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ff1f4-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ff1f4-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-226">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="ff1f4-226">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ff1f4-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ff1f4-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-229">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ff1f4-229">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ff1f4-230"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-230"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-231">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ff1f4-231">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ff1f4-232"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-232"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-233">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ff1f4-233">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ff1f4-234"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-234"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-235">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ff1f4-235">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ff1f4-236"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-236"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-237">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ff1f4-237">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ff1f4-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-239">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ff1f4-239">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ff1f4-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ff1f4-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ff1f4-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ff1f4-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ff1f4-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ff1f4-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ff1f4-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ff1f4-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ff1f4-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ff1f4-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ff1f4-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ff1f4-251"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-252">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="ff1f4-252">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ff1f4-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-254">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="ff1f4-254">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ff1f4-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-256">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="ff1f4-256">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ff1f4-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-258">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ff1f4-258">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ff1f4-259"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-259"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ff1f4-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ff1f4-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ff1f4-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ff1f4-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ff1f4-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-265">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="ff1f4-265">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ff1f4-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ff1f4-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ff1f4-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ff1f4-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-270">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ff1f4-270">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ff1f4-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ff1f4-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ff1f4-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ff1f4-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ff1f4-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ff1f4-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ff1f4-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ff1f4-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ff1f4-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ff1f4-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ff1f4-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-282">Palm OS</span><span class="sxs-lookup"><span data-stu-id="ff1f4-282">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ff1f4-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ff1f4-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ff1f4-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ff1f4-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ff1f4-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ff1f4-288">**Targetoperatingsystemerwünscht**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-288">**TargetOperatingSystemDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-289">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-291">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Softwareelement**](cim-softwareelement.md)".**TargetOperatingSystem**")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-291">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-292">Das Ziel Betriebssystem des Software Elements, das geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-292">Target operating system of the software element being checked.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ff1f4-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ff1f4-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ff1f4-295"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-296">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ff1f4-296">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ff1f4-297"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-298">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="ff1f4-298">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ff1f4-299"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ff1f4-300"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ff1f4-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ff1f4-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-303">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="ff1f4-303">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ff1f4-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-305">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ff1f4-305">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ff1f4-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ff1f4-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ff1f4-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ff1f4-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ff1f4-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-311">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="ff1f4-311">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ff1f4-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ff1f4-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-314">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ff1f4-314">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ff1f4-315"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-315"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-316">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ff1f4-316">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ff1f4-317"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-317"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-318">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ff1f4-318">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ff1f4-319"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-319"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-320">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ff1f4-320">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ff1f4-321"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-321"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-322">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ff1f4-322">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ff1f4-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-324">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ff1f4-324">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ff1f4-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ff1f4-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ff1f4-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ff1f4-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ff1f4-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ff1f4-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ff1f4-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ff1f4-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ff1f4-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ff1f4-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ff1f4-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ff1f4-336"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-337">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="ff1f4-337">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ff1f4-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-339">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="ff1f4-339">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ff1f4-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-341">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="ff1f4-341">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ff1f4-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-343">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ff1f4-343">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ff1f4-344"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-344"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ff1f4-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ff1f4-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ff1f4-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ff1f4-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ff1f4-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-350">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="ff1f4-350">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ff1f4-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ff1f4-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ff1f4-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ff1f4-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-355">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ff1f4-355">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ff1f4-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ff1f4-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ff1f4-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ff1f4-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ff1f4-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ff1f4-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ff1f4-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ff1f4-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ff1f4-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ff1f4-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ff1f4-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ff1f4-367">Palm OS</span><span class="sxs-lookup"><span data-stu-id="ff1f4-367">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ff1f4-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ff1f4-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ff1f4-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ff1f4-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ff1f4-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ff1f4-373">**Uppersoftwareelementversion**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-373">**UpperSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-376">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Softwareelement**](cim-softwareelement.md)".**Version**")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-376">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-377">Die maximale Version eines Software Elements, das geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-377">Maximum version of a software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="ff1f4-378">**Version**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-378">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff1f4-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff1f4-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff1f4-381">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="ff1f4-381">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ff1f4-382">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-382">Version of the operation.</span></span>

<span data-ttu-id="ff1f4-383">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="ff1f4-383">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ff1f4-384"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="ff1f4-384"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="ff1f4-385"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="ff1f4-385"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="ff1f4-386">Diese Eigenschaft wird von der [**CIM- \_ Check**](cim-check.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-386">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff1f4-387">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff1f4-387">Remarks</span></span>

<span data-ttu-id="ff1f4-388">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-388">WMI does not implement this class.</span></span>

<span data-ttu-id="ff1f4-389">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-389">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff1f4-390">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ff1f4-390">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1f4-391">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff1f4-391">Requirements</span></span>



| <span data-ttu-id="ff1f4-392">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff1f4-392">Requirement</span></span> | <span data-ttu-id="ff1f4-393">Wert</span><span class="sxs-lookup"><span data-stu-id="ff1f4-393">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1f4-394">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-394">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1f4-395">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff1f4-395">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff1f4-396">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff1f4-396">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1f4-397">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff1f4-397">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff1f4-398">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff1f4-398">Namespace</span></span><br/>                | <span data-ttu-id="ff1f4-399">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ff1f4-399">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff1f4-400">MOF</span><span class="sxs-lookup"><span data-stu-id="ff1f4-400">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff1f4-401"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ff1f4-401"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff1f4-402">DLL</span><span class="sxs-lookup"><span data-stu-id="ff1f4-402">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff1f4-403"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff1f4-403"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff1f4-404">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff1f4-404">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1f4-405">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="ff1f4-405">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

