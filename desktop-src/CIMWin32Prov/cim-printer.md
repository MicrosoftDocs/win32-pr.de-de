---
description: Die CIM \_ -Drucker Klasse stellt die Funktionen und die Verwaltung des logischen Drucker Geräts dar.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: CIM_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127657"
---
# <a name="cim_printer-class"></a><span data-ttu-id="111b0-103">CIM- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="111b0-103">CIM\_Printer class</span></span>

<span data-ttu-id="111b0-104">Die **CIM- \_ Drucker** Klasse stellt die Funktionen und die Verwaltung des logischen Drucker Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="111b0-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="111b0-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="111b0-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="111b0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="111b0-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="111b0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="111b0-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="111b0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="111b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="111b0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="111b0-110">Member</span><span class="sxs-lookup"><span data-stu-id="111b0-110">Members</span></span>

<span data-ttu-id="111b0-111">Die **CIM- \_ Drucker** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="111b0-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="111b0-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="111b0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="111b0-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="111b0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="111b0-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="111b0-114">Methods</span></span>

<span data-ttu-id="111b0-115">Die **CIM- \_ Drucker** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="111b0-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="111b0-116">Methode</span><span class="sxs-lookup"><span data-stu-id="111b0-116">Method</span></span>                                                             | <span data-ttu-id="111b0-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="111b0-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111b0-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="111b0-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="111b0-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="111b0-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="111b0-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="111b0-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="111b0-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="111b0-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="111b0-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="111b0-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="111b0-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="111b0-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="111b0-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="111b0-124">Properties</span></span>

<span data-ttu-id="111b0-125">Die **CIM- \_ Drucker** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="111b0-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="111b0-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="111b0-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="111b0-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="111b0-130">Availability and status of the device.</span></span>

<span data-ttu-id="111b0-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="111b0-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-135">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="111b0-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="111b0-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="111b0-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="111b0-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="111b0-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="111b0-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="111b0-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="111b0-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="111b0-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="111b0-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="111b0-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="111b0-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-146">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="111b0-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="111b0-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-148">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="111b0-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="111b0-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="111b0-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-150">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="111b0-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="111b0-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-153">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="111b0-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="111b0-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-155">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="111b0-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="111b0-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-157">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="111b0-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="111b0-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-159">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="111b0-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="111b0-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="111b0-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-161">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="111b0-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-162">**Availablejobsheets**</span><span class="sxs-lookup"><span data-stu-id="111b0-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-163">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-165">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Requirements djobsheets")</span><span class="sxs-lookup"><span data-stu-id="111b0-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-166">Beschreibt alle Auftrags Blätter, die auf dem Drucker verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="111b0-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="111b0-167">Dies kann auch verwendet werden, um das Banner zu beschreiben, das ein Drucker am Anfang jedes Auftrags bereitstellen kann, oder andere vom Benutzer angegebene Optionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="111b0-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-168">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="111b0-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-169">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="111b0-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-171">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**". Capabilitybeschreibungen "," CIM \_ PrintJob. Finish "," CIM \_ printservice. Funktionalitäten ")</span><span class="sxs-lookup"><span data-stu-id="111b0-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-172">Druckerfunktionen.</span><span class="sxs-lookup"><span data-stu-id="111b0-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="111b0-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="111b0-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Druck** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="111b0-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="111b0-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="111b0-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Heften (6** )</span><span class="sxs-lookup"><span data-stu-id="111b0-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="111b0-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenz Druck** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="111b0-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punsch** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="111b0-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Abdeckung** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="111b0-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="111b0-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-und weiß Druck** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="111b0-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Eine Seite** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-186">Einseitige</span><span class="sxs-lookup"><span data-stu-id="111b0-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="111b0-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-188">Zweiseitiger langer Rand</span><span class="sxs-lookup"><span data-stu-id="111b0-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="111b0-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiges kurzes Edge** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-190">Zweiseitiger kurzer Rand</span><span class="sxs-lookup"><span data-stu-id="111b0-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="111b0-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>Hoch **Format (15** )</span><span class="sxs-lookup"><span data-stu-id="111b0-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="111b0-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Quer** Format (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="111b0-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes** Hochformat (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="111b0-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrtes quer** Format (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="111b0-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Hohe Qualität** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-196">Hohe Qualität</span><span class="sxs-lookup"><span data-stu-id="111b0-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="111b0-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality normal** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-198">Qualität normal</span><span class="sxs-lookup"><span data-stu-id="111b0-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="111b0-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)</span><span class="sxs-lookup"><span data-stu-id="111b0-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-200">Qualität niedrig</span><span class="sxs-lookup"><span data-stu-id="111b0-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-201">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="111b0-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-202">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-204">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="111b0-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-205">Freiform-Zeichen folgen, die ausführliche Erläuterungen **zu den im Funktions Array angegebenen** Drucker Features bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="111b0-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="111b0-206">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="111b0-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="111b0-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="111b0-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-210">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="111b0-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-211">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="111b0-211">Short textual description of the object.</span></span>

<span data-ttu-id="111b0-212">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-213">**Char* unterstützt*\*</span><span class="sxs-lookup"><span data-stu-id="111b0-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-214">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-216">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Charset"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| -Drucker-MIB. prtlocalizationcharakterisezeichensatz ")</span><span class="sxs-lookup"><span data-stu-id="111b0-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-217">Verfügbare Zeichensätze für die Ausgabe von Text, der sich auf die Verwaltung des Druckers bezieht.</span><span class="sxs-lookup"><span data-stu-id="111b0-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="111b0-218">Die in dieser Eigenschaft bereitgestellten Zeichen folgen sollten der Semantik und Syntax entsprechen, die von Abschnitt 4.1.2 ("charset-Parameter") in RFC 2046 (MIME-Teil 2) und in der IANA-Zeichensatz Registrierung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="111b0-219">Beispiele hierfür sind "UTF-8", "US-ASCII" und "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="111b0-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="111b0-220">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="111b0-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-221">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-223">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="111b0-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-224">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="111b0-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="111b0-225">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="111b0-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="111b0-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="111b0-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-228">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="111b0-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="111b0-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="111b0-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="111b0-230">(1)</span><span class="sxs-lookup"><span data-stu-id="111b0-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-231">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="111b0-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="111b0-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="111b0-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="111b0-233">(2)</span><span class="sxs-lookup"><span data-stu-id="111b0-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="111b0-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="111b0-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="111b0-235">(3)</span><span class="sxs-lookup"><span data-stu-id="111b0-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-236">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="111b0-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="111b0-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="111b0-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="111b0-238">(4)</span><span class="sxs-lookup"><span data-stu-id="111b0-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-239">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="111b0-239">Device is not working properly.</span></span> <span data-ttu-id="111b0-240">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="111b0-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="111b0-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="111b0-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="111b0-242">(5)</span><span class="sxs-lookup"><span data-stu-id="111b0-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-243">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="111b0-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="111b0-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="111b0-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="111b0-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-246">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="111b0-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="111b0-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="111b0-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="111b0-248">(7)</span><span class="sxs-lookup"><span data-stu-id="111b0-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="111b0-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="111b0-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="111b0-250">(8)</span><span class="sxs-lookup"><span data-stu-id="111b0-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-251">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="111b0-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="111b0-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="111b0-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="111b0-253">(9)</span><span class="sxs-lookup"><span data-stu-id="111b0-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-254">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="111b0-254">Device is not working properly.</span></span> <span data-ttu-id="111b0-255">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="111b0-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="111b0-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="111b0-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="111b0-257">(10)</span><span class="sxs-lookup"><span data-stu-id="111b0-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-258">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="111b0-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="111b0-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="111b0-260">(11)</span><span class="sxs-lookup"><span data-stu-id="111b0-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-261">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="111b0-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="111b0-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="111b0-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="111b0-263">(12)</span><span class="sxs-lookup"><span data-stu-id="111b0-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-264">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="111b0-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="111b0-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="111b0-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="111b0-266">(13)</span><span class="sxs-lookup"><span data-stu-id="111b0-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-267">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="111b0-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="111b0-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="111b0-269">(14)</span><span class="sxs-lookup"><span data-stu-id="111b0-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-270">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="111b0-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="111b0-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="111b0-272">(15)</span><span class="sxs-lookup"><span data-stu-id="111b0-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-273">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="111b0-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="111b0-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="111b0-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="111b0-275">(16)</span><span class="sxs-lookup"><span data-stu-id="111b0-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-276">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="111b0-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="111b0-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="111b0-278">(17)</span><span class="sxs-lookup"><span data-stu-id="111b0-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-279">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="111b0-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="111b0-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="111b0-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="111b0-281">(18)</span><span class="sxs-lookup"><span data-stu-id="111b0-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-282">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="111b0-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="111b0-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="111b0-284">(19)</span><span class="sxs-lookup"><span data-stu-id="111b0-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="111b0-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="111b0-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="111b0-286">(20)</span><span class="sxs-lookup"><span data-stu-id="111b0-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-287">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="111b0-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="111b0-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="111b0-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="111b0-289">(21)</span><span class="sxs-lookup"><span data-stu-id="111b0-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-290">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="111b0-290">System failure.</span></span> <span data-ttu-id="111b0-291">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="111b0-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="111b0-292">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="111b0-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="111b0-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="111b0-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="111b0-294">(22)</span><span class="sxs-lookup"><span data-stu-id="111b0-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-295">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="111b0-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="111b0-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="111b0-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="111b0-297">(23)</span><span class="sxs-lookup"><span data-stu-id="111b0-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-298">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="111b0-298">System failure.</span></span> <span data-ttu-id="111b0-299">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="111b0-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="111b0-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="111b0-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="111b0-301">(24)</span><span class="sxs-lookup"><span data-stu-id="111b0-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-302">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="111b0-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="111b0-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="111b0-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="111b0-304">(25)</span><span class="sxs-lookup"><span data-stu-id="111b0-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-305">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="111b0-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="111b0-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="111b0-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="111b0-307">(26)</span><span class="sxs-lookup"><span data-stu-id="111b0-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-308">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="111b0-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="111b0-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="111b0-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="111b0-310">(27)</span><span class="sxs-lookup"><span data-stu-id="111b0-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-311">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="111b0-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="111b0-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="111b0-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="111b0-313">(28)</span><span class="sxs-lookup"><span data-stu-id="111b0-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-314">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="111b0-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="111b0-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="111b0-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="111b0-316">(29)</span><span class="sxs-lookup"><span data-stu-id="111b0-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-317">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="111b0-317">Device is disabled.</span></span> <span data-ttu-id="111b0-318">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="111b0-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="111b0-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="111b0-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="111b0-320">(30)</span><span class="sxs-lookup"><span data-stu-id="111b0-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-321">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="111b0-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="111b0-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="111b0-323">31,5</span><span class="sxs-lookup"><span data-stu-id="111b0-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-324">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="111b0-324">Device is not working properly.</span></span> <span data-ttu-id="111b0-325">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-326">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="111b0-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-327">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="111b0-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-329">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="111b0-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-330">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="111b0-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="111b0-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-332">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="111b0-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-335">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="111b0-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="111b0-336">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="111b0-337">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="111b0-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-339">**Currentfunktionalitäten**</span><span class="sxs-lookup"><span data-stu-id="111b0-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-340">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="111b0-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-342">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="111b0-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-343">Finisen und andere Funktionen des Druckers, die zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="111b0-344">Jeder Eintrag in dieser Eigenschaft sollte auch im **Funktions Array aufgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="111b0-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="111b0-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Druck** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="111b0-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="111b0-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="111b0-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Heften (6** )</span><span class="sxs-lookup"><span data-stu-id="111b0-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="111b0-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenz Druck** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="111b0-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punsch** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="111b0-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Abdeckung** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="111b0-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="111b0-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-und weiß Druck** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="111b0-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Eine Seite** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-358">Einseitige</span><span class="sxs-lookup"><span data-stu-id="111b0-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="111b0-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-360">Zweiseitiger langer Rand</span><span class="sxs-lookup"><span data-stu-id="111b0-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="111b0-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiges kurzes Edge** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-362">Zweiseitiger kurzer Rand</span><span class="sxs-lookup"><span data-stu-id="111b0-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="111b0-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>Hoch **Format (15** )</span><span class="sxs-lookup"><span data-stu-id="111b0-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="111b0-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Quer** Format (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="111b0-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes** Hochformat (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="111b0-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrtes quer** Format (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="111b0-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Hohe Qualität** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-368">Hohe Qualität</span><span class="sxs-lookup"><span data-stu-id="111b0-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="111b0-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality normal** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-370">Qualität normal</span><span class="sxs-lookup"><span data-stu-id="111b0-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="111b0-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)</span><span class="sxs-lookup"><span data-stu-id="111b0-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-372">Qualität niedrig</span><span class="sxs-lookup"><span data-stu-id="111b0-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-373">**Currentcharset**</span><span class="sxs-lookup"><span data-stu-id="111b0-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-376">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".\**Char* unterstützt\*\*")</span><span class="sxs-lookup"><span data-stu-id="111b0-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-377">Aktueller Zeichensatz, der für die Ausgabe von Text im Zusammenhang mit der Verwaltung des Druckers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="111b0-378">Der von dieser Eigenschaft beschriebene Zeichensatz sollte auch in der Eigenschaft **charsetsupported** aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="111b0-379">Die durch diese Eigenschaft angegebene Zeichenfolge sollte der Semantik und Syntax entsprechen, die durch Abschnitt 4.1.2 ("charset-Parameter") in RFC 2046 (MIME-Teil 2) und in der IANA-Zeichensatz Registrierung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="111b0-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="111b0-380">Beispiele hierfür sind "UTF-8", "US-ASCII" und "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="111b0-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="111b0-381">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="111b0-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-382">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-384">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**". LanguagesSupported "," CIM \_ Printer. currentmimetype ")</span><span class="sxs-lookup"><span data-stu-id="111b0-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-385">Aktuell verwendete Druckersprache; die Sprache sollte auch in der **LanguagesSupported** -Eigenschaft aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-386">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-387">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="111b0-388">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="111b0-389">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="111b0-390">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="111b0-391">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="111b0-392">**Psprinter** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="111b0-393">**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="111b0-394">**Ppds** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="111b0-395">**Escapep** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="111b0-396">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="111b0-397">**Ddif** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="111b0-398">**InterPress** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="111b0-399">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="111b0-400">**Zeilendaten** (15)</span><span class="sxs-lookup"><span data-stu-id="111b0-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="111b0-401">**Modca** (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="111b0-402">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="111b0-403">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="111b0-404">**Spdl** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="111b0-405">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="111b0-406">Physischer **(21** )</span><span class="sxs-lookup"><span data-stu-id="111b0-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="111b0-407">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="111b0-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="111b0-408">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="111b0-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="111b0-409">**Dscdse** (24)</span><span class="sxs-lookup"><span data-stu-id="111b0-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="111b0-410">**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="111b0-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="111b0-411">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="111b0-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="111b0-412">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="111b0-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="111b0-413">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="111b0-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="111b0-414">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="111b0-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="111b0-415">**Decppl** (30)</span><span class="sxs-lookup"><span data-stu-id="111b0-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="111b0-416">**Einfacher Text** (31)</span><span class="sxs-lookup"><span data-stu-id="111b0-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="111b0-417">**Npap** (32)</span><span class="sxs-lookup"><span data-stu-id="111b0-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="111b0-418">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="111b0-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="111b0-419">**beeindrucken** (34)</span><span class="sxs-lookup"><span data-stu-id="111b0-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="111b0-420">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="111b0-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="111b0-421">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="111b0-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="111b0-422">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="111b0-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="111b0-423">**Automatisch** (38)</span><span class="sxs-lookup"><span data-stu-id="111b0-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="111b0-424">**Seiten** (39)</span><span class="sxs-lookup"><span data-stu-id="111b0-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="111b0-425">**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="111b0-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="111b0-426">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="111b0-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="111b0-427">**Diagnose** (42)</span><span class="sxs-lookup"><span data-stu-id="111b0-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="111b0-428">**CAPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="111b0-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="111b0-429">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="111b0-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="111b0-430">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="111b0-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="111b0-431">**XEs** (46)</span><span class="sxs-lookup"><span data-stu-id="111b0-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="111b0-432">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="111b0-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-433">**Currentmimetype**</span><span class="sxs-lookup"><span data-stu-id="111b0-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-436">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="111b0-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-437">Der MIME-Typ wird derzeit vom Drucker verwendet, wenn die **CurrentLanguage** -Eigenschaft auf festgelegt ist, um anzugeben, dass ein MIME-Typ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-438">**Currentnaturallanguage**</span><span class="sxs-lookup"><span data-stu-id="111b0-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-441">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**Naturallanguagessupported**")</span><span class="sxs-lookup"><span data-stu-id="111b0-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-442">Aktuelle Sprache, die vom Drucker für die Verwaltung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="111b0-443">Die hier aufgeführte Sprache sollte auch in **naturallanguagessupported** aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-444">**Currentpapertype**</span><span class="sxs-lookup"><span data-stu-id="111b0-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-447">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**Taschen typesavailable**")</span><span class="sxs-lookup"><span data-stu-id="111b0-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-448">Papiertyp, der derzeit vom Drucker verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="111b0-449">Die Zeichenfolge sollte in dem Format ausgedrückt werden, das von der ISO/IEC 10175-Dokument Druckanwendung (dpa) angegeben wird. diese wird auch in Anhang C von RFC 1759 (Drucker-MIB) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="111b0-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-450">**Default-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="111b0-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-451">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="111b0-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-453">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="111b0-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-454">Standardmäßige finisen und andere Funktionen des Druckers.</span><span class="sxs-lookup"><span data-stu-id="111b0-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="111b0-455">Jeder Eintrag in dieser Eigenschaft sollte auch im **Funktions Array aufgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="111b0-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="111b0-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Druck** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="111b0-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="111b0-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="111b0-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Heften (6** )</span><span class="sxs-lookup"><span data-stu-id="111b0-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="111b0-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenz Druck** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="111b0-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punsch** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="111b0-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Abdeckung** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="111b0-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="111b0-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-und weiß Druck** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="111b0-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Eine Seite** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-469">Einseitige</span><span class="sxs-lookup"><span data-stu-id="111b0-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="111b0-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-471">Zweiseitiger langer Rand</span><span class="sxs-lookup"><span data-stu-id="111b0-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="111b0-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiges kurzes Edge** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-473">Zweiseitiger kurzer Rand</span><span class="sxs-lookup"><span data-stu-id="111b0-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="111b0-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>Hoch **Format (15** )</span><span class="sxs-lookup"><span data-stu-id="111b0-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="111b0-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Quer** Format (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="111b0-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes** Hochformat (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="111b0-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrtes quer** Format (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="111b0-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Hohe Qualität** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-479">Hohe Qualität</span><span class="sxs-lookup"><span data-stu-id="111b0-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="111b0-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality normal** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-481">Qualität normal</span><span class="sxs-lookup"><span data-stu-id="111b0-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="111b0-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)</span><span class="sxs-lookup"><span data-stu-id="111b0-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-483">Qualität niedrig</span><span class="sxs-lookup"><span data-stu-id="111b0-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-484">**Defaultkopien**</span><span class="sxs-lookup"><span data-stu-id="111b0-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-485">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-487">Die Anzahl der Kopien, die von einem einzelnen Auftrag erzeugt werden, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="111b0-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="111b0-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-489">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-490">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-491">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**". LanguagesSupported "," CIM \_ Printer. defaultmimetype ")</span><span class="sxs-lookup"><span data-stu-id="111b0-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-492">Standarddrucker Sprache.</span><span class="sxs-lookup"><span data-stu-id="111b0-492">Default printer language.</span></span> <span data-ttu-id="111b0-493">Die Sprache sollte auch in der **LanguagesSupported** -Eigenschaft aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-494">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-495">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="111b0-496">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="111b0-497">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="111b0-498">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="111b0-499">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="111b0-500">**Psprinter** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="111b0-501">**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="111b0-502">**Ppds** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="111b0-503">**Escapep** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="111b0-504">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="111b0-505">**Ddif** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="111b0-506">**InterPress** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="111b0-507">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="111b0-508">**Zeilendaten** (15)</span><span class="sxs-lookup"><span data-stu-id="111b0-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="111b0-509">**Modca** (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="111b0-510">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="111b0-511">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="111b0-512">**Spdl** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="111b0-513">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="111b0-514">Physischer **(21** )</span><span class="sxs-lookup"><span data-stu-id="111b0-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="111b0-515">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="111b0-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="111b0-516">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="111b0-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="111b0-517">**Dscdse** (24)</span><span class="sxs-lookup"><span data-stu-id="111b0-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="111b0-518">**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="111b0-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="111b0-519">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="111b0-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="111b0-520">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="111b0-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="111b0-521">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="111b0-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="111b0-522">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="111b0-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="111b0-523">**Decppl** (30)</span><span class="sxs-lookup"><span data-stu-id="111b0-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="111b0-524">**Einfacher Text** (31)</span><span class="sxs-lookup"><span data-stu-id="111b0-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="111b0-525">**Npap** (32)</span><span class="sxs-lookup"><span data-stu-id="111b0-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="111b0-526">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="111b0-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="111b0-527">**beeindrucken** (34)</span><span class="sxs-lookup"><span data-stu-id="111b0-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="111b0-528">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="111b0-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="111b0-529">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="111b0-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="111b0-530">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="111b0-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="111b0-531">**Automatisch** (38)</span><span class="sxs-lookup"><span data-stu-id="111b0-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="111b0-532">**Seiten** (39)</span><span class="sxs-lookup"><span data-stu-id="111b0-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="111b0-533">**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="111b0-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="111b0-534">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="111b0-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="111b0-535">**Diagnose** (42)</span><span class="sxs-lookup"><span data-stu-id="111b0-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="111b0-536">**CAPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="111b0-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="111b0-537">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="111b0-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="111b0-538">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="111b0-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="111b0-539">**XEs** (46)</span><span class="sxs-lookup"><span data-stu-id="111b0-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="111b0-540">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="111b0-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-541">**Defaultmimetype**</span><span class="sxs-lookup"><span data-stu-id="111b0-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-542">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-543">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-544">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="111b0-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-545">Standard-MIME-Typ, der vom Drucker verwendet wird, wenn die **defaultLanguage** -Eigenschaft festgelegt ist, um anzugeben, dass ein MIME-Typ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-546">**Defaultnummerieren**</span><span class="sxs-lookup"><span data-stu-id="111b0-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-547">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-549">Die Anzahl der Seiten für den Druckdaten Strom, die der Drucker auf einem einzelnen Medien Blatt rendern soll, es sei denn, ein Auftrag ist anderweitig angegeben.</span><span class="sxs-lookup"><span data-stu-id="111b0-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-550">**Defaultpapertype**</span><span class="sxs-lookup"><span data-stu-id="111b0-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-551">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-552">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-553">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**Taschen typesavailable**")</span><span class="sxs-lookup"><span data-stu-id="111b0-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-554">Papiertyp, den der Drucker verwendet, wenn PrintJob keinen bestimmten Typ angibt.</span><span class="sxs-lookup"><span data-stu-id="111b0-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="111b0-555">Die Zeichenfolge sollte in dem Format ausgedrückt werden, das von der ISO/IEC 10175-Dokument Druckanwendung (dpa) angegeben wird. diese wird auch in Anhang C von RFC 1759 (Drucker-MIB) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="111b0-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-556">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="111b0-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-557">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-558">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-559">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="111b0-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-560">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="111b0-560">Textual description of the object.</span></span>

<span data-ttu-id="111b0-561">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-562">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="111b0-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-563">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-564">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-565">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**ErrorInformation**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. IETF \| -Drucker-MIB. hrprinterdetectederrorstate ")</span><span class="sxs-lookup"><span data-stu-id="111b0-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-566">Drucker Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="111b0-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-567">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-568">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="111b0-569">**Kein Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="111b0-570">**Niedriges Papier** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="111b0-571">**Kein Papier** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="111b0-572">**Niedriger Toner** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="111b0-573">**Kein Toner** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="111b0-574">**Tür geöffnet** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="111b0-575">**Jammed** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="111b0-576">**Offline** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="111b0-577">**Angeforderter Dienst** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="111b0-578">**Ausgabe bin voll** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-579">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="111b0-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-580">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-581">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-582">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="111b0-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="111b0-583">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="111b0-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="111b0-584">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-585">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="111b0-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-586">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="111b0-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-587">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-588">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="111b0-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="111b0-589">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="111b0-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-591">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-592">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-593">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="111b0-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="111b0-594">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-595">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="111b0-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-596">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-597">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="111b0-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="111b0-598">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**".**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="111b0-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-599">Array, das zusätzliche Informationen für den aktuellen Fehlerstatus bereitstellt, die in der **DetectedErrorState** -Eigenschaft angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="111b0-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="111b0-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-601">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-602">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-603">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel pro Zoll")</span><span class="sxs-lookup"><span data-stu-id="111b0-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-604">Horizontale Auflösung in Pixel pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="111b0-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="111b0-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-606">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="111b0-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-607">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-608">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="111b0-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-609">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="111b0-609">Date and time the object was installed.</span></span> <span data-ttu-id="111b0-610">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="111b0-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="111b0-611">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-612">**Jobzählset**</span><span class="sxs-lookup"><span data-stu-id="111b0-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-613">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-614">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-615">Qualifizierer: **Counter**</span><span class="sxs-lookup"><span data-stu-id="111b0-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="111b0-616">Drucker Aufträge, die seit der letzten zurück Setzung verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="111b0-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="111b0-617">Diese Aufträge können von einer oder mehreren Druck Warteschlangen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-618">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="111b0-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-619">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="111b0-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-620">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-621">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| -Drucker-MIB. prtinterpreterlangfamily ") [**, modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**". Mimetypessupported "," CIM \_ PrintJob. language "," CIM \_ printservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="111b0-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-622">Druck Sprachen, die nativ unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-623">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-624">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="111b0-625">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="111b0-626">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="111b0-627">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="111b0-628">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="111b0-629">**Psprinter** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="111b0-630">**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="111b0-631">**Ppds** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="111b0-632">**Escapep** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="111b0-633">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="111b0-634">**Ddif** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="111b0-635">**InterPress** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="111b0-636">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="111b0-637">**Zeilendaten** (15)</span><span class="sxs-lookup"><span data-stu-id="111b0-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="111b0-638">**Modca** (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="111b0-639">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="111b0-640">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="111b0-641">**Spdl** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="111b0-642">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="111b0-643">Physischer **(21** )</span><span class="sxs-lookup"><span data-stu-id="111b0-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="111b0-644">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="111b0-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="111b0-645">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="111b0-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="111b0-646">**Dscdse** (24)</span><span class="sxs-lookup"><span data-stu-id="111b0-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="111b0-647">**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="111b0-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="111b0-648">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="111b0-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="111b0-649">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="111b0-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="111b0-650">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="111b0-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="111b0-651">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="111b0-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="111b0-652">**Decppl** (30)</span><span class="sxs-lookup"><span data-stu-id="111b0-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="111b0-653">**Einfacher Text** (31)</span><span class="sxs-lookup"><span data-stu-id="111b0-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="111b0-654">**Npap** (32)</span><span class="sxs-lookup"><span data-stu-id="111b0-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="111b0-655">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="111b0-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="111b0-656">**beeindrucken** (34)</span><span class="sxs-lookup"><span data-stu-id="111b0-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="111b0-657">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="111b0-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="111b0-658">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="111b0-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="111b0-659">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="111b0-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="111b0-660">**Automatisch** (38)</span><span class="sxs-lookup"><span data-stu-id="111b0-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="111b0-661">**Seiten** (39)</span><span class="sxs-lookup"><span data-stu-id="111b0-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="111b0-662">**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="111b0-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="111b0-663">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="111b0-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="111b0-664">**Diagnose** (42)</span><span class="sxs-lookup"><span data-stu-id="111b0-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="111b0-665">**CAPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="111b0-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="111b0-666">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="111b0-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="111b0-667">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="111b0-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="111b0-668">**XEs** (46)</span><span class="sxs-lookup"><span data-stu-id="111b0-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="111b0-669">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="111b0-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="111b0-670">**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="111b0-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="111b0-671">**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="111b0-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="111b0-672">**Pclxl** (50)</span><span class="sxs-lookup"><span data-stu-id="111b0-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-673">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="111b0-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-674">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-675">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-676">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="111b0-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="111b0-677">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-678">**Markingtechnology**</span><span class="sxs-lookup"><span data-stu-id="111b0-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-679">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-680">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-681">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| -Drucker-MIB. prtmarkermarktech ")</span><span class="sxs-lookup"><span data-stu-id="111b0-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-682">Markierte Technologie, die vom Drucker verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-683">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-684">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="111b0-685">**Elektrophotoled** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="111b0-686">**Elektrofotolaser** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="111b0-687">**Anderes elektrophotographic** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="111b0-688">**Auswirkung verschiebenden Head-Punkt Matrix 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="111b0-689">Auswirkung der Verschieb **enden Kopf Punkt Matrix 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="111b0-690">Auswirkung der Verschieb **enden Hauptpunkt Matrix** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="111b0-691">Auswirkung der Verschiebungs **Kopfzeile vollständig geformt** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="111b0-692">**Auswirkungs Band** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="111b0-693">**Sonstige Auswirkung** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="111b0-694">**Inkjet-Aqueous** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="111b0-695">**Vollstrahl-Solid** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="111b0-696">**Anderes Inkjet** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="111b0-697">**Stift** (15)</span><span class="sxs-lookup"><span data-stu-id="111b0-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="111b0-698">**Thermische Übertragung** (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="111b0-699">**Thermische sensible** (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="111b0-700">**Thermische Diffusion** (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="111b0-701">**Anderes thermisches** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="111b0-702">**Elektroerosion** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="111b0-703">**Elektrostatisch** (21)</span><span class="sxs-lookup"><span data-stu-id="111b0-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="111b0-704">**Fotomikrofiche** (22)</span><span class="sxs-lookup"><span data-stu-id="111b0-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="111b0-705">**Fotografische imagesesse** (23)</span><span class="sxs-lookup"><span data-stu-id="111b0-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="111b0-706">**Anderes Foto** (24)</span><span class="sxs-lookup"><span data-stu-id="111b0-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="111b0-707">**Ionen Ablage** (25)</span><span class="sxs-lookup"><span data-stu-id="111b0-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="111b0-708">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="111b0-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="111b0-709">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="111b0-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-710">**Maxkopien**</span><span class="sxs-lookup"><span data-stu-id="111b0-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-711">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-712">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-713">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Kopien")</span><span class="sxs-lookup"><span data-stu-id="111b0-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-714">Maximale Anzahl von Kopien, die vom Drucker aus einem einzelnen Auftrag erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="111b0-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-715">**Maximal zulässige Anzahl**</span><span class="sxs-lookup"><span data-stu-id="111b0-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-716">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-717">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-718">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. numup")</span><span class="sxs-lookup"><span data-stu-id="111b0-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-719">Maximale Anzahl von Druckdaten Strom Seiten, die der Drucker auf einem einzelnen Medien Blatt darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="111b0-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-720">**Maxsizesupportiert**</span><span class="sxs-lookup"><span data-stu-id="111b0-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-721">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-722">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-723">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. JobSize"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="111b0-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-724">Der größte Auftrag (als Bytestream), den der Drucker in Kilobyte-Einheiten akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="111b0-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="111b0-725">Der Wert 0 (null) gibt an, dass keine Begrenzung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="111b0-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-726">**Mimetypessupported**</span><span class="sxs-lookup"><span data-stu-id="111b0-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-727">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-728">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-729">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Drucker**". LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ printservice. mimetypessupported ")</span><span class="sxs-lookup"><span data-stu-id="111b0-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-730">Freiform-Zeichen folgen, die ausführliche Erläuterungen zu MIME-Typen bereitstellen, die vom Drucker unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="111b0-731">Wenn für diese Eigenschaft Daten bereitgestellt werden, sollte der Wert 47 ("MIME") in der **LanguagesSupported** -Eigenschaft enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="111b0-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-732">**Name**</span><span class="sxs-lookup"><span data-stu-id="111b0-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-733">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-734">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-735">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="111b0-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-736">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="111b0-736">Label by which the object is known.</span></span> <span data-ttu-id="111b0-737">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="111b0-738">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-739">**Naturallanguagessupported**</span><span class="sxs-lookup"><span data-stu-id="111b0-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-740">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-741">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-742">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| -Drucker-MIB. prtlocalizationlanguage ") [**, modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="111b0-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-743">Verfügbare Sprachen für Zeichen folgen, die vom Drucker für die Ausgabe der Verwaltungsinformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="111b0-744">Die Zeichen folgen sollten RFC 1766 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="111b0-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="111b0-745">Beispielsweise wird "en" für Englisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="111b0-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-746">**Unterstützt unterstützt**</span><span class="sxs-lookup"><span data-stu-id="111b0-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-747">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="111b0-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-748">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-749">Unterstützte Dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="111b0-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-750">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-751">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="111b0-752">**A** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="111b0-753">**B** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="111b0-754">**C** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="111b0-755">**D** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="111b0-756">**E** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="111b0-757">**Buchstabe** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="111b0-758">**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="111b0-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="111b0-759">**Na-10x13-Umschlag** (9)</span><span class="sxs-lookup"><span data-stu-id="111b0-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="111b0-760">**Na-9x12-Umschlag** (10)</span><span class="sxs-lookup"><span data-stu-id="111b0-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="111b0-761">**Na-Number-10-Umschlag** (11)</span><span class="sxs-lookup"><span data-stu-id="111b0-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="111b0-762">**Na-7x9-Umschlag** (12)</span><span class="sxs-lookup"><span data-stu-id="111b0-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="111b0-763">**Na-9x11-Umschlag** (13)</span><span class="sxs-lookup"><span data-stu-id="111b0-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="111b0-764">**Na-10x14-Umschlag** (14)</span><span class="sxs-lookup"><span data-stu-id="111b0-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="111b0-765">**Na-Number-9-Umschlag** (15)</span><span class="sxs-lookup"><span data-stu-id="111b0-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="111b0-766">**Na-6x9-Umschlag** (16)</span><span class="sxs-lookup"><span data-stu-id="111b0-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="111b0-767">**Na-10x15-Umschlag** (17)</span><span class="sxs-lookup"><span data-stu-id="111b0-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="111b0-768">**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="111b0-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="111b0-769">**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="111b0-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="111b0-770">**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="111b0-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="111b0-771">**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="111b0-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="111b0-772">**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="111b0-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="111b0-773">**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="111b0-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="111b0-774">**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="111b0-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="111b0-775">**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="111b0-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="111b0-776">**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="111b0-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="111b0-777">**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="111b0-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="111b0-778">**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="111b0-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="111b0-779">**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="111b0-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="111b0-780">**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="111b0-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="111b0-781">**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="111b0-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="111b0-782">**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="111b0-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="111b0-783">**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="111b0-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="111b0-784">**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="111b0-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="111b0-785">**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="111b0-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="111b0-786">**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="111b0-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="111b0-787">**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="111b0-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="111b0-788">**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="111b0-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="111b0-789">**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="111b0-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="111b0-790">**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="111b0-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="111b0-791">**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="111b0-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="111b0-792">**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="111b0-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="111b0-793">**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="111b0-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="111b0-794">**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="111b0-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="111b0-795">**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="111b0-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="111b0-796">**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="111b0-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="111b0-797">**ISO-bestimmt** (47)</span><span class="sxs-lookup"><span data-stu-id="111b0-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="111b0-798">**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="111b0-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="111b0-799">**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="111b0-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="111b0-800">**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="111b0-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="111b0-801">**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="111b0-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="111b0-802">**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="111b0-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="111b0-803">**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="111b0-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="111b0-804">**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="111b0-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="111b0-805">**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="111b0-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="111b0-806">**JIS-B8** (56)</span><span class="sxs-lookup"><span data-stu-id="111b0-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="111b0-807">**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="111b0-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="111b0-808">**JIS-B10** (58)</span><span class="sxs-lookup"><span data-stu-id="111b0-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="111b0-809">**Na-Buchstabe** (59)</span><span class="sxs-lookup"><span data-stu-id="111b0-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="111b0-810">**Na-legal** (60)</span><span class="sxs-lookup"><span data-stu-id="111b0-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="111b0-811">**B4-Umschlag** (61)</span><span class="sxs-lookup"><span data-stu-id="111b0-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="111b0-812">**B5-Umschlag** (62)</span><span class="sxs-lookup"><span data-stu-id="111b0-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="111b0-813">**C3-Umschlag** (63)</span><span class="sxs-lookup"><span data-stu-id="111b0-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="111b0-814">**C4-Umschlag** (64)</span><span class="sxs-lookup"><span data-stu-id="111b0-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="111b0-815">**C5-Umschlag** (65)</span><span class="sxs-lookup"><span data-stu-id="111b0-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="111b0-816">**C6-Umschlag** (66)</span><span class="sxs-lookup"><span data-stu-id="111b0-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="111b0-817">Festgelegt **-langer Umschlag** (67)</span><span class="sxs-lookup"><span data-stu-id="111b0-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="111b0-818">**Monarch-Umschlag** (68)</span><span class="sxs-lookup"><span data-stu-id="111b0-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="111b0-819">**Executive** (69)</span><span class="sxs-lookup"><span data-stu-id="111b0-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="111b0-820">**Folien** (70)</span><span class="sxs-lookup"><span data-stu-id="111b0-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="111b0-821">**Rechnung** (71)</span><span class="sxs-lookup"><span data-stu-id="111b0-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="111b0-822">**Ledger** (72)</span><span class="sxs-lookup"><span data-stu-id="111b0-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="111b0-823">**Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="111b0-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-824">**Taschenbuch verfügbar**</span><span class="sxs-lookup"><span data-stu-id="111b0-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-825">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="111b0-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-826">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-827">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Requirements dtaschen Type", "CIM \_ printservice. papertypesavailable"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| -Drucker-MIB. prtinputmedianame ")</span><span class="sxs-lookup"><span data-stu-id="111b0-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-828">Freiform-Zeichen folgen, die die Papiertypen angeben, die derzeit für den Drucker verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="111b0-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="111b0-829">Jede Zeichenfolge sollte in dem Format ausgedrückt werden, das von der ISO/IEC 10175-Dokument Druckanwendung (dpa) angegeben wird. diese wird auch in Anhang C von RFC 1759 (Drucker-MIB) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="111b0-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="111b0-830">Beispiele für gültige Zeichen folgen sind "ISO-A4-farbige" und "na-10x14-Envelope".</span><span class="sxs-lookup"><span data-stu-id="111b0-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="111b0-831">Definitionsgemäß sollte ein Papierformat, das verfügbar ist und in der Eigenschaft **Taschen typesavailable** aufgeführt ist, auch in der Eigenschaft " **tabpersizessupported** " angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="111b0-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-833">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-834">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-835">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="111b0-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-836">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="111b0-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="111b0-837">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="111b0-838">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="111b0-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="111b0-839">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="111b0-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-840">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="111b0-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="111b0-841">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-842">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="111b0-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="111b0-843">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="111b0-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="111b0-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="111b0-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="111b0-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-848">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="111b0-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="111b0-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-850">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="111b0-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="111b0-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-852">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="111b0-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="111b0-853">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="111b0-854">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="111b0-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="111b0-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-856">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="111b0-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="111b0-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="111b0-858">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="111b0-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-859">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="111b0-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-860">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="111b0-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-861">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-862">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="111b0-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="111b0-863">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="111b0-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="111b0-864">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="111b0-865">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="111b0-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="111b0-866">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-867">**Printerstatus**</span><span class="sxs-lookup"><span data-stu-id="111b0-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-868">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-869">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-870">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| -Drucker-MIB. hrprinterstatus ")</span><span class="sxs-lookup"><span data-stu-id="111b0-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-871">Status Informationen, die nicht in der **Availability** -Eigenschaft angegeben sind, für einen Drucker.</span><span class="sxs-lookup"><span data-stu-id="111b0-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-872">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-873">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="111b0-874">Im **Leerlauf** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="111b0-875">**Drucken** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="111b0-876">**Aufwärm** Dauer (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="111b0-877">**Druck beendet** (6)</span><span class="sxs-lookup"><span data-stu-id="111b0-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="111b0-878">**Offline** (7)</span><span class="sxs-lookup"><span data-stu-id="111b0-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-879">**Status**</span><span class="sxs-lookup"><span data-stu-id="111b0-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-880">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-881">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-882">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="111b0-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-883">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="111b0-883">Current status of the object.</span></span> <span data-ttu-id="111b0-884">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="111b0-885">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="111b0-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="111b0-886">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="111b0-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="111b0-887">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="111b0-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="111b0-888">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="111b0-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-889">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="111b0-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="111b0-890">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="111b0-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="111b0-891">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="111b0-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="111b0-892">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="111b0-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="111b0-893">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="111b0-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="111b0-894">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="111b0-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="111b0-895">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="111b0-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="111b0-896">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="111b0-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="111b0-897">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="111b0-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="111b0-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-899">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="111b0-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-900">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-901">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="111b0-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-902">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="111b0-902">State of the logical device.</span></span> <span data-ttu-id="111b0-903">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="111b0-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="111b0-904">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="111b0-905">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="111b0-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="111b0-906">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="111b0-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="111b0-907">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="111b0-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="111b0-908">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="111b0-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="111b0-909">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="111b0-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="111b0-910">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="111b0-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-911">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-912">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-913">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="111b0-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="111b0-914">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="111b0-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="111b0-915">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-916">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="111b0-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-917">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="111b0-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-918">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-919">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="111b0-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="111b0-920">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="111b0-920">Scoping system's name.</span></span>

<span data-ttu-id="111b0-921">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="111b0-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="111b0-922">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="111b0-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-923">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="111b0-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-924">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="111b0-925">Zeitpunkt der letzten Drucker Zurücksetzung.</span><span class="sxs-lookup"><span data-stu-id="111b0-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="111b0-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="111b0-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="111b0-927">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="111b0-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="111b0-928">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="111b0-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="111b0-929">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel pro Zoll")</span><span class="sxs-lookup"><span data-stu-id="111b0-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="111b0-930">Vertikale Auflösung in Pixel pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="111b0-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="111b0-931">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="111b0-931">Remarks</span></span>

<span data-ttu-id="111b0-932">Die **CIM- \_ Drucker** Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="111b0-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="111b0-933">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="111b0-933">WMI does not implement this class.</span></span> <span data-ttu-id="111b0-934">Informationen zu WMI, die vom **CIM- \_ Drucker** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="111b0-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="111b0-935">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="111b0-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="111b0-936">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="111b0-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="111b0-937">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="111b0-937">Requirements</span></span>



| <span data-ttu-id="111b0-938">Anforderung</span><span class="sxs-lookup"><span data-stu-id="111b0-938">Requirement</span></span> | <span data-ttu-id="111b0-939">Wert</span><span class="sxs-lookup"><span data-stu-id="111b0-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="111b0-940">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="111b0-940">Minimum supported client</span></span><br/> | <span data-ttu-id="111b0-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="111b0-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="111b0-942">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="111b0-942">Minimum supported server</span></span><br/> | <span data-ttu-id="111b0-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="111b0-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="111b0-944">Namespace</span><span class="sxs-lookup"><span data-stu-id="111b0-944">Namespace</span></span><br/>                | <span data-ttu-id="111b0-945">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="111b0-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="111b0-946">MOF</span><span class="sxs-lookup"><span data-stu-id="111b0-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="111b0-947"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="111b0-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="111b0-948">DLL</span><span class="sxs-lookup"><span data-stu-id="111b0-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="111b0-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="111b0-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="111b0-950">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="111b0-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111b0-951">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="111b0-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

