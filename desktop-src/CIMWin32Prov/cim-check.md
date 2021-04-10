---
description: Die CIM- \_ Check-Klasse stellt eine Bedingung oder ein Merkmal dar, die in einer Umgebung erwartungsgemäß definiert ist, die von einer Instanz einer CIM Computersystem-Klasse definiert oder festgelegt wird \_ .
ms.assetid: f7862fe5-4412-4d57-b5fa-03c939ddba02
ms.tgt_platform: multiple
title: CIM_Check-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check
- CIM_Check.CheckID
- CIM_Check.Caption
- CIM_Check.Description
- CIM_Check.CheckMode
- CIM_Check.Name
- CIM_Check.TargetOperatingSystem
- CIM_Check.Version
- CIM_Check.SoftwareElementID
- CIM_Check.SoftwareElementState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cbe742fb4cd2510ec4c502f89b3b3b1eb79bc47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861348"
---
# <a name="cim_check-class"></a><span data-ttu-id="81dee-103">CIM- \_ Check-Klasse</span><span class="sxs-lookup"><span data-stu-id="81dee-103">CIM\_Check class</span></span>

<span data-ttu-id="81dee-104">Die **CIM- \_ Check** -Klasse stellt eine Bedingung oder ein Merkmal dar, die in einer Umgebung erwartungsgemäß definiert ist, die von einer Instanz einer [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse definiert oder festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="81dee-104">The **CIM\_Check** class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="81dee-105">Die Überprüfungen, die einem bestimmten Softwareelement zugeordnet sind, werden in einer von zwei Gruppen organisiert, wobei die **Phase** -Eigenschaft der [**CIM- \_ softwareelementchecks**](cim-softwareelementchecks.md) -Zuordnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81dee-105">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

<span data-ttu-id="81dee-106">Bedingungen, die erwartungsgemäß erfüllt werden, wenn sich ein Softwareelement in einer bestimmten Umgebung befindet, werden als Zustands Zustände bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="81dee-106">Conditions that are expected to be satisfied when a software element is in a particular environment are known as in-state conditions.</span></span> <span data-ttu-id="81dee-107">Bedingungen, die erfüllt sein müssen, um das aktuelle Softwareelement in seinen nächsten Zustand zu versetzen, werden als Bedingungen des nächsten Zustands bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="81dee-107">Conditions that must be satisfied to transition the current software element to its next state are known as next-state conditions.</span></span>

<span data-ttu-id="81dee-108">Ein [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt stellt die Umgebung dar, in der ein [**CIM- \_ Softwareelement**](cim-softwareelement.md) bereits installiert ist oder in dem ein **CIM- \_ Softwareelement** installiert wird.</span><span class="sxs-lookup"><span data-stu-id="81dee-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) object represents the environment in which a [**CIM\_SoftwareElement**](cim-softwareelement.md) is already installed, or in which a **CIM\_SoftwareElement** will be installed.</span></span> <span data-ttu-id="81dee-109">Für den Fall, in dem ein Softwareelement bereits installiert ist, wird die [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) -Zuordnung verwendet, um das **CIM \_ Computersystem** -Objekt zu identifizieren, das die "Umgebung" darstellt.</span><span class="sxs-lookup"><span data-stu-id="81dee-109">For the case in which a software element is already installed, the [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association is used to identify the **CIM\_ComputerSystem** object that represents the "environment."</span></span> <span data-ttu-id="81dee-110">Wenn ein Softwareelement verteilt und auf einem anderen Computer installiert wird, ist das **CIM \_ Computersystem** -Objekt für das Zielsystem die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="81dee-110">When a software element is being distributed and installed on a different computer, the **CIM\_ComputerSystem** object for the targeted system is the environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81dee-111">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="81dee-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81dee-112">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81dee-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81dee-113">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="81dee-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="81dee-114">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="81dee-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dee-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="81dee-115">Syntax</span></span>

``` syntax
[UUID("{7A9135CA-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Check
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
};
```

## <a name="members"></a><span data-ttu-id="81dee-116">Member</span><span class="sxs-lookup"><span data-stu-id="81dee-116">Members</span></span>

<span data-ttu-id="81dee-117">Die **CIM- \_ Check** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="81dee-117">The **CIM\_Check** class has these types of members:</span></span>

-   [<span data-ttu-id="81dee-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="81dee-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="81dee-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81dee-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81dee-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="81dee-120">Methods</span></span>

<span data-ttu-id="81dee-121">Die **CIM- \_ Check** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="81dee-121">The **CIM\_Check** class has these methods.</span></span>



| <span data-ttu-id="81dee-122">Methode</span><span class="sxs-lookup"><span data-stu-id="81dee-122">Method</span></span>                                             | <span data-ttu-id="81dee-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81dee-123">Description</span></span>                                                   |
|:---------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="81dee-124">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="81dee-124">**Invoke**</span></span>](invoke-method-in-class-cim-check.md) | <span data-ttu-id="81dee-125">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="81dee-125">Takes a particular action.</span></span> <span data-ttu-id="81dee-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="81dee-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81dee-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81dee-127">Properties</span></span>

<span data-ttu-id="81dee-128">Die **CIM- \_ Check** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81dee-128">The **CIM\_Check** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81dee-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="81dee-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81dee-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-132">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="81dee-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81dee-133">Eine kurze Textbeschreibung des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="81dee-133">A short textual description of the subject.</span></span>

</dd> <dt>

<span data-ttu-id="81dee-134">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="81dee-134">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81dee-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-137">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="81dee-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="81dee-138">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81dee-138">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

</dd> <dt>

<span data-ttu-id="81dee-139">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="81dee-139">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="81dee-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81dee-142">Wenn der Wert **true** ist, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="81dee-142">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="81dee-143">Beispielsweise wird erwartet, dass eine Datei auf einem System ausgeführt wird, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="81dee-143">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="81dee-144">Wenn der Wert **false** ist, wird erwartet, dass die Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="81dee-144">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="81dee-145">Eine Datei befindet sich z. b. nicht in einem System, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="81dee-145">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="81dee-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81dee-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81dee-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81dee-149">Eine Beschreibung der-Objekte.</span><span class="sxs-lookup"><span data-stu-id="81dee-149">A description of the objects.</span></span>

</dd> <dt>

<span data-ttu-id="81dee-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="81dee-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81dee-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-153">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="81dee-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="81dee-154">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81dee-154">Name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="81dee-155">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="81dee-155">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81dee-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-158">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="81dee-158">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="81dee-159">Dies ist ein Bezeichner für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="81dee-159">This is an identifier for this software element.</span></span>

</dd> <dt>

<span data-ttu-id="81dee-160">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="81dee-160">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81dee-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-163">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81dee-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81dee-164">Der Softwareelement Zustand eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="81dee-164">The software element state of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="81dee-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="81dee-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-166">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81dee-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="81dee-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="81dee-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-168">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81dee-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="81dee-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="81dee-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-170">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81dee-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="81dee-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="81dee-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-172">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="81dee-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81dee-173">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="81dee-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-174">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81dee-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-176">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="81dee-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="81dee-177">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="81dee-177">Target operating system of the software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81dee-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="81dee-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81dee-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="81dee-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="81dee-180"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="81dee-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-181">Mac OS</span><span class="sxs-lookup"><span data-stu-id="81dee-181">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="81dee-182"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="81dee-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-183">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="81dee-183">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="81dee-184"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="81dee-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="81dee-185"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="81dee-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="81dee-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="81dee-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="81dee-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="81dee-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-188">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="81dee-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="81dee-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="81dee-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="81dee-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="81dee-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="81dee-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="81dee-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="81dee-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="81dee-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="81dee-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="81dee-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="81dee-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="81dee-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="81dee-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-196">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="81dee-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="81dee-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="81dee-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="81dee-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="81dee-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-199">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="81dee-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="81dee-200"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="81dee-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="81dee-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="81dee-202"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="81dee-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="81dee-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="81dee-204"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="81dee-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="81dee-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="81dee-206"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="81dee-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="81dee-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="81dee-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="81dee-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-209">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="81dee-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="81dee-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="81dee-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="81dee-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="81dee-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="81dee-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="81dee-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="81dee-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="81dee-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="81dee-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="81dee-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="81dee-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="81dee-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="81dee-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="81dee-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="81dee-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="81dee-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="81dee-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="81dee-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="81dee-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="81dee-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="81dee-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="81dee-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="81dee-221"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="81dee-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-222">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="81dee-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="81dee-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="81dee-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-224">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="81dee-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="81dee-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="81dee-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-226">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="81dee-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="81dee-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="81dee-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="81dee-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="81dee-229"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="81dee-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="81dee-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="81dee-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="81dee-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="81dee-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="81dee-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="81dee-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="81dee-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="81dee-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="81dee-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="81dee-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-235">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="81dee-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="81dee-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="81dee-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="81dee-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="81dee-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="81dee-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="81dee-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="81dee-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="81dee-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="81dee-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="81dee-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="81dee-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="81dee-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="81dee-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="81dee-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="81dee-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="81dee-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="81dee-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="81dee-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="81dee-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="81dee-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="81dee-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="81dee-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="81dee-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="81dee-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="81dee-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="81dee-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="81dee-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="81dee-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="81dee-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="81dee-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="81dee-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="81dee-252">Palm OS</span><span class="sxs-lookup"><span data-stu-id="81dee-252">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="81dee-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="81dee-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="81dee-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="81dee-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="81dee-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="81dee-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="81dee-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="81dee-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="81dee-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="81dee-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81dee-258">**Version**</span><span class="sxs-lookup"><span data-stu-id="81dee-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81dee-259">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81dee-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81dee-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dee-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81dee-261">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="81dee-261">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="81dee-262">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="81dee-262">Version of the operation.</span></span>

<span data-ttu-id="81dee-263">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="81dee-263">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="81dee-264"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="81dee-264"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="81dee-265"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="81dee-265"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81dee-266">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81dee-266">Remarks</span></span>

<span data-ttu-id="81dee-267">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="81dee-267">WMI does not implement this class.</span></span> <span data-ttu-id="81dee-268">Weitere Informationen zu von CIM-Prüfungen abgeleiteten Klassen finden **\_ Sie** unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="81dee-268">For more information about classes derived from **CIM\_Check**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="81dee-269">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="81dee-269">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81dee-270">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="81dee-270">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81dee-271">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81dee-271">Requirements</span></span>



| <span data-ttu-id="81dee-272">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81dee-272">Requirement</span></span> | <span data-ttu-id="81dee-273">Wert</span><span class="sxs-lookup"><span data-stu-id="81dee-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81dee-274">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81dee-274">Minimum supported client</span></span><br/> | <span data-ttu-id="81dee-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81dee-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81dee-276">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81dee-276">Minimum supported server</span></span><br/> | <span data-ttu-id="81dee-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81dee-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81dee-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="81dee-278">Namespace</span></span><br/>                | <span data-ttu-id="81dee-279">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81dee-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81dee-280">MOF</span><span class="sxs-lookup"><span data-stu-id="81dee-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81dee-281"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81dee-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81dee-282">DLL</span><span class="sxs-lookup"><span data-stu-id="81dee-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81dee-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81dee-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

