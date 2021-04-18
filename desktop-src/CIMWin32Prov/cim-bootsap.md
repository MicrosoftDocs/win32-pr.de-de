---
description: Die CIM- \_ bootsap-Klasse stellt die Zugriffspunkte eines Start Dienstanbieter dar.
ms.assetid: eea6d6c5-3930-4e20-b7d3-b6d5722662cd
ms.tgt_platform: multiple
title: CIM_BootSAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootSAP
- CIM_BootSAP.Caption
- CIM_BootSAP.Description
- CIM_BootSAP.InstallDate
- CIM_BootSAP.Status
- CIM_BootSAP.CreationClassName
- CIM_BootSAP.Name
- CIM_BootSAP.SystemCreationClassName
- CIM_BootSAP.SystemName
- CIM_BootSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4868497c2d604457a45273b1c0cc609ae361ad9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344834"
---
# <a name="cim_bootsap-class"></a><span data-ttu-id="c7e24-103">CIM- \_ bootsap-Klasse</span><span class="sxs-lookup"><span data-stu-id="c7e24-103">CIM\_BootSAP class</span></span>

<span data-ttu-id="c7e24-104">Die **CIM- \_ bootsap** -Klasse stellt die Zugriffspunkte eines Start Dienstanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="c7e24-104">The **CIM\_BootSAP** class represents the access points of a boot service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7e24-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c7e24-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c7e24-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c7e24-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c7e24-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c7e24-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c7e24-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c7e24-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e24-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7e24-109">Syntax</span></span>

``` syntax
[UUID("{F6FEF20A-E3D2-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootSAP : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="c7e24-110">Member</span><span class="sxs-lookup"><span data-stu-id="c7e24-110">Members</span></span>

<span data-ttu-id="c7e24-111">Die **CIM- \_ bootsap** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c7e24-111">The **CIM\_BootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="c7e24-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7e24-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7e24-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7e24-113">Properties</span></span>

<span data-ttu-id="c7e24-114">Die **CIM- \_ bootsap** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7e24-114">The **CIM\_BootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7e24-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c7e24-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c7e24-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c7e24-119">A short textual description of the object.</span></span>

<span data-ttu-id="c7e24-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-121">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c7e24-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-124">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7e24-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-125">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7e24-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c7e24-126">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c7e24-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c7e24-127">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7e24-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-131">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c7e24-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-132">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c7e24-132">A textual description of the object.</span></span>

<span data-ttu-id="c7e24-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c7e24-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7e24-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c7e24-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-138">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7e24-138">Indicates when the object was installed.</span></span> <span data-ttu-id="c7e24-139">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c7e24-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c7e24-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="c7e24-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-144">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7e24-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-145">Identifiziert den Dienst Zugriffspunkt eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="c7e24-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="c7e24-146">Diese Funktionalität wird in der Description-Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7e24-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="c7e24-147">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="c7e24-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c7e24-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-152">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="c7e24-153">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7e24-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c7e24-154">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7e24-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c7e24-155">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c7e24-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c7e24-156">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7e24-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c7e24-157">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c7e24-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c7e24-158">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c7e24-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c7e24-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c7e24-160">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c7e24-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c7e24-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c7e24-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c7e24-162">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c7e24-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c7e24-163">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c7e24-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7e24-164">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c7e24-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c7e24-165">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c7e24-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c7e24-166">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c7e24-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c7e24-167">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c7e24-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c7e24-168">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c7e24-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c7e24-169">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c7e24-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c7e24-170">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c7e24-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c7e24-171">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c7e24-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c7e24-172">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c7e24-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7e24-173">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c7e24-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-176">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7e24-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-177">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c7e24-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="c7e24-178">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-179">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c7e24-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7e24-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-182">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7e24-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-183">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c7e24-183">The scoping system's name.</span></span>

<span data-ttu-id="c7e24-184">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7e24-185">**Type**</span><span class="sxs-lookup"><span data-stu-id="c7e24-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e24-186">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7e24-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7e24-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e24-188">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c7e24-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7e24-189">Typ von SAP, z. b. angefügt oder umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c7e24-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="c7e24-190">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c7e24-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="c7e24-191">**Schreiben** (1)</span><span class="sxs-lookup"><span data-stu-id="c7e24-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="c7e24-192">**Lesen** (2)</span><span class="sxs-lookup"><span data-stu-id="c7e24-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="c7e24-193">**Umgeleitet** (4)</span><span class="sxs-lookup"><span data-stu-id="c7e24-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="c7e24-194">**Net \_ Angefügt** (8)</span><span class="sxs-lookup"><span data-stu-id="c7e24-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7e24-195">**unbekannt** (16)</span><span class="sxs-lookup"><span data-stu-id="c7e24-195">**unknown** (16)</span></span>


<span data-ttu-id="c7e24-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c7e24-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c7e24-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7e24-197">Remarks</span></span>

<span data-ttu-id="c7e24-198">Die **CIM- \_ bootsap** -Klasse wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c7e24-198">The **CIM\_BootSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="c7e24-199">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c7e24-199">WMI does not implement this class.</span></span>

<span data-ttu-id="c7e24-200">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c7e24-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c7e24-201">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c7e24-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e24-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7e24-202">Requirements</span></span>



| <span data-ttu-id="c7e24-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7e24-203">Requirement</span></span> | <span data-ttu-id="c7e24-204">Wert</span><span class="sxs-lookup"><span data-stu-id="c7e24-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e24-205">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7e24-205">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e24-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7e24-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7e24-207">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7e24-207">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e24-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7e24-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7e24-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7e24-209">Namespace</span></span><br/>                | <span data-ttu-id="c7e24-210">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c7e24-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7e24-211">MOF</span><span class="sxs-lookup"><span data-stu-id="c7e24-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7e24-212"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c7e24-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7e24-213">DLL</span><span class="sxs-lookup"><span data-stu-id="c7e24-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7e24-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7e24-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e24-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7e24-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e24-216">**CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="c7e24-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

