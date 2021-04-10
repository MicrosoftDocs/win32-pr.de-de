---
description: Die CIM \_ osversioncheck-Klasse gibt die Versionen des Betriebssystems an, die ein Softwareelement unterstützen können.
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: CIM_OSVersionCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041450"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="dd6c5-103">CIM- \_ osversioncheck-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd6c5-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="dd6c5-104">Die **CIM \_ osversioncheck** -Klasse gibt die Versionen des Betriebssystems an, die ein Softwareelement unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="dd6c5-105">Die Überprüfung kann für ein bestimmtes, maximales, maximales oder eine Reihe von Betriebssystemversionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="dd6c5-106">Zum Angeben einer bestimmten Betriebssystemversion müssen die minimalen und maximalen Versionen gleich sein.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="dd6c5-107">Zum Angeben der Mindestversion muss nur die Mindestversion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="dd6c5-108">Zum Angeben einer maximalen Version muss die maximal zulässige Version angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="dd6c5-109">Um einen Bereich anzugeben, müssen sowohl die Mindest-als auch die maximale Version angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="dd6c5-110">Der Typ des Betriebssystems wird in der **TargetOperatingSystem** -Eigenschaft des besitzenden Software Elements angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="dd6c5-111">Die Details der Überprüfungen werden mit den entsprechenden Details in einem [**CIM- \_ OperatingSystem**](cim-operatingsystem.md) -Objekt verglichen, auf das von einer [**CIM- \_ instanalledos**](cim-installedos.md) -Zuordnung für das [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt verwiesen wird, das die Umgebung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="dd6c5-112">Mindestens eine **CIM- \_ OperatingSystem** -Klasse muss die Details der Bedingung erfüllen, damit die Überprüfung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="dd6c5-113">Anders ausgedrückt: nicht alle Betriebssysteme auf dem relevanten Computersystem müssen die Bedingung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="dd6c5-114">Außerdem muss die **OSType** -Eigenschaft der **CIM \_ OperatingSystem** -Klasse mit dem Typ der **TargetOperatingSystem** -Eigenschaft identisch sein.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd6c5-115">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dd6c5-116">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dd6c5-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dd6c5-117">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dd6c5-118">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd6c5-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd6c5-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="dd6c5-120">Member</span><span class="sxs-lookup"><span data-stu-id="dd6c5-120">Members</span></span>

<span data-ttu-id="dd6c5-121">Die **CIM \_ osversioncheck** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd6c5-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="dd6c5-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd6c5-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd6c5-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd6c5-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd6c5-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd6c5-124">Methods</span></span>

<span data-ttu-id="dd6c5-125">Die **CIM \_ osversioncheck** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="dd6c5-126">Methode</span><span class="sxs-lookup"><span data-stu-id="dd6c5-126">Method</span></span>                                                      | <span data-ttu-id="dd6c5-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd6c5-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="dd6c5-128">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="dd6c5-129">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-129">Takes a particular action.</span></span> <span data-ttu-id="dd6c5-130">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd6c5-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd6c5-131">Properties</span></span>

<span data-ttu-id="dd6c5-132">Die **CIM \_ osversioncheck** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd6c5-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-136">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-137">Eine kurze Textbeschreibung des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-137">A short textual description of the subject.</span></span>

<span data-ttu-id="dd6c5-138">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-139">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-142">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-143">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="dd6c5-144">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-145">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd6c5-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-148">Wenn der Wert **true** ist, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="dd6c5-149">Beispielsweise wird erwartet, dass eine Datei auf einem System ausgeführt wird, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="dd6c5-150">Wenn der Wert **false** ist, wird erwartet, dass die Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="dd6c5-151">Eine Datei befindet sich z. b. nicht in einem System, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="dd6c5-152">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-156">Eine Beschreibung der-Objekte.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-156">A description of the objects.</span></span>

<span data-ttu-id="dd6c5-157">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-161">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="dd6c5-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-162">Maximale Version des erforderlichen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="dd6c5-163">Der Wert wird in einer der folgenden Formen codiert:</span><span class="sxs-lookup"><span data-stu-id="dd6c5-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="dd6c5-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="dd6c5-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="dd6c5-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="dd6c5-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-169">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="dd6c5-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-170">Mindestens erforderliche Version des erforderlichen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="dd6c5-171">Der Wert wird in einer der folgenden Formen codiert:</span><span class="sxs-lookup"><span data-stu-id="dd6c5-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="dd6c5-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="dd6c5-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="dd6c5-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="dd6c5-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-174">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-177">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-178">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-178">Name used to identify the software element</span></span>

<span data-ttu-id="dd6c5-179">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-180">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-183">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-184">Dies ist ein Bezeichner für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="dd6c5-185">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd6c5-186">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-189">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-190">Der Softwareelement Zustand eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-190">The software element state of a software element.</span></span>

<span data-ttu-id="dd6c5-191">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="dd6c5-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-193">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="dd6c5-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-195">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="dd6c5-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-197">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="dd6c5-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-199">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd6c5-200">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-201">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-203">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="dd6c5-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-204">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-204">Target operating system of the software element.</span></span>

<span data-ttu-id="dd6c5-205">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd6c5-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd6c5-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="dd6c5-208"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-209">Mac OS</span><span class="sxs-lookup"><span data-stu-id="dd6c5-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="dd6c5-210"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-211">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="dd6c5-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="dd6c5-212"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="dd6c5-213"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="dd6c5-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="dd6c5-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-216">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="dd6c5-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="dd6c5-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="dd6c5-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="dd6c5-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="dd6c5-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="dd6c5-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="dd6c5-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="dd6c5-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-224">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="dd6c5-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="dd6c5-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="dd6c5-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-227">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="dd6c5-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="dd6c5-228"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="dd6c5-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="dd6c5-230"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="dd6c5-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="dd6c5-232"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="dd6c5-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="dd6c5-234"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="dd6c5-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="dd6c5-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-237">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="dd6c5-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="dd6c5-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="dd6c5-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="dd6c5-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="dd6c5-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="dd6c5-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="dd6c5-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="dd6c5-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="dd6c5-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="dd6c5-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="dd6c5-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="dd6c5-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="dd6c5-249"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-250">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="dd6c5-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="dd6c5-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-252">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="dd6c5-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="dd6c5-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-254">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="dd6c5-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="dd6c5-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="dd6c5-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="dd6c5-257"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="dd6c5-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="dd6c5-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="dd6c5-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="dd6c5-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="dd6c5-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-263">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="dd6c5-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="dd6c5-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="dd6c5-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="dd6c5-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="dd6c5-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="dd6c5-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="dd6c5-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="dd6c5-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="dd6c5-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="dd6c5-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="dd6c5-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="dd6c5-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="dd6c5-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="dd6c5-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="dd6c5-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="dd6c5-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="dd6c5-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="dd6c5-280">Palm OS</span><span class="sxs-lookup"><span data-stu-id="dd6c5-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="dd6c5-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="dd6c5-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="dd6c5-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="dd6c5-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="dd6c5-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd6c5-286">**Version**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6c5-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6c5-289">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="dd6c5-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="dd6c5-290">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-290">Version of the operation.</span></span>

<span data-ttu-id="dd6c5-291">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="dd6c5-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="dd6c5-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="dd6c5-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="dd6c5-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="dd6c5-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="dd6c5-294">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd6c5-295">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd6c5-295">Remarks</span></span>

<span data-ttu-id="dd6c5-296">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-296">WMI does not implement this class.</span></span>

<span data-ttu-id="dd6c5-297">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dd6c5-298">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6c5-299">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd6c5-299">Requirements</span></span>



| <span data-ttu-id="dd6c5-300">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd6c5-300">Requirement</span></span> | <span data-ttu-id="dd6c5-301">Wert</span><span class="sxs-lookup"><span data-stu-id="dd6c5-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6c5-302">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-302">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6c5-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd6c5-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd6c5-304">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-304">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6c5-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd6c5-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd6c5-306">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd6c5-306">Namespace</span></span><br/>                | <span data-ttu-id="dd6c5-307">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dd6c5-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd6c5-308">MOF</span><span class="sxs-lookup"><span data-stu-id="dd6c5-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd6c5-309"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd6c5-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd6c5-310">DLL</span><span class="sxs-lookup"><span data-stu-id="dd6c5-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd6c5-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd6c5-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd6c5-312">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd6c5-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6c5-313">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="dd6c5-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

