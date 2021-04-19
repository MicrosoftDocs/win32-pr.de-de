---
description: Die CIM \_ applicationsystem-Klasse stellt ein Anwendungs-oder Softwaresystem dar, das eine bestimmte Geschäftsfunktion unterstützt, die als unabhängige Einheit verwaltet werden kann.
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: CIM_ApplicationSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344965"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="0a140-103">CIM- \_ applicationsystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a140-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="0a140-104">Die **CIM \_ applicationsystem** -Klasse stellt ein Anwendungs-oder Softwaresystem dar, das eine bestimmte Geschäftsfunktion unterstützt, die als unabhängige Einheit verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a140-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="0a140-105">Ein solches System kann mithilfe der [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Klasse in seine funktionalen Komponenten zerlegt werden.</span><span class="sxs-lookup"><span data-stu-id="0a140-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="0a140-106">Die Software Features für eine bestimmte Anwendung oder ein bestimmtes Softwaresystem werden mithilfe der [**CIM \_ applicationsystemsoftwarefeature-Zuordnung**](cim-applicationsystemsoftwarefeature.md) gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a140-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a140-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a140-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a140-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0a140-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0a140-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0a140-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0a140-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0a140-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a140-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a140-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
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

## <a name="members"></a><span data-ttu-id="0a140-112">Member</span><span class="sxs-lookup"><span data-stu-id="0a140-112">Members</span></span>

<span data-ttu-id="0a140-113">Die **CIM- \_ applicationsystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0a140-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="0a140-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a140-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a140-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a140-115">Properties</span></span>

<span data-ttu-id="0a140-116">Die **CIM \_ applicationsystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a140-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a140-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0a140-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0a140-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0a140-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0a140-121">A short textual description of the object.</span></span>

<span data-ttu-id="0a140-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-123">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0a140-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-126">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0a140-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0a140-127">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a140-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0a140-128">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0a140-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0a140-129">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a140-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-133">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0a140-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0a140-134">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0a140-134">A textual description of the object.</span></span>

<span data-ttu-id="0a140-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0a140-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-137">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0a140-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="0a140-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0a140-140">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0a140-140">Indicates when the object was installed.</span></span> <span data-ttu-id="0a140-141">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0a140-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0a140-142">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a140-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0a140-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0a140-147">Definiert die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0a140-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="0a140-148">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="0a140-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a140-152">Gibt an, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0a140-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="0a140-153">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-154">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="0a140-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a140-157">Wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer oder e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="0a140-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="0a140-158">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-159">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="0a140-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0a140-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0a140-163">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="0a140-163">Name of the primary system owner.</span></span>

<span data-ttu-id="0a140-164">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-165">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="0a140-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-166">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0a140-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0a140-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0a140-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0a140-168">Rollen, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="0a140-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="0a140-169">Unterklassen des Systems können diese Eigenschaft überschreiben, um explizite Rollen Werte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0a140-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="0a140-170">Alternativ kann eine Arbeitsgruppe die Heuristik, Konventionen und Richtlinien zum Angeben von Rollen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0a140-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="0a140-171">Beispielsweise kann für eine Instanz eines Netzwerksystems diese Eigenschaft die Zeichenfolge "Switch" oder "Bridge" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a140-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="0a140-172">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a140-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="0a140-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a140-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a140-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a140-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a140-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a140-176">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0a140-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0a140-177">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="0a140-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="0a140-178">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a140-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0a140-179">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a140-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0a140-180">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="0a140-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0a140-181">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a140-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0a140-182">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0a140-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0a140-183">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0a140-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0a140-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0a140-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0a140-185">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="0a140-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0a140-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0a140-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0a140-187">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0a140-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0a140-188">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0a140-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a140-189">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0a140-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0a140-190">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0a140-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0a140-191">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0a140-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0a140-192">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="0a140-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0a140-193">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0a140-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0a140-194">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="0a140-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0a140-195">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="0a140-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0a140-196">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="0a140-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0a140-197">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="0a140-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="0a140-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a140-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0a140-199">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a140-199">Remarks</span></span>

<span data-ttu-id="0a140-200">Die **CIM- \_ applicationsystem** -Klasse wird vom [**CIM- \_ System**](cim-system.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0a140-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="0a140-201">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0a140-201">WMI does not implement this class.</span></span>

<span data-ttu-id="0a140-202">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0a140-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a140-203">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0a140-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a140-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a140-204">Requirements</span></span>



| <span data-ttu-id="0a140-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a140-205">Requirement</span></span> | <span data-ttu-id="0a140-206">Wert</span><span class="sxs-lookup"><span data-stu-id="0a140-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a140-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a140-207">Minimum supported client</span></span><br/> | <span data-ttu-id="0a140-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a140-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a140-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a140-209">Minimum supported server</span></span><br/> | <span data-ttu-id="0a140-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a140-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a140-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a140-211">Namespace</span></span><br/>                | <span data-ttu-id="0a140-212">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0a140-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a140-213">MOF</span><span class="sxs-lookup"><span data-stu-id="0a140-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a140-214"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0a140-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a140-215">DLL</span><span class="sxs-lookup"><span data-stu-id="0a140-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a140-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a140-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a140-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a140-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a140-218">**CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="0a140-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

