---
description: Die Win32 \_ componentcategory-WMI-Klasse stellt eine Komponenten Kategorie dar.
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Win32_ComponentCategory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958514"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="5e40e-103">Win32 \_ componentcategory-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e40e-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="5e40e-104">Die **Win32 \_ componentcategory** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt eine Komponenten Kategorie dar.</span><span class="sxs-lookup"><span data-stu-id="5e40e-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="5e40e-105">Komponenten Kategorien sind Gruppen von Component Object Model (com)-Klassen, für die ein definierter Funktionssatz zwischen Ihnen gemeinsam verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e40e-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="5e40e-106">Ein Client, der diese Schnittstellen verwendet, fragt die Registrierung nach dem Kategorietitel und dem eindeutigen Bezeichner namens **CategoryID** ab, der aus einer Globally Unique Identifier (GUID) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5e40e-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="5e40e-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e40e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5e40e-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5e40e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e40e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e40e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="5e40e-110">Member</span><span class="sxs-lookup"><span data-stu-id="5e40e-110">Members</span></span>

<span data-ttu-id="5e40e-111">Die **Win32 \_ componentcategory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5e40e-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="5e40e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e40e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e40e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e40e-113">Properties</span></span>

<span data-ttu-id="5e40e-114">Die **Win32 \_ componentcategory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e40e-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e40e-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5e40e-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e40e-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e40e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e40e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5e40e-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5e40e-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5e40e-119">A short textual description of the object.</span></span>

<span data-ttu-id="5e40e-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5e40e-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e40e-121">**CategoryID**</span><span class="sxs-lookup"><span data-stu-id="5e40e-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e40e-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e40e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e40e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-124">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Component Categories \| [**categoryinfo**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| CATID")</span><span class="sxs-lookup"><span data-stu-id="5e40e-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="5e40e-125">GUID für diese Komponenten Kategorie.</span><span class="sxs-lookup"><span data-stu-id="5e40e-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="5e40e-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e40e-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e40e-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e40e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e40e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-129">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5e40e-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5e40e-130">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5e40e-130">A textual description of the object.</span></span>

<span data-ttu-id="5e40e-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5e40e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e40e-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5e40e-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e40e-133">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e40e-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e40e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-135">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="5e40e-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5e40e-136">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e40e-136">Indicates when the object was installed.</span></span> <span data-ttu-id="5e40e-137">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5e40e-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5e40e-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5e40e-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e40e-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="5e40e-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e40e-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e40e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e40e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-142">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Component Categories \| [**categoryinfo**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| szDescription")</span><span class="sxs-lookup"><span data-stu-id="5e40e-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="5e40e-143">Die Name-Eigenschaft gibt einen beschreibenden Namen für diese Komponenten Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="5e40e-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="5e40e-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="5e40e-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e40e-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e40e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e40e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e40e-147">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="5e40e-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5e40e-148">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="5e40e-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="5e40e-149">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e40e-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5e40e-150">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e40e-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5e40e-151">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="5e40e-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5e40e-152">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e40e-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5e40e-153">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5e40e-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5e40e-154">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="5e40e-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5e40e-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5e40e-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5e40e-156">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="5e40e-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5e40e-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5e40e-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5e40e-158">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5e40e-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5e40e-159">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5e40e-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e40e-160">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5e40e-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5e40e-161">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5e40e-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5e40e-162">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5e40e-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5e40e-163">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="5e40e-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5e40e-164">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5e40e-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5e40e-165">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="5e40e-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5e40e-166">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="5e40e-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5e40e-167">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="5e40e-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5e40e-168">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="5e40e-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5e40e-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5e40e-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5e40e-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e40e-170">Remarks</span></span>

<span data-ttu-id="5e40e-171">Die **Win32 \_ componentcategory** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5e40e-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e40e-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e40e-172">Requirements</span></span>



| <span data-ttu-id="5e40e-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e40e-173">Requirement</span></span> | <span data-ttu-id="5e40e-174">Wert</span><span class="sxs-lookup"><span data-stu-id="5e40e-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e40e-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e40e-175">Minimum supported client</span></span><br/> | <span data-ttu-id="5e40e-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e40e-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e40e-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e40e-177">Minimum supported server</span></span><br/> | <span data-ttu-id="5e40e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e40e-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e40e-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e40e-179">Namespace</span></span><br/>                | <span data-ttu-id="5e40e-180">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5e40e-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e40e-181">MOF</span><span class="sxs-lookup"><span data-stu-id="5e40e-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e40e-182"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5e40e-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e40e-183">DLL</span><span class="sxs-lookup"><span data-stu-id="5e40e-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e40e-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e40e-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e40e-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e40e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e40e-186">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5e40e-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="5e40e-187">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e40e-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

