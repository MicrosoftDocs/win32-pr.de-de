---
description: Die Win32 \_ classiccomclass-WMI-Klasse stellt die Eigenschaften einer COM-Komponente dar.
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Win32_ClassicCOMClass-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346647"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="eca74-103">Win32 \_ classiccomclass-Klasse</span><span class="sxs-lookup"><span data-stu-id="eca74-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="eca74-104">Die **Win32 \_ classiccomclass** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Eigenschaften einer COM-Komponente dar.</span><span class="sxs-lookup"><span data-stu-id="eca74-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="eca74-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eca74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="eca74-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eca74-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca74-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca74-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="eca74-108">Member</span><span class="sxs-lookup"><span data-stu-id="eca74-108">Members</span></span>

<span data-ttu-id="eca74-109">Die **Win32 \_ classiccomclass** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eca74-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="eca74-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eca74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eca74-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eca74-111">Properties</span></span>

<span data-ttu-id="eca74-112">Die **Win32 \_ classiccomclass** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eca74-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eca74-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eca74-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca74-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eca74-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eca74-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca74-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca74-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="eca74-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eca74-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eca74-117">A short textual description of the object.</span></span>

<span data-ttu-id="eca74-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eca74-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eca74-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="eca74-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca74-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eca74-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eca74-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca74-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca74-122">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes Software Classes \\ \\ CLSID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="eca74-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="eca74-123">GUID (Global Unique Identifier) dieser com-Klasse.</span><span class="sxs-lookup"><span data-stu-id="eca74-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="eca74-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eca74-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca74-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eca74-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eca74-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca74-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca74-127">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="eca74-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eca74-128">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eca74-128">A textual description of the object.</span></span>

<span data-ttu-id="eca74-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eca74-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eca74-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eca74-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca74-131">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eca74-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eca74-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca74-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca74-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="eca74-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eca74-134">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="eca74-134">Indicates when the object was installed.</span></span> <span data-ttu-id="eca74-135">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eca74-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="eca74-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eca74-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eca74-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="eca74-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca74-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eca74-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eca74-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca74-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca74-140">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="eca74-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="eca74-141">Die Name-Eigenschaft enthält den lesbaren Namen für die com-Klasse.</span><span class="sxs-lookup"><span data-stu-id="eca74-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="eca74-142">**Status**</span><span class="sxs-lookup"><span data-stu-id="eca74-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca74-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eca74-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eca74-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca74-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca74-145">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="eca74-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eca74-146">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="eca74-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="eca74-147">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="eca74-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="eca74-148">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="eca74-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="eca74-149">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="eca74-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="eca74-150">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="eca74-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="eca74-151">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="eca74-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="eca74-152">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="eca74-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="eca74-153">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eca74-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eca74-154">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="eca74-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eca74-155">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="eca74-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eca74-156">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="eca74-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eca74-157">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="eca74-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eca74-158">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="eca74-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eca74-159">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="eca74-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eca74-160">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="eca74-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eca74-161">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="eca74-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eca74-162">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="eca74-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eca74-163">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="eca74-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eca74-164">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="eca74-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eca74-165">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="eca74-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eca74-166">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="eca74-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="eca74-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eca74-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="eca74-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eca74-168">Remarks</span></span>

<span data-ttu-id="eca74-169">Die **Win32 \_ classiccomclass** -Klasse wird von der [**Win32 \_ ComClass**](win32-comclass.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eca74-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eca74-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eca74-170">Requirements</span></span>



| <span data-ttu-id="eca74-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eca74-171">Requirement</span></span> | <span data-ttu-id="eca74-172">Wert</span><span class="sxs-lookup"><span data-stu-id="eca74-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eca74-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eca74-173">Minimum supported client</span></span><br/> | <span data-ttu-id="eca74-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eca74-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eca74-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eca74-175">Minimum supported server</span></span><br/> | <span data-ttu-id="eca74-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eca74-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eca74-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="eca74-177">Namespace</span></span><br/>                | <span data-ttu-id="eca74-178">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eca74-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eca74-179">MOF</span><span class="sxs-lookup"><span data-stu-id="eca74-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eca74-180"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eca74-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eca74-181">DLL</span><span class="sxs-lookup"><span data-stu-id="eca74-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eca74-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eca74-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca74-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eca74-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca74-184">**Win32- \_ ComClass**</span><span class="sxs-lookup"><span data-stu-id="eca74-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="eca74-185">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eca74-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

