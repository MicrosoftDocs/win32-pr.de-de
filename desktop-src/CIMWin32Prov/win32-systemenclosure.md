---
description: Stellt die Eigenschaften dar, die einem physischen Systemgehäuse zugeordnet sind.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Win32_SystemEnclosure-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958574"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="31be6-103">Win32 \_ systemenclosure-Klasse</span><span class="sxs-lookup"><span data-stu-id="31be6-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="31be6-104">Die **Win32 \_ systemenclosure** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Eigenschaften dar, die einem physischen Systemgehäuse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="31be6-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="31be6-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31be6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="31be6-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="31be6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31be6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="31be6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="31be6-108">Member</span><span class="sxs-lookup"><span data-stu-id="31be6-108">Members</span></span>

<span data-ttu-id="31be6-109">Die **Win32- \_ systemenclosure** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="31be6-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="31be6-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="31be6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="31be6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31be6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31be6-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="31be6-112">Methods</span></span>

<span data-ttu-id="31be6-113">Die **Win32- \_ systemenclosure** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="31be6-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="31be6-114">Methode</span><span class="sxs-lookup"><span data-stu-id="31be6-114">Method</span></span>           | <span data-ttu-id="31be6-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31be6-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="31be6-116">**Iskompatibel**</span><span class="sxs-lookup"><span data-stu-id="31be6-116">**IsCompatible**</span></span> | <span data-ttu-id="31be6-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="31be6-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="31be6-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31be6-118">Properties</span></span>

<span data-ttu-id="31be6-119">Die **Win32- \_ systemenclosure** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31be6-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31be6-120">**Audiblealarm**</span><span class="sxs-lookup"><span data-stu-id="31be6-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-121">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-123">**True** gibt an, dass der Frame mit einem hörbaren Alarm ausgestattet ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="31be6-124">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-125">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="31be6-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-128">Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Securityverletzungs**")</span><span class="sxs-lookup"><span data-stu-id="31be6-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-129">Eine frei Form Zeichenfolge, die weitere Informationen bereitstellt, wenn die **securityverletzungs** -Eigenschaft angibt, dass ein Sicherheits bezogenes Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="31be6-130">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-131">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="31be6-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-134">Eine frei Form Zeichenfolge, die Informationen darüber enthält, wie die verschiedenen Kabel mit dem Frame verbunden und gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="31be6-135">Dank vieler Netzwerk-, Speicher-und Netzkabel kann die Kabel Verwaltung ein komplexes und anspruchsvolles Unterfangen sein.</span><span class="sxs-lookup"><span data-stu-id="31be6-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="31be6-136">Diese Eigenschaft enthält Informationen, um die Assembly und den Dienst des Frames zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="31be6-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="31be6-137">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="31be6-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-141">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="31be6-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-142">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="31be6-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="31be6-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-144">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="31be6-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-145">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="31be6-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31be6-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-147">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Physischer DMTF- \| Container globale Tabelle \| 002,1 "), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Chassis**](cim-chassis.md)".**Typebeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="31be6-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-148">Array von Chassistypen.</span><span class="sxs-lookup"><span data-stu-id="31be6-148">Array of chassis types.</span></span>

<span data-ttu-id="31be6-149">Dieser Wert stammt vom **Typmember** des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="31be6-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="31be6-150">Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31be6-151">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="31be6-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31be6-152">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="31be6-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="31be6-153">**Desktop** (3)</span><span class="sxs-lookup"><span data-stu-id="31be6-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="31be6-154">**Desktop mit niedrigem Profil** (4)</span><span class="sxs-lookup"><span data-stu-id="31be6-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="31be6-155">**Pizza Box** (5)</span><span class="sxs-lookup"><span data-stu-id="31be6-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="31be6-156">**Mini Turm** (6)</span><span class="sxs-lookup"><span data-stu-id="31be6-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="31be6-157">**Turm** (7)</span><span class="sxs-lookup"><span data-stu-id="31be6-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="31be6-158">**Portabel** (8)</span><span class="sxs-lookup"><span data-stu-id="31be6-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="31be6-159">**Laptop** (9)</span><span class="sxs-lookup"><span data-stu-id="31be6-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="31be6-160">**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="31be6-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="31be6-161">**Hand gehalten** (11)</span><span class="sxs-lookup"><span data-stu-id="31be6-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="31be6-162">**Docking Station** (12)</span><span class="sxs-lookup"><span data-stu-id="31be6-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="31be6-163">**Alle in eins** (13)</span><span class="sxs-lookup"><span data-stu-id="31be6-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="31be6-164">**Sub Notebook** (14)</span><span class="sxs-lookup"><span data-stu-id="31be6-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="31be6-165">**Speicherplatz** (15)</span><span class="sxs-lookup"><span data-stu-id="31be6-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="31be6-166">**Mittags Feld** (16)</span><span class="sxs-lookup"><span data-stu-id="31be6-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="31be6-167">**Haupt Betriebssystem-Chassis** (17)</span><span class="sxs-lookup"><span data-stu-id="31be6-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="31be6-168">**Erweiterungs Chassis** (18)</span><span class="sxs-lookup"><span data-stu-id="31be6-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="31be6-169">**Subchassis** (19)</span><span class="sxs-lookup"><span data-stu-id="31be6-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="31be6-170">**Buserweiterungs Chassis** (20)</span><span class="sxs-lookup"><span data-stu-id="31be6-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="31be6-171">**Peripherie Chassis** (21)</span><span class="sxs-lookup"><span data-stu-id="31be6-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="31be6-172">**Speicherchassis** (22)</span><span class="sxs-lookup"><span data-stu-id="31be6-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="31be6-173">**Rack Mount Chassis** (23)</span><span class="sxs-lookup"><span data-stu-id="31be6-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="31be6-174">**Sealed-Case-PC** (24)</span><span class="sxs-lookup"><span data-stu-id="31be6-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="31be6-175">**Tablet** (30)</span><span class="sxs-lookup"><span data-stu-id="31be6-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="31be6-176">**Konvertierbar** (31)</span><span class="sxs-lookup"><span data-stu-id="31be6-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="31be6-177">**Ablösbar (32** )</span><span class="sxs-lookup"><span data-stu-id="31be6-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31be6-178">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="31be6-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-181">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="31be6-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-182">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31be6-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="31be6-183">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="31be6-184">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-185">**Currentrequirements dorerzeugte**</span><span class="sxs-lookup"><span data-stu-id="31be6-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-186">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="31be6-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-188">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Amps bei 120 Volt")</span><span class="sxs-lookup"><span data-stu-id="31be6-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-189">Aktuell, der vom Chassis bei 120V benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="31be6-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="31be6-190">Wenn die Stromversorgung vom Chassis bereitgestellt wird – wie bei einer unterbrechungsfreien Stromversorgung (USV) – kann diese Eigenschaft auf die erzeugte AMPERAGE (als negative Zahl) hindeuten.</span><span class="sxs-lookup"><span data-stu-id="31be6-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="31be6-191">Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-192">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="31be6-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-193">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="31be6-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-195">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="31be6-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-196">Tiefe des physischen Pakets – in Zoll.</span><span class="sxs-lookup"><span data-stu-id="31be6-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="31be6-197">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-198">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31be6-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-201">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="31be6-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-202">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="31be6-202">Description of the object.</span></span>

<span data-ttu-id="31be6-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-204">**Heatgene Ration**</span><span class="sxs-lookup"><span data-stu-id="31be6-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-205">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31be6-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-207">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("BTU pro Stunde")</span><span class="sxs-lookup"><span data-stu-id="31be6-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-208">Menge der Wärme, die vom Gehäuse in BTU/Stunde generiert wird.</span><span class="sxs-lookup"><span data-stu-id="31be6-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="31be6-209">Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-210">**Height**</span><span class="sxs-lookup"><span data-stu-id="31be6-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-211">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="31be6-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-213">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="31be6-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-214">Höhe des physischen Pakets – in Zoll.</span><span class="sxs-lookup"><span data-stu-id="31be6-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="31be6-215">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-216">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="31be6-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-217">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-219">**True** gibt an, dass ein physisches Paket im laufenden Betrieb ausgetauscht werden kann (wenn es möglich ist, das Element durch einen physisch abweichenden, aber entsprechenden Wert zu ersetzen, während für das enthaltene Paket eine Stromversorgung angewendet wurde).</span><span class="sxs-lookup"><span data-stu-id="31be6-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="31be6-220">Beispielsweise ist ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wird, wechselseitig austauschbar.</span><span class="sxs-lookup"><span data-stu-id="31be6-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="31be6-221">Alle Pakete, die sich im laufenden Betrieb austauschen lassen, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="31be6-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="31be6-222">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31be6-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-224">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="31be6-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-226">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="31be6-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-227">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="31be6-227">Date and time the object was installed.</span></span> <span data-ttu-id="31be6-228">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="31be6-229">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-230">**Sperre vorhanden**</span><span class="sxs-lookup"><span data-stu-id="31be6-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-233">**True** gibt an, dass der Frame durch eine Sperre geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="31be6-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="31be6-234">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-235">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="31be6-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-238">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="31be6-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-239">Der Name der Organisation, die das physische Element erzeugt.</span><span class="sxs-lookup"><span data-stu-id="31be6-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="31be6-240">Dieser Wert stammt aus dem **Hersteller** Mitglied des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="31be6-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="31be6-241">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-242">**Modell**</span><span class="sxs-lookup"><span data-stu-id="31be6-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-245">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="31be6-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-246">Der Name, mit dem das physische Element bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="31be6-247">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-248">**Name**</span><span class="sxs-lookup"><span data-stu-id="31be6-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-251">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="31be6-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-252">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-252">Label by which the object is known.</span></span> <span data-ttu-id="31be6-253">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="31be6-254">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-255">**Anzahl von powercords**</span><span class="sxs-lookup"><span data-stu-id="31be6-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-256">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31be6-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-258">Anzahl der Netzkabel, die mit dem Chassis verbunden werden müssen, damit alle Komponenten funktionieren.</span><span class="sxs-lookup"><span data-stu-id="31be6-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="31be6-259">Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="31be6-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-263">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="31be6-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="31be6-264">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="31be6-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="31be6-265">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** und die Barcode-Daten, die als Klassen Schlüssel verwendet werden, in der Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="31be6-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="31be6-266">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-267">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="31be6-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-270">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="31be6-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-271">Teilenummer, die von der Organisation zugewiesen wird, die das physische Element erzeugt oder herstellt.</span><span class="sxs-lookup"><span data-stu-id="31be6-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="31be6-272">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-273">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="31be6-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-274">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-276">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="31be6-277">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-278">**Ab**</span><span class="sxs-lookup"><span data-stu-id="31be6-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-279">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-281">**True** gibt an, dass ein physisches Paket entfernt werden kann (wenn es so konzipiert ist, dass es in den physischen Container übernommen wird, in dem es normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird).</span><span class="sxs-lookup"><span data-stu-id="31be6-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="31be6-282">Ein Paket kann weiterhin entfernt werden, wenn die Stromversorgung "Off" sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="31be6-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="31be6-283">Wenn das Paket entfernt werden kann, während die Stromversorgung aktiviert ist, kann das Element entfernt werden, und das Element kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="31be6-284">Beispielsweise ist ein zusätzlicher Akku in einem Laptop Wechsel Datenträger, ebenso wie ein Laufwerks Paket, das mithilfe von SCA-Connectors (Server Configuration Application) eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="31be6-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="31be6-285">Der letztere kann jedoch im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="31be6-286">Eine Laptop Anzeige kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil.</span><span class="sxs-lookup"><span data-stu-id="31be6-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="31be6-287">Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="31be6-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="31be6-288">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-289">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="31be6-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-290">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-292">**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="31be6-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="31be6-293">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="31be6-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="31be6-294">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="31be6-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="31be6-295">Ein weiteres Beispiel ist ein Stromversorgung-Paket, das auf gleitenden Schienen eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="31be6-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="31be6-296">Alle Wechsel Pakete sind von Natur aus austauschbar.</span><span class="sxs-lookup"><span data-stu-id="31be6-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="31be6-297">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-298">**Security-Verletzung**</span><span class="sxs-lookup"><span data-stu-id="31be6-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-299">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31be6-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-301">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Physischer DMTF- \| Container Global Table \| 002,12 "), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="31be6-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-302">Status einer physischen Verletzung des Frames.</span><span class="sxs-lookup"><span data-stu-id="31be6-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="31be6-303">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31be6-304">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="31be6-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31be6-305">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="31be6-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="31be6-306">**Keine Verletzung** (3)</span><span class="sxs-lookup"><span data-stu-id="31be6-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="31be6-307">**Versuchte Sicherheitsverletzung** (4)</span><span class="sxs-lookup"><span data-stu-id="31be6-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="31be6-308">**Verletzung erfolgreich** (5)</span><span class="sxs-lookup"><span data-stu-id="31be6-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31be6-309">**SecurityStatus**</span><span class="sxs-lookup"><span data-stu-id="31be6-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-310">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31be6-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-312">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 3 \| Sicherheits Status")</span><span class="sxs-lookup"><span data-stu-id="31be6-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-313">Sicherheitseinstellungen für externe Eingaben, z. b. eine Tastatur, auf einen Computer.</span><span class="sxs-lookup"><span data-stu-id="31be6-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="31be6-314">Dieser Wert stammt aus dem **Sicherheits Status** Mitglied des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="31be6-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31be6-315">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="31be6-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31be6-316">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="31be6-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="31be6-317">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="31be6-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="31be6-318">**Externe Schnittstelle gesperrt** (4)</span><span class="sxs-lookup"><span data-stu-id="31be6-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="31be6-319">**Externe Schnittstelle aktiviert** (5)</span><span class="sxs-lookup"><span data-stu-id="31be6-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31be6-320">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="31be6-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-323">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="31be6-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-324">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="31be6-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="31be6-325">Dieser Wert stammt aus dem **Seriennummern** Element des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="31be6-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="31be6-326">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-327">**Service Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="31be6-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-328">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="31be6-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="31be6-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-330">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="31be6-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-331">Array Ausführlichere Erläuterungen zu den Einträgen im **ServicePhilosophy** -Array.</span><span class="sxs-lookup"><span data-stu-id="31be6-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="31be6-332">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag in **ServicePhilosophy** verknüpft ist, der sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="31be6-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="31be6-333">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-334">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="31be6-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-335">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="31be6-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31be6-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-337">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Service Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="31be6-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-338">Ein Array, das einschließt, ob der Frame vom oberen, dem Vorder-oder Seitenrand bedient wird, ob der Frame gleitende tablettfächer oder Wechsel Seiten aufweist und ob der Frame beweglich ist – z. b. mithilfe von Walzen.</span><span class="sxs-lookup"><span data-stu-id="31be6-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="31be6-339">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31be6-340">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="31be6-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31be6-341">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="31be6-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="31be6-342">**Dienst von oben** (2)</span><span class="sxs-lookup"><span data-stu-id="31be6-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="31be6-343">**Dienst von Front** (3)</span><span class="sxs-lookup"><span data-stu-id="31be6-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="31be6-344">**Dienst von hinten** (4)</span><span class="sxs-lookup"><span data-stu-id="31be6-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="31be6-345">**Dienst von Seite** (5)</span><span class="sxs-lookup"><span data-stu-id="31be6-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="31be6-346">**Gleitende Tabletts** (6)</span><span class="sxs-lookup"><span data-stu-id="31be6-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="31be6-347">Wechsel **Seiten** (7)</span><span class="sxs-lookup"><span data-stu-id="31be6-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="31be6-348">**Verschiebbare** (8)</span><span class="sxs-lookup"><span data-stu-id="31be6-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31be6-349">**SKU**</span><span class="sxs-lookup"><span data-stu-id="31be6-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-352">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="31be6-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-353">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="31be6-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="31be6-354">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="31be6-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-358">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 3 \| Asset Tag")</span><span class="sxs-lookup"><span data-stu-id="31be6-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-359">Assettagnummer des System Gehäuses.</span><span class="sxs-lookup"><span data-stu-id="31be6-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="31be6-360">Dieser Wert stammt aus dem **Asset-tagnummern** Element des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="31be6-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="31be6-361">**Status**</span><span class="sxs-lookup"><span data-stu-id="31be6-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-362">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-364">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="31be6-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-365">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="31be6-365">Current status of the object.</span></span> <span data-ttu-id="31be6-366">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="31be6-367">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="31be6-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="31be6-368">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="31be6-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="31be6-369">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="31be6-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="31be6-370">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="31be6-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="31be6-371">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="31be6-372">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="31be6-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="31be6-373">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="31be6-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="31be6-374">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="31be6-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31be6-375">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="31be6-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31be6-376">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="31be6-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="31be6-377">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="31be6-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="31be6-378">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="31be6-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="31be6-379">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="31be6-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="31be6-380">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="31be6-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="31be6-381">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="31be6-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="31be6-382">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="31be6-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="31be6-383">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="31be6-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="31be6-384">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="31be6-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31be6-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="31be6-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-386">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-388">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="31be6-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-389">Eindeutiger Bezeichner des System Gehäuses.</span><span class="sxs-lookup"><span data-stu-id="31be6-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="31be6-390">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="31be6-391">Beispiel: "System Gehäuse 1"</span><span class="sxs-lookup"><span data-stu-id="31be6-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="31be6-392">**Typebeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="31be6-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-393">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="31be6-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="31be6-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-395">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Chassis**](cim-chassis.md).**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="31be6-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-396">Array mit weiteren Informationen über die **ChassisTypes** -Array Einträge.</span><span class="sxs-lookup"><span data-stu-id="31be6-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="31be6-397">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag in **ChassisTypes** verknüpft ist, der sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="31be6-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="31be6-398">Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-399">**Version**</span><span class="sxs-lookup"><span data-stu-id="31be6-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31be6-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-402">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="31be6-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="31be6-403">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="31be6-403">Version of the physical element.</span></span>

<span data-ttu-id="31be6-404">Dieser Wert stammt aus dem  Versionsmember des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="31be6-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="31be6-405">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-406">**Visiblealarm**</span><span class="sxs-lookup"><span data-stu-id="31be6-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-407">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31be6-409">**True** gibt an, dass die Ausrüstung einen sichtbaren Alarm enthält.</span><span class="sxs-lookup"><span data-stu-id="31be6-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="31be6-410">Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-411">**Weight**</span><span class="sxs-lookup"><span data-stu-id="31be6-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-412">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="31be6-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-414">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pfund")</span><span class="sxs-lookup"><span data-stu-id="31be6-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-415">Gewichtung des physischen Pakets in Pfund.</span><span class="sxs-lookup"><span data-stu-id="31be6-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="31be6-416">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31be6-417">**Width**</span><span class="sxs-lookup"><span data-stu-id="31be6-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31be6-418">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="31be6-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="31be6-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31be6-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31be6-420">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="31be6-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="31be6-421">Breite des physischen Pakets in Zoll.</span><span class="sxs-lookup"><span data-stu-id="31be6-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="31be6-422">Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="31be6-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31be6-423">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31be6-423">Remarks</span></span>

<span data-ttu-id="31be6-424">Die **Win32- \_ systemenclosure** -Klasse wird vom [**CIM- \_ Chassis**](cim-chassis.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="31be6-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31be6-425">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31be6-425">Examples</span></span>

<span data-ttu-id="31be6-426">Das PowerShell-Beispiel für [Multithreaded-System Ressourcen mit PowerShell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) in der TechNet Gallery verwendet eine Reihe von Klassen, einschließlich **Win32- \_ systemenclosure**, um Daten von einem System abzurufen.</span><span class="sxs-lookup"><span data-stu-id="31be6-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="31be6-427">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31be6-427">Requirements</span></span>



| <span data-ttu-id="31be6-428">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31be6-428">Requirement</span></span> | <span data-ttu-id="31be6-429">Wert</span><span class="sxs-lookup"><span data-stu-id="31be6-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31be6-430">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31be6-430">Minimum supported client</span></span><br/> | <span data-ttu-id="31be6-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31be6-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31be6-432">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31be6-432">Minimum supported server</span></span><br/> | <span data-ttu-id="31be6-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31be6-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31be6-434">Namespace</span><span class="sxs-lookup"><span data-stu-id="31be6-434">Namespace</span></span><br/>                | <span data-ttu-id="31be6-435">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="31be6-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31be6-436">MOF</span><span class="sxs-lookup"><span data-stu-id="31be6-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31be6-437"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="31be6-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31be6-438">DLL</span><span class="sxs-lookup"><span data-stu-id="31be6-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31be6-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31be6-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31be6-440">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31be6-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31be6-441">**CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="31be6-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="31be6-442">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="31be6-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="31be6-443">WMI-Tasks: Computer Hardware</span><span class="sxs-lookup"><span data-stu-id="31be6-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
