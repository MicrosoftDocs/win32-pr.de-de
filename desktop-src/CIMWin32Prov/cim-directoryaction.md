---
description: Die \_ abstrakte directoryaction-Klasse wird Verzeichnisse verwaltet. Die Verzeichnis Erstellung wird von der CIM \_ -Klasse "kreatedirectoryaction" verarbeitet, und die Verzeichnis Entfernung erfolgt durch die CIM- \_ removedirectoryaction-Klasse.
ms.assetid: 3c1e7023-cf54-4321-a340-b8616300c4c0
ms.tgt_platform: multiple
title: CIM_DirectoryAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction
- CIM_DirectoryAction.ActionID
- CIM_DirectoryAction.Caption
- CIM_DirectoryAction.Description
- CIM_DirectoryAction.Direction
- CIM_DirectoryAction.Name
- CIM_DirectoryAction.SoftwareElementID
- CIM_DirectoryAction.SoftwareElementState
- CIM_DirectoryAction.TargetOperatingSystem
- CIM_DirectoryAction.Version
- CIM_DirectoryAction.DirectoryName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 130284e8cf19640e7861b17d80a4612b130f7062
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861404"
---
# <a name="cim_directoryaction-class"></a><span data-ttu-id="265f2-104">CIM- \_ directoryaction-Klasse</span><span class="sxs-lookup"><span data-stu-id="265f2-104">CIM\_DirectoryAction class</span></span>

<span data-ttu-id="265f2-105">Die **abstrakte \_ directoryaction** -Klasse wird Verzeichnisse verwaltet.</span><span class="sxs-lookup"><span data-stu-id="265f2-105">The **CIM\_DirectoryAction** abstract class manages directories.</span></span> <span data-ttu-id="265f2-106">Die Verzeichnis Erstellung wird von der CIM-Klasse " [**\_ kreatedirectoryaction**](cim-createdirectoryaction.md) " verarbeitet, und die Verzeichnis Entfernung erfolgt durch die [**CIM- \_ removedirectoryaction**](cim-removedirectoryaction.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="265f2-106">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="265f2-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="265f2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="265f2-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="265f2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="265f2-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="265f2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="265f2-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="265f2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="265f2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="265f2-111">Syntax</span></span>

``` syntax
[UUID("{8875A39E-DB29-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DirectoryAction : CIM_Action
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
  string DirectoryName;
};
```

## <a name="members"></a><span data-ttu-id="265f2-112">Member</span><span class="sxs-lookup"><span data-stu-id="265f2-112">Members</span></span>

<span data-ttu-id="265f2-113">Die **CIM- \_ directoryaction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="265f2-113">The **CIM\_DirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="265f2-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="265f2-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="265f2-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="265f2-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="265f2-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="265f2-116">Methods</span></span>

<span data-ttu-id="265f2-117">Die **CIM- \_ directoryaction** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="265f2-117">The **CIM\_DirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="265f2-118">Methode</span><span class="sxs-lookup"><span data-stu-id="265f2-118">Method</span></span>                                                       | <span data-ttu-id="265f2-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="265f2-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="265f2-120">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="265f2-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryaction.md) | <span data-ttu-id="265f2-121">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="265f2-121">Takes a particular action.</span></span> <span data-ttu-id="265f2-122">Diese Methode wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="265f2-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="265f2-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="265f2-123">Properties</span></span>

<span data-ttu-id="265f2-124">Die **CIM- \_ directoryaction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="265f2-124">The **CIM\_DirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="265f2-125">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="265f2-125">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-128">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="265f2-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="265f2-129">Ein eindeutiger Bezeichner, der einer bestimmten Aktion für ein Softwareelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="265f2-129">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="265f2-130">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-130">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="265f2-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="265f2-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-134">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="265f2-134">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="265f2-135">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="265f2-135">Short textual description of the object.</span></span>

<span data-ttu-id="265f2-136">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-136">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="265f2-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="265f2-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="265f2-140">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="265f2-140">Description of the object.</span></span>

<span data-ttu-id="265f2-141">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-141">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="265f2-142">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="265f2-142">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="265f2-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="265f2-145">Gibt an, ob ein bestimmtes [**CIM- \_ Aktions**](cim-action.md) Objekt Teil einer Sequenz von Aktionen ist, um das aktuelle Softwareelement in seinen nächsten Zustand (z. b. "Install") zu übertragen, oder um das aktuelle Softwareelement zu entfernen, z. b. "deinstallieren".</span><span class="sxs-lookup"><span data-stu-id="265f2-145">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="265f2-146">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-146">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="265f2-147">**Installieren** (0)</span><span class="sxs-lookup"><span data-stu-id="265f2-147">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="265f2-148">**Deinstallieren** (1)</span><span class="sxs-lookup"><span data-stu-id="265f2-148">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="265f2-149">**Verzeichnisname**</span><span class="sxs-lookup"><span data-stu-id="265f2-149">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-152">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="265f2-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="265f2-153">Der Name des Verzeichnisses, für das die Aktion gilt.</span><span class="sxs-lookup"><span data-stu-id="265f2-153">Name of the directory to which the action applies.</span></span>

</dd> <dt>

<span data-ttu-id="265f2-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="265f2-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-157">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="265f2-157">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="265f2-158">Identifiziert das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="265f2-158">Identifies the software element.</span></span>

<span data-ttu-id="265f2-159">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-159">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="265f2-160">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="265f2-160">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-163">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="265f2-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="265f2-164">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="265f2-164">Identifier for the software element.</span></span>

<span data-ttu-id="265f2-165">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-165">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="265f2-166">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="265f2-166">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="265f2-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-169">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="265f2-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="265f2-170">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="265f2-170">State of a software element.</span></span>

<span data-ttu-id="265f2-171">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-171">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="265f2-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="265f2-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-173">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="265f2-173">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="265f2-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="265f2-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-175">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="265f2-175">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="265f2-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="265f2-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-177">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="265f2-177">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="265f2-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="265f2-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-179">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="265f2-179">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="265f2-180">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="265f2-180">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-181">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="265f2-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-183">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="265f2-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="265f2-184">Ziel Betriebssystem des besitzenden Software Elements.</span><span class="sxs-lookup"><span data-stu-id="265f2-184">Target operating system of the owning software element.</span></span>

<span data-ttu-id="265f2-185">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-185">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="265f2-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="265f2-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="265f2-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="265f2-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="265f2-188"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="265f2-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-189">Mac OS</span><span class="sxs-lookup"><span data-stu-id="265f2-189">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="265f2-190"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="265f2-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="265f2-191"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="265f2-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="265f2-192"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="265f2-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="265f2-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="265f2-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="265f2-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="265f2-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-195">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="265f2-195">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="265f2-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="265f2-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-197">HP-UX</span><span class="sxs-lookup"><span data-stu-id="265f2-197">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="265f2-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="265f2-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="265f2-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="265f2-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="265f2-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="265f2-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="265f2-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="265f2-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="265f2-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="265f2-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-203">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="265f2-203">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="265f2-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="265f2-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="265f2-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="265f2-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-206">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="265f2-206">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="265f2-207"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="265f2-207"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-208">Windows 95</span><span class="sxs-lookup"><span data-stu-id="265f2-208">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="265f2-209"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="265f2-209"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-210">Windows 98</span><span class="sxs-lookup"><span data-stu-id="265f2-210">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="265f2-211"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="265f2-211"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-212">Windows NT</span><span class="sxs-lookup"><span data-stu-id="265f2-212">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="265f2-213"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="265f2-213"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-214">Windows CE</span><span class="sxs-lookup"><span data-stu-id="265f2-214">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="265f2-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="265f2-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-216">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="265f2-216">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="265f2-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="265f2-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="265f2-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="265f2-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="265f2-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="265f2-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="265f2-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="265f2-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="265f2-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="265f2-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="265f2-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="265f2-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="265f2-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="265f2-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="265f2-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="265f2-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="265f2-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="265f2-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="265f2-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="265f2-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="265f2-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="265f2-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="265f2-228"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="265f2-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-229">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="265f2-229">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="265f2-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="265f2-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-231">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="265f2-231">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="265f2-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="265f2-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-233">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="265f2-233">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="265f2-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="265f2-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-235">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="265f2-235">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="265f2-236"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="265f2-236"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="265f2-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="265f2-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="265f2-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="265f2-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="265f2-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="265f2-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="265f2-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="265f2-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="265f2-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="265f2-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-242">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="265f2-242">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="265f2-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="265f2-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="265f2-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="265f2-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="265f2-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="265f2-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="265f2-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="265f2-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-247">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="265f2-247">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="265f2-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="265f2-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="265f2-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="265f2-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="265f2-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="265f2-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="265f2-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="265f2-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="265f2-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="265f2-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="265f2-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="265f2-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="265f2-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="265f2-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="265f2-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="265f2-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-256">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="265f2-256">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="265f2-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="265f2-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="265f2-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="265f2-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="265f2-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="265f2-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="265f2-260">Palm OS</span><span class="sxs-lookup"><span data-stu-id="265f2-260">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="265f2-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="265f2-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="265f2-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="265f2-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="265f2-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="265f2-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="265f2-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="265f2-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="265f2-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="265f2-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="265f2-266">**Version**</span><span class="sxs-lookup"><span data-stu-id="265f2-266">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265f2-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="265f2-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="265f2-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="265f2-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265f2-269">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="265f2-269">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="265f2-270">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="265f2-270">Version of the operation.</span></span>

<span data-ttu-id="265f2-271">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="265f2-271">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="265f2-272"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="265f2-272"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="265f2-273"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="265f2-273"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="265f2-274">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="265f2-274">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="265f2-275">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="265f2-275">Remarks</span></span>

<span data-ttu-id="265f2-276">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="265f2-276">WMI does not implement this class.</span></span>

<span data-ttu-id="265f2-277">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="265f2-277">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="265f2-278">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="265f2-278">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="265f2-279">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="265f2-279">Requirements</span></span>



| <span data-ttu-id="265f2-280">Anforderung</span><span class="sxs-lookup"><span data-stu-id="265f2-280">Requirement</span></span> | <span data-ttu-id="265f2-281">Wert</span><span class="sxs-lookup"><span data-stu-id="265f2-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="265f2-282">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="265f2-282">Minimum supported client</span></span><br/> | <span data-ttu-id="265f2-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="265f2-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="265f2-284">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="265f2-284">Minimum supported server</span></span><br/> | <span data-ttu-id="265f2-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="265f2-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="265f2-286">Namespace</span><span class="sxs-lookup"><span data-stu-id="265f2-286">Namespace</span></span><br/>                | <span data-ttu-id="265f2-287">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="265f2-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="265f2-288">MOF</span><span class="sxs-lookup"><span data-stu-id="265f2-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="265f2-289"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="265f2-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="265f2-290">DLL</span><span class="sxs-lookup"><span data-stu-id="265f2-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="265f2-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265f2-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="265f2-292">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="265f2-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="265f2-293">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="265f2-293">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

