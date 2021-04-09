---
title: Win32_TSRemoteDesktop-Klasse
description: Beschreibt eine Remote Desktop Verbindung, die über Remotedesktop Webzugriff (RD Webzugriff) verfügbar ist.
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteDesktop-Klasse Remotedesktopdienste
- Win32_TSRemoteDesktop Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103006"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="35ab3-105">Win32 \_ -Klasse "Klasse-Remotedesktop"</span><span class="sxs-lookup"><span data-stu-id="35ab3-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="35ab3-106">Beschreibt eine Remote Desktop Verbindung, die über Remotedesktop Webzugriff (RD Webzugriff) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="35ab3-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="35ab3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35ab3-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="35ab3-108">Member</span><span class="sxs-lookup"><span data-stu-id="35ab3-108">Members</span></span>

<span data-ttu-id="35ab3-109">Die **Win32 \_ -Klasse "zremotedesktop** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="35ab3-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="35ab3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35ab3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35ab3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35ab3-111">Properties</span></span>

<span data-ttu-id="35ab3-112">Die **Win32-Klasse "Klasse \_ -Remotedesktop** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="35ab3-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35ab3-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="35ab3-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-116">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="35ab3-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-117">Der Alias der Remote Desktop Verbindung.</span><span class="sxs-lookup"><span data-stu-id="35ab3-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="35ab3-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="35ab3-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-122">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="35ab3-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="35ab3-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="35ab3-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35ab3-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-127">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="35ab3-127">Description of the object.</span></span>

<span data-ttu-id="35ab3-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="35ab3-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-129">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="35ab3-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-130">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="35ab3-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-132">Der Byte Inhalt des Symbols, das der Remote Desktop Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="35ab3-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-133">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="35ab3-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-134">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="35ab3-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-136">Der Index oder die ID des Symbols für die Remote Desktop Verbindung.</span><span class="sxs-lookup"><span data-stu-id="35ab3-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-137">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="35ab3-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-140">Der Pfad des Symbols für die Remote Desktop Verbindung.</span><span class="sxs-lookup"><span data-stu-id="35ab3-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35ab3-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-142">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="35ab3-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="35ab3-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-145">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="35ab3-145">The date the object was installed.</span></span> <span data-ttu-id="35ab3-146">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="35ab3-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="35ab3-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="35ab3-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-148">**Isvmfarm**</span><span class="sxs-lookup"><span data-stu-id="35ab3-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-149">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="35ab3-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-151">Gibt an, ob diese Remote Desktop Verbindung zu einer Farm virtueller Maschinen gehört.</span><span class="sxs-lookup"><span data-stu-id="35ab3-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="35ab3-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-155">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="35ab3-155">The name of the object.</span></span>

<span data-ttu-id="35ab3-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="35ab3-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-157">**Rdpfilecontents**</span><span class="sxs-lookup"><span data-stu-id="35ab3-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-160">Inhalt der RDP-Datei, die der Remote Desktop Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="35ab3-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="35ab3-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-164">Eine Sicherheits Beschreibung, die den Zugriff auf die Remote Desktop Verbindung im SDDL-Format steuert.</span><span class="sxs-lookup"><span data-stu-id="35ab3-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="35ab3-165">Eine leere Zeichenfolge impliziert den gesamten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="35ab3-165">An empty string implies allow all access.</span></span> <span data-ttu-id="35ab3-166">Diese Sicherheits Beschreibung unterstützt keine deny-ACEs oder ACEs, die auf Benutzer oder Gruppen von nicht-Domänen verweisen.</span><span class="sxs-lookup"><span data-stu-id="35ab3-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-167">**Showinportal**</span><span class="sxs-lookup"><span data-stu-id="35ab3-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="35ab3-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-170">Gibt an, ob die Remote Desktop Verbindung in RD-Webzugriff angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35ab3-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="35ab3-171">**Status**</span><span class="sxs-lookup"><span data-stu-id="35ab3-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-174">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="35ab3-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-175">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="35ab3-175">Current status of the object.</span></span> <span data-ttu-id="35ab3-176">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="35ab3-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="35ab3-177">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="35ab3-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="35ab3-178">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="35ab3-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="35ab3-179">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="35ab3-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="35ab3-180">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="35ab3-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="35ab3-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="35ab3-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="35ab3-182">("OK")</span><span class="sxs-lookup"><span data-stu-id="35ab3-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-183">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="35ab3-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-184">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="35ab3-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-185">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="35ab3-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-186">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="35ab3-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-187">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="35ab3-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-188">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="35ab3-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35ab3-189">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="35ab3-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35ab3-190">**Vmfarmsettings**</span><span class="sxs-lookup"><span data-stu-id="35ab3-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ab3-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35ab3-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ab3-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="35ab3-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35ab3-193">Farm Einstellungen der virtuellen Maschine für die Remote Desktop Verbindung.</span><span class="sxs-lookup"><span data-stu-id="35ab3-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35ab3-194">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35ab3-194">Remarks</span></span>

<span data-ttu-id="35ab3-195">Sie müssen Mitglied der Gruppe "Administratoren" sein, um Eigenschaften mithilfe dieser Klasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="35ab3-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="35ab3-196">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="35ab3-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="35ab3-197">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="35ab3-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="35ab3-198">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="35ab3-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="35ab3-199">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="35ab3-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="35ab3-200">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="35ab3-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35ab3-201">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="35ab3-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="35ab3-202">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="35ab3-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35ab3-203">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="35ab3-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="35ab3-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35ab3-204">Requirements</span></span>



| <span data-ttu-id="35ab3-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35ab3-205">Requirement</span></span> | <span data-ttu-id="35ab3-206">Wert</span><span class="sxs-lookup"><span data-stu-id="35ab3-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35ab3-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35ab3-207">Minimum supported client</span></span><br/> | <span data-ttu-id="35ab3-208">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="35ab3-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="35ab3-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35ab3-209">Minimum supported server</span></span><br/> | <span data-ttu-id="35ab3-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35ab3-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35ab3-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="35ab3-211">Namespace</span></span><br/>                | <span data-ttu-id="35ab3-212">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="35ab3-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="35ab3-213">MOF</span><span class="sxs-lookup"><span data-stu-id="35ab3-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35ab3-214"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="35ab3-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="35ab3-215">DLL</span><span class="sxs-lookup"><span data-stu-id="35ab3-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ab3-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ab3-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

