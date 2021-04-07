---
description: Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863115"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="299d1-103">MSVM- \_ bioselements-Klasse</span><span class="sxs-lookup"><span data-stu-id="299d1-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="299d1-104">Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten.</span><span class="sxs-lookup"><span data-stu-id="299d1-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="299d1-105">Das BIOS ist kein logisches Gerät, daher sollte das virtuelle BIOS nicht als Gerät eines virtuellen Computers betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="299d1-106">Da es sich nicht um ein Gerät handelt, verfügt es nicht über einen entsprechenden Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="299d1-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="299d1-107">Das BIOS-Objekt wird der virtuellen Maschine über die [**MSVM- \_ Systembios**](msvm-systembios.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="299d1-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="299d1-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="299d1-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="299d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="299d1-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="299d1-110">Member</span><span class="sxs-lookup"><span data-stu-id="299d1-110">Members</span></span>

<span data-ttu-id="299d1-111">Die **MSVM \_ bioselements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="299d1-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="299d1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="299d1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="299d1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="299d1-113">Properties</span></span>

<span data-ttu-id="299d1-114">Die **MSVM \_ bioselements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="299d1-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="299d1-115">**Baseboardserialnumber**</span><span class="sxs-lookup"><span data-stu-id="299d1-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-118">Die Seriennummer für das Basisboard auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="299d1-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-119">**Biosguid**</span><span class="sxs-lookup"><span data-stu-id="299d1-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-122">Der eindeutige Bezeichner für das BIOS.</span><span class="sxs-lookup"><span data-stu-id="299d1-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-123">**Biosnumlock**</span><span class="sxs-lookup"><span data-stu-id="299d1-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="299d1-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-126">Der aktivierte Status der NUM-Sperre im BIOS.</span><span class="sxs-lookup"><span data-stu-id="299d1-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="299d1-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-130">Die Seriennummer für das BIOS.</span><span class="sxs-lookup"><span data-stu-id="299d1-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-131">**"Bootorder"**</span><span class="sxs-lookup"><span data-stu-id="299d1-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-132">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="299d1-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="299d1-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-134">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="299d1-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-135">Die Reihenfolge, in der Geräte beim Start nach einem Startsektor durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="299d1-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-139">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-140">Der interne Bezeichner für diese Kompilierung des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="299d1-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="299d1-141">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf 14 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="299d1-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-145">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-146">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="299d1-146">A short description of the object.</span></span> <span data-ttu-id="299d1-147">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-148">**Chassisassettag**</span><span class="sxs-lookup"><span data-stu-id="299d1-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-151">Wird automatisch durch das BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="299d1-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-152">**Chassisserialnumber**</span><span class="sxs-lookup"><span data-stu-id="299d1-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-155">Wird automatisch durch das BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="299d1-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-156">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="299d1-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-159">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-160">Der vom Softwareelement verwendete Codesatz.</span><span class="sxs-lookup"><span data-stu-id="299d1-160">The code set used by the software element.</span></span> <span data-ttu-id="299d1-161">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-162">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="299d1-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-165">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="299d1-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="299d1-166">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="299d1-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-168">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="299d1-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-171">Die aktuell für das BIOS ausgewählte Sprache.</span><span class="sxs-lookup"><span data-stu-id="299d1-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="299d1-172">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "en \| US \| ISO8859-1" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="299d1-173">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="299d1-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-176">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="299d1-176">A description of the object.</span></span> <span data-ttu-id="299d1-177">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="299d1-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-181">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="299d1-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="299d1-182">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="299d1-183">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="299d1-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-187">Ein Anzeige Name für das Element.</span><span class="sxs-lookup"><span data-stu-id="299d1-187">A display name for the element.</span></span> <span data-ttu-id="299d1-188">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="299d1-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-192">Gibt den aktuellen Zustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="299d1-192">Specifies the current health of the element.</span></span> <span data-ttu-id="299d1-193">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="299d1-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="299d1-194">Wenn ein kritischer Fehler auftritt, finden Sie im Ereignisprotokoll weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="299d1-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="299d1-195">Die **enabledstate** -Eigenschaft kann auch weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="299d1-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="299d1-196">Wenn z. b. der Speicherplatz kritisch ist, ist **healthstate** auf 25 festgelegt, der virtuelle Computer wird angehalten, und **enabledstate** wird auf 32768 (angehalten) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="299d1-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="299d1-198">Wert</span><span class="sxs-lookup"><span data-stu-id="299d1-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="299d1-199">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="299d1-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="299d1-200"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="299d1-201">Der virtuelle Computer ist voll funktionsfähig und wird in normalen Betriebsparametern und ohne Fehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="299d1-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="299d1-202"><dt>**Hauptfehler**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="299d1-203">Der virtuelle Computer hat einen schwerwiegenden Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="299d1-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="299d1-204">Dieser Wert wird verwendet, wenn auf einem oder mehreren Datenträgern, die die virtuellen Festplatten des virtuellen Computers enthalten, wenig Speicherplatz auf dem Datenträger und die virtuelle Maschine angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="299d1-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="299d1-205"><dt>**Kritischer Fehler**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="299d1-206">Das Element ist nicht funktionsfähig, und die Wiederherstellung ist möglicherweise nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="299d1-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="299d1-207">Dies kann darauf hinweisen, dass der Arbeitsprozess für den virtuellen Computer (Vmwp.exe) nicht auf Steuerungs-oder Informationsanforderungen antwortet oder dass auf einem oder mehreren Datenträgern, die die virtuellen Festplatten für die virtuelle Maschine enthalten, wenig Speicherplatz zur Neige ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="299d1-208">**Identificationcode**</span><span class="sxs-lookup"><span data-stu-id="299d1-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-211">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-212">Der Bezeichner des Herstellers für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="299d1-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="299d1-213">Häufig handelt es sich hierbei um eine Stock Keeping Unit (SKU) oder eine Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="299d1-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="299d1-214">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="299d1-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-216">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="299d1-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-218">Wird automatisch durch das BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="299d1-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="299d1-219">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="299d1-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-223">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="299d1-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="299d1-224">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="299d1-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="299d1-225">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-226">**Languageedition**</span><span class="sxs-lookup"><span data-stu-id="299d1-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-229">Qualifizierer: **maxlen** (32)</span><span class="sxs-lookup"><span data-stu-id="299d1-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-230">Die Language Edition dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="299d1-230">The language edition of this software element.</span></span> <span data-ttu-id="299d1-231">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-232">**ListOf-Sprachen**</span><span class="sxs-lookup"><span data-stu-id="299d1-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-233">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="299d1-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="299d1-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-235">Eine Liste installier barer Sprachen für das BIOS.</span><span class="sxs-lookup"><span data-stu-id="299d1-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="299d1-236">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "en \| US \| ISO8859-1" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="299d1-237">**Loadedendingaddress**</span><span class="sxs-lookup"><span data-stu-id="299d1-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-238">Datentyp: **unit64**</span><span class="sxs-lookup"><span data-stu-id="299d1-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-240">Die Endadresse des Speichers, der von diesem BIOS belegt wird.</span><span class="sxs-lookup"><span data-stu-id="299d1-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="299d1-241">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf 0xFFFFF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-242">**Loadedstartingaddress**</span><span class="sxs-lookup"><span data-stu-id="299d1-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-243">Datentyp: **unit64**</span><span class="sxs-lookup"><span data-stu-id="299d1-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-245">Die Startadresse des Speichers, der von diesem BIOS belegt wird.</span><span class="sxs-lookup"><span data-stu-id="299d1-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="299d1-246">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf 0xe0000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-247">**Loadutilityinformation**</span><span class="sxs-lookup"><span data-stu-id="299d1-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-250">Eine Zeichenfolge, die das zum Aktualisieren des BIOS-Elements erforderliche BIOS-Flash-/Auslastungs-Hilfsprogramm beschreibt.</span><span class="sxs-lookup"><span data-stu-id="299d1-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="299d1-251">Die Version und andere Informationen können in dieser Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="299d1-252">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-253">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="299d1-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-256">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="299d1-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-257">Der Hersteller dieses BIOS.</span><span class="sxs-lookup"><span data-stu-id="299d1-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="299d1-258">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "Microsoft Corporation" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="299d1-259">**Name**</span><span class="sxs-lookup"><span data-stu-id="299d1-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-262">Qualifizierer: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="299d1-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-263">Der Name, der zum Identifizieren dieses Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="299d1-263">The name used to identify this software element.</span></span> <span data-ttu-id="299d1-264">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="299d1-265">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf "BIOS" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="299d1-266">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="299d1-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-269">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="299d1-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="299d1-270">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="299d1-271">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="299d1-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-273">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="299d1-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="299d1-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-275">Ein Array, das die aktuellen Status des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="299d1-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="299d1-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="299d1-277">Der Wert bei Index NULL (0) ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="299d1-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="299d1-278">Wert</span><span class="sxs-lookup"><span data-stu-id="299d1-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="299d1-279">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="299d1-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="299d1-280"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="299d1-281">Der virtuelle Computer ist funktionsfähig und funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="299d1-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="299d1-282"><dt></dt> Heruntergestuft <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="299d1-283">Der virtuelle Computer ist nur teilweise funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="299d1-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="299d1-284">Dies gibt an, dass auf den Speicher, der die Konfiguration enthält, nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="299d1-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="299d1-285">Ein virtueller Computer in diesem Zustand kann nur ausgeschaltet oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="299d1-286"><dt>**Vorhersagefehler**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="299d1-287">Der virtuelle Computer ist funktionsfähig, kann aber in Zukunft fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="299d1-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="299d1-288">Dies deutet darauf hin, dass der Speicherplatz im Speicher, der die virtuelle Festplatte des virtuellen Computers enthält, nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="299d1-289">Der virtuelle Computer wird angehalten, wenn kein Speicherplatz mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="299d1-290"><dt></dt> <dt>10</dt> beendet</span><span class="sxs-lookup"><span data-stu-id="299d1-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="299d1-291">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="299d1-291">This value is not supported.</span></span> <span data-ttu-id="299d1-292">Wenn der virtuelle Computer beendet wird, hat die **enabledstate** -Eigenschaft den Wert 3 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="299d1-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="299d1-293"><dt>**In Dienst**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="299d1-294">Die virtuelle Maschine verarbeitet eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="299d1-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="299d1-295"><dt>**Ruhender**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="299d1-296">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="299d1-296">This value is not supported.</span></span> <span data-ttu-id="299d1-297">Wenn die virtuelle Maschine angehalten oder angehalten wird, hat die **enabledstate** -Eigenschaft den Wert 32769 (angehalten) oder 32768 (angehalten).</span><span class="sxs-lookup"><span data-stu-id="299d1-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="299d1-298">Der Wert bei Index eins (1) ist optional und enthält sekundäre Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="299d1-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="299d1-299">Ein Client sollte den primären Status von Index 0 (null) verwenden, um zu bestimmen, ob eine neue Anforderung an den virtuellen Computer ausgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="299d1-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="299d1-300">Wenn **OperationalStatus** \[ 0 \] den Wert 2 (OK) hat, kann der von **OperationalStatus** 1 festgestellte Vorgang \[ \] unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="299d1-301">Der Wert für **OperationalStatus** \[ 1 \] ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="299d1-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="299d1-302">Wert</span><span class="sxs-lookup"><span data-stu-id="299d1-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="299d1-303">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="299d1-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="299d1-304"><dt>**Erstellen der Momentaufnahme**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="299d1-305">Für den virtuellen Computer wird gerade eine Momentaufnahme erstellt.</span><span class="sxs-lookup"><span data-stu-id="299d1-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="299d1-306"><dt>**Anwenden der Momentaufnahme**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="299d1-307">Eine Momentaufnahme wird gerade auf den virtuellen Computer angewendet.</span><span class="sxs-lookup"><span data-stu-id="299d1-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="299d1-308"><dt>**Momentaufnahme**</dt> <dt>32770</dt> wird gelöscht</span><span class="sxs-lookup"><span data-stu-id="299d1-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="299d1-309">Eine Momentaufnahme wird gerade vom virtuellen Computer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="299d1-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="299d1-310"><dt>**Warten auf Start**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="299d1-311">Der virtuelle Computer wird gestartet, nachdem die automatische Startverzögerung abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="299d1-312"><dt></dt> Zusammenführen von Datenträgern <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="299d1-313">Virtuelle Festplatten aus zuvor gelöschten Momentaufnahmen werden zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="299d1-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="299d1-314"><dt>**Virtueller Computer wird exportiert**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="299d1-315">Der virtuelle Computer wird exportiert.</span><span class="sxs-lookup"><span data-stu-id="299d1-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="299d1-316"><dt>**Virtuelle Maschine**</dt> <dt>32774</dt> wird migriert.</span><span class="sxs-lookup"><span data-stu-id="299d1-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="299d1-317">Der virtuelle Computer wird Live von einem physischen Computer zu einem anderen migriert.</span><span class="sxs-lookup"><span data-stu-id="299d1-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="299d1-318">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="299d1-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-321">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-322">Der Hersteller und das Betriebssystem für ein Softwareelement, wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 (Sonstiges) aufweist, was erfordert, dass die **OtherTargetOS** -Eigenschaft einen nicht-**null** -Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="299d1-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="299d1-323">Für alle anderen Werte von **TargetOperatingSystem** muss die **OtherTargetOS** -Eigenschaft **null** sein.</span><span class="sxs-lookup"><span data-stu-id="299d1-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="299d1-324">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-325">**Primarybios**</span><span class="sxs-lookup"><span data-stu-id="299d1-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-326">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="299d1-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-328">True gibt an, dass dies das primäre BIOS des Computer Systems ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="299d1-329">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-330">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="299d1-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-331">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-333">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="299d1-333">Provides high level status information.</span></span> <span data-ttu-id="299d1-334">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="299d1-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="299d1-335">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="299d1-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="299d1-336">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-337">**Registryuris**</span><span class="sxs-lookup"><span data-stu-id="299d1-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-338">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="299d1-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="299d1-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-340">Ein Array von Zeichen folgen, das den Veröffentlichungs Speicherort der BIOS-Attribut Registrierung oder Registrierungen darstellt, denen die Implementierung entspricht.</span><span class="sxs-lookup"><span data-stu-id="299d1-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="299d1-341">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-342">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="299d1-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-343">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="299d1-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-345">Das Datum, an dem das BIOS freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="299d1-345">The date that the BIOS was released.</span></span> <span data-ttu-id="299d1-346">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-347">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="299d1-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-350">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-351">Die zugewiesene Seriennummer des BIOS.</span><span class="sxs-lookup"><span data-stu-id="299d1-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="299d1-352">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-353">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="299d1-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-354">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-356">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="299d1-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-357">Ein Bezeichner für das Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="299d1-357">An identifier for the software element.</span></span> <span data-ttu-id="299d1-358">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf "Microsoft:*GUID* \\ *gerätespezifische Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="299d1-359">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="299d1-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-360">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-362">Der Status des Lebenszyklus eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="299d1-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="299d1-363">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf 2 (ausführbare Datei) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-364">**Status**</span><span class="sxs-lookup"><span data-stu-id="299d1-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-367">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="299d1-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="299d1-368">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="299d1-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-369">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="299d1-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="299d1-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-371">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="299d1-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="299d1-372">Ein Array, das Zeichen folgen enthält, die die entsprechenden **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="299d1-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="299d1-373">Wenn z. b. 11 (in Service) der Wert ist, der **OperationalStatus** \[ 0 zugewiesen ist \] , enthält **Statusbeschreibungen** \[ 0 \] möglicherweise eine Erläuterung, warum der virtuelle Computer eine Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="299d1-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="299d1-374">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="299d1-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-375">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="299d1-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-376">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="299d1-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="299d1-378">Die Betriebssystemumgebung des-Elements.</span><span class="sxs-lookup"><span data-stu-id="299d1-378">The element's operating system environment.</span></span> <span data-ttu-id="299d1-379">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf 0 (unbekannt) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="299d1-380">**Version**</span><span class="sxs-lookup"><span data-stu-id="299d1-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="299d1-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="299d1-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="299d1-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="299d1-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="299d1-383">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="299d1-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="299d1-384">Die BIOS-Version.</span><span class="sxs-lookup"><span data-stu-id="299d1-384">The version of the BIOS.</span></span> <span data-ttu-id="299d1-385">Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "8.02.00" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299d1-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="299d1-386">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="299d1-386">Remarks</span></span>

<span data-ttu-id="299d1-387">Der Zugriff auf die **MSVM-Klasse " \_ bioselements** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="299d1-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="299d1-388">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="299d1-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="299d1-389">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="299d1-389">Requirements</span></span>



| <span data-ttu-id="299d1-390">Anforderung</span><span class="sxs-lookup"><span data-stu-id="299d1-390">Requirement</span></span> | <span data-ttu-id="299d1-391">Wert</span><span class="sxs-lookup"><span data-stu-id="299d1-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299d1-392">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="299d1-392">Minimum supported client</span></span><br/> | <span data-ttu-id="299d1-393">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="299d1-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="299d1-394">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="299d1-394">Minimum supported server</span></span><br/> | <span data-ttu-id="299d1-395">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="299d1-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="299d1-396">Namespace</span><span class="sxs-lookup"><span data-stu-id="299d1-396">Namespace</span></span><br/>                | <span data-ttu-id="299d1-397">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="299d1-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="299d1-398">MOF</span><span class="sxs-lookup"><span data-stu-id="299d1-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="299d1-399"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="299d1-400">DLL</span><span class="sxs-lookup"><span data-stu-id="299d1-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="299d1-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="299d1-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="299d1-402">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="299d1-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299d1-403">**CIM- \_ bioselare**</span><span class="sxs-lookup"><span data-stu-id="299d1-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="299d1-404">BIOS-Klassen</span><span class="sxs-lookup"><span data-stu-id="299d1-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="299d1-405">**CIM- \_ bioselare**</span><span class="sxs-lookup"><span data-stu-id="299d1-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

