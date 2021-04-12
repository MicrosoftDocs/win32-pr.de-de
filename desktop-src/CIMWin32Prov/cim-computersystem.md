---
description: Eine CIM \_ Computersystem-Klasse stellt eine spezielle Auflistung von CIM \_ ManagedSystemElement-Instanzen dar.
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: CIM_ComputerSystem-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483534"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="129b6-103">CIM_ComputerSystem-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="129b6-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="129b6-104">Eine **CIM \_ Computersystem** -Klasse stellt eine spezielle Auflistung von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Instanzen dar.</span><span class="sxs-lookup"><span data-stu-id="129b6-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="129b6-105">Diese Sammlung bietet Computerfunktionen und dient als Aggregations Punkt zum Zuordnen eines oder mehrerer der folgenden Elemente: Dateisystem, Betriebssystem, Prozessor und Arbeitsspeicher (flüchtiger und nicht flüchtiger Speicher).</span><span class="sxs-lookup"><span data-stu-id="129b6-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="129b6-106">Diese Klasse wird vom [**CIM- \_ System**](cim-system.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="129b6-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="129b6-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="129b6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="129b6-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="129b6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="129b6-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="129b6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="129b6-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="129b6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="129b6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="129b6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="129b6-112">Member</span><span class="sxs-lookup"><span data-stu-id="129b6-112">Members</span></span>

<span data-ttu-id="129b6-113">Die **CIM \_ Computersystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="129b6-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="129b6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="129b6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="129b6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="129b6-115">Properties</span></span>

<span data-ttu-id="129b6-116">Die **CIM \_ Computersystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="129b6-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="129b6-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="129b6-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="129b6-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="129b6-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="129b6-121">A short textual description of the object.</span></span>

<span data-ttu-id="129b6-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-123">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="129b6-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-126">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="129b6-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="129b6-127">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="129b6-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="129b6-128">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="129b6-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="129b6-129">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="129b6-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-133">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="129b6-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="129b6-134">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="129b6-134">A textual description of the object.</span></span>

<span data-ttu-id="129b6-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="129b6-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-137">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="129b6-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="129b6-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="129b6-140">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="129b6-140">Indicates when the object was installed.</span></span> <span data-ttu-id="129b6-141">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="129b6-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="129b6-142">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="129b6-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="129b6-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="129b6-147">Definiert die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="129b6-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="129b6-148">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="129b6-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-152">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="129b6-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="129b6-153">Gibt an, wie der Name des Computer Systems mithilfe einer heuristischen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="129b6-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="129b6-154">Die Heuristik wird ausführlich in der Common-Model-Spezifikation von CIM V2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="129b6-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="129b6-155">Dabei wird davon ausgegangen, dass die dokumentierten Regeln in der richtigen Reihenfolge durchlaufen werden, um einen Namen zu ermitteln und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="129b6-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="129b6-156">In der Liste **NameFormat** -Werte ist die Rangfolge zum Zuweisen des Computersystem namens definiert.</span><span class="sxs-lookup"><span data-stu-id="129b6-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="129b6-157">Mehrere Regeln werden dem gleichen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="129b6-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="129b6-158">Beachten Sie, dass der **Name** des Objekts mit der Heuristik berechnet wird, ist der Schlüsselwert des Systems.</span><span class="sxs-lookup"><span data-stu-id="129b6-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="129b6-159">Andere Namen können mithilfe von Aliasen zugewiesen und für das Objekt verwendet werden, das für das Unternehmen besser geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="129b6-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="129b6-160">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="129b6-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="129b6-161">**Dial** ("Dial")</span><span class="sxs-lookup"><span data-stu-id="129b6-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="129b6-162">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="129b6-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="129b6-163">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="129b6-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="129b6-164">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="129b6-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="129b6-165">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="129b6-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="129b6-166">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="129b6-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="129b6-167">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="129b6-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="129b6-168">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="129b6-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="129b6-169">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="129b6-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="129b6-170">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="129b6-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="129b6-171">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="129b6-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="129b6-172">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="129b6-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="129b6-173">**Sonstige** ("Sonstige")</span><span class="sxs-lookup"><span data-stu-id="129b6-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="129b6-174">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="129b6-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="129b6-177">Wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer oder e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="129b6-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="129b6-178">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-179">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="129b6-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-182">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="129b6-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="129b6-183">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="129b6-183">Name of the primary system owner.</span></span>

<span data-ttu-id="129b6-184">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-185">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="129b6-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-186">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="129b6-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="129b6-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="129b6-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="129b6-188">Rollen, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="129b6-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="129b6-189">Unterklassen des Systems können diese Eigenschaft überschreiben, um explizite Rollen Werte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="129b6-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="129b6-190">Alternativ kann eine Arbeitsgruppe die Heuristik, Konventionen und Richtlinien zum Angeben von Rollen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="129b6-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="129b6-191">Beispielsweise kann für eine Instanz eines Netzwerksystems diese Eigenschaft die Zeichenfolge "Switch" oder "Bridge" enthalten.</span><span class="sxs-lookup"><span data-stu-id="129b6-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="129b6-192">Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="129b6-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="129b6-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="129b6-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="129b6-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="129b6-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="129b6-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="129b6-196">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="129b6-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="129b6-197">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="129b6-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="129b6-198">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="129b6-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="129b6-199">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="129b6-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="129b6-200">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="129b6-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="129b6-201">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="129b6-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="129b6-202">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="129b6-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="129b6-203">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="129b6-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="129b6-204">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="129b6-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="129b6-205">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="129b6-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="129b6-206">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="129b6-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="129b6-207">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="129b6-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="129b6-208">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="129b6-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="129b6-209">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="129b6-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="129b6-210">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="129b6-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="129b6-211">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="129b6-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="129b6-212">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="129b6-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="129b6-213">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="129b6-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="129b6-214">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="129b6-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="129b6-215">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="129b6-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="129b6-216">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="129b6-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="129b6-217">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="129b6-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="129b6-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="129b6-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="129b6-219">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="129b6-219">Remarks</span></span>

<span data-ttu-id="129b6-220">Die **CIM \_ Computersystem** -Klasse wird vom [**CIM- \_ System**](cim-system.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="129b6-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="129b6-221">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="129b6-221">WMI does not implement this class.</span></span> <span data-ttu-id="129b6-222">Weitere Informationen zu von **CIM \_ Computersystem** abgeleiteten Klassen finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="129b6-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="129b6-223">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="129b6-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="129b6-224">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="129b6-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="129b6-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="129b6-225">Requirements</span></span>



| <span data-ttu-id="129b6-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="129b6-226">Requirement</span></span> | <span data-ttu-id="129b6-227">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="129b6-228">Minimum supported client</span></span><br/> | <span data-ttu-id="129b6-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="129b6-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="129b6-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="129b6-230">Minimum supported server</span></span><br/> | <span data-ttu-id="129b6-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="129b6-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="129b6-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="129b6-232">Namespace</span></span><br/>                | <span data-ttu-id="129b6-233">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="129b6-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="129b6-234">MOF</span><span class="sxs-lookup"><span data-stu-id="129b6-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="129b6-235"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="129b6-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="129b6-236">DLL</span><span class="sxs-lookup"><span data-stu-id="129b6-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="129b6-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="129b6-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="129b6-238">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="129b6-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="129b6-239">**CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="129b6-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

