---
description: Win32 \_ PageFileUsage&\# 8194; WMI-Klasse stellt die Datei dar, die zum Verarbeiten des Austauschs von virtuellen Speicherdateien in einem Win32-System verwendet wird. Informationen, die in Objekten enthalten sind, die von dieser Klasse instanziiert werden, geben den Lauf Zeit Zustand der Auslagerungs Datei an.
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Win32_PageFileUsage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524096"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="d1f95-104">Win32 \_ PageFileUsage-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1f95-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="d1f95-105">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ PageFileUsage**" stellt die Datei dar, die zum Verarbeiten des Austauschs von virtuellen Speicherdateien in einem Win32-System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1f95-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="d1f95-106">Informationen, die in Objekten enthalten sind, die von dieser Klasse instanziiert werden, geben den Lauf Zeit Zustand der Auslagerungs Datei an.</span><span class="sxs-lookup"><span data-stu-id="d1f95-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="d1f95-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1f95-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1f95-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1f95-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f95-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1f95-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="d1f95-110">Member</span><span class="sxs-lookup"><span data-stu-id="d1f95-110">Members</span></span>

<span data-ttu-id="d1f95-111">Die **Win32-Klasse \_ PageFileUsage** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d1f95-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="d1f95-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1f95-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1f95-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1f95-113">Properties</span></span>

<span data-ttu-id="d1f95-114">Die **Win32-Klasse \_ PageFileUsage** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1f95-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1f95-115">**"Zubei Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="d1f95-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1f95-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-118">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabyte")</span><span class="sxs-lookup"><span data-stu-id="d1f95-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-119">Tatsächlicher Speicherplatz, der für die Verwendung mit dieser Auslagerungs Datei reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="d1f95-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="d1f95-120">Dieser Wert entspricht dem Bereich, der in [**Win32 \_ pagefilesetting**](win32-pagefilesetting.md) unter den Eigenschaften **InitialSize** und **MaximumSize** festgelegt wird, die beim Systemstart festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d1f95-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="d1f95-121">Beispiel: 178</span><span class="sxs-lookup"><span data-stu-id="d1f95-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1f95-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1f95-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-125">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1f95-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-126">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d1f95-126">A short textual description of the object.</span></span>

<span data-ttu-id="d1f95-127">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1f95-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-128">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="d1f95-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1f95-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-131">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabyte")</span><span class="sxs-lookup"><span data-stu-id="d1f95-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-132">Menge an Speicherplatz, der derzeit von der Auslagerungs Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1f95-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1f95-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1f95-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-136">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d1f95-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-137">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d1f95-137">A textual description of the object.</span></span>

<span data-ttu-id="d1f95-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1f95-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1f95-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1f95-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-142">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="d1f95-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-143">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1f95-143">Indicates when the object was installed.</span></span> <span data-ttu-id="d1f95-144">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1f95-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1f95-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1f95-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1f95-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1f95-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-149">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1f95-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-150">Der Name der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="d1f95-150">Name of the page file.</span></span>

<span data-ttu-id="d1f95-151">Beispiel: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="d1f95-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-152">**Peer Usage**</span><span class="sxs-lookup"><span data-stu-id="d1f95-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1f95-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-155">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabyte")</span><span class="sxs-lookup"><span data-stu-id="d1f95-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-156">Die Datei mit der höchsten Verwendungs Seite.</span><span class="sxs-lookup"><span data-stu-id="d1f95-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="d1f95-157">**Status**</span><span class="sxs-lookup"><span data-stu-id="d1f95-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1f95-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-160">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d1f95-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-161">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="d1f95-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1f95-162">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1f95-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1f95-163">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1f95-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1f95-164">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="d1f95-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1f95-165">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1f95-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1f95-166">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d1f95-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1f95-167">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="d1f95-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1f95-168">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1f95-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1f95-169">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="d1f95-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1f95-170">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d1f95-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1f95-171">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="d1f95-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1f95-172">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="d1f95-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1f95-173">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d1f95-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1f95-174">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d1f95-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1f95-175">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="d1f95-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1f95-176">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="d1f95-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1f95-177">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="d1f95-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1f95-178">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="d1f95-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1f95-179">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="d1f95-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1f95-180">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="d1f95-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1f95-181">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="d1f95-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1f95-182">**Temppagefile**</span><span class="sxs-lookup"><span data-stu-id="d1f95-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1f95-183">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d1f95-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1f95-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1f95-185">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| temppagefile")</span><span class="sxs-lookup"><span data-stu-id="d1f95-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="d1f95-186">**True** gibt an, dass eine temporäre Auslagerungs Datei erstellt wurde, in der Regel, weil keine permanente Auslagerungs Datei auf dem aktuellen Computersystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d1f95-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1f95-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1f95-187">Remarks</span></span>

<span data-ttu-id="d1f95-188">Die **Win32-Klasse \_ PageFileUsage** ist von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1f95-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f95-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1f95-189">Requirements</span></span>



| <span data-ttu-id="d1f95-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1f95-190">Requirement</span></span> | <span data-ttu-id="d1f95-191">Wert</span><span class="sxs-lookup"><span data-stu-id="d1f95-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f95-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1f95-192">Minimum supported client</span></span><br/> | <span data-ttu-id="d1f95-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1f95-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1f95-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1f95-194">Minimum supported server</span></span><br/> | <span data-ttu-id="d1f95-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1f95-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1f95-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1f95-196">Namespace</span></span><br/>                | <span data-ttu-id="d1f95-197">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1f95-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1f95-198">MOF</span><span class="sxs-lookup"><span data-stu-id="d1f95-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1f95-199"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1f95-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1f95-200">DLL</span><span class="sxs-lookup"><span data-stu-id="d1f95-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1f95-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1f95-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1f95-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1f95-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f95-203">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d1f95-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="d1f95-204">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="d1f95-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
