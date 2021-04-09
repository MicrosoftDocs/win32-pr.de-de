---
description: Die CIM \_ unitarycomputersystem-Klasse stellt einen Desktop-, Mobil-, Netzwerk Computer-, Server-oder anderen Typ eines Computer Systems mit einem einzelnen Knoten dar.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: CIM_UnitaryComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958242"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="46e7a-103">CIM \_ unitarycomputersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="46e7a-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="46e7a-104">Die **CIM \_ unitarycomputersystem** -Klasse stellt einen Desktop-, Mobil-, Netzwerk Computer-, Server-oder anderen Typ eines Computer Systems mit einem einzelnen Knoten dar.</span><span class="sxs-lookup"><span data-stu-id="46e7a-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46e7a-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="46e7a-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="46e7a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="46e7a-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46e7a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="46e7a-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="46e7a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e7a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e7a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="46e7a-110">Member</span><span class="sxs-lookup"><span data-stu-id="46e7a-110">Members</span></span>

<span data-ttu-id="46e7a-111">Die **CIM \_ unitarycomputersystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="46e7a-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="46e7a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="46e7a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="46e7a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46e7a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="46e7a-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="46e7a-114">Methods</span></span>

<span data-ttu-id="46e7a-115">Die **CIM \_ unitarycomputersystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="46e7a-116">Methode</span><span class="sxs-lookup"><span data-stu-id="46e7a-116">Method</span></span>                                                                           | <span data-ttu-id="46e7a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46e7a-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46e7a-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="46e7a-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="46e7a-119">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46e7a-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="46e7a-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="46e7a-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="46e7a-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46e7a-121">Properties</span></span>

<span data-ttu-id="46e7a-122">Die **CIM \_ unitarycomputersystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46e7a-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46e7a-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="46e7a-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-126">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="46e7a-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-127">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e7a-127">Short textual description of the object.</span></span>

<span data-ttu-id="46e7a-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-129">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="46e7a-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-132">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46e7a-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-133">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46e7a-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="46e7a-134">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="46e7a-135">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46e7a-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-139">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="46e7a-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-140">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e7a-140">Textual description of the object.</span></span>

<span data-ttu-id="46e7a-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-142">**Initizuadinfo**</span><span class="sxs-lookup"><span data-stu-id="46e7a-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-143">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="46e7a-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-145">Daten, die erforderlich sind, um das anfängliche Lade Gerät (seinen Schlüssel) oder den Start Dienst zu ermitteln, um das Betriebssystem zu starten.</span><span class="sxs-lookup"><span data-stu-id="46e7a-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="46e7a-146">Außerdem können die Lade Parameter (d. h. ein Pfadname und Parameter) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46e7a-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-148">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="46e7a-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-150">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="46e7a-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-151">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e7a-151">Date and time the object was installed.</span></span> <span data-ttu-id="46e7a-152">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="46e7a-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="46e7a-153">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-154">**Lastloadinfo**</span><span class="sxs-lookup"><span data-stu-id="46e7a-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-157">Daten, die entweder das anfängliche Lade Gerät (seinen Schlüssel) oder den Start Dienst identifizieren, der die letzte Last des Betriebssystems angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="46e7a-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="46e7a-158">Außerdem können die Lade Parameter (d. h. ein Pfadname und Parameter) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-159">**Name**</span><span class="sxs-lookup"><span data-stu-id="46e7a-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-162">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46e7a-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-163">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="46e7a-163">Label by which the object is known.</span></span> <span data-ttu-id="46e7a-164">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="46e7a-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-166">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="46e7a-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-169">Das [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt und seine Ableitungen sind Objekte der obersten Ebene von CIM, die den Bereich für zahlreiche Komponenten bereitstellen und eindeutige [**CIM- \_ System**](cim-system.md) Schlüssel erfordern.</span><span class="sxs-lookup"><span data-stu-id="46e7a-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="46e7a-170">Es wird eine Heuristik definiert, um den Namen des **CIM- \_ Computer Systems** zu erstellen, bei dem versucht wird, unabhängig vom Discovery-Protokoll immer denselben Systemnamen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="46e7a-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="46e7a-171">Dies verhindert Inventur-und Verwaltungsprobleme, bei denen das gleiche Asset oder die gleiche Entität mehrmals erkannt wird, aber nicht in ein einzelnes Objekt aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="46e7a-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="46e7a-172">Diese Eigenschaft gibt an, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="46e7a-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="46e7a-173">Die Heuristik wird in der allgemeinen Modell Spezifikation von CIM V2 beschrieben und geht davon aus, dass die dokumentierten Regeln durchlaufen werden, um einen Namen zu ermitteln und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="46e7a-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="46e7a-174">In der Liste **NameFormat** -Werte ist die Rangfolge für die Zuweisung des System namens mit mehreren Regeln definiert, die demselben Wert zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="46e7a-175">Beachten Sie, dass der Name des **CIM- \_ Computer Systems** , der mit der Heuristik berechnet wird, der Schlüsselwert des Systems ist.</span><span class="sxs-lookup"><span data-stu-id="46e7a-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="46e7a-176">Andere Namen können zugewiesen und für das CIM- **\_ Computersystem** verwendet werden, das für das Unternehmen besser geeignet ist. dabei werden Aliase verwendet.</span><span class="sxs-lookup"><span data-stu-id="46e7a-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="46e7a-177">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="46e7a-178">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="46e7a-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="46e7a-179">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="46e7a-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="46e7a-180">**Dial** ("Dial")</span><span class="sxs-lookup"><span data-stu-id="46e7a-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="46e7a-181">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="46e7a-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="46e7a-182">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="46e7a-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="46e7a-183">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="46e7a-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="46e7a-184">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="46e7a-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="46e7a-185">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="46e7a-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="46e7a-186">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="46e7a-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="46e7a-187">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="46e7a-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="46e7a-188">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="46e7a-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="46e7a-189">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="46e7a-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="46e7a-190">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="46e7a-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="46e7a-191">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="46e7a-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46e7a-192">**Sonstige** ("Sonstige")</span><span class="sxs-lookup"><span data-stu-id="46e7a-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46e7a-193">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="46e7a-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-194">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="46e7a-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-196">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Energiesteuerung \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="46e7a-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-197">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="46e7a-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="46e7a-198">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46e7a-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="46e7a-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="46e7a-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="46e7a-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46e7a-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="46e7a-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46e7a-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="46e7a-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-203">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46e7a-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="46e7a-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="46e7a-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-205">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="46e7a-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="46e7a-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="46e7a-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-207">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="46e7a-208">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="46e7a-209">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="46e7a-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="46e7a-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="46e7a-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-211">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="46e7a-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="46e7a-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="46e7a-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-213">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="46e7a-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e7a-214">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="46e7a-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-215">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="46e7a-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-217">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="46e7a-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="46e7a-218">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="46e7a-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="46e7a-219">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="46e7a-220">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="46e7a-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-221">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="46e7a-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-222">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46e7a-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-224">Aktueller Energiezustand des Computer Systems und des zugehörigen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="46e7a-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46e7a-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="46e7a-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-226">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="46e7a-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="46e7a-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Vollstrom** (1)</span><span class="sxs-lookup"><span data-stu-id="46e7a-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-228">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="46e7a-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="46e7a-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (2)</span><span class="sxs-lookup"><span data-stu-id="46e7a-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-230">Das System befindet sich in einem Energiespar Zustand und funktioniert weiterhin, kann jedoch die Leistung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="46e7a-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="46e7a-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-232">Das System funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="46e7a-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="46e7a-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (4)</span><span class="sxs-lookup"><span data-stu-id="46e7a-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-234">Es ist bekannt, dass sich das System in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="46e7a-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (5)</span><span class="sxs-lookup"><span data-stu-id="46e7a-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-236">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="46e7a-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="46e7a-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (6)</span><span class="sxs-lookup"><span data-stu-id="46e7a-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-238">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="46e7a-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="46e7a-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (7)</span><span class="sxs-lookup"><span data-stu-id="46e7a-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-240">Das System befindet sich in einem Warnungs Status und auch in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="46e7a-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="46e7a-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Energiespar Speicher-** Ruhezustand (8)</span><span class="sxs-lookup"><span data-stu-id="46e7a-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-242">Energie sparen Sie den Ruhezustand.</span><span class="sxs-lookup"><span data-stu-id="46e7a-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="46e7a-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save-Soft Off** (9)</span><span class="sxs-lookup"><span data-stu-id="46e7a-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="46e7a-244">Power Save Soft aus.</span><span class="sxs-lookup"><span data-stu-id="46e7a-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e7a-245">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="46e7a-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-248">Eine Zeichenfolge, die Informationen zum Erreichen des primären System Besitzers (z. b. Telefonnummer, e-Mail-Adresse usw.) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="46e7a-249">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-250">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="46e7a-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-253">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="46e7a-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-254">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="46e7a-254">Name of the primary system owner.</span></span>

<span data-ttu-id="46e7a-255">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-256">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="46e7a-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46e7a-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-259">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| System Hardware Security \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="46e7a-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-260">Wenn diese Option aktiviert ist, kann das einheitliche Computersystem mit Hardware zurückgesetzt werden (z. b. mit den Schaltflächen Strom und zurücksetzen).</span><span class="sxs-lookup"><span data-stu-id="46e7a-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="46e7a-261">Wenn diese Option deaktiviert ist, ist die Hardware Zurücksetzung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="46e7a-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46e7a-262">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="46e7a-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46e7a-263">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="46e7a-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46e7a-264">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="46e7a-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46e7a-265">**Aktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="46e7a-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="46e7a-266">**Nicht implementiert** (5)</span><span class="sxs-lookup"><span data-stu-id="46e7a-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46e7a-267">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="46e7a-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-268">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="46e7a-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-269">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="46e7a-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-270">Rollen, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="46e7a-271">Unterklassen des Systems können diese Eigenschaft überschreiben, um explizite Rollen Werte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="46e7a-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="46e7a-272">Alternativ kann eine Arbeitsgruppe die Heuristik, Konventionen und Richtlinien zum Angeben von Rollen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="46e7a-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="46e7a-273">Beispielsweise kann für eine Instanz eines Netzwerksystems diese Eigenschaft die Zeichenfolge "Switch" oder "Bridge" enthalten.</span><span class="sxs-lookup"><span data-stu-id="46e7a-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="46e7a-274">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-275">**Status**</span><span class="sxs-lookup"><span data-stu-id="46e7a-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e7a-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e7a-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e7a-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e7a-278">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="46e7a-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="46e7a-279">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e7a-279">Current status of the object.</span></span> <span data-ttu-id="46e7a-280">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e7a-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="46e7a-281">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="46e7a-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="46e7a-282">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="46e7a-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="46e7a-283">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="46e7a-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="46e7a-284">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="46e7a-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46e7a-285">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="46e7a-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="46e7a-286">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="46e7a-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="46e7a-287">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="46e7a-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="46e7a-288">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="46e7a-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="46e7a-289">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="46e7a-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="46e7a-290">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="46e7a-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="46e7a-291">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="46e7a-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="46e7a-292">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="46e7a-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="46e7a-293">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="46e7a-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="46e7a-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46e7a-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="46e7a-295">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46e7a-295">Remarks</span></span>

<span data-ttu-id="46e7a-296">Die **CIM \_ unitarycomputersystem** -Klasse wird von [**CIM \_ Computersystem**](cim-computersystem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="46e7a-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="46e7a-297">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="46e7a-297">WMI does not implement this class.</span></span> <span data-ttu-id="46e7a-298">Informationen zu WMI-Klassen, die von **CIM \_ unitarycomputersystem** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="46e7a-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="46e7a-299">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="46e7a-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="46e7a-300">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="46e7a-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e7a-301">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46e7a-301">Requirements</span></span>



| <span data-ttu-id="46e7a-302">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46e7a-302">Requirement</span></span> | <span data-ttu-id="46e7a-303">Wert</span><span class="sxs-lookup"><span data-stu-id="46e7a-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e7a-304">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46e7a-304">Minimum supported client</span></span><br/> | <span data-ttu-id="46e7a-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46e7a-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46e7a-306">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46e7a-306">Minimum supported server</span></span><br/> | <span data-ttu-id="46e7a-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46e7a-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46e7a-308">Namespace</span><span class="sxs-lookup"><span data-stu-id="46e7a-308">Namespace</span></span><br/>                | <span data-ttu-id="46e7a-309">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46e7a-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46e7a-310">MOF</span><span class="sxs-lookup"><span data-stu-id="46e7a-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46e7a-311"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46e7a-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46e7a-312">DLL</span><span class="sxs-lookup"><span data-stu-id="46e7a-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e7a-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46e7a-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e7a-314">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46e7a-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e7a-315">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="46e7a-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

