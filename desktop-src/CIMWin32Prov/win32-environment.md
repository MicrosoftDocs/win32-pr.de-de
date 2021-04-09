---
description: Stellt eine Umgebung oder eine System Umgebungs Einstellung auf einem Windows-Computersystem dar.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Win32_Environment-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861715"
---
# <a name="win32_environment-class"></a><span data-ttu-id="add92-103">Win32- \_ Umgebungs Klasse</span><span class="sxs-lookup"><span data-stu-id="add92-103">Win32\_Environment class</span></span>

<span data-ttu-id="add92-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32- \_ Umgebung** stellt eine Umgebung oder eine System Umgebungs Einstellung auf einem Windows-Computersystem dar.</span><span class="sxs-lookup"><span data-stu-id="add92-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="add92-105">Durch Abfragen dieser Klasse werden die Umgebungsvariablen zurückgegeben, die in gefunden werden</span><span class="sxs-lookup"><span data-stu-id="add92-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="add92-106">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SessionManager** \\ **Environment**</span><span class="sxs-lookup"><span data-stu-id="add92-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="add92-107">und</span><span class="sxs-lookup"><span data-stu-id="add92-107">and</span></span>

<span data-ttu-id="add92-108">**HKEY \_** Benutzerumgebung für \\ **< Benutzer >** \\ </span><span class="sxs-lookup"><span data-stu-id="add92-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="add92-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="add92-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="add92-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="add92-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="add92-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="add92-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="add92-112">Member</span><span class="sxs-lookup"><span data-stu-id="add92-112">Members</span></span>

<span data-ttu-id="add92-113">Die **Win32- \_ Umgebungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="add92-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="add92-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="add92-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="add92-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="add92-115">Properties</span></span>

<span data-ttu-id="add92-116">Die **Win32- \_ Umgebungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="add92-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="add92-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="add92-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="add92-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add92-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="add92-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add92-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="add92-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="add92-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="add92-121">A short textual description of the object.</span></span>

<span data-ttu-id="add92-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="add92-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="add92-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="add92-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="add92-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add92-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="add92-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add92-126">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="add92-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="add92-127">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="add92-127">A textual description of the object.</span></span>

<span data-ttu-id="add92-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="add92-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="add92-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="add92-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="add92-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="add92-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="add92-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add92-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="add92-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="add92-133">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="add92-133">Indicates when the object was installed.</span></span> <span data-ttu-id="add92-134">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="add92-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="add92-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="add92-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="add92-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="add92-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="add92-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add92-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="add92-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="add92-139">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="add92-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="add92-140">Zeichenfolge, die den Namen einer Windows-basierten Umgebungsvariablen angibt.</span><span class="sxs-lookup"><span data-stu-id="add92-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="add92-141">Wenn Sie den Namen einer Variablen angeben, die noch nicht vorhanden ist, erstellt eine Anwendung eine neue Umgebungsvariable.</span><span class="sxs-lookup"><span data-stu-id="add92-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="add92-142">Beispiel: "Path"</span><span class="sxs-lookup"><span data-stu-id="add92-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="add92-143">**Status**</span><span class="sxs-lookup"><span data-stu-id="add92-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="add92-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add92-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="add92-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add92-146">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="add92-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="add92-147">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="add92-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="add92-148">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="add92-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="add92-149">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="add92-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="add92-150">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="add92-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="add92-151">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="add92-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="add92-152">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="add92-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="add92-153">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="add92-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="add92-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="add92-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="add92-155">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="add92-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="add92-156">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="add92-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="add92-157">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="add92-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="add92-158">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="add92-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="add92-159">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="add92-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="add92-160">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="add92-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="add92-161">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="add92-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="add92-162">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="add92-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="add92-163">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="add92-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="add92-164">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="add92-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="add92-165">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="add92-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="add92-166">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="add92-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="add92-167">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="add92-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="add92-168">**Systemvariable**</span><span class="sxs-lookup"><span data-stu-id="add92-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-169">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="add92-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="add92-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="add92-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add92-171">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="add92-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="add92-172">Gibt an, ob die Variable eine Systemvariable ist.</span><span class="sxs-lookup"><span data-stu-id="add92-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="add92-173">Eine Systemvariable wird vom Betriebssystem festgelegt und ist unabhängig von den Einstellungen der Benutzerumgebung.</span><span class="sxs-lookup"><span data-stu-id="add92-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="add92-174">**UserName**</span><span class="sxs-lookup"><span data-stu-id="add92-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="add92-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add92-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="add92-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add92-177">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="add92-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="add92-178">Der Name des Besitzers der Umgebungs Einstellung.</span><span class="sxs-lookup"><span data-stu-id="add92-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="add92-179">Der Wert ist <SYSTEM> für Einstellungen festgelegt, die für das Windows-basierte System (im Gegensatz zu einem bestimmten Benutzer) und <DEFAULT> für Standardbenutzer Einstellungen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="add92-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="add92-180">Beispiel: "jsmith"</span><span class="sxs-lookup"><span data-stu-id="add92-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="add92-181">**VariableValue**</span><span class="sxs-lookup"><span data-stu-id="add92-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add92-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="add92-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add92-183">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="add92-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="add92-184">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="add92-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="add92-185">Platzhalter Variable einer Windows-basierten Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="add92-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="add92-186">Informationen wie das Dateisystem Verzeichnis können von Computer zu Computer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="add92-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="add92-187">Das Betriebssystem ersetzt Platzhalter für diese.</span><span class="sxs-lookup"><span data-stu-id="add92-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="add92-188">Beispiel: "% SystemRoot%"</span><span class="sxs-lookup"><span data-stu-id="add92-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="add92-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="add92-189">Remarks</span></span>

<span data-ttu-id="add92-190">Die **Win32- \_ Umgebungs** Klasse wird von [**CIM \_ Systemresource**](cim-systemresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="add92-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="add92-191">Sie können diese Klasse verwenden, um die Pfade spezieller Ordner, wie z. b. den System Ordner oder die Programmdateien auf einem Remote Computer, zu suchen.</span><span class="sxs-lookup"><span data-stu-id="add92-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="add92-192">Einige Beispiele sind: windir, systemroot, Program Files und User Profile.</span><span class="sxs-lookup"><span data-stu-id="add92-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="add92-193">**Win32 \_ Die Umgebung** gibt im Grunde Folgendes zurück:</span><span class="sxs-lookup"><span data-stu-id="add92-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="add92-194">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SessionManager** \\ **Environment**</span><span class="sxs-lookup"><span data-stu-id="add92-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="add92-195">und</span><span class="sxs-lookup"><span data-stu-id="add92-195">and</span></span>

<span data-ttu-id="add92-196">**HKEY \_** Benutzerumgebung für \\ **< Benutzer >** \\ </span><span class="sxs-lookup"><span data-stu-id="add92-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="add92-197">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="add92-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="add92-198">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="add92-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="add92-199">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="add92-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="add92-200">Beispiele</span><span class="sxs-lookup"><span data-stu-id="add92-200">Examples</span></span>

<span data-ttu-id="add92-201">Im Beispiel [Umgebungsvariablen auf einem Computer auflisten](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) wird WMI verwendet, um Informationen zu allen Umgebungsvariablen auf einem Computer zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="add92-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="add92-202">Im folgenden VBScript-Codebeispiel werden die Umgebungsvariablen auf dem lokalen Computer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="add92-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="add92-203">Im folgenden VBScript-Codebeispiel wird eine Umgebungsvariable mit dem Namen \_ Buildtyp in einen vom Benutzer eingegebenen Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="add92-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="add92-204">Das Skript geht davon aus, dass die \_ Buildtyp Variable bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="add92-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="add92-205">Wenn Sie nicht vorhanden ist, wird das Skript beendet.</span><span class="sxs-lookup"><span data-stu-id="add92-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="add92-206">Der Eingabe Wert ist aktiviert: er muss entweder "Build1", "Build2" oder "Build3" lauten, und es wird kein anderer Wert akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="add92-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="add92-207">Die VBScript- [UCase](https://msdn.microsoft.com/library/aa902519.aspx) -Funktion macht die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="add92-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="add92-208">Wenn das, was in eingegeben wird, nicht einer der drei zulässigen Werte ist, wird das Skript beendet.</span><span class="sxs-lookup"><span data-stu-id="add92-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="add92-209">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="add92-209">Requirements</span></span>



| <span data-ttu-id="add92-210">Anforderung</span><span class="sxs-lookup"><span data-stu-id="add92-210">Requirement</span></span> | <span data-ttu-id="add92-211">Wert</span><span class="sxs-lookup"><span data-stu-id="add92-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="add92-212">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="add92-212">Minimum supported client</span></span><br/> | <span data-ttu-id="add92-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="add92-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="add92-214">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="add92-214">Minimum supported server</span></span><br/> | <span data-ttu-id="add92-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="add92-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="add92-216">Namespace</span><span class="sxs-lookup"><span data-stu-id="add92-216">Namespace</span></span><br/>                | <span data-ttu-id="add92-217">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="add92-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="add92-218">MOF</span><span class="sxs-lookup"><span data-stu-id="add92-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="add92-219"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="add92-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="add92-220">DLL</span><span class="sxs-lookup"><span data-stu-id="add92-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="add92-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="add92-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add92-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="add92-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add92-223">**CIM- \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="add92-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="add92-224">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="add92-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

