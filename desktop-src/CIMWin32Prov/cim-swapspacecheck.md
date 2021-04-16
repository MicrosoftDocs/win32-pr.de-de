---
description: Die CIM \_ swapspacecheck-Klasse gibt die Menge an Auslagerungs Bereich an, die auf dem System verfügbar sein muss.
ms.assetid: c5e5ec68-bc62-4bdf-93b7-ce868e738dee
ms.tgt_platform: multiple
title: CIM_SwapSpaceCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwapSpaceCheck
- CIM_SwapSpaceCheck.CheckID
- CIM_SwapSpaceCheck.Caption
- CIM_SwapSpaceCheck.Description
- CIM_SwapSpaceCheck.CheckMode
- CIM_SwapSpaceCheck.Name
- CIM_SwapSpaceCheck.TargetOperatingSystem
- CIM_SwapSpaceCheck.Version
- CIM_SwapSpaceCheck.SoftwareElementID
- CIM_SwapSpaceCheck.SoftwareElementState
- CIM_SwapSpaceCheck.SwapSpaceSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992d8a314797c7a977e9a672ecb9d3dcdb561292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523811"
---
# <a name="cim_swapspacecheck-class"></a><span data-ttu-id="45654-103">CIM- \_ Klasse "tauapspacecheck"</span><span class="sxs-lookup"><span data-stu-id="45654-103">CIM\_SwapSpaceCheck class</span></span>

<span data-ttu-id="45654-104">Die **CIM \_ swapspacecheck** -Klasse gibt die Menge an Auslagerungs Bereich an, die auf dem System verfügbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="45654-104">The **CIM\_SwapSpaceCheck** class specifies the amount of swap space that must be available on the system.</span></span> <span data-ttu-id="45654-105">Der Wert wird in der Eigenschaft " **Swap** -Eigenschaft" angegeben.</span><span class="sxs-lookup"><span data-stu-id="45654-105">The amount is specified in the **SwapSpaceSize** property.</span></span> <span data-ttu-id="45654-106">Die Details dieser Überprüfung werden mit den entsprechenden Details in einem [**CIM- \_ OperatingSystem**](cim-operatingsystem.md) -Objekt verglichen, auf das von der [**CIM \_ installedos**](cim-installedos.md) -Zuordnung für das [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt verwiesen wird, das die Umgebung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="45654-106">Details of this check are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by the [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="45654-107">Wenn der Wert der **totaltauapspacesize** -Eigenschaft größer oder gleich dem Wert ist, der in der Eigenschaft " **Swap** -Eigenschaft" angegeben ist, wird die Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="45654-107">When the value of the **TotalSwapSpaceSize** property is greater than or equal to the value specified in the **SwapSpaceSize** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45654-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="45654-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="45654-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="45654-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="45654-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45654-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="45654-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45654-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45654-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="45654-112">Syntax</span></span>

``` syntax
[UUID("{A5AE701E-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SwapSpaceCheck : CIM_Check
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
  uint64  SwapSpaceSize;
};
```

## <a name="members"></a><span data-ttu-id="45654-113">Member</span><span class="sxs-lookup"><span data-stu-id="45654-113">Members</span></span>

<span data-ttu-id="45654-114">Die CIM-Klasse " **\_ tauapspacecheck** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="45654-114">The **CIM\_SwapSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="45654-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="45654-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="45654-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45654-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45654-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="45654-117">Methods</span></span>

<span data-ttu-id="45654-118">Die CIM-Klasse " **\_ tauapspacecheck** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="45654-118">The **CIM\_SwapSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="45654-119">Methode</span><span class="sxs-lookup"><span data-stu-id="45654-119">Method</span></span>                                                      | <span data-ttu-id="45654-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45654-120">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="45654-121">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="45654-121">**Invoke**</span></span>](invoke-method-in-class-cim-swapspacecheck.md) | <span data-ttu-id="45654-122">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="45654-122">Takes a particular action.</span></span> <span data-ttu-id="45654-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="45654-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45654-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45654-124">Properties</span></span>

<span data-ttu-id="45654-125">Die CIM-Klasse " **\_ tauapspacecheck** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45654-125">The **CIM\_SwapSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45654-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45654-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45654-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45654-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45654-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45654-130">Eine kurze Textbeschreibung des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="45654-130">A short textual description of the subject.</span></span>

<span data-ttu-id="45654-131">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="45654-132">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="45654-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45654-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45654-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-135">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45654-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45654-136">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45654-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="45654-137">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="45654-138">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="45654-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="45654-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45654-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45654-141">Wenn der Wert **true** ist, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="45654-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="45654-142">Beispielsweise wird erwartet, dass eine Datei auf einem System ausgeführt wird, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="45654-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="45654-143">Wenn der Wert **false** ist, wird erwartet, dass die Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="45654-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="45654-144">Eine Datei befindet sich z. b. nicht in einem System, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="45654-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="45654-145">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="45654-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45654-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45654-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45654-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45654-149">Eine Beschreibung der-Objekte.</span><span class="sxs-lookup"><span data-stu-id="45654-149">A description of the objects.</span></span>

<span data-ttu-id="45654-150">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="45654-151">**Name**</span><span class="sxs-lookup"><span data-stu-id="45654-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45654-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45654-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-154">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45654-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45654-155">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45654-155">Name used to identify the software element</span></span>

<span data-ttu-id="45654-156">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-156">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="45654-157">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="45654-157">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45654-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45654-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-160">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45654-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45654-161">Dies ist ein Bezeichner für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="45654-161">This is an identifier for this software element.</span></span>

<span data-ttu-id="45654-162">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="45654-163">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="45654-163">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45654-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45654-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-166">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45654-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45654-167">Der Softwareelement Zustand eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="45654-167">The software element state of a software element.</span></span>

<span data-ttu-id="45654-168">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="45654-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="45654-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="45654-170">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="45654-170">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="45654-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="45654-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="45654-172">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="45654-172">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="45654-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="45654-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="45654-174">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="45654-174">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="45654-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="45654-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="45654-176">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="45654-176">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45654-177">**"Austauschen"**</span><span class="sxs-lookup"><span data-stu-id="45654-177">**SwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-178">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45654-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45654-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-180">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**Totaltauapspacesize**"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="45654-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="45654-181">Minimale Größe des Auslagerungs Raums in Kilobyte, die auf dem Zielsystem verfügbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="45654-181">Minimum swap-space size, in kilobytes, that must be available on the target system.</span></span>

<span data-ttu-id="45654-182">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="45654-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="45654-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="45654-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45654-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45654-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-186">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="45654-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="45654-187">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="45654-187">Target operating system of the software element.</span></span>

<span data-ttu-id="45654-188">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45654-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="45654-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45654-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="45654-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="45654-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="45654-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="45654-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="45654-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="45654-193"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="45654-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="45654-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="45654-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="45654-195"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="45654-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="45654-196"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="45654-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="45654-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="45654-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="45654-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="45654-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="45654-199">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="45654-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="45654-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="45654-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="45654-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="45654-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="45654-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="45654-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="45654-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="45654-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="45654-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="45654-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="45654-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="45654-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="45654-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="45654-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="45654-207">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="45654-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="45654-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="45654-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="45654-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="45654-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="45654-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="45654-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="45654-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="45654-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="45654-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="45654-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="45654-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="45654-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="45654-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="45654-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="45654-215"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="45654-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="45654-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="45654-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="45654-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="45654-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="45654-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="45654-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="45654-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="45654-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="45654-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="45654-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="45654-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="45654-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="45654-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="45654-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="45654-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="45654-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="45654-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="45654-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="45654-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="45654-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="45654-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="45654-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="45654-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="45654-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="45654-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="45654-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="45654-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="45654-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="45654-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="45654-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="45654-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="45654-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="45654-232"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="45654-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="45654-233">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="45654-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="45654-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="45654-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="45654-235">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="45654-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="45654-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="45654-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="45654-237">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="45654-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="45654-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="45654-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="45654-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="45654-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="45654-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="45654-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="45654-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="45654-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="45654-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="45654-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="45654-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="45654-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="45654-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="45654-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="45654-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="45654-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="45654-246">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="45654-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="45654-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="45654-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="45654-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="45654-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="45654-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="45654-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="45654-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="45654-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="45654-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="45654-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="45654-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="45654-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="45654-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="45654-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="45654-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="45654-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="45654-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="45654-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="45654-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="45654-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="45654-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="45654-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="45654-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="45654-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="45654-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="45654-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="45654-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="45654-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="45654-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="45654-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="45654-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="45654-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="45654-263">Palm OS</span><span class="sxs-lookup"><span data-stu-id="45654-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="45654-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="45654-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="45654-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="45654-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="45654-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="45654-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="45654-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="45654-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="45654-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="45654-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45654-269">**Version**</span><span class="sxs-lookup"><span data-stu-id="45654-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45654-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45654-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45654-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45654-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45654-272">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="45654-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="45654-273">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="45654-273">Version of the operation.</span></span>

<span data-ttu-id="45654-274">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="45654-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="45654-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="45654-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="45654-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="45654-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="45654-277">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45654-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45654-278">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45654-278">Remarks</span></span>

<span data-ttu-id="45654-279">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="45654-279">WMI does not implement this class.</span></span>

<span data-ttu-id="45654-280">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="45654-280">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="45654-281">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="45654-281">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="45654-282">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45654-282">Requirements</span></span>



| <span data-ttu-id="45654-283">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45654-283">Requirement</span></span> | <span data-ttu-id="45654-284">Wert</span><span class="sxs-lookup"><span data-stu-id="45654-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45654-285">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45654-285">Minimum supported client</span></span><br/> | <span data-ttu-id="45654-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45654-286">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45654-287">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45654-287">Minimum supported server</span></span><br/> | <span data-ttu-id="45654-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45654-288">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45654-289">Namespace</span><span class="sxs-lookup"><span data-stu-id="45654-289">Namespace</span></span><br/>                | <span data-ttu-id="45654-290">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="45654-290">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45654-291">MOF</span><span class="sxs-lookup"><span data-stu-id="45654-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45654-292"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="45654-292"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45654-293">DLL</span><span class="sxs-lookup"><span data-stu-id="45654-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45654-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45654-294"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45654-295">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45654-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45654-296">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="45654-296">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

