---
description: Die CIM \_ executeprogram-Klasse stellt Dateien dar, die auf dem System ausgeführt werden können, auf dem das Softwareelement installiert ist.
ms.assetid: 4329d228-4069-4a5a-b1eb-2dbad9644118
ms.tgt_platform: multiple
title: CIM_ExecuteProgram-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram
- CIM_ExecuteProgram.ActionID
- CIM_ExecuteProgram.Caption
- CIM_ExecuteProgram.Description
- CIM_ExecuteProgram.Direction
- CIM_ExecuteProgram.Name
- CIM_ExecuteProgram.SoftwareElementID
- CIM_ExecuteProgram.SoftwareElementState
- CIM_ExecuteProgram.TargetOperatingSystem
- CIM_ExecuteProgram.Version
- CIM_ExecuteProgram.CommandLine
- CIM_ExecuteProgram.ProgramPath
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76743d255bc50d213a4ce3f44057d97830078ccd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126985"
---
# <a name="cim_executeprogram-class"></a><span data-ttu-id="85dc8-103">CIM \_ executeprogram-Klasse</span><span class="sxs-lookup"><span data-stu-id="85dc8-103">CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="85dc8-104">Die **CIM \_ executeprogram** -Klasse stellt Dateien dar, die auf dem System ausgeführt werden können, auf dem das Softwareelement installiert ist.</span><span class="sxs-lookup"><span data-stu-id="85dc8-104">The **CIM\_ExecuteProgram** class represents files that can be executed on the system where the software element is installed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85dc8-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="85dc8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="85dc8-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="85dc8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="85dc8-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="85dc8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="85dc8-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="85dc8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85dc8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="85dc8-109">Syntax</span></span>

``` syntax
[UUID("{149ADDEE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ExecuteProgram : CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
  string CommandLine;
  string ProgramPath;
};
```

## <a name="members"></a><span data-ttu-id="85dc8-110">Member</span><span class="sxs-lookup"><span data-stu-id="85dc8-110">Members</span></span>

<span data-ttu-id="85dc8-111">Die **CIM \_ executeprogram** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85dc8-111">The **CIM\_ExecuteProgram** class has these types of members:</span></span>

-   [<span data-ttu-id="85dc8-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="85dc8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="85dc8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85dc8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85dc8-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="85dc8-114">Methods</span></span>

<span data-ttu-id="85dc8-115">Die **CIM \_ executeprogram** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="85dc8-115">The **CIM\_ExecuteProgram** class has these methods.</span></span>



| <span data-ttu-id="85dc8-116">Methode</span><span class="sxs-lookup"><span data-stu-id="85dc8-116">Method</span></span>                                                      | <span data-ttu-id="85dc8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85dc8-117">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="85dc8-118">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="85dc8-118">**Invoke**</span></span>](invoke-method-in-class-cim-executeprogram.md) | <span data-ttu-id="85dc8-119">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="85dc8-119">Takes a particular action.</span></span> <span data-ttu-id="85dc8-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="85dc8-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="85dc8-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85dc8-121">Properties</span></span>

<span data-ttu-id="85dc8-122">Die **CIM \_ executeprogram** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85dc8-122">The **CIM\_ExecuteProgram** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85dc8-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="85dc8-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-126">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85dc8-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-127">Ein eindeutiger Bezeichner, der einer bestimmten Aktion für ein Softwareelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="85dc8-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="85dc8-128">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="85dc8-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-132">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="85dc8-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-133">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="85dc8-133">Short textual description of the object.</span></span>

<span data-ttu-id="85dc8-134">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-135">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="85dc8-135">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-138">Eine Zeichenfolge, die in einer System Befehlszeile aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="85dc8-138">String that can be invoked on a system command line.</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85dc8-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-142">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="85dc8-142">Description of the object.</span></span>

<span data-ttu-id="85dc8-143">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-143">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-144">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="85dc8-144">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85dc8-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-147">Gibt an, ob ein bestimmtes [**CIM- \_ Aktions**](cim-action.md) Objekt Teil einer Sequenz von Aktionen ist, um das aktuelle Softwareelement in seinen nächsten Zustand (z. b. "Install") zu übertragen, oder um das aktuelle Softwareelement zu entfernen, z. b. "deinstallieren".</span><span class="sxs-lookup"><span data-stu-id="85dc8-147">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="85dc8-148">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="85dc8-149">**Installieren** (0)</span><span class="sxs-lookup"><span data-stu-id="85dc8-149">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="85dc8-150">**Deinstallieren** (1)</span><span class="sxs-lookup"><span data-stu-id="85dc8-150">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85dc8-151">**Name**</span><span class="sxs-lookup"><span data-stu-id="85dc8-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-154">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85dc8-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-155">Identifiziert das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="85dc8-155">Identifies the software element.</span></span>

<span data-ttu-id="85dc8-156">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-156">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-157">**Programpath**</span><span class="sxs-lookup"><span data-stu-id="85dc8-157">**ProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-160">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="85dc8-160">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-161">Der Pfad zum Programm.</span><span class="sxs-lookup"><span data-stu-id="85dc8-161">Path to the program.</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-162">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="85dc8-162">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-165">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85dc8-165">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-166">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="85dc8-166">Identifier for the software element.</span></span>

<span data-ttu-id="85dc8-167">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-167">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="85dc8-168">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="85dc8-168">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-169">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85dc8-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-171">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="85dc8-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-172">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="85dc8-172">State of a software element.</span></span>

<span data-ttu-id="85dc8-173">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-173">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="85dc8-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="85dc8-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-175">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85dc8-175">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="85dc8-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="85dc8-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-177">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85dc8-177">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="85dc8-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="85dc8-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-179">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85dc8-179">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="85dc8-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="85dc8-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-181">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="85dc8-181">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85dc8-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="85dc8-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85dc8-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-185">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="85dc8-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-186">Ziel Betriebssystem des besitzenden Software Elements.</span><span class="sxs-lookup"><span data-stu-id="85dc8-186">Target operating system of the owning software element.</span></span>

<span data-ttu-id="85dc8-187">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-187">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="85dc8-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="85dc8-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="85dc8-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="85dc8-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="85dc8-190"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="85dc8-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="85dc8-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="85dc8-192"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="85dc8-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="85dc8-193"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="85dc8-193"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="85dc8-194"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="85dc8-194"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="85dc8-195"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="85dc8-195"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="85dc8-196"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="85dc8-196"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-197">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="85dc8-197">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="85dc8-198"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="85dc8-198"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-199">HP-UX</span><span class="sxs-lookup"><span data-stu-id="85dc8-199">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="85dc8-200"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="85dc8-200"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="85dc8-201"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="85dc8-201"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="85dc8-202"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="85dc8-202"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="85dc8-203"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="85dc8-203"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="85dc8-204"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="85dc8-204"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-205">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="85dc8-205">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="85dc8-206"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="85dc8-206"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="85dc8-207"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="85dc8-207"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-208">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="85dc8-208">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="85dc8-209"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="85dc8-209"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-210">Windows 95</span><span class="sxs-lookup"><span data-stu-id="85dc8-210">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="85dc8-211"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="85dc8-211"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-212">Windows 98</span><span class="sxs-lookup"><span data-stu-id="85dc8-212">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="85dc8-213"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="85dc8-213"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-214">Windows NT</span><span class="sxs-lookup"><span data-stu-id="85dc8-214">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="85dc8-215"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="85dc8-215"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-216">Windows CE</span><span class="sxs-lookup"><span data-stu-id="85dc8-216">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="85dc8-217"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="85dc8-217"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-218">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="85dc8-218">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="85dc8-219"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="85dc8-219"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="85dc8-220"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="85dc8-220"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="85dc8-221"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="85dc8-221"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="85dc8-222"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="85dc8-222"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="85dc8-223"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="85dc8-223"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="85dc8-224"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="85dc8-224"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="85dc8-225"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="85dc8-225"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="85dc8-226"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="85dc8-226"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="85dc8-227"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="85dc8-227"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="85dc8-228"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="85dc8-228"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="85dc8-229"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="85dc8-229"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="85dc8-230"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="85dc8-230"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-231">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="85dc8-231">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="85dc8-232"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="85dc8-232"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-233">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="85dc8-233">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="85dc8-234"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="85dc8-234"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-235">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="85dc8-235">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="85dc8-236"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="85dc8-236"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-237">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="85dc8-237">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="85dc8-238"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="85dc8-238"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="85dc8-239"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="85dc8-239"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="85dc8-240"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="85dc8-240"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="85dc8-241"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="85dc8-241"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="85dc8-242"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="85dc8-242"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="85dc8-243"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="85dc8-243"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-244">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="85dc8-244">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="85dc8-245"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="85dc8-245"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="85dc8-246"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="85dc8-246"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="85dc8-247"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="85dc8-247"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="85dc8-248"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="85dc8-248"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-249">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="85dc8-249">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="85dc8-250"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="85dc8-250"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="85dc8-251"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="85dc8-251"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="85dc8-252"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="85dc8-252"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="85dc8-253"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="85dc8-253"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="85dc8-254"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="85dc8-254"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="85dc8-255"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="85dc8-255"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="85dc8-256"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="85dc8-256"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="85dc8-257"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="85dc8-257"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-258">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="85dc8-258">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="85dc8-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="85dc8-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="85dc8-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="85dc8-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="85dc8-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="85dc8-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="85dc8-262">Palm OS</span><span class="sxs-lookup"><span data-stu-id="85dc8-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="85dc8-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="85dc8-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="85dc8-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="85dc8-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="85dc8-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="85dc8-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="85dc8-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="85dc8-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="85dc8-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="85dc8-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85dc8-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="85dc8-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85dc8-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85dc8-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85dc8-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85dc8-271">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="85dc8-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="85dc8-272">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="85dc8-272">Version of the operation.</span></span>

<span data-ttu-id="85dc8-273">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="85dc8-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="85dc8-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="85dc8-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="85dc8-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="85dc8-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="85dc8-276">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="85dc8-276">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85dc8-277">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85dc8-277">Remarks</span></span>

<span data-ttu-id="85dc8-278">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="85dc8-278">WMI does not implement this class.</span></span>

<span data-ttu-id="85dc8-279">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="85dc8-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="85dc8-280">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85dc8-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="85dc8-281">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85dc8-281">Requirements</span></span>



| <span data-ttu-id="85dc8-282">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85dc8-282">Requirement</span></span> | <span data-ttu-id="85dc8-283">Wert</span><span class="sxs-lookup"><span data-stu-id="85dc8-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85dc8-284">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85dc8-284">Minimum supported client</span></span><br/> | <span data-ttu-id="85dc8-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85dc8-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85dc8-286">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85dc8-286">Minimum supported server</span></span><br/> | <span data-ttu-id="85dc8-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85dc8-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85dc8-288">Namespace</span><span class="sxs-lookup"><span data-stu-id="85dc8-288">Namespace</span></span><br/>                | <span data-ttu-id="85dc8-289">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="85dc8-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="85dc8-290">MOF</span><span class="sxs-lookup"><span data-stu-id="85dc8-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85dc8-291"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85dc8-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="85dc8-292">DLL</span><span class="sxs-lookup"><span data-stu-id="85dc8-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85dc8-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85dc8-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85dc8-294">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85dc8-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85dc8-295">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="85dc8-295">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

