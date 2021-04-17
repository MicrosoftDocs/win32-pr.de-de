---
description: Die CIM \_ serviceaccesspoint-Klasse stellt die Möglichkeit dar, einen Dienst zu verwenden oder aufzurufen. Zugriffspunkte stellen Dienste dar, die von anderen Entitäten verwendet werden können.
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: CIM_ServiceAccessPoint-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523483"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="58ede-104">CIM_ServiceAccessPoint-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="58ede-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="58ede-105">Die **CIM \_ serviceaccesspoint** -Klasse stellt die Möglichkeit dar, einen Dienst zu verwenden oder aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="58ede-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="58ede-106">Zugriffspunkte stellen Dienste dar, die von anderen Entitäten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="58ede-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58ede-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="58ede-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58ede-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58ede-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58ede-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="58ede-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="58ede-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58ede-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ede-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="58ede-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="58ede-112">Member</span><span class="sxs-lookup"><span data-stu-id="58ede-112">Members</span></span>

<span data-ttu-id="58ede-113">Die **CIM \_ serviceaccesspoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58ede-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="58ede-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58ede-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58ede-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58ede-115">Properties</span></span>

<span data-ttu-id="58ede-116">Die **CIM \_ serviceaccesspoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58ede-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58ede-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="58ede-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="58ede-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="58ede-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="58ede-121">A short textual description of the object.</span></span>

<span data-ttu-id="58ede-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58ede-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58ede-123">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="58ede-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-126">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58ede-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58ede-127">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58ede-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="58ede-128">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="58ede-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="58ede-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58ede-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-132">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="58ede-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="58ede-133">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="58ede-133">A textual description of the object.</span></span>

<span data-ttu-id="58ede-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58ede-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58ede-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="58ede-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-136">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="58ede-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="58ede-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="58ede-139">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="58ede-139">Indicates when the object was installed.</span></span> <span data-ttu-id="58ede-140">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="58ede-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="58ede-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58ede-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58ede-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="58ede-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-145">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58ede-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58ede-146">Identifiziert den Dienst Zugriffspunkt eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="58ede-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="58ede-147">Diese Funktionalität wird in der Description-Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58ede-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="58ede-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="58ede-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="58ede-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="58ede-152">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="58ede-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="58ede-153">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="58ede-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="58ede-154">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="58ede-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="58ede-155">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="58ede-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="58ede-156">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="58ede-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="58ede-157">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="58ede-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="58ede-158">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="58ede-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="58ede-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58ede-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="58ede-160">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="58ede-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="58ede-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="58ede-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="58ede-162">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="58ede-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="58ede-163">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="58ede-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58ede-164">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="58ede-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="58ede-165">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="58ede-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="58ede-166">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="58ede-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="58ede-167">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="58ede-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="58ede-168">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="58ede-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="58ede-169">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="58ede-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="58ede-170">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="58ede-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="58ede-171">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="58ede-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="58ede-172">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="58ede-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58ede-173">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="58ede-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-176">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58ede-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58ede-177">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="58ede-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="58ede-178">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="58ede-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58ede-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-181">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58ede-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58ede-182">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="58ede-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="58ede-183">**Type**</span><span class="sxs-lookup"><span data-stu-id="58ede-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58ede-184">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58ede-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58ede-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58ede-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58ede-186">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="58ede-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="58ede-187">Typ von SAP, z. b. angefügt oder umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58ede-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="58ede-188">**Schreiben** (1)</span><span class="sxs-lookup"><span data-stu-id="58ede-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="58ede-189">**Lesen** (2)</span><span class="sxs-lookup"><span data-stu-id="58ede-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="58ede-190">**Umgeleitet** (4)</span><span class="sxs-lookup"><span data-stu-id="58ede-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="58ede-191">**Net \_ Angefügt** (8)</span><span class="sxs-lookup"><span data-stu-id="58ede-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58ede-192">**unbekannt** (16)</span><span class="sxs-lookup"><span data-stu-id="58ede-192">**unknown** (16)</span></span>


<span data-ttu-id="58ede-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="58ede-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="58ede-194">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58ede-194">Remarks</span></span>

<span data-ttu-id="58ede-195">Die **CIM- \_ serviceaccesspoint** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58ede-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="58ede-196">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="58ede-196">WMI does not implement this class.</span></span> <span data-ttu-id="58ede-197">Informationen zu WMI-Klassen, die von **CIM \_ serviceaccesspoint** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="58ede-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="58ede-198">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58ede-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58ede-199">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="58ede-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ede-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58ede-200">Requirements</span></span>



| <span data-ttu-id="58ede-201">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58ede-201">Requirement</span></span> | <span data-ttu-id="58ede-202">Wert</span><span class="sxs-lookup"><span data-stu-id="58ede-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ede-203">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58ede-203">Minimum supported client</span></span><br/> | <span data-ttu-id="58ede-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58ede-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58ede-205">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58ede-205">Minimum supported server</span></span><br/> | <span data-ttu-id="58ede-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58ede-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58ede-207">Namespace</span><span class="sxs-lookup"><span data-stu-id="58ede-207">Namespace</span></span><br/>                | <span data-ttu-id="58ede-208">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58ede-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58ede-209">MOF</span><span class="sxs-lookup"><span data-stu-id="58ede-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58ede-210"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58ede-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58ede-211">DLL</span><span class="sxs-lookup"><span data-stu-id="58ede-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58ede-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ede-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ede-213">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58ede-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ede-214">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="58ede-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

