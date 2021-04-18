---
description: Die \_ WMI-Klasse von Win32 dcomapplication stellt die Eigenschaften einer DCOM-Anwendung dar.
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Win32_DCOMApplication-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338931"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="37cea-103">Win32 \_ dcomapplication-Klasse</span><span class="sxs-lookup"><span data-stu-id="37cea-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="37cea-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) von **Win32 \_ dcomapplication** stellt die Eigenschaften einer DCOM-Anwendung dar.</span><span class="sxs-lookup"><span data-stu-id="37cea-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="37cea-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37cea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="37cea-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="37cea-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37cea-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="37cea-108">Member</span><span class="sxs-lookup"><span data-stu-id="37cea-108">Members</span></span>

<span data-ttu-id="37cea-109">Die **Win32 \_ dcomapplication** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37cea-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="37cea-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37cea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37cea-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37cea-111">Properties</span></span>

<span data-ttu-id="37cea-112">Die **Win32 \_ dcomapplication** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37cea-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37cea-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="37cea-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cea-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37cea-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37cea-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cea-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37cea-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="37cea-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="37cea-117">GUID (Global Unique Identifier) für die DCOM-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="37cea-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="37cea-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="37cea-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cea-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37cea-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37cea-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cea-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37cea-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="37cea-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="37cea-122">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="37cea-122">A short textual description of the object.</span></span>

<span data-ttu-id="37cea-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cea-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37cea-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37cea-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cea-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37cea-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37cea-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cea-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37cea-127">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="37cea-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="37cea-128">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="37cea-128">A textual description of the object.</span></span>

<span data-ttu-id="37cea-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cea-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37cea-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="37cea-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cea-131">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="37cea-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37cea-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cea-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37cea-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="37cea-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="37cea-134">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="37cea-134">Indicates when the object was installed.</span></span> <span data-ttu-id="37cea-135">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="37cea-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="37cea-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cea-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37cea-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="37cea-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cea-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37cea-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37cea-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cea-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37cea-140">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="37cea-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="37cea-141">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="37cea-141">Label by which the object is known.</span></span> <span data-ttu-id="37cea-142">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="37cea-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="37cea-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cea-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37cea-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="37cea-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37cea-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="37cea-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37cea-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37cea-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37cea-147">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="37cea-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="37cea-148">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="37cea-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="37cea-149">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="37cea-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="37cea-150">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="37cea-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="37cea-151">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="37cea-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="37cea-152">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="37cea-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="37cea-153">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="37cea-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="37cea-154">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="37cea-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="37cea-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="37cea-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="37cea-156">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="37cea-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="37cea-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="37cea-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="37cea-158">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="37cea-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37cea-159">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="37cea-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37cea-160">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="37cea-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="37cea-161">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="37cea-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="37cea-162">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="37cea-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="37cea-163">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="37cea-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="37cea-164">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="37cea-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="37cea-165">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="37cea-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="37cea-166">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="37cea-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="37cea-167">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="37cea-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="37cea-168">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="37cea-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="37cea-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="37cea-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="37cea-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37cea-170">Remarks</span></span>

<span data-ttu-id="37cea-171">Die **Win32 \_ dcomapplication** -Klasse wird von [**Win32 \_ comapplication**](win32-comapplication.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="37cea-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37cea-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37cea-172">Requirements</span></span>



| <span data-ttu-id="37cea-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37cea-173">Requirement</span></span> | <span data-ttu-id="37cea-174">Wert</span><span class="sxs-lookup"><span data-stu-id="37cea-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37cea-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37cea-175">Minimum supported client</span></span><br/> | <span data-ttu-id="37cea-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37cea-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37cea-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37cea-177">Minimum supported server</span></span><br/> | <span data-ttu-id="37cea-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37cea-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37cea-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="37cea-179">Namespace</span></span><br/>                | <span data-ttu-id="37cea-180">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37cea-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37cea-181">MOF</span><span class="sxs-lookup"><span data-stu-id="37cea-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37cea-182"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37cea-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37cea-183">DLL</span><span class="sxs-lookup"><span data-stu-id="37cea-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37cea-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37cea-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37cea-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37cea-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cea-186">**Win32- \_ comapplication**</span><span class="sxs-lookup"><span data-stu-id="37cea-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="37cea-187">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37cea-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

