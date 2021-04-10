---
description: Die CIM \_ -Chassis-Klasse stellt die physischen Elemente dar, die andere Elemente einschließen und definierbare Funktionen bereitstellen, wie z. b. einen Desktop, Verarbeitungs Knoten, UPS, Datenträger-oder Band Speicher oder eine Kombination dieser Elemente.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: CIM_Chassis-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127116"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="7c287-103">CIM- \_ Chassis-Klasse</span><span class="sxs-lookup"><span data-stu-id="7c287-103">CIM\_Chassis class</span></span>

<span data-ttu-id="7c287-104">Die **CIM- \_ Chassis** -Klasse stellt die physischen Elemente dar, die andere Elemente einschließen und definierbare Funktionen bereitstellen, wie z. b. einen Desktop, Verarbeitungs Knoten, UPS, Datenträger-oder Band Speicher oder eine Kombination dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="7c287-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c287-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c287-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c287-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7c287-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7c287-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7c287-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7c287-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c287-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c287-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="7c287-110">Member</span><span class="sxs-lookup"><span data-stu-id="7c287-110">Members</span></span>

<span data-ttu-id="7c287-111">Die **CIM- \_ Chassis** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7c287-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="7c287-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7c287-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c287-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c287-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c287-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="7c287-114">Methods</span></span>

<span data-ttu-id="7c287-115">Die **CIM- \_ Chassis** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7c287-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="7c287-116">Methode</span><span class="sxs-lookup"><span data-stu-id="7c287-116">Method</span></span>                                                           | <span data-ttu-id="7c287-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c287-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c287-118">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="7c287-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="7c287-119">Überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c287-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="7c287-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="7c287-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7c287-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c287-121">Properties</span></span>

<span data-ttu-id="7c287-122">Die **CIM- \_ Chassis** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7c287-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c287-123">**Audiblealarm**</span><span class="sxs-lookup"><span data-stu-id="7c287-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-126">**True** gibt an, dass der Frame mit einem hörbaren Alarm ausgestattet ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="7c287-127">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="7c287-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-131">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Securityverletzungs**")</span><span class="sxs-lookup"><span data-stu-id="7c287-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-132">Eine frei Form Zeichenfolge, die weitere Informationen bereitstellt, wenn die **securityverletzungs** -Eigenschaft angibt, dass eine Sicherheitsverletzung oder ein anderes Sicherheits bezogenes Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="7c287-133">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-134">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="7c287-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-137">Eine frei Form Zeichenfolge, die Informationen darüber enthält, wie die verschiedenen Kabel mit dem Frame verbunden und gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="7c287-138">Dank vieler Netzwerk-, Speicher-und Netzkabel kann die Kabel Verwaltung ein komplexes und anspruchsvolles Unterfangen sein.</span><span class="sxs-lookup"><span data-stu-id="7c287-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="7c287-139">Diese Zeichen folgen Eigenschaft enthält Informationen, um die Assembly und den Dienst des Frames zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7c287-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="7c287-140">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7c287-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-144">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7c287-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-145">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7c287-145">A short textual description of the object.</span></span>

<span data-ttu-id="7c287-146">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-147">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="7c287-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7c287-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c287-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-150">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physischer DMTF- \| Container globale Tabelle \| 002,1 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Chassis**".**Typebeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="7c287-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-151">Enumerationsarray mit ganzzahligen Werten, das den Typ des Chassis angibt.</span><span class="sxs-lookup"><span data-stu-id="7c287-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c287-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7c287-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-153">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="7c287-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c287-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7c287-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-155">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="7c287-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="7c287-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span><span class="sxs-lookup"><span data-stu-id="7c287-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-157">Desktop:</span><span class="sxs-lookup"><span data-stu-id="7c287-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="7c287-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Desktop mit niedrigem Profil** (4)</span><span class="sxs-lookup"><span data-stu-id="7c287-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-159">Desktop mit niedrigem Profil</span><span class="sxs-lookup"><span data-stu-id="7c287-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="7c287-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span><span class="sxs-lookup"><span data-stu-id="7c287-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-161">Pizza Box.</span><span class="sxs-lookup"><span data-stu-id="7c287-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="7c287-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Turm** (6)</span><span class="sxs-lookup"><span data-stu-id="7c287-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-163">Mini Turm.</span><span class="sxs-lookup"><span data-stu-id="7c287-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="7c287-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Turm** (7)</span><span class="sxs-lookup"><span data-stu-id="7c287-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-165">Tower:</span><span class="sxs-lookup"><span data-stu-id="7c287-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="7c287-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portabel** (8)</span><span class="sxs-lookup"><span data-stu-id="7c287-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-167">Tabel.</span><span class="sxs-lookup"><span data-stu-id="7c287-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="7c287-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span><span class="sxs-lookup"><span data-stu-id="7c287-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-169">Laptop:</span><span class="sxs-lookup"><span data-stu-id="7c287-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="7c287-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="7c287-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-171">Noten.</span><span class="sxs-lookup"><span data-stu-id="7c287-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="7c287-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand gehalten** (11)</span><span class="sxs-lookup"><span data-stu-id="7c287-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-173">Hand halten.</span><span class="sxs-lookup"><span data-stu-id="7c287-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="7c287-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span><span class="sxs-lookup"><span data-stu-id="7c287-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-175">Andockstation.</span><span class="sxs-lookup"><span data-stu-id="7c287-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="7c287-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Alle in eins** (13)</span><span class="sxs-lookup"><span data-stu-id="7c287-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-177">Vollständig.</span><span class="sxs-lookup"><span data-stu-id="7c287-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="7c287-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span><span class="sxs-lookup"><span data-stu-id="7c287-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-179">Unter Notebook.</span><span class="sxs-lookup"><span data-stu-id="7c287-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="7c287-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Speicherplatz** (15)</span><span class="sxs-lookup"><span data-stu-id="7c287-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-181">Speicherplatz wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7c287-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="7c287-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Mittags Feld** (16)</span><span class="sxs-lookup"><span data-stu-id="7c287-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-183">Das mittags Kästchen.</span><span class="sxs-lookup"><span data-stu-id="7c287-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="7c287-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Haupt Betriebssystem-Chassis** (17)</span><span class="sxs-lookup"><span data-stu-id="7c287-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-185">Haupt Betriebssystem des Systems.</span><span class="sxs-lookup"><span data-stu-id="7c287-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="7c287-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Erweiterungs Chassis** (18)</span><span class="sxs-lookup"><span data-stu-id="7c287-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-187">Erweiterungs Chassis.</span><span class="sxs-lookup"><span data-stu-id="7c287-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="7c287-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**Subchassis** (19)</span><span class="sxs-lookup"><span data-stu-id="7c287-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-189">Subchassis.</span><span class="sxs-lookup"><span data-stu-id="7c287-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="7c287-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Buserweiterungs Chassis** (20)</span><span class="sxs-lookup"><span data-stu-id="7c287-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-191">Buserweiterungs Chassis.</span><span class="sxs-lookup"><span data-stu-id="7c287-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="7c287-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripherie Chassis** (21)</span><span class="sxs-lookup"><span data-stu-id="7c287-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-193">Peripherie Chassis.</span><span class="sxs-lookup"><span data-stu-id="7c287-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="7c287-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Speicherchassis** (22)</span><span class="sxs-lookup"><span data-stu-id="7c287-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-195">Speicher Chassis.</span><span class="sxs-lookup"><span data-stu-id="7c287-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="7c287-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span><span class="sxs-lookup"><span data-stu-id="7c287-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-197">Rack einbinden des Chassis.</span><span class="sxs-lookup"><span data-stu-id="7c287-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="7c287-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case-PC** (24)</span><span class="sxs-lookup"><span data-stu-id="7c287-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="7c287-199">Sealed-Case-Computer.</span><span class="sxs-lookup"><span data-stu-id="7c287-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7c287-200">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7c287-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-203">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c287-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-204">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c287-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7c287-205">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7c287-206">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-207">**Currentrequirements dorerzeugte**</span><span class="sxs-lookup"><span data-stu-id="7c287-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-208">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="7c287-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-210">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Amps bei 120 Volt")</span><span class="sxs-lookup"><span data-stu-id="7c287-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-211">Wird derzeit vom Chassis bei 120 Volt benötigt.</span><span class="sxs-lookup"><span data-stu-id="7c287-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="7c287-212">Wenn die Stromversorgung vom Chassis bereitgestellt wird (wie im Fall von a-UPS), kann diese Eigenschaft den erstellten AMPERAGE als negative Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="7c287-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="7c287-213">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="7c287-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-214">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="7c287-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-216">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="7c287-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-217">Die Tiefe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="7c287-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="7c287-218">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-219">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c287-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-222">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7c287-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-223">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7c287-223">A textual description of the object.</span></span>

<span data-ttu-id="7c287-224">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-225">**Heatgene Ration**</span><span class="sxs-lookup"><span data-stu-id="7c287-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-226">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c287-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-228">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU pro Stunde")</span><span class="sxs-lookup"><span data-stu-id="7c287-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-229">Menge der vom Chassis in BTU/Stunde erzeugten Heat.</span><span class="sxs-lookup"><span data-stu-id="7c287-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="7c287-230">**Height**</span><span class="sxs-lookup"><span data-stu-id="7c287-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-231">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="7c287-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-233">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="7c287-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-234">Höhe des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="7c287-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="7c287-235">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-236">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="7c287-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-237">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-239">**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c287-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="7c287-240">Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="7c287-241">Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="7c287-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="7c287-242">Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="7c287-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="7c287-243">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7c287-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-245">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c287-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-247">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7c287-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-248">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c287-248">Indicates when the object was installed.</span></span> <span data-ttu-id="7c287-249">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7c287-250">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-251">**Sperre vorhanden**</span><span class="sxs-lookup"><span data-stu-id="7c287-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-252">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-254">**True** gibt an, dass der Frame durch eine Sperre geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="7c287-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="7c287-255">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-256">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="7c287-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-259">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c287-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-260">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="7c287-261">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="7c287-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="7c287-262">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-263">**Modell**</span><span class="sxs-lookup"><span data-stu-id="7c287-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-266">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7c287-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-267">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="7c287-268">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-269">**Name**</span><span class="sxs-lookup"><span data-stu-id="7c287-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-272">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7c287-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-273">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-273">Label by which the object is known.</span></span> <span data-ttu-id="7c287-274">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7c287-275">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-276">**Anzahl von powercords**</span><span class="sxs-lookup"><span data-stu-id="7c287-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-277">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c287-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-279">Anzahl der Netzkabel, die mit dem Chassis verbunden werden müssen, damit alle Komponenten funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="7c287-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="7c287-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7c287-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-283">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7c287-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="7c287-284">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7c287-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="7c287-285">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c287-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="7c287-286">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-287">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="7c287-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-290">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c287-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-291">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="7c287-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="7c287-292">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-293">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="7c287-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-294">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-296">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="7c287-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="7c287-297">Andernfalls ist Sie zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7c287-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="7c287-298">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-299">**Ab**</span><span class="sxs-lookup"><span data-stu-id="7c287-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-300">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-302">**True** gibt an, dass das Paket in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="7c287-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="7c287-303">Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung deaktiviert sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7c287-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="7c287-304">Wenn die Stromversorgung aktiviert und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="7c287-305">Beispielsweise kann ein erweiterbarer Prozessor Chip entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="7c287-306">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-307">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="7c287-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-308">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-310">Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="7c287-311">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="7c287-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="7c287-312">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7c287-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="7c287-313">Alle wechselkomponenten sind von Natur aus ersetzbar.</span><span class="sxs-lookup"><span data-stu-id="7c287-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="7c287-314">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-315">**Security-Verletzung**</span><span class="sxs-lookup"><span data-stu-id="7c287-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-316">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c287-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-318">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physischer DMTF- \| Container Global Table \| 002,12 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="7c287-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-319">Gibt an, ob ein physischer Verstoß gegen den Frame versucht wurde, jedoch nicht erfolgreich war oder ob versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="7c287-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="7c287-320">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c287-321">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7c287-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c287-322">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7c287-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="7c287-323">**Keine Verletzung** (3)</span><span class="sxs-lookup"><span data-stu-id="7c287-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="7c287-324">**Versuchte Sicherheitsverletzung** (4)</span><span class="sxs-lookup"><span data-stu-id="7c287-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="7c287-325">**Verletzung erfolgreich** (5)</span><span class="sxs-lookup"><span data-stu-id="7c287-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c287-326">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7c287-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-329">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7c287-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-330">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7c287-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="7c287-331">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-332">**Service Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="7c287-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-333">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7c287-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c287-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-335">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="7c287-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-336">Freiform-Zeichen folgen, die ausführliche Erläuterungen zu Einträgen im **ServicePhilosophy** -Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c287-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="7c287-337">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **ServicePhilosophy** -Array, das sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="7c287-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="7c287-338">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-339">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="7c287-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-340">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7c287-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c287-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-342">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Service Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="7c287-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-343">Gibt an, ob der Frame vom oberen Rand, von der Vorderseite, von hinten oder von der Seite bedient wird. und ob Schiebe Fächer oder Wechsel Seiten vorhanden sind, und ob der Frame beweglich ist (z. b. über Walzen).</span><span class="sxs-lookup"><span data-stu-id="7c287-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="7c287-344">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c287-345">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7c287-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c287-346">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7c287-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="7c287-347">**Dienst von oben** (2)</span><span class="sxs-lookup"><span data-stu-id="7c287-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="7c287-348">**Dienst von Front** (3)</span><span class="sxs-lookup"><span data-stu-id="7c287-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="7c287-349">**Dienst von hinten** (4)</span><span class="sxs-lookup"><span data-stu-id="7c287-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="7c287-350">**Dienst von Seite** (5)</span><span class="sxs-lookup"><span data-stu-id="7c287-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="7c287-351">**Gleitende Tabletts** (6)</span><span class="sxs-lookup"><span data-stu-id="7c287-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="7c287-352">Wechsel **Seiten** (7)</span><span class="sxs-lookup"><span data-stu-id="7c287-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="7c287-353">**Verschiebbare** (8)</span><span class="sxs-lookup"><span data-stu-id="7c287-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c287-354">**SKU**</span><span class="sxs-lookup"><span data-stu-id="7c287-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-357">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7c287-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-358">Die Stock Keeping Unit-Nummer für dieses physische Element.</span><span class="sxs-lookup"><span data-stu-id="7c287-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="7c287-359">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-360">**Status**</span><span class="sxs-lookup"><span data-stu-id="7c287-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-363">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7c287-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-364">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="7c287-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="7c287-365">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7c287-366">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c287-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7c287-367">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="7c287-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7c287-368">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c287-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7c287-369">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="7c287-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7c287-370">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7c287-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7c287-371">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7c287-372">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7c287-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7c287-373">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7c287-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7c287-374">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7c287-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7c287-375">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7c287-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c287-376">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7c287-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7c287-377">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7c287-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7c287-378">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7c287-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7c287-379">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7c287-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7c287-380">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7c287-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7c287-381">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7c287-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7c287-382">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7c287-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7c287-383">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7c287-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7c287-384">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7c287-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c287-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="7c287-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-386">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-388">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c287-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-389">Identifiziert das physische Element eindeutig und fungiert als Schlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="7c287-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="7c287-390">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="7c287-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="7c287-391">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7c287-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="7c287-392">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="7c287-393">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7c287-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="7c287-394">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="7c287-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="7c287-395">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-396">**Typebeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="7c287-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-397">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7c287-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c287-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-399">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Chassis**.**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="7c287-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-400">Array von Freiform-Zeichen folgen, das Informationen über die **ChassisTypes** -Array Einträge bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7c287-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="7c287-401">Jeder Array Eintrag bezieht sich auf den Eintrag in der **ChassisTypes** -Eigenschaft, der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="7c287-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="7c287-402">**Version**</span><span class="sxs-lookup"><span data-stu-id="7c287-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c287-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-405">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7c287-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7c287-406">Gibt die Version des physischen Elements an.</span><span class="sxs-lookup"><span data-stu-id="7c287-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="7c287-407">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-408">**Visiblealarm**</span><span class="sxs-lookup"><span data-stu-id="7c287-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-409">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c287-411">**True** gibt an, dass die Ausrüstung einen sichtbaren Alarm enthält.</span><span class="sxs-lookup"><span data-stu-id="7c287-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="7c287-412">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-413">**Weight**</span><span class="sxs-lookup"><span data-stu-id="7c287-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-414">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="7c287-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-416">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="7c287-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-417">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="7c287-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="7c287-418">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c287-419">**Width**</span><span class="sxs-lookup"><span data-stu-id="7c287-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c287-420">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="7c287-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="7c287-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c287-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c287-422">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="7c287-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="7c287-423">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="7c287-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="7c287-424">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7c287-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c287-425">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c287-425">Remarks</span></span>

<span data-ttu-id="7c287-426">Die **CIM- \_ Chassis** -Klasse wird von [**CIM \_ physicalframe**](cim-physicalframe.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c287-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="7c287-427">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7c287-427">WMI does not implement this class.</span></span> <span data-ttu-id="7c287-428">Weitere Informationen zu Klassen, die vom **CIM- \_ Chassis** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c287-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7c287-429">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c287-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c287-430">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c287-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c287-431">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c287-431">Requirements</span></span>



| <span data-ttu-id="7c287-432">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c287-432">Requirement</span></span> | <span data-ttu-id="7c287-433">Wert</span><span class="sxs-lookup"><span data-stu-id="7c287-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c287-434">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c287-434">Minimum supported client</span></span><br/> | <span data-ttu-id="7c287-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c287-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c287-436">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c287-436">Minimum supported server</span></span><br/> | <span data-ttu-id="7c287-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c287-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c287-438">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c287-438">Namespace</span></span><br/>                | <span data-ttu-id="7c287-439">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7c287-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c287-440">MOF</span><span class="sxs-lookup"><span data-stu-id="7c287-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c287-441"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7c287-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c287-442">DLL</span><span class="sxs-lookup"><span data-stu-id="7c287-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c287-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c287-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c287-444">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c287-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c287-445">**CIM- \_ physicalframe**</span><span class="sxs-lookup"><span data-stu-id="7c287-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

