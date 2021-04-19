---
description: Die CIM- \_ Dienstklasse stellt ein logisches Element dar, das Informationen zur Darstellung und Verwaltung der von einem Gerät oder einer Software Funktion bereitgestellten Funktionen enthält.
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: CIM_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346636"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="d8a8a-103">CIM_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="d8a8a-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d8a8a-104">Die **CIM- \_ Dienst** Klasse stellt ein logisches Element dar, das Informationen zur Darstellung und Verwaltung der von einem Gerät oder einer Software Funktion bereitgestellten Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="d8a8a-105">Bei einem Dienst handelt es sich um ein allgemeines Objekt, um die Implementierung von Funktionen zu konfigurieren und zu verwalten. Es handelt sich nicht um die eigentliche Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8a8a-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d8a8a-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d8a8a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d8a8a-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d8a8a-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a8a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8a8a-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="d8a8a-111">Member</span><span class="sxs-lookup"><span data-stu-id="d8a8a-111">Members</span></span>

<span data-ttu-id="d8a8a-112">Die **CIM- \_ Dienst** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8a8a-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="d8a8a-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8a8a-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="d8a8a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8a8a-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d8a8a-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8a8a-115">Methods</span></span>

<span data-ttu-id="d8a8a-116">Die **CIM- \_ Dienst** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="d8a8a-117">Methode</span><span class="sxs-lookup"><span data-stu-id="d8a8a-117">Method</span></span>                                                           | <span data-ttu-id="d8a8a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8a8a-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8a8a-119">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="d8a8a-120">Versucht, den Dienst in seinen Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="d8a8a-121">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="d8a8a-122">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="d8a8a-123">Klassenmethode, die den Dienst in den Status "beendet" versetzt.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="d8a8a-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d8a8a-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8a8a-125">Properties</span></span>

<span data-ttu-id="d8a8a-126">Die **CIM- \_ Dienst** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8a8a-127">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-131">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-131">A short textual description of the object.</span></span>

<span data-ttu-id="d8a8a-132">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-133">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-136">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-137">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d8a8a-138">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-142">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-143">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-143">A textual description of the object.</span></span>

<span data-ttu-id="d8a8a-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-149">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-149">Indicates when the object was installed.</span></span> <span data-ttu-id="d8a8a-150">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d8a8a-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-155">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8a8a-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-156">Die Name-Eigenschaft identifiziert den Dienst eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="d8a8a-157">Diese Funktionalität wird in der Description-Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-158">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-159">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d8a8a-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-161">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-162">**True** gibt an, dass der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-163">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-166">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-167">Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="d8a8a-168">**Automatisch** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="d8a8a-169">**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8a8a-170">**Status**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-173">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-174">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="d8a8a-175">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d8a8a-176">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d8a8a-177">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="d8a8a-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d8a8a-178">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d8a8a-179">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d8a8a-180">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d8a8a-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d8a8a-182">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="d8a8a-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d8a8a-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d8a8a-184">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d8a8a-185">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8a8a-186">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d8a8a-187">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d8a8a-188">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d8a8a-189">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d8a8a-190">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d8a8a-191">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d8a8a-192">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d8a8a-193">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d8a8a-194">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8a8a-195">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-198">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-199">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d8a8a-200">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a8a-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8a8a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8a8a-203">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="d8a8a-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d8a8a-204">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8a8a-205">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8a8a-205">Remarks</span></span>

<span data-ttu-id="d8a8a-206">Die **CIM- \_ Dienst** Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d8a8a-207">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-207">WMI does not implement this class.</span></span> <span data-ttu-id="d8a8a-208">Informationen zu WMI-Klassen, die vom **CIM- \_ Dienst** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d8a8a-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d8a8a-209">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d8a8a-210">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a8a-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8a8a-211">Requirements</span></span>



| <span data-ttu-id="d8a8a-212">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8a8a-212">Requirement</span></span> | <span data-ttu-id="d8a8a-213">Wert</span><span class="sxs-lookup"><span data-stu-id="d8a8a-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a8a-214">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8a8a-214">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a8a-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8a8a-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8a8a-216">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8a8a-216">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a8a-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8a8a-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8a8a-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8a8a-218">Namespace</span></span><br/>                | <span data-ttu-id="d8a8a-219">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d8a8a-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8a8a-220">MOF</span><span class="sxs-lookup"><span data-stu-id="d8a8a-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8a8a-221"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d8a8a-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8a8a-222">DLL</span><span class="sxs-lookup"><span data-stu-id="d8a8a-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8a8a-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8a8a-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a8a-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8a8a-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a8a-225">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d8a8a-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

