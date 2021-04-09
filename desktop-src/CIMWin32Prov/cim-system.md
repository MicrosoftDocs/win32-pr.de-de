---
description: Die CIM- \_ System Klasse aggregiert einen Aufzähl baren Satz verwalteter System Elemente.
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: CIM_System-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958443"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="3951f-103">CIM_System-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="3951f-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3951f-104">Die **CIM- \_ System** Klasse aggregiert einen Aufzähl baren Satz verwalteter System Elemente.</span><span class="sxs-lookup"><span data-stu-id="3951f-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="3951f-105">Die Aggregation funktioniert als Ganzes funktionstüchtig.</span><span class="sxs-lookup"><span data-stu-id="3951f-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="3951f-106">Innerhalb einer bestimmten Unterklasse des Systems gibt es eine klar definierte Liste der verwalteten System Element Klassen, deren Instanzen aggregiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3951f-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="3951f-107">Das **CIM- \_ System** Objekt und seine Ableitungen sind Objekte der obersten Ebene von CIM.</span><span class="sxs-lookup"><span data-stu-id="3951f-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="3951f-108">Sie stellen den Bereich für zahlreiche Komponenten bereit und sind für eindeutige Systemschlüssel erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3951f-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3951f-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3951f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3951f-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3951f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3951f-111">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3951f-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3951f-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3951f-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3951f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3951f-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="3951f-114">Member</span><span class="sxs-lookup"><span data-stu-id="3951f-114">Members</span></span>

<span data-ttu-id="3951f-115">Die **CIM- \_ System** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3951f-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="3951f-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3951f-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3951f-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3951f-117">Properties</span></span>

<span data-ttu-id="3951f-118">Die **CIM- \_ System** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3951f-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3951f-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3951f-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3951f-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3951f-123">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3951f-123">A short textual description of the object.</span></span>

<span data-ttu-id="3951f-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3951f-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3951f-125">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="3951f-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-128">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3951f-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3951f-129">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3951f-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3951f-130">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3951f-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="3951f-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3951f-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-134">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3951f-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3951f-135">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3951f-135">A textual description of the object.</span></span>

<span data-ttu-id="3951f-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3951f-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3951f-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3951f-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3951f-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="3951f-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3951f-141">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3951f-141">Indicates when the object was installed.</span></span> <span data-ttu-id="3951f-142">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3951f-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3951f-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3951f-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3951f-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="3951f-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-147">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3951f-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3951f-148">Definiert die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3951f-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="3951f-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="3951f-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3951f-152">Gibt an, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3951f-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="3951f-153">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="3951f-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3951f-156">Wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer oder e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="3951f-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="3951f-157">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="3951f-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-160">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3951f-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3951f-161">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="3951f-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="3951f-162">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="3951f-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-163">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3951f-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3951f-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3951f-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3951f-165">Rollen, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="3951f-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="3951f-166">Unterklassen des Systems können diese Eigenschaft überschreiben, um explizite Rollen Werte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3951f-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="3951f-167">Alternativ kann eine Arbeitsgruppe die Heuristik, Konventionen und Richtlinien zum Angeben von Rollen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3951f-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="3951f-168">Beispielsweise kann für eine Instanz eines Netzwerksystems diese Eigenschaft die Zeichenfolge "Switch" oder "Bridge" enthalten.</span><span class="sxs-lookup"><span data-stu-id="3951f-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="3951f-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="3951f-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3951f-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3951f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3951f-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3951f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3951f-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3951f-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3951f-173">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="3951f-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="3951f-174">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3951f-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3951f-175">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="3951f-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3951f-176">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="3951f-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3951f-177">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="3951f-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3951f-178">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="3951f-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3951f-179">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="3951f-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3951f-180">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3951f-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3951f-181">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3951f-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3951f-182">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3951f-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3951f-183">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3951f-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3951f-184">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3951f-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3951f-185">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3951f-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3951f-186">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3951f-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3951f-187">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3951f-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3951f-188">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="3951f-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3951f-189">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3951f-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3951f-190">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="3951f-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3951f-191">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="3951f-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3951f-192">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="3951f-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3951f-193">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="3951f-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="3951f-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3951f-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3951f-195">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3951f-195">Remarks</span></span>

<span data-ttu-id="3951f-196">Die **CIM- \_ System** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3951f-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="3951f-197">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3951f-197">WMI does not implement this class.</span></span> <span data-ttu-id="3951f-198">Informationen zu WMI-Klassen, die vom **CIM- \_ System** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="3951f-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3951f-199">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3951f-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3951f-200">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3951f-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3951f-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3951f-201">Requirements</span></span>



| <span data-ttu-id="3951f-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3951f-202">Requirement</span></span> | <span data-ttu-id="3951f-203">Wert</span><span class="sxs-lookup"><span data-stu-id="3951f-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3951f-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3951f-204">Minimum supported client</span></span><br/> | <span data-ttu-id="3951f-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3951f-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3951f-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3951f-206">Minimum supported server</span></span><br/> | <span data-ttu-id="3951f-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3951f-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3951f-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="3951f-208">Namespace</span></span><br/>                | <span data-ttu-id="3951f-209">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3951f-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3951f-210">MOF</span><span class="sxs-lookup"><span data-stu-id="3951f-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3951f-211"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3951f-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3951f-212">DLL</span><span class="sxs-lookup"><span data-stu-id="3951f-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3951f-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3951f-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3951f-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3951f-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3951f-215">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="3951f-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

