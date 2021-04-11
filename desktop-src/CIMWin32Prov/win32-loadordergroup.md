---
description: Die \_ WMI-Klasse von Win32 LoadOrderGroup stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren.
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Win32_LoadOrderGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127484"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="27a02-103">Win32 \_ LoadOrderGroup-Klasse</span><span class="sxs-lookup"><span data-stu-id="27a02-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="27a02-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) von **Win32 \_ LoadOrderGroup** stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="27a02-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="27a02-105">Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="27a02-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="27a02-106">Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="27a02-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="27a02-107">Die Daten in dieser Klasse werden vom Anbieter vom Registrierungsschlüssel abgeleitet: **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**.</span><span class="sxs-lookup"><span data-stu-id="27a02-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="27a02-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27a02-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="27a02-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="27a02-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a02-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="27a02-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="27a02-111">Member</span><span class="sxs-lookup"><span data-stu-id="27a02-111">Members</span></span>

<span data-ttu-id="27a02-112">Die **Win32 \_ LoadOrderGroup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27a02-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="27a02-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27a02-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27a02-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27a02-114">Properties</span></span>

<span data-ttu-id="27a02-115">Die **Win32 \_ LoadOrderGroup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27a02-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27a02-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="27a02-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27a02-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="27a02-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-120">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="27a02-120">A short textual description of the object.</span></span>

<span data-ttu-id="27a02-121">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27a02-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27a02-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27a02-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27a02-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-125">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="27a02-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-126">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="27a02-126">A textual description of the object.</span></span>

<span data-ttu-id="27a02-127">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27a02-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27a02-128">**Driveraktiviert**</span><span class="sxs-lookup"><span data-stu-id="27a02-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27a02-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ grouporderlist")</span><span class="sxs-lookup"><span data-stu-id="27a02-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-132">Gibt an, ob diese Gruppe der Lade Reihenfolge Treiber und Systemdienste enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="27a02-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="27a02-133">**GroupOrder**</span><span class="sxs-lookup"><span data-stu-id="27a02-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27a02-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-136">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ grouporderlist")</span><span class="sxs-lookup"><span data-stu-id="27a02-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-137">Die Reihenfolge, in der diese Dienstgruppe auf das Betriebssystem geladen wird.</span><span class="sxs-lookup"><span data-stu-id="27a02-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="27a02-138">Beispiel: 2</span><span class="sxs-lookup"><span data-stu-id="27a02-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="27a02-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="27a02-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="27a02-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="27a02-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-143">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="27a02-143">Indicates when the object was installed.</span></span> <span data-ttu-id="27a02-144">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="27a02-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="27a02-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27a02-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27a02-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="27a02-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27a02-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-149">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ grouporderlist")</span><span class="sxs-lookup"><span data-stu-id="27a02-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-150">Der Name der Gruppe der Lade Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="27a02-150">Name of the load order group.</span></span>

<span data-ttu-id="27a02-151">Beispiel: "primärer Datenträger"</span><span class="sxs-lookup"><span data-stu-id="27a02-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="27a02-152">**Status**</span><span class="sxs-lookup"><span data-stu-id="27a02-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27a02-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27a02-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27a02-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27a02-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27a02-155">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="27a02-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="27a02-156">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="27a02-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="27a02-157">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="27a02-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="27a02-158">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="27a02-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="27a02-159">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="27a02-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="27a02-160">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="27a02-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="27a02-161">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="27a02-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="27a02-162">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="27a02-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="27a02-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27a02-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="27a02-164">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="27a02-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="27a02-165">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="27a02-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="27a02-166">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="27a02-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27a02-167">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="27a02-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27a02-168">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="27a02-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="27a02-169">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="27a02-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="27a02-170">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="27a02-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="27a02-171">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="27a02-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="27a02-172">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="27a02-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="27a02-173">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="27a02-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="27a02-174">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="27a02-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="27a02-175">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="27a02-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="27a02-176">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="27a02-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="27a02-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="27a02-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="27a02-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27a02-178">Remarks</span></span>

<span data-ttu-id="27a02-179">Die **Win32 \_ LoadOrderGroup** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="27a02-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27a02-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27a02-180">Requirements</span></span>



| <span data-ttu-id="27a02-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27a02-181">Requirement</span></span> | <span data-ttu-id="27a02-182">Wert</span><span class="sxs-lookup"><span data-stu-id="27a02-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27a02-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27a02-183">Minimum supported client</span></span><br/> | <span data-ttu-id="27a02-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27a02-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27a02-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27a02-185">Minimum supported server</span></span><br/> | <span data-ttu-id="27a02-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27a02-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27a02-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="27a02-187">Namespace</span></span><br/>                | <span data-ttu-id="27a02-188">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="27a02-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27a02-189">MOF</span><span class="sxs-lookup"><span data-stu-id="27a02-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27a02-190"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="27a02-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27a02-191">DLL</span><span class="sxs-lookup"><span data-stu-id="27a02-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27a02-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27a02-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27a02-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27a02-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a02-194">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="27a02-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="27a02-195">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27a02-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

