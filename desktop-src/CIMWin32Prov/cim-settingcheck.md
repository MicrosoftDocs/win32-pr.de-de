---
description: Die CIM \_ settingcheck-Klasse gibt Informationen an, die erforderlich sind, um eine bestimmte Einstellungsdatei für einen bestimmten Eintrag zu überprüfen, der einen Wert gleich dem angegebenen Wert enthält. Bei allen vergleichen wird die Groß-/Kleinschreibung nicht beachtet.
ms.assetid: 0e40276c-e794-4ea1-8937-c6d7f110f97d
ms.tgt_platform: multiple
title: CIM_SettingCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck
- CIM_SettingCheck.Caption
- CIM_SettingCheck.CheckID
- CIM_SettingCheck.CheckMode
- CIM_SettingCheck.CheckType
- CIM_SettingCheck.Description
- CIM_SettingCheck.EntryName
- CIM_SettingCheck.EntryValue
- CIM_SettingCheck.FileName
- CIM_SettingCheck.Name
- CIM_SettingCheck.SectionKey
- CIM_SettingCheck.SoftwareElementID
- CIM_SettingCheck.SoftwareElementState
- CIM_SettingCheck.TargetOperatingSystem
- CIM_SettingCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4b360833f216d9feb839a4ed84a0e1ba4cd61ebf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338902"
---
# <a name="cim_settingcheck-class"></a><span data-ttu-id="068f6-104">CIM \_ settingcheck-Klasse</span><span class="sxs-lookup"><span data-stu-id="068f6-104">CIM\_SettingCheck class</span></span>

<span data-ttu-id="068f6-105">Die **CIM \_ settingcheck** -Klasse gibt Informationen an, die erforderlich sind, um eine bestimmte Einstellungsdatei für einen bestimmten Eintrag zu überprüfen, der einen Wert gleich dem angegebenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="068f6-105">The **CIM\_SettingCheck** class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="068f6-106">Bei allen vergleichen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="068f6-106">All comparisons are assumed to be case insensitive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="068f6-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="068f6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="068f6-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="068f6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="068f6-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="068f6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="068f6-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="068f6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="068f6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="068f6-111">Syntax</span></span>

``` syntax
[UUID("{DC1D8140-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SettingCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  uint16  CheckType;
  string  Description;
  string  EntryName;
  string  EntryValue;
  string  FileName;
  string  Name;
  string  SectionKey;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="068f6-112">Member</span><span class="sxs-lookup"><span data-stu-id="068f6-112">Members</span></span>

<span data-ttu-id="068f6-113">Die **CIM \_ settingcheck** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="068f6-113">The **CIM\_SettingCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="068f6-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="068f6-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="068f6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="068f6-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="068f6-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="068f6-116">Methods</span></span>

<span data-ttu-id="068f6-117">Die **CIM \_ settingcheck** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="068f6-117">The **CIM\_SettingCheck** class has these methods.</span></span>



| <span data-ttu-id="068f6-118">Methode</span><span class="sxs-lookup"><span data-stu-id="068f6-118">Method</span></span>                                                    | <span data-ttu-id="068f6-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="068f6-119">Description</span></span>                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="068f6-120">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="068f6-120">**Invoke**</span></span>](invoke-method-in-class-cim-settingcheck.md) | <span data-ttu-id="068f6-121">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="068f6-121">Takes a particular action.</span></span> <span data-ttu-id="068f6-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="068f6-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="068f6-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="068f6-123">Properties</span></span>

<span data-ttu-id="068f6-124">Die **CIM \_ settingcheck** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="068f6-124">The **CIM\_SettingCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="068f6-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="068f6-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-128">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="068f6-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-129">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="068f6-129">Short textual description of the object.</span></span>

<span data-ttu-id="068f6-130">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="068f6-131">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="068f6-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-134">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="068f6-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-135">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="068f6-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span> <span data-ttu-id="068f6-136">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="068f6-137">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="068f6-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="068f6-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="068f6-140">Wenn **true**, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist (wenn sich z. b. eine Datei auf einem System befindet, sollte die [**Aufruf**](invoke-method-in-class-cim-settingcheck.md) Methode **true** zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="068f6-140">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-settingcheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="068f6-141">Wenn **false**, sollte die Bedingung nicht vorhanden sein (wenn sich z. b. eine Datei nicht auf einem System befindet, sollte die **Aufruf** Methode **false** zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="068f6-141">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="068f6-142">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="068f6-143">**Checktype**</span><span class="sxs-lookup"><span data-stu-id="068f6-143">**CheckType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="068f6-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="068f6-146">Die Art und Weise, in der der Einstellungs Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="068f6-146">Way in which the setting value should be compared.</span></span>

<dt>

<span id="Matches"></span><span id="matches"></span><span id="MATCHES"></span>

<span data-ttu-id="068f6-147">**Übereinstimmungen** (0)</span><span class="sxs-lookup"><span data-stu-id="068f6-147">**Matches** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Contains"></span><span id="contains"></span><span id="CONTAINS"></span>

<span data-ttu-id="068f6-148">**Enthält** (1)</span><span class="sxs-lookup"><span data-stu-id="068f6-148">**Contains** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="068f6-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="068f6-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="068f6-152">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="068f6-152">Description of the object.</span></span>

<span data-ttu-id="068f6-153">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-153">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="068f6-154">**Entryname**</span><span class="sxs-lookup"><span data-stu-id="068f6-154">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-157">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="068f6-157">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-158">Der Name des zu überprüfenden Eintrags.</span><span class="sxs-lookup"><span data-stu-id="068f6-158">Name of the entry to be checked</span></span>

</dd> <dt>

<span data-ttu-id="068f6-159">**Entryvalue**</span><span class="sxs-lookup"><span data-stu-id="068f6-159">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="068f6-162">Der Wert, der dem zu überprüfen benannten Eintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="068f6-162">Value that is associated with the named entry to check.</span></span>

</dd> <dt>

<span data-ttu-id="068f6-163">**FileName**</span><span class="sxs-lookup"><span data-stu-id="068f6-163">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-166">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="068f6-166">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-167">Der Dateiname der Einstellungsdatei, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="068f6-167">File name of the setting file to check.</span></span>

</dd> <dt>

<span data-ttu-id="068f6-168">**Name**</span><span class="sxs-lookup"><span data-stu-id="068f6-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-171">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="068f6-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-172">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="068f6-172">Name used to identify the software element.</span></span> <span data-ttu-id="068f6-173">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="068f6-174">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="068f6-174">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-177">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="068f6-177">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-178">Der Schlüssel des Abschnitts, der die zu Überprüfungen enden Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="068f6-178">Key of section that contains the settings to check.</span></span>

</dd> <dt>

<span data-ttu-id="068f6-179">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="068f6-179">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-182">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="068f6-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-183">Der Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="068f6-183">Identifier for the software element.</span></span>

<span data-ttu-id="068f6-184">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-184">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="068f6-185">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="068f6-185">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-186">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="068f6-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-188">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="068f6-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="068f6-189">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="068f6-189">State of a software element.</span></span>

<span data-ttu-id="068f6-190">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-190">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="068f6-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="068f6-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-192">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="068f6-192">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="068f6-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="068f6-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-194">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="068f6-194">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="068f6-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="068f6-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-196">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="068f6-196">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="068f6-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="068f6-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-198">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="068f6-198">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="068f6-199">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="068f6-199">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-200">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="068f6-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-202">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="068f6-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="068f6-203">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="068f6-203">Target operating system of the software element.</span></span>

<span data-ttu-id="068f6-204">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="068f6-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="068f6-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="068f6-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="068f6-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="068f6-207"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="068f6-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-208">Mac OS</span><span class="sxs-lookup"><span data-stu-id="068f6-208">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="068f6-209"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="068f6-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-210">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="068f6-210">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="068f6-211"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="068f6-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="068f6-212"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="068f6-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="068f6-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="068f6-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="068f6-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="068f6-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-215">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="068f6-215">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="068f6-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="068f6-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-217">HP-UX</span><span class="sxs-lookup"><span data-stu-id="068f6-217">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="068f6-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="068f6-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="068f6-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="068f6-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="068f6-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="068f6-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="068f6-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="068f6-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="068f6-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="068f6-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-223">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="068f6-223">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="068f6-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="068f6-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="068f6-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="068f6-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-226">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="068f6-226">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="068f6-227"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="068f6-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-228">Windows 95</span><span class="sxs-lookup"><span data-stu-id="068f6-228">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="068f6-229"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="068f6-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-230">Windows 98</span><span class="sxs-lookup"><span data-stu-id="068f6-230">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="068f6-231"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="068f6-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-232">Windows NT</span><span class="sxs-lookup"><span data-stu-id="068f6-232">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="068f6-233"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="068f6-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-234">Windows CE</span><span class="sxs-lookup"><span data-stu-id="068f6-234">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="068f6-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="068f6-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-236">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="068f6-236">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="068f6-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="068f6-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="068f6-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="068f6-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="068f6-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="068f6-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="068f6-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="068f6-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="068f6-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="068f6-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="068f6-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="068f6-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="068f6-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="068f6-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="068f6-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="068f6-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="068f6-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="068f6-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="068f6-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="068f6-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="068f6-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="068f6-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="068f6-248"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="068f6-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-249">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="068f6-249">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="068f6-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="068f6-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-251">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="068f6-251">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="068f6-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="068f6-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-253">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="068f6-253">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="068f6-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="068f6-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-255">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="068f6-255">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="068f6-256"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="068f6-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="068f6-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="068f6-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="068f6-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="068f6-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="068f6-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="068f6-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="068f6-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="068f6-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="068f6-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="068f6-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-262">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="068f6-262">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="068f6-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="068f6-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="068f6-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="068f6-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="068f6-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="068f6-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="068f6-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="068f6-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-267">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="068f6-267">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="068f6-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="068f6-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="068f6-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="068f6-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="068f6-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="068f6-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="068f6-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="068f6-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="068f6-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="068f6-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="068f6-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="068f6-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="068f6-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="068f6-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="068f6-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="068f6-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="068f6-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="068f6-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="068f6-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="068f6-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="068f6-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="068f6-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="068f6-279">Palm OS</span><span class="sxs-lookup"><span data-stu-id="068f6-279">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="068f6-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="068f6-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="068f6-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="068f6-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="068f6-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="068f6-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="068f6-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="068f6-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="068f6-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="068f6-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="068f6-285">**Version**</span><span class="sxs-lookup"><span data-stu-id="068f6-285">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068f6-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="068f6-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068f6-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="068f6-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068f6-288">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="068f6-288">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="068f6-289">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="068f6-289">Version of the operation.</span></span>

<span data-ttu-id="068f6-290">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="068f6-290">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="068f6-291"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="068f6-291"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="068f6-292"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="068f6-292"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="068f6-293">Diese Eigenschaft wird von der [**CIM- \_ Check**](cim-check.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="068f6-293">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="068f6-294">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="068f6-294">Remarks</span></span>

<span data-ttu-id="068f6-295">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="068f6-295">WMI does not implement this class.</span></span>

<span data-ttu-id="068f6-296">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="068f6-296">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="068f6-297">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="068f6-297">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="068f6-298">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="068f6-298">Requirements</span></span>



| <span data-ttu-id="068f6-299">Anforderung</span><span class="sxs-lookup"><span data-stu-id="068f6-299">Requirement</span></span> | <span data-ttu-id="068f6-300">Wert</span><span class="sxs-lookup"><span data-stu-id="068f6-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="068f6-301">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="068f6-301">Minimum supported client</span></span><br/> | <span data-ttu-id="068f6-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="068f6-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="068f6-303">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="068f6-303">Minimum supported server</span></span><br/> | <span data-ttu-id="068f6-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="068f6-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="068f6-305">Namespace</span><span class="sxs-lookup"><span data-stu-id="068f6-305">Namespace</span></span><br/>                | <span data-ttu-id="068f6-306">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="068f6-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="068f6-307">MOF</span><span class="sxs-lookup"><span data-stu-id="068f6-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="068f6-308"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="068f6-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="068f6-309">DLL</span><span class="sxs-lookup"><span data-stu-id="068f6-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="068f6-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="068f6-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068f6-311">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="068f6-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068f6-312">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="068f6-312">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

