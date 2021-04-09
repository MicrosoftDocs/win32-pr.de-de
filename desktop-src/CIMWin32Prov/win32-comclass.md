---
description: Die \_ WMI-Klasse für eine abstrakte ComClass-Klasse stellt die Eigenschaften einer COM-Komponente (Component Object Model) dar.
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Win32_COMClass-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958515"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="0aa33-103">Win32 \_ ComClass-Klasse</span><span class="sxs-lookup"><span data-stu-id="0aa33-103">Win32\_COMClass class</span></span>

<span data-ttu-id="0aa33-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für eine abstrakte **\_ ComClass** -Klasse stellt die Eigenschaften einer COM-Komponente (Component Object Model) dar.</span><span class="sxs-lookup"><span data-stu-id="0aa33-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="0aa33-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0aa33-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0aa33-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0aa33-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa33-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0aa33-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="0aa33-108">Member</span><span class="sxs-lookup"><span data-stu-id="0aa33-108">Members</span></span>

<span data-ttu-id="0aa33-109">Die **Win32 \_ ComClass** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0aa33-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="0aa33-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0aa33-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0aa33-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0aa33-111">Properties</span></span>

<span data-ttu-id="0aa33-112">Die **Win32 \_ ComClass** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0aa33-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0aa33-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0aa33-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aa33-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa33-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0aa33-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0aa33-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0aa33-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0aa33-117">A short textual description of the object.</span></span>

<span data-ttu-id="0aa33-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0aa33-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0aa33-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0aa33-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aa33-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa33-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0aa33-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-122">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0aa33-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0aa33-123">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0aa33-123">A textual description of the object.</span></span>

<span data-ttu-id="0aa33-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0aa33-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0aa33-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0aa33-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aa33-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0aa33-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0aa33-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="0aa33-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0aa33-129">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0aa33-129">Indicates when the object was installed.</span></span> <span data-ttu-id="0aa33-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0aa33-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0aa33-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0aa33-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0aa33-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="0aa33-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aa33-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa33-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0aa33-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-135">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0aa33-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0aa33-136">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0aa33-136">Label by which the object is known.</span></span> <span data-ttu-id="0aa33-137">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0aa33-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0aa33-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0aa33-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0aa33-139">**Status**</span><span class="sxs-lookup"><span data-stu-id="0aa33-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aa33-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa33-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0aa33-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0aa33-142">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0aa33-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0aa33-143">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="0aa33-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="0aa33-144">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0aa33-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0aa33-145">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aa33-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0aa33-146">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="0aa33-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0aa33-147">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aa33-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0aa33-148">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0aa33-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0aa33-149">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0aa33-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0aa33-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0aa33-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0aa33-151">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="0aa33-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0aa33-152">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0aa33-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0aa33-153">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0aa33-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0aa33-154">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0aa33-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0aa33-155">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0aa33-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0aa33-156">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0aa33-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0aa33-157">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0aa33-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0aa33-158">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="0aa33-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0aa33-159">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0aa33-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0aa33-160">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="0aa33-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0aa33-161">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="0aa33-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0aa33-162">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="0aa33-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0aa33-163">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="0aa33-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="0aa33-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0aa33-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0aa33-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0aa33-165">Remarks</span></span>

<span data-ttu-id="0aa33-166">Die **Win32 \_ ComClass** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0aa33-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa33-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aa33-167">Requirements</span></span>



| <span data-ttu-id="0aa33-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0aa33-168">Requirement</span></span> | <span data-ttu-id="0aa33-169">Wert</span><span class="sxs-lookup"><span data-stu-id="0aa33-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa33-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0aa33-170">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa33-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0aa33-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0aa33-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0aa33-172">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa33-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0aa33-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0aa33-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="0aa33-174">Namespace</span></span><br/>                | <span data-ttu-id="0aa33-175">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0aa33-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0aa33-176">MOF</span><span class="sxs-lookup"><span data-stu-id="0aa33-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0aa33-177"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0aa33-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0aa33-178">DLL</span><span class="sxs-lookup"><span data-stu-id="0aa33-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aa33-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aa33-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa33-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aa33-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa33-181">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="0aa33-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="0aa33-182">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0aa33-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

