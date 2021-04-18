---
description: Die CIM- \_ Bootservice-Klasse stellt die Funktionalität dar, die von einem Gerät oder einer Software oder von einem Netzwerk bereitgestellt wird, um ein Betriebssystem auf einem einheitlichen Computersystem zu laden.
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: CIM_BootService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338916"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="4e821-103">CIM- \_ Bootservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="4e821-103">CIM\_BootService class</span></span>

<span data-ttu-id="4e821-104">Die **CIM- \_ Bootservice** -Klasse stellt die Funktionalität dar, die von einem Gerät oder einer Software oder von einem Netzwerk bereitgestellt wird, um ein Betriebssystem auf einem einheitlichen Computersystem zu laden.</span><span class="sxs-lookup"><span data-stu-id="4e821-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e821-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4e821-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e821-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e821-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e821-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="4e821-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4e821-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4e821-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e821-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e821-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="4e821-110">Member</span><span class="sxs-lookup"><span data-stu-id="4e821-110">Members</span></span>

<span data-ttu-id="4e821-111">Die **CIM- \_ Bootservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4e821-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="4e821-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4e821-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e821-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e821-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e821-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="4e821-114">Methods</span></span>

<span data-ttu-id="4e821-115">Die **CIM- \_ Bootservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4e821-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="4e821-116">Methode</span><span class="sxs-lookup"><span data-stu-id="4e821-116">Method</span></span>                                                               | <span data-ttu-id="4e821-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e821-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="4e821-118">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="4e821-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="4e821-119">Versetzt den Dienst in den Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="4e821-119">Puts the service in the started state.</span></span> <span data-ttu-id="4e821-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e821-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="4e821-121">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="4e821-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="4e821-122">Versetzt den Dienst in den Status "beendet".</span><span class="sxs-lookup"><span data-stu-id="4e821-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="4e821-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e821-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e821-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e821-124">Properties</span></span>

<span data-ttu-id="4e821-125">Die **CIM- \_ Bootservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e821-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e821-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4e821-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4e821-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-130">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4e821-130">A short textual description of the object.</span></span>

<span data-ttu-id="4e821-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-132">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4e821-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-135">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="4e821-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-136">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e821-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4e821-137">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4e821-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4e821-138">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e821-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-142">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4e821-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-143">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4e821-143">A textual description of the object.</span></span>

<span data-ttu-id="4e821-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e821-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e821-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="4e821-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-149">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4e821-149">Indicates when the object was installed.</span></span> <span data-ttu-id="4e821-150">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4e821-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4e821-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="4e821-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e821-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e821-156">Die Name-Eigenschaft identifiziert den Dienst eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="4e821-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="4e821-157">Diese Funktionalität wird in der **Description** -Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e821-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="4e821-158">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-159">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="4e821-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-160">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4e821-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-162">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="4e821-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-163">**True** gibt an, dass der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4e821-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="4e821-164">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-165">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4e821-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-168">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="4e821-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-169">Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4e821-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="4e821-170">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="4e821-171">**Automatisch** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="4e821-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4e821-172">**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="4e821-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e821-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="4e821-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-176">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4e821-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-177">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="4e821-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="4e821-178">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e821-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4e821-179">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e821-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4e821-180">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="4e821-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4e821-181">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e821-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4e821-182">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="4e821-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4e821-183">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="4e821-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4e821-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4e821-185">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4e821-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4e821-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4e821-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4e821-187">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="4e821-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e821-188">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="4e821-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e821-189">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4e821-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4e821-190">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4e821-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4e821-191">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="4e821-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4e821-192">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="4e821-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4e821-193">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="4e821-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4e821-194">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="4e821-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4e821-195">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="4e821-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4e821-196">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="4e821-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4e821-197">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="4e821-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e821-198">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="4e821-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-201">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="4e821-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-202">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4e821-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="4e821-203">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e821-204">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="4e821-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e821-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e821-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e821-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e821-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e821-207">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="4e821-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e821-208">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="4e821-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="4e821-209">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e821-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e821-210">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e821-210">Remarks</span></span>

<span data-ttu-id="4e821-211">Die **CIM- \_ Bootservice** -Klasse wird vom [**CIM- \_ Dienst**](cim-service.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e821-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="4e821-212">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e821-212">WMI does not implement this class.</span></span>

<span data-ttu-id="4e821-213">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e821-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e821-214">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4e821-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e821-215">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e821-215">Requirements</span></span>



| <span data-ttu-id="4e821-216">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e821-216">Requirement</span></span> | <span data-ttu-id="4e821-217">Wert</span><span class="sxs-lookup"><span data-stu-id="4e821-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e821-218">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e821-218">Minimum supported client</span></span><br/> | <span data-ttu-id="4e821-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e821-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e821-220">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e821-220">Minimum supported server</span></span><br/> | <span data-ttu-id="4e821-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e821-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e821-222">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e821-222">Namespace</span></span><br/>                | <span data-ttu-id="4e821-223">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e821-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e821-224">MOF</span><span class="sxs-lookup"><span data-stu-id="4e821-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e821-225"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4e821-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e821-226">DLL</span><span class="sxs-lookup"><span data-stu-id="4e821-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e821-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e821-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e821-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e821-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e821-229">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="4e821-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

