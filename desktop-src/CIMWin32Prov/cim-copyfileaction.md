---
description: Die CIM \_ copyfileaction-Klasse stellt das Verschieben oder Kopieren von Dateien von einem Computersystem an einen neuen Speicherort dar.
ms.assetid: c80b5002-d489-4b7e-b9a2-4460c3596958
ms.tgt_platform: multiple
title: CIM_CopyFileAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction
- CIM_CopyFileAction.ActionID
- CIM_CopyFileAction.Caption
- CIM_CopyFileAction.Description
- CIM_CopyFileAction.Direction
- CIM_CopyFileAction.Name
- CIM_CopyFileAction.SoftwareElementID
- CIM_CopyFileAction.SoftwareElementState
- CIM_CopyFileAction.TargetOperatingSystem
- CIM_CopyFileAction.Version
- CIM_CopyFileAction.DeleteAfterCopy
- CIM_CopyFileAction.Destination
- CIM_CopyFileAction.Source
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0303f4696d1baa5129d93cd2e6a7703be611ed9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342767"
---
# <a name="cim_copyfileaction-class"></a><span data-ttu-id="417bb-103">CIM \_ copyfileaction-Klasse</span><span class="sxs-lookup"><span data-stu-id="417bb-103">CIM\_CopyFileAction class</span></span>

<span data-ttu-id="417bb-104">Die **CIM \_ copyfileaction** -Klasse stellt das Verschieben oder Kopieren von Dateien von einem Computersystem an einen neuen Speicherort dar.</span><span class="sxs-lookup"><span data-stu-id="417bb-104">The **CIM\_CopyFileAction** class represents moving or copying files from a computer system to a new location.</span></span>

<span data-ttu-id="417bb-105">Speicherort Informationen für den Kopiervorgang werden entweder mithilfe der [**CIM- \_ Verzeichnis**](cim-todirectoryspecification.md) Zuordnungs Spezifikation und der [**CIM \_ fromdirector yspecification**](cim-fromdirectoryspecification.md) -Zuordnungen oder der [**CIM- \_ zudirector-Action**](cim-todirectoryaction.md) -und [**CIM \_ fromdirector Action**](cim-fromdirectoryaction.md) -Zuordnungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="417bb-105">Location information for copying is specified by using either the [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) and [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) associations, or the [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) and [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) associations.</span></span> <span data-ttu-id="417bb-106">Der erste Satz wird verwendet, wenn die Quelle oder das Ziel vorhanden ist, bevor Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="417bb-106">The first set is used when the source or target are to exist before any actions are taken.</span></span> <span data-ttu-id="417bb-107">Die zweite Gruppe wird verwendet, wenn die Quelle oder das Ziel als Teil einer vorherigen Aktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="417bb-107">The second set is used when the source or target are created as a part of a previous action.</span></span> <span data-ttu-id="417bb-108">Im letzteren Fall muss die Aktion zum Erstellen des Verzeichnisses vor dem **CIM- \_ copyfileaction** -Objekt erfolgen.</span><span class="sxs-lookup"><span data-stu-id="417bb-108">In the latter case, the action to create the directory must occur prior to the **CIM\_CopyFileAction** object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="417bb-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="417bb-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="417bb-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="417bb-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="417bb-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="417bb-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="417bb-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="417bb-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="417bb-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="417bb-113">Syntax</span></span>

``` syntax
[UUID("{73553260-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CopyFileAction : CIM_FileAction
{
  string  ActionID;
  string  Caption;
  string  Description;
  uint16  Direction;
  string  Name;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
  boolean DeleteAfterCopy;
  string  Destination;
  string  Source;
};
```

## <a name="members"></a><span data-ttu-id="417bb-114">Member</span><span class="sxs-lookup"><span data-stu-id="417bb-114">Members</span></span>

<span data-ttu-id="417bb-115">Die **CIM \_ copyfileaction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="417bb-115">The **CIM\_CopyFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="417bb-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="417bb-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="417bb-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="417bb-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="417bb-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="417bb-118">Methods</span></span>

<span data-ttu-id="417bb-119">Die **CIM \_ copyfileaction** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="417bb-119">The **CIM\_CopyFileAction** class has these methods.</span></span>



| <span data-ttu-id="417bb-120">Methode</span><span class="sxs-lookup"><span data-stu-id="417bb-120">Method</span></span>                                                      | <span data-ttu-id="417bb-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="417bb-121">Description</span></span>                                                                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="417bb-122">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="417bb-122">**Invoke**</span></span>](invoke-method-in-class-cim-copyfileaction.md) | <span data-ttu-id="417bb-123">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="417bb-123">Takes a particular action.</span></span> <span data-ttu-id="417bb-124">Die Details, wie die Methode die Aktion ausführt, sind Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="417bb-124">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="417bb-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="417bb-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="417bb-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="417bb-126">Properties</span></span>

<span data-ttu-id="417bb-127">Die **CIM \_ copyfileaction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="417bb-127">The **CIM\_CopyFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="417bb-128">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="417bb-128">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-131">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="417bb-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-132">Ein eindeutiger Bezeichner, der einer bestimmten Aktion für ein Softwareelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="417bb-132">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="417bb-133">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-133">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="417bb-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="417bb-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-137">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="417bb-137">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-138">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="417bb-138">Short textual description of the object.</span></span>

<span data-ttu-id="417bb-139">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="417bb-140">**Deleteaftercopy**</span><span class="sxs-lookup"><span data-stu-id="417bb-140">**DeleteAfterCopy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-141">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="417bb-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="417bb-143">**True** gibt an, dass die Quelldatei nach dem Kopiervorgang gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="417bb-143">If **TRUE**, the source file is deleted after the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="417bb-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="417bb-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="417bb-147">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="417bb-147">Description of the object.</span></span>

<span data-ttu-id="417bb-148">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="417bb-149">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="417bb-149">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-152">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="417bb-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-153">Der voll qualifizierte Name der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="417bb-153">Fully qualified destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="417bb-154">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="417bb-154">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="417bb-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="417bb-157">Gibt an, ob ein bestimmtes [**CIM- \_ Aktions**](cim-action.md) Objekt Teil einer Sequenz von Aktionen ist, um das aktuelle Softwareelement in seinen nächsten Zustand (z. b. "Install") zu übertragen, oder um das aktuelle Softwareelement zu entfernen, z. b. "deinstallieren".</span><span class="sxs-lookup"><span data-stu-id="417bb-157">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="417bb-158">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-158">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="417bb-159">**Installieren** (0)</span><span class="sxs-lookup"><span data-stu-id="417bb-159">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="417bb-160">**Deinstallieren** (1)</span><span class="sxs-lookup"><span data-stu-id="417bb-160">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="417bb-161">**Name**</span><span class="sxs-lookup"><span data-stu-id="417bb-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-164">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="417bb-164">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-165">Identifiziert das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="417bb-165">Identifies the software element.</span></span>

<span data-ttu-id="417bb-166">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-166">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="417bb-167">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="417bb-167">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-170">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="417bb-170">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-171">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="417bb-171">Identifier for the software element.</span></span>

<span data-ttu-id="417bb-172">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-172">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="417bb-173">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="417bb-173">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-174">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="417bb-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-176">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="417bb-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-177">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="417bb-177">State of a software element.</span></span>

<span data-ttu-id="417bb-178">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-178">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="417bb-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="417bb-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-180">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="417bb-180">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="417bb-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="417bb-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-182">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="417bb-182">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="417bb-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="417bb-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-184">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="417bb-184">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="417bb-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="417bb-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-186">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="417bb-186">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="417bb-187">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="417bb-187">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-190">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="417bb-190">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="417bb-191">Der voll qualifizierte Quell Dateiname.</span><span class="sxs-lookup"><span data-stu-id="417bb-191">Fully qualified source file name.</span></span>

</dd> <dt>

<span data-ttu-id="417bb-192">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="417bb-192">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="417bb-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-195">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="417bb-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="417bb-196">Ziel Betriebssystem des besitzenden Software Elements.</span><span class="sxs-lookup"><span data-stu-id="417bb-196">Target operating system of the owning software element.</span></span>

<span data-ttu-id="417bb-197">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-197">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="417bb-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="417bb-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="417bb-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="417bb-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="417bb-200"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="417bb-200"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-201">Mac OS</span><span class="sxs-lookup"><span data-stu-id="417bb-201">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="417bb-202"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="417bb-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="417bb-203"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="417bb-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="417bb-204"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="417bb-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="417bb-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="417bb-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="417bb-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="417bb-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-207">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="417bb-207">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="417bb-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="417bb-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-209">HP-UX</span><span class="sxs-lookup"><span data-stu-id="417bb-209">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="417bb-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="417bb-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="417bb-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="417bb-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="417bb-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="417bb-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="417bb-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="417bb-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="417bb-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="417bb-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-215">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="417bb-215">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="417bb-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="417bb-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="417bb-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="417bb-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-218">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="417bb-218">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="417bb-219"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="417bb-219"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-220">Windows 95</span><span class="sxs-lookup"><span data-stu-id="417bb-220">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="417bb-221"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="417bb-221"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-222">Windows 98</span><span class="sxs-lookup"><span data-stu-id="417bb-222">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="417bb-223"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="417bb-223"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-224">Windows NT</span><span class="sxs-lookup"><span data-stu-id="417bb-224">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="417bb-225"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="417bb-225"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-226">Windows CE</span><span class="sxs-lookup"><span data-stu-id="417bb-226">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="417bb-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="417bb-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-228">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="417bb-228">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="417bb-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="417bb-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="417bb-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="417bb-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="417bb-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="417bb-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="417bb-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="417bb-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="417bb-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="417bb-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="417bb-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="417bb-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="417bb-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="417bb-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="417bb-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="417bb-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="417bb-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="417bb-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="417bb-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="417bb-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="417bb-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="417bb-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="417bb-240"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="417bb-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-241">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="417bb-241">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="417bb-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="417bb-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-243">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="417bb-243">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="417bb-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="417bb-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-245">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="417bb-245">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="417bb-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="417bb-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-247">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="417bb-247">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="417bb-248"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="417bb-248"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="417bb-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="417bb-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="417bb-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="417bb-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="417bb-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="417bb-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="417bb-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="417bb-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="417bb-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="417bb-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-254">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="417bb-254">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="417bb-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="417bb-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="417bb-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="417bb-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="417bb-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="417bb-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="417bb-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="417bb-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-259">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="417bb-259">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="417bb-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="417bb-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="417bb-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="417bb-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="417bb-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="417bb-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="417bb-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="417bb-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="417bb-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="417bb-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="417bb-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="417bb-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="417bb-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="417bb-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="417bb-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="417bb-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-268">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="417bb-268">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="417bb-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="417bb-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="417bb-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="417bb-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="417bb-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="417bb-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="417bb-272">Palm OS</span><span class="sxs-lookup"><span data-stu-id="417bb-272">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="417bb-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="417bb-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="417bb-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="417bb-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="417bb-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="417bb-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="417bb-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="417bb-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="417bb-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="417bb-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="417bb-278">**Version**</span><span class="sxs-lookup"><span data-stu-id="417bb-278">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417bb-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="417bb-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417bb-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="417bb-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417bb-281">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="417bb-281">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="417bb-282">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="417bb-282">Version of the operation.</span></span>

<span data-ttu-id="417bb-283">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="417bb-283">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="417bb-284"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="417bb-284"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="417bb-285"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="417bb-285"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="417bb-286">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="417bb-286">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="417bb-287">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="417bb-287">Remarks</span></span>

<span data-ttu-id="417bb-288">Die **CIM- \_ copyfileaction** -Klasse wird von [**CIM \_ fileaction**](cim-fileaction.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="417bb-288">The **CIM\_CopyFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="417bb-289">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="417bb-289">WMI does not implement this class.</span></span> <span data-ttu-id="417bb-290">Weitere Informationen zu Klassen, die von **CIM \_ copyfileaction** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="417bb-290">For more information about classes derived from **CIM\_CopyFileAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="417bb-291">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="417bb-291">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="417bb-292">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="417bb-292">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="417bb-293">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="417bb-293">Requirements</span></span>



| <span data-ttu-id="417bb-294">Anforderung</span><span class="sxs-lookup"><span data-stu-id="417bb-294">Requirement</span></span> | <span data-ttu-id="417bb-295">Wert</span><span class="sxs-lookup"><span data-stu-id="417bb-295">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="417bb-296">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="417bb-296">Minimum supported client</span></span><br/> | <span data-ttu-id="417bb-297">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="417bb-297">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="417bb-298">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="417bb-298">Minimum supported server</span></span><br/> | <span data-ttu-id="417bb-299">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="417bb-299">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="417bb-300">Namespace</span><span class="sxs-lookup"><span data-stu-id="417bb-300">Namespace</span></span><br/>                | <span data-ttu-id="417bb-301">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="417bb-301">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="417bb-302">MOF</span><span class="sxs-lookup"><span data-stu-id="417bb-302">MOF</span></span><br/>                      | <dl> <span data-ttu-id="417bb-303"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="417bb-303"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="417bb-304">DLL</span><span class="sxs-lookup"><span data-stu-id="417bb-304">DLL</span></span><br/>                      | <dl> <span data-ttu-id="417bb-305"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="417bb-305"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="417bb-306">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="417bb-306">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417bb-307">**CIM- \_ fileaction**</span><span class="sxs-lookup"><span data-stu-id="417bb-307">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

