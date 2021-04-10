---
description: Die CIM \_ clusteringsap-Klasse stellt die Zugriffspunkte eines Clustering-Dienstanbieter dar.
ms.assetid: 7a95f4b0-b9fc-4dba-ad2d-1b6db1539a57
ms.tgt_platform: multiple
title: CIM_ClusteringSAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringSAP
- CIM_ClusteringSAP.Caption
- CIM_ClusteringSAP.Description
- CIM_ClusteringSAP.InstallDate
- CIM_ClusteringSAP.Status
- CIM_ClusteringSAP.CreationClassName
- CIM_ClusteringSAP.Name
- CIM_ClusteringSAP.SystemCreationClassName
- CIM_ClusteringSAP.SystemName
- CIM_ClusteringSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc2d0296201e06382563cc3a0c34fec4d668cd58
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214210"
---
# <a name="cim_clusteringsap-class"></a><span data-ttu-id="8d03d-103">CIM \_ clusteringsap-Klasse</span><span class="sxs-lookup"><span data-stu-id="8d03d-103">CIM\_ClusteringSAP class</span></span>

<span data-ttu-id="8d03d-104">Die **CIM \_ clusteringsap** -Klasse stellt die Zugriffspunkte eines Clustering-Dienstanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="8d03d-104">The **CIM\_ClusteringSAP** class represents the access points of a clustering service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d03d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8d03d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d03d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d03d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d03d-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8d03d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8d03d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8d03d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d03d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d03d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2bb2b772-ffed-4aa6-b1b3-3d0cb74fc613}"), AMENDMENT]
class CIM_ClusteringSAP : CIM_ServiceAccessPoint
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

## <a name="members"></a><span data-ttu-id="8d03d-110">Member</span><span class="sxs-lookup"><span data-stu-id="8d03d-110">Members</span></span>

<span data-ttu-id="8d03d-111">Die **CIM \_ clusteringsap** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8d03d-111">The **CIM\_ClusteringSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="8d03d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d03d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d03d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d03d-113">Properties</span></span>

<span data-ttu-id="8d03d-114">Die **CIM \_ clusteringsap** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d03d-114">The **CIM\_ClusteringSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d03d-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8d03d-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8d03d-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d03d-119">A short textual description of the object.</span></span>

<span data-ttu-id="8d03d-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-121">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="8d03d-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-124">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8d03d-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-125">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d03d-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8d03d-126">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8d03d-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8d03d-127">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d03d-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-131">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8d03d-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-132">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d03d-132">A textual description of the object.</span></span>

<span data-ttu-id="8d03d-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8d03d-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d03d-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="8d03d-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-138">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8d03d-138">Indicates when the object was installed.</span></span> <span data-ttu-id="8d03d-139">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d03d-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8d03d-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d03d-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-144">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8d03d-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-145">Identifiziert den Dienst Zugriffspunkt eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="8d03d-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="8d03d-146">Diese Funktionalität wird in der Description-Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d03d-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="8d03d-147">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="8d03d-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8d03d-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-152">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="8d03d-153">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d03d-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8d03d-154">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d03d-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8d03d-155">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="8d03d-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8d03d-156">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d03d-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8d03d-157">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="8d03d-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8d03d-158">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8d03d-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8d03d-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8d03d-160">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8d03d-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8d03d-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8d03d-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8d03d-162">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8d03d-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8d03d-163">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8d03d-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8d03d-164">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8d03d-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8d03d-165">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8d03d-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8d03d-166">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8d03d-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8d03d-167">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="8d03d-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8d03d-168">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8d03d-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8d03d-169">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="8d03d-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8d03d-170">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="8d03d-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8d03d-171">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="8d03d-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8d03d-172">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="8d03d-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d03d-173">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="8d03d-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-176">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8d03d-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-177">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="8d03d-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="8d03d-178">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-179">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="8d03d-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d03d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-182">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8d03d-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-183">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="8d03d-183">The scoping system's name.</span></span>

<span data-ttu-id="8d03d-184">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d03d-185">**Type**</span><span class="sxs-lookup"><span data-stu-id="8d03d-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d03d-186">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d03d-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d03d-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d03d-188">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8d03d-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8d03d-189">Typ von SAP, z. b. angefügt oder umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8d03d-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="8d03d-190">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d03d-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="8d03d-191">**Schreiben** (1)</span><span class="sxs-lookup"><span data-stu-id="8d03d-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="8d03d-192">**Lesen** (2)</span><span class="sxs-lookup"><span data-stu-id="8d03d-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="8d03d-193">**Umgeleitet** (4)</span><span class="sxs-lookup"><span data-stu-id="8d03d-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="8d03d-194">**Net \_ Angefügt** (8)</span><span class="sxs-lookup"><span data-stu-id="8d03d-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8d03d-195">**unbekannt** (16)</span><span class="sxs-lookup"><span data-stu-id="8d03d-195">**unknown** (16)</span></span>


<span data-ttu-id="8d03d-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8d03d-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8d03d-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d03d-197">Remarks</span></span>

<span data-ttu-id="8d03d-198">Die **CIM \_ clusteringsap** -Klasse wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8d03d-198">The **CIM\_ClusteringSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="8d03d-199">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8d03d-199">WMI does not implement this class.</span></span>

<span data-ttu-id="8d03d-200">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8d03d-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d03d-201">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8d03d-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d03d-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d03d-202">Requirements</span></span>



| <span data-ttu-id="8d03d-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d03d-203">Requirement</span></span> | <span data-ttu-id="8d03d-204">Wert</span><span class="sxs-lookup"><span data-stu-id="8d03d-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d03d-205">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d03d-205">Minimum supported client</span></span><br/> | <span data-ttu-id="8d03d-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d03d-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d03d-207">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d03d-207">Minimum supported server</span></span><br/> | <span data-ttu-id="8d03d-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d03d-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d03d-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d03d-209">Namespace</span></span><br/>                | <span data-ttu-id="8d03d-210">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8d03d-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d03d-211">MOF</span><span class="sxs-lookup"><span data-stu-id="8d03d-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d03d-212"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8d03d-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d03d-213">DLL</span><span class="sxs-lookup"><span data-stu-id="8d03d-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d03d-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d03d-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d03d-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d03d-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d03d-216">**CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="8d03d-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

