---
description: Die CIM \_ modifysettingaction-Klasse stellt die Informationen zum Ändern einer bestimmten Einstellungsdatei für einen bestimmten Eintrag mit einem bestimmten Wert dar.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: CIM_ModifySettingAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748689"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="8dd0e-103">CIM \_ modifysettingaction-Klasse</span><span class="sxs-lookup"><span data-stu-id="8dd0e-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="8dd0e-104">Die **CIM \_ modifysettingaction** -Klasse stellt die Informationen zum Ändern einer bestimmten Einstellungsdatei für einen bestimmten Eintrag mit einem bestimmten Wert dar.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dd0e-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8dd0e-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8dd0e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8dd0e-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8dd0e-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd0e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dd0e-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
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
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="8dd0e-110">Member</span><span class="sxs-lookup"><span data-stu-id="8dd0e-110">Members</span></span>

<span data-ttu-id="8dd0e-111">Die **CIM \_ modifysettingaction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8dd0e-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="8dd0e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8dd0e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8dd0e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dd0e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8dd0e-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="8dd0e-114">Methods</span></span>

<span data-ttu-id="8dd0e-115">Die **CIM \_ modifysettingaction** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="8dd0e-116">Methode</span><span class="sxs-lookup"><span data-stu-id="8dd0e-116">Method</span></span>                                                           | <span data-ttu-id="8dd0e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dd0e-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="8dd0e-118">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="8dd0e-119">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-119">Takes a specific action.</span></span> <span data-ttu-id="8dd0e-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8dd0e-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dd0e-121">Properties</span></span>

<span data-ttu-id="8dd0e-122">Die **CIM \_ modifysettingaction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dd0e-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-126">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-127">Ein eindeutiger Bezeichner, der einer bestimmten Aktion für ein Softwareelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="8dd0e-128">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-129">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-132">Der Typ der Aktion, die für den angegebenen Einstellungs Eintrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="8dd0e-133">Bei Ergänzungen wird die Groß-/Kleinschreibung beachtet. bei der Entfernung wird jedoch davon ausgegangen, dass die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="8dd0e-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="8dd0e-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Erstellen** (0)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-135">Erstellt den angegebenen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="8dd0e-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Löschen** (1)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-137">Löscht den angegebenen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="8dd0e-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Anfügen** (2)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-139">Fügt am Ende des angegebenen Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="8dd0e-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Entfernen** (3)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-141">Entfernt den Wert aus dem angegebenen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dd0e-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-145">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-146">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-146">Short textual description of the object.</span></span>

<span data-ttu-id="8dd0e-147">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-148">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-151">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-151">Description of the object.</span></span>

<span data-ttu-id="8dd0e-152">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-153">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-156">Gibt an, ob ein bestimmtes [**CIM- \_ Aktions**](cim-action.md) Objekt Teil einer Sequenz von Aktionen ist, um das aktuelle Softwareelement in seinen nächsten Zustand (z. b. "Install") zu übertragen, oder um das aktuelle Softwareelement zu entfernen, z. b. "deinstallieren".</span><span class="sxs-lookup"><span data-stu-id="8dd0e-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="8dd0e-157">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="8dd0e-158">**Installieren** (0)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="8dd0e-159">**Deinstallieren** (1)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8dd0e-160">**Entryname**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-163">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-164">Der Name des Eintrags, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-165">**Entryvalue**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-168">Der Wert, der hinzugefügt, angefügt oder ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-173">Der Dateiname des Einstellungsdatei Eintrags, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-174">**Name**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-177">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-178">Identifiziert das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-178">Identifies the software element.</span></span>

<span data-ttu-id="8dd0e-179">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-180">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-183">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-184">Der Abschnitts Schlüssel des Einstellungs Eintrags, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-185">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-188">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-189">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-189">Identifier for the software element.</span></span>

<span data-ttu-id="8dd0e-190">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd0e-191">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-192">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-194">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-195">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-195">State of a software element.</span></span>

<span data-ttu-id="8dd0e-196">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="8dd0e-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-198">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="8dd0e-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-200">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="8dd0e-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-202">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="8dd0e-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-204">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dd0e-205">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-206">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-208">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="8dd0e-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-209">Ziel Betriebssystem des besitzenden Software Elements.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="8dd0e-210">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8dd0e-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8dd0e-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="8dd0e-213"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-214">Mac OS</span><span class="sxs-lookup"><span data-stu-id="8dd0e-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="8dd0e-215"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="8dd0e-216"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="8dd0e-217"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="8dd0e-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="8dd0e-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-220">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="8dd0e-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="8dd0e-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="8dd0e-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="8dd0e-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="8dd0e-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="8dd0e-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="8dd0e-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="8dd0e-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-228">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="8dd0e-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="8dd0e-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="8dd0e-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-231">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="8dd0e-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="8dd0e-232"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="8dd0e-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="8dd0e-234"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8dd0e-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="8dd0e-236"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="8dd0e-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="8dd0e-238"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="8dd0e-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="8dd0e-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-241">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="8dd0e-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="8dd0e-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="8dd0e-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="8dd0e-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="8dd0e-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="8dd0e-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="8dd0e-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="8dd0e-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="8dd0e-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="8dd0e-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="8dd0e-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="8dd0e-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="8dd0e-253"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-254">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="8dd0e-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="8dd0e-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-256">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="8dd0e-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="8dd0e-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-258">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="8dd0e-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="8dd0e-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="8dd0e-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="8dd0e-261"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="8dd0e-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="8dd0e-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="8dd0e-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="8dd0e-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="8dd0e-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-267">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="8dd0e-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="8dd0e-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="8dd0e-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="8dd0e-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="8dd0e-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="8dd0e-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="8dd0e-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="8dd0e-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="8dd0e-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="8dd0e-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="8dd0e-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="8dd0e-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="8dd0e-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="8dd0e-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-281">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8dd0e-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="8dd0e-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="8dd0e-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="8dd0e-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="8dd0e-285">Palm OS</span><span class="sxs-lookup"><span data-stu-id="8dd0e-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="8dd0e-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="8dd0e-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="8dd0e-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="8dd0e-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="8dd0e-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8dd0e-291">**Version**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd0e-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dd0e-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dd0e-294">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="8dd0e-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="8dd0e-295">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-295">Version of the operation.</span></span>

<span data-ttu-id="8dd0e-296">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="8dd0e-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="8dd0e-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="8dd0e-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="8dd0e-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="8dd0e-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="8dd0e-299">Diese Eigenschaft wird von der [**CIM- \_ Aktion**](cim-action.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dd0e-300">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dd0e-300">Remarks</span></span>

<span data-ttu-id="8dd0e-301">Die **CIM- \_ modifysettingaction** -Klasse wird von der [**CIM- \_ Aktion**](cim-action.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="8dd0e-302">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-302">WMI does not implement this class.</span></span>

<span data-ttu-id="8dd0e-303">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8dd0e-304">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd0e-305">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dd0e-305">Requirements</span></span>



| <span data-ttu-id="8dd0e-306">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dd0e-306">Requirement</span></span> | <span data-ttu-id="8dd0e-307">Wert</span><span class="sxs-lookup"><span data-stu-id="8dd0e-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd0e-308">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-308">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd0e-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dd0e-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8dd0e-310">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-310">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd0e-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dd0e-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8dd0e-312">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dd0e-312">Namespace</span></span><br/>                | <span data-ttu-id="8dd0e-313">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8dd0e-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8dd0e-314">MOF</span><span class="sxs-lookup"><span data-stu-id="8dd0e-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dd0e-315"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8dd0e-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dd0e-316">DLL</span><span class="sxs-lookup"><span data-stu-id="8dd0e-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dd0e-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dd0e-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dd0e-318">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dd0e-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd0e-319">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="8dd0e-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

