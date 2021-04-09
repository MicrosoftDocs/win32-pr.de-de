---
description: Beschreibt die primäre Zeichen Oberfläche auf einem Anzeige Controller.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Msvm_VideoHead-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130320"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="9f45f-103">MSVM- \_ videoheadklasse</span><span class="sxs-lookup"><span data-stu-id="9f45f-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="9f45f-104">Beschreibt die primäre Zeichen Oberfläche auf einem Anzeige Controller.</span><span class="sxs-lookup"><span data-stu-id="9f45f-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="9f45f-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f45f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f45f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f45f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="9f45f-107">Member</span><span class="sxs-lookup"><span data-stu-id="9f45f-107">Members</span></span>

<span data-ttu-id="9f45f-108">Die **MSVM- \_ videoheadklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9f45f-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="9f45f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="9f45f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f45f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f45f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f45f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9f45f-111">Methods</span></span>

<span data-ttu-id="9f45f-112">Die **MSVM- \_ videohead** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9f45f-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="9f45f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="9f45f-113">Method</span></span>                                                          | <span data-ttu-id="9f45f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f45f-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9f45f-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="9f45f-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="9f45f-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9f45f-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="9f45f-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="9f45f-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9f45f-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="9f45f-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="9f45f-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9f45f-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9f45f-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="9f45f-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="9f45f-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9f45f-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="9f45f-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="9f45f-124">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="9f45f-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9f45f-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="9f45f-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="9f45f-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9f45f-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="9f45f-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="9f45f-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9f45f-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9f45f-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="9f45f-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f45f-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f45f-131">Properties</span></span>

<span data-ttu-id="9f45f-132">Die **MSVM- \_ videohead** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f45f-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f45f-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="9f45f-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-136">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="9f45f-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="9f45f-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="9f45f-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-141">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-141">The primary availability and status of the device.</span></span> <span data-ttu-id="9f45f-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="9f45f-143">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-143">Value</span></span>                                                                        | <span data-ttu-id="9f45f-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f45f-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9f45f-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="9f45f-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9f45f-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9f45f-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="9f45f-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="9f45f-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9f45f-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9f45f-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-155">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-155">A short description of the object.</span></span> <span data-ttu-id="9f45f-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-157">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="9f45f-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-160">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="9f45f-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9f45f-161">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9f45f-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9f45f-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9f45f-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="9f45f-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9f45f-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="9f45f-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="9f45f-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9f45f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9f45f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9f45f-170">)</span><span class="sxs-lookup"><span data-stu-id="9f45f-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f45f-171">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9f45f-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-174">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f45f-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9f45f-175">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-176">**Currentbitsperpixel**</span><span class="sxs-lookup"><span data-stu-id="9f45f-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-179">Qualifizierer: **Einheiten** ("Bits")</span><span class="sxs-lookup"><span data-stu-id="9f45f-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-180">Die Anzahl der Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f45f-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="9f45f-181">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-182">**Ereignis Auflösung**</span><span class="sxs-lookup"><span data-stu-id="9f45f-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-185">Qualifizierer: **Einheiten** ("Pixel")</span><span class="sxs-lookup"><span data-stu-id="9f45f-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-186">Die aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="9f45f-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="9f45f-187">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-188">**Currentzahlofcolors**</span><span class="sxs-lookup"><span data-stu-id="9f45f-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-189">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f45f-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-191">Die Anzahl von Farben, die in den aktuellen Auflösungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9f45f-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="9f45f-192">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-193">**Currentzahlofcolumns**</span><span class="sxs-lookup"><span data-stu-id="9f45f-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-194">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-196">Im Zeichenmodus die Anzahl der Spalten für diesen Anzeige Controller.</span><span class="sxs-lookup"><span data-stu-id="9f45f-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="9f45f-197">Andernfalls ist es 0.</span><span class="sxs-lookup"><span data-stu-id="9f45f-197">Otherwise, 0.</span></span> <span data-ttu-id="9f45f-198">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-199">**Currentnumofrows**</span><span class="sxs-lookup"><span data-stu-id="9f45f-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-200">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-202">Im Zeichenmodus die Anzahl der Zeilen für diesen Videocontroller.</span><span class="sxs-lookup"><span data-stu-id="9f45f-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="9f45f-203">Andernfalls ist es 0.</span><span class="sxs-lookup"><span data-stu-id="9f45f-203">Otherwise, 0.</span></span> <span data-ttu-id="9f45f-204">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-205">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="9f45f-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-206">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-208">Qualifizierer: **Einheiten** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="9f45f-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-209">Die aktuelle Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="9f45f-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="9f45f-210">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-211">**Currentscanmode**</span><span class="sxs-lookup"><span data-stu-id="9f45f-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-214">Der aktuelle Scanmodus.</span><span class="sxs-lookup"><span data-stu-id="9f45f-214">The current scan mode.</span></span> <span data-ttu-id="9f45f-215">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9f45f-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9f45f-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9f45f-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="9f45f-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Nicht-Interlacing-Vorgang** (3)</span><span class="sxs-lookup"><span data-stu-id="9f45f-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>Zeilen Sprung **Vorgang** (4)</span><span class="sxs-lookup"><span data-stu-id="9f45f-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f45f-221">**Currentverticalresolution**</span><span class="sxs-lookup"><span data-stu-id="9f45f-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-222">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-224">Qualifizierer: **Einheiten** ("Pixel")</span><span class="sxs-lookup"><span data-stu-id="9f45f-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-225">Die aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="9f45f-225">The current number of vertical pixels.</span></span> <span data-ttu-id="9f45f-226">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-227">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f45f-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-230">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-230">A description of the object.</span></span> <span data-ttu-id="9f45f-231">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9f45f-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-233">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-235">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="9f45f-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9f45f-236">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9f45f-237">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9f45f-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="9f45f-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="9f45f-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="9f45f-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="9f45f-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="9f45f-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="9f45f-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9f45f-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9f45f-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9f45f-246">)</span><span class="sxs-lookup"><span data-stu-id="9f45f-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f45f-247">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f45f-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-250">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ Head \\ *Index*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9f45f-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-254">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-254">A display name for the object.</span></span> <span data-ttu-id="9f45f-255">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-256">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="9f45f-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-259">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="9f45f-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9f45f-260">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="9f45f-261">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-261">Value</span></span>                                                                        | <span data-ttu-id="9f45f-262">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f45f-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9f45f-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9f45f-264">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="9f45f-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="9f45f-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9f45f-266">Disabled</span><span class="sxs-lookup"><span data-stu-id="9f45f-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9f45f-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9f45f-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-270">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="9f45f-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9f45f-271">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="9f45f-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9f45f-272">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9f45f-273">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-273">Value</span></span>                                                                        | <span data-ttu-id="9f45f-274">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f45f-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9f45f-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9f45f-276">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="9f45f-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="9f45f-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9f45f-278">Disabled</span><span class="sxs-lookup"><span data-stu-id="9f45f-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9f45f-279">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="9f45f-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-280">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-282">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9f45f-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="9f45f-283">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9f45f-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-287">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9f45f-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="9f45f-288">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9f45f-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-290">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-292">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="9f45f-292">The current health of the element.</span></span> <span data-ttu-id="9f45f-293">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9f45f-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9f45f-294">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9f45f-295">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="9f45f-296">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-296">Value</span></span>                                                                        | <span data-ttu-id="9f45f-297">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f45f-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="9f45f-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="9f45f-299">OK</span><span class="sxs-lookup"><span data-stu-id="9f45f-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9f45f-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9f45f-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-301">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-303">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9f45f-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="9f45f-304">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9f45f-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-306">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9f45f-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-308">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="9f45f-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9f45f-309">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f45f-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-313">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9f45f-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-314">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9f45f-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9f45f-315">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9f45f-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-317">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-319">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9f45f-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="9f45f-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-321">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="9f45f-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-322">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f45f-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-324">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-324">This property has been deprecated.</span></span> <span data-ttu-id="9f45f-325">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-326">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="9f45f-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-327">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-329">Qualifizierer: **Einheiten** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="9f45f-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-330">Die maximale Aktualisierungsrate des Anzeige Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="9f45f-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="9f45f-331">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-332">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="9f45f-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-333">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f45f-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-335">Qualifizierer: **Einheiten** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="9f45f-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-336">Die minimale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="9f45f-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="9f45f-337">Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-338">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f45f-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-339">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-341">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-341">The label by which the object is known.</span></span> <span data-ttu-id="9f45f-342">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9f45f-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-343">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="9f45f-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-346">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9f45f-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9f45f-347">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9f45f-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9f45f-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9f45f-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="9f45f-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="9f45f-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="9f45f-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="9f45f-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="9f45f-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="9f45f-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="9f45f-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="9f45f-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="9f45f-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="9f45f-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="9f45f-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="9f45f-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="9f45f-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="9f45f-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="9f45f-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="9f45f-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9f45f-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9f45f-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9f45f-368">)</span><span class="sxs-lookup"><span data-stu-id="9f45f-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f45f-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9f45f-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-370">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-372">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-372">The current statuses of the object.</span></span> <span data-ttu-id="9f45f-373">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-374">**Othercurrentscanmode**</span><span class="sxs-lookup"><span data-stu-id="9f45f-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-375">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-377">Der aktuelle Scanmodus, wenn die **currentscanmode** -Eigenschaft der Instanz 1 (Other) ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="9f45f-378">Diese Eigenschaft wird von [**CIM \_ videohead**](/previous-versions//cc136948(v=vs.85)) geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-379">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="9f45f-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-380">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-382">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9f45f-383">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9f45f-384">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9f45f-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-386">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-388">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="9f45f-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9f45f-389">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-390">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="9f45f-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-391">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-393">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-393">The power management capabilities of the device.</span></span> <span data-ttu-id="9f45f-394">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-395">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="9f45f-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-396">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-398">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9f45f-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9f45f-399">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-400">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="9f45f-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-401">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f45f-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-403">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="9f45f-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="9f45f-404">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-405">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="9f45f-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-406">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-408">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="9f45f-408">Provides high level status information.</span></span> <span data-ttu-id="9f45f-409">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9f45f-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9f45f-410">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9f45f-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9f45f-411">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9f45f-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9f45f-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9f45f-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="9f45f-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="9f45f-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9f45f-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="9f45f-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9f45f-418">)</span><span class="sxs-lookup"><span data-stu-id="9f45f-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f45f-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9f45f-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-420">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-422">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="9f45f-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="9f45f-423">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9f45f-424">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9f45f-425">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-425">Value</span></span>                                                                         | <span data-ttu-id="9f45f-426">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f45f-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9f45f-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9f45f-428">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9f45f-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9f45f-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="9f45f-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-432">Eine Zeichenfolge, die den aktuellen Status des-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="9f45f-433">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-434">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="9f45f-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-435">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9f45f-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-437">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f45f-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9f45f-438">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9f45f-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-440">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-442">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f45f-442">The current state of the logical device.</span></span> <span data-ttu-id="9f45f-443">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-444">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="9f45f-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-447">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="9f45f-447">The scoping system's creation class name.</span></span> <span data-ttu-id="9f45f-448">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-449">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="9f45f-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-450">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f45f-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-452">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="9f45f-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="9f45f-453">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-454">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="9f45f-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-455">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9f45f-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-457">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f45f-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9f45f-458">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-459">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="9f45f-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-460">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f45f-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-461">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-462">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="9f45f-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9f45f-463">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f45f-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f45f-464">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="9f45f-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f45f-465">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f45f-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f45f-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f45f-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f45f-467">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="9f45f-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9f45f-468">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f45f-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9f45f-469">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-469">Value</span></span>                                                                         | <span data-ttu-id="9f45f-470">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f45f-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9f45f-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9f45f-472">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9f45f-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f45f-473">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f45f-473">Remarks</span></span>

<span data-ttu-id="9f45f-474">Der Zugriff auf die **MSVM- \_ videoheadklasse** kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="9f45f-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9f45f-475">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9f45f-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f45f-476">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f45f-476">Requirements</span></span>



| <span data-ttu-id="9f45f-477">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f45f-477">Requirement</span></span> | <span data-ttu-id="9f45f-478">Wert</span><span class="sxs-lookup"><span data-stu-id="9f45f-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f45f-479">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f45f-479">Minimum supported client</span></span><br/> | <span data-ttu-id="9f45f-480">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f45f-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9f45f-481">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f45f-481">Minimum supported server</span></span><br/> | <span data-ttu-id="9f45f-482">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f45f-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f45f-483">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f45f-483">Namespace</span></span><br/>                | <span data-ttu-id="9f45f-484">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f45f-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f45f-485">MOF</span><span class="sxs-lookup"><span data-stu-id="9f45f-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f45f-486"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f45f-487">DLL</span><span class="sxs-lookup"><span data-stu-id="9f45f-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f45f-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f45f-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f45f-489">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f45f-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f45f-490">**CIM- \_ videohead**</span><span class="sxs-lookup"><span data-stu-id="9f45f-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="9f45f-491">[**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f45f-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9f45f-492">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="9f45f-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

