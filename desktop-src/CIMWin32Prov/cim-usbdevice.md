---
description: Die CIM- \_ Klasse "-Klasse" stellt die Verwaltungsmerkmale eines USB-Geräts dar.
ms.assetid: 0ff39701-826a-434b-a628-0af586600a80
ms.tgt_platform: multiple
title: CIM_USBDevice-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.Availability
- CIM_USBDevice.Caption
- CIM_USBDevice.ClassCode
- CIM_USBDevice.ConfigManagerErrorCode
- CIM_USBDevice.ConfigManagerUserConfig
- CIM_USBDevice.CreationClassName
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.Description
- CIM_USBDevice.DeviceID
- CIM_USBDevice.ErrorCleared
- CIM_USBDevice.ErrorDescription
- CIM_USBDevice.InstallDate
- CIM_USBDevice.LastErrorCode
- CIM_USBDevice.Name
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.PNPDeviceID
- CIM_USBDevice.PowerManagementCapabilities
- CIM_USBDevice.PowerManagementSupported
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.Status
- CIM_USBDevice.StatusInfo
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.SystemCreationClassName
- CIM_USBDevice.SystemName
- CIM_USBDevice.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21b927980716d4ee7ee2e22a352c5c3b34b363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125822"
---
# <a name="cim_usbdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="e72c7-103">CIM_USBDevice-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="e72c7-103">CIM_USBDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e72c7-104">Die **CIM \_** -Klasse "-Klasse" stellt die Verwaltungsmerkmale eines USB-Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="e72c7-104">The **CIM\_USBDevice** class represents the management characteristics of a USB device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e72c7-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e72c7-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e72c7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e72c7-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e72c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e72c7-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72c7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e72c7-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="e72c7-110">Member</span><span class="sxs-lookup"><span data-stu-id="e72c7-110">Members</span></span>

<span data-ttu-id="e72c7-111">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e72c7-111">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="e72c7-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="e72c7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e72c7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e72c7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e72c7-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="e72c7-114">Methods</span></span>

<span data-ttu-id="e72c7-115">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-115">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="e72c7-116">Methode</span><span class="sxs-lookup"><span data-stu-id="e72c7-116">Method</span></span>                                                               | <span data-ttu-id="e72c7-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e72c7-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e72c7-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e72c7-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md) | <span data-ttu-id="e72c7-119">Gibt den USB-Gerätedeskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="e72c7-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="e72c7-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="e72c7-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="e72c7-121">**Reset**</span></span>](reset-method-in-class-cim-usbdevice.md)                 | <span data-ttu-id="e72c7-122">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="e72c7-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="e72c7-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e72c7-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e72c7-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbdevice.md) | <span data-ttu-id="e72c7-125">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e72c7-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e72c7-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e72c7-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e72c7-127">Properties</span></span>

<span data-ttu-id="e72c7-128">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e72c7-128">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e72c7-129">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="e72c7-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e72c7-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="e72c7-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-133">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-133">Availability and status of the device.</span></span>

<span data-ttu-id="e72c7-134">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e72c7-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="e72c7-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e72c7-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="e72c7-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e72c7-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="e72c7-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-138">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="e72c7-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e72c7-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="e72c7-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e72c7-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="e72c7-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e72c7-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="e72c7-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e72c7-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="e72c7-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e72c7-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="e72c7-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e72c7-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="e72c7-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e72c7-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="e72c7-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e72c7-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="e72c7-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e72c7-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="e72c7-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e72c7-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="e72c7-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-149">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e72c7-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="e72c7-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-151">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e72c7-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e72c7-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="e72c7-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-153">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e72c7-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="e72c7-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e72c7-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="e72c7-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-156">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e72c7-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="e72c7-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-158">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="e72c7-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e72c7-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="e72c7-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-160">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="e72c7-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e72c7-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="e72c7-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-162">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e72c7-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="e72c7-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-164">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="e72c7-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e72c7-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e72c7-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-168">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e72c7-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-169">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-169">Short textual description of the object.</span></span>

<span data-ttu-id="e72c7-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-171">**Classcode**</span><span class="sxs-lookup"><span data-stu-id="e72c7-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-172">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e72c7-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-174">USB-Klassen Code.</span><span class="sxs-lookup"><span data-stu-id="e72c7-174">USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-175">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="e72c7-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-176">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e72c7-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-178">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e72c7-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-179">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e72c7-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e72c7-180">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e72c7-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e72c7-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="e72c7-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-183">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e72c7-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e72c7-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e72c7-185">(1)</span><span class="sxs-lookup"><span data-stu-id="e72c7-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-186">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e72c7-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e72c7-188">(2)</span><span class="sxs-lookup"><span data-stu-id="e72c7-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e72c7-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e72c7-190">(3)</span><span class="sxs-lookup"><span data-stu-id="e72c7-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-191">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e72c7-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e72c7-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e72c7-193">(4)</span><span class="sxs-lookup"><span data-stu-id="e72c7-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-194">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e72c7-194">Device is not working properly.</span></span> <span data-ttu-id="e72c7-195">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e72c7-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e72c7-197">(5)</span><span class="sxs-lookup"><span data-stu-id="e72c7-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-198">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e72c7-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e72c7-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e72c7-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="e72c7-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-201">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="e72c7-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e72c7-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e72c7-203">(7)</span><span class="sxs-lookup"><span data-stu-id="e72c7-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e72c7-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e72c7-205">(8)</span><span class="sxs-lookup"><span data-stu-id="e72c7-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-206">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e72c7-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e72c7-208">(9)</span><span class="sxs-lookup"><span data-stu-id="e72c7-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-209">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e72c7-209">Device is not working properly.</span></span> <span data-ttu-id="e72c7-210">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="e72c7-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e72c7-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e72c7-212">(10)</span><span class="sxs-lookup"><span data-stu-id="e72c7-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-213">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e72c7-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e72c7-215">(11)</span><span class="sxs-lookup"><span data-stu-id="e72c7-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-216">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="e72c7-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e72c7-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e72c7-218">(12)</span><span class="sxs-lookup"><span data-stu-id="e72c7-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-219">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e72c7-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e72c7-221">(13)</span><span class="sxs-lookup"><span data-stu-id="e72c7-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-222">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e72c7-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e72c7-224">(14)</span><span class="sxs-lookup"><span data-stu-id="e72c7-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-225">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e72c7-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e72c7-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e72c7-227">(15)</span><span class="sxs-lookup"><span data-stu-id="e72c7-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-228">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e72c7-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e72c7-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e72c7-230">(16)</span><span class="sxs-lookup"><span data-stu-id="e72c7-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-231">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e72c7-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e72c7-233">(17)</span><span class="sxs-lookup"><span data-stu-id="e72c7-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-234">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="e72c7-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e72c7-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e72c7-236">(18)</span><span class="sxs-lookup"><span data-stu-id="e72c7-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-237">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e72c7-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e72c7-239">(19)</span><span class="sxs-lookup"><span data-stu-id="e72c7-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e72c7-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e72c7-241">(20)</span><span class="sxs-lookup"><span data-stu-id="e72c7-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-242">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e72c7-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e72c7-244">(21)</span><span class="sxs-lookup"><span data-stu-id="e72c7-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-245">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="e72c7-245">System failure.</span></span> <span data-ttu-id="e72c7-246">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e72c7-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e72c7-247">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e72c7-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e72c7-249">(22)</span><span class="sxs-lookup"><span data-stu-id="e72c7-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-250">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e72c7-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e72c7-252">(23)</span><span class="sxs-lookup"><span data-stu-id="e72c7-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-253">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="e72c7-253">System failure.</span></span> <span data-ttu-id="e72c7-254">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e72c7-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e72c7-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e72c7-256">(24)</span><span class="sxs-lookup"><span data-stu-id="e72c7-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-257">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e72c7-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e72c7-259">(25)</span><span class="sxs-lookup"><span data-stu-id="e72c7-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-260">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e72c7-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e72c7-262">(26)</span><span class="sxs-lookup"><span data-stu-id="e72c7-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-263">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e72c7-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e72c7-265">(27)</span><span class="sxs-lookup"><span data-stu-id="e72c7-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-266">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e72c7-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e72c7-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e72c7-268">(28)</span><span class="sxs-lookup"><span data-stu-id="e72c7-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-269">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e72c7-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e72c7-271">(29)</span><span class="sxs-lookup"><span data-stu-id="e72c7-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-272">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-272">Device is disabled.</span></span> <span data-ttu-id="e72c7-273">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e72c7-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e72c7-275">(30)</span><span class="sxs-lookup"><span data-stu-id="e72c7-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-276">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e72c7-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e72c7-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="e72c7-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e72c7-278">31,5</span><span class="sxs-lookup"><span data-stu-id="e72c7-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-279">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e72c7-279">Device is not working properly.</span></span> <span data-ttu-id="e72c7-280">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e72c7-281">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="e72c7-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-282">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e72c7-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-284">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e72c7-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-285">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e72c7-286">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-287">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="e72c7-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-290">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e72c7-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-291">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e72c7-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e72c7-292">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e72c7-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-294">**Currentalternative esettings**</span><span class="sxs-lookup"><span data-stu-id="e72c7-294">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-295">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="e72c7-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-297">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Start **\_ Gerät**".**Currentconfigvalue**")</span><span class="sxs-lookup"><span data-stu-id="e72c7-297">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-298">Alternative USB-Einstellungen für jede Schnittstelle in der aktuell ausgewählten Konfiguration (angegeben durch die **currentconfigvalue** -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="e72c7-298">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="e72c7-299">Dieses Array enthält einen Eintrag für jede Schnittstelle in der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e72c7-299">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="e72c7-300">Wenn die **currentconfigvalue** -Eigenschaft den Wert 0 (null) aufweist, was darauf hinweist, dass das Gerät nicht konfiguriert ist, ist das Array nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-300">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="e72c7-301">Weitere Informationen zum Auswerten dieser Oktett-Zeichenfolge finden Sie in der USB-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e72c7-301">For more information about parsing this octet string, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-302">**Currentconfigvalue**</span><span class="sxs-lookup"><span data-stu-id="e72c7-302">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-303">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e72c7-303">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-305">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Start **\_ Gerät**".**Currentalternativ esettings**")</span><span class="sxs-lookup"><span data-stu-id="e72c7-305">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-306">Konfiguration, die zurzeit für das Gerät ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e72c7-306">Configuration currently selected for the device.</span></span> <span data-ttu-id="e72c7-307">Wenn der Wert 0 (null) ist, wird das Gerät nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-307">If the value is 0 (zero), the device is unconfigured.</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-308">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e72c7-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-311">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e72c7-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-312">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-312">Textual description of the object.</span></span>

<span data-ttu-id="e72c7-313">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e72c7-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-317">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e72c7-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-318">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="e72c7-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e72c7-319">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-320">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="e72c7-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-321">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e72c7-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-323">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e72c7-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e72c7-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e72c7-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-328">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="e72c7-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e72c7-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e72c7-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-331">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e72c7-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-333">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="e72c7-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-334">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-334">Date and time the object was installed.</span></span> <span data-ttu-id="e72c7-335">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e72c7-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e72c7-336">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e72c7-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-338">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e72c7-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-340">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e72c7-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e72c7-341">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-342">**Name**</span><span class="sxs-lookup"><span data-stu-id="e72c7-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-345">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e72c7-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-346">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e72c7-346">Label by which the object is known.</span></span> <span data-ttu-id="e72c7-347">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e72c7-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-349">**Anzahlungskonfigurationen**</span><span class="sxs-lookup"><span data-stu-id="e72c7-349">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-350">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e72c7-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-352">Anzahl der Geräte Konfigurationen, die für das Gerät definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e72c7-352">Number of device configurations that are defined for the device.</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-353">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e72c7-353">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-354">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-356">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e72c7-356">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-357">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-357">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e72c7-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e72c7-359">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e72c7-359">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-360">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="e72c7-360">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-361">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e72c7-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-363">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-363">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e72c7-364">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-364">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e72c7-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e72c7-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e72c7-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e72c7-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e72c7-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e72c7-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e72c7-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e72c7-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-369">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e72c7-369">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e72c7-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="e72c7-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-371">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="e72c7-371">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e72c7-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="e72c7-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-373">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e72c7-374">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-374">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e72c7-375">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e72c7-375">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e72c7-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="e72c7-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-377">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e72c7-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e72c7-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="e72c7-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e72c7-379">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e72c7-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e72c7-380">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="e72c7-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-381">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e72c7-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-383">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="e72c7-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e72c7-384">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="e72c7-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e72c7-385">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e72c7-386">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="e72c7-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e72c7-387">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-388">**Protocolcode**</span><span class="sxs-lookup"><span data-stu-id="e72c7-388">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-389">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e72c7-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-391">USB-Protokollcode.</span><span class="sxs-lookup"><span data-stu-id="e72c7-391">USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-392">**Status**</span><span class="sxs-lookup"><span data-stu-id="e72c7-392">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-393">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-395">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e72c7-395">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-396">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-396">Current status of the object.</span></span> <span data-ttu-id="e72c7-397">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-397">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e72c7-398">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="e72c7-398">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e72c7-399">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e72c7-399">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e72c7-400">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="e72c7-400">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e72c7-401">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="e72c7-401">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e72c7-402">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="e72c7-402">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e72c7-403">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e72c7-403">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e72c7-404">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="e72c7-404">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e72c7-405">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="e72c7-405">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e72c7-406">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="e72c7-406">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e72c7-407">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="e72c7-407">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e72c7-408">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="e72c7-408">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e72c7-409">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="e72c7-409">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e72c7-410">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="e72c7-410">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e72c7-411">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e72c7-411">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-412">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e72c7-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-414">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e72c7-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-415">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="e72c7-415">State of the logical device.</span></span> <span data-ttu-id="e72c7-416">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e72c7-416">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e72c7-417">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e72c7-418">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="e72c7-418">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e72c7-419">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="e72c7-419">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e72c7-420">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e72c7-420">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e72c7-421">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="e72c7-421">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e72c7-422">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="e72c7-422">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e72c7-423">**Subclasscode**</span><span class="sxs-lookup"><span data-stu-id="e72c7-423">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-424">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e72c7-424">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-426">USB-Unterklassen Code.</span><span class="sxs-lookup"><span data-stu-id="e72c7-426">USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-427">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="e72c7-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-430">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e72c7-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-431">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e72c7-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="e72c7-432">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-433">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="e72c7-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e72c7-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-436">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e72c7-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-437">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e72c7-437">Scoping system's name.</span></span>

<span data-ttu-id="e72c7-438">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e72c7-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e72c7-439">**Start Version**</span><span class="sxs-lookup"><span data-stu-id="e72c7-439">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e72c7-440">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e72c7-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e72c7-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e72c7-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e72c7-442">Neueste vom USB-Gerät Unterstützte USB-Version.</span><span class="sxs-lookup"><span data-stu-id="e72c7-442">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="e72c7-443">Diese Eigenschaft wird als Binary-Coded Decimal (BCD) ausgedrückt, wobei ein Dezimaltrennzeichen zwischen den zweiten und dritten Ziffern impliziert wird.</span><span class="sxs-lookup"><span data-stu-id="e72c7-443">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="e72c7-444">Der Wert 0x201 gibt z. b. an, dass Version 2,01 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e72c7-444">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e72c7-445">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e72c7-445">Remarks</span></span>

<span data-ttu-id="e72c7-446">Die **CIM \_** -Klasse "-Klasse" ist von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-446">The **CIM\_USBDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e72c7-447">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e72c7-447">WMI does not implement this class.</span></span> <span data-ttu-id="e72c7-448">Informationen zu WMI-Klassen, die CIM-Start **\_ Gerät** implementieren, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e72c7-448">For WMI classes that implement **CIM\_USBDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e72c7-449">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e72c7-449">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e72c7-450">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e72c7-450">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e72c7-451">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e72c7-451">Requirements</span></span>



| <span data-ttu-id="e72c7-452">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e72c7-452">Requirement</span></span> | <span data-ttu-id="e72c7-453">Wert</span><span class="sxs-lookup"><span data-stu-id="e72c7-453">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e72c7-454">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e72c7-454">Minimum supported client</span></span><br/> | <span data-ttu-id="e72c7-455">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e72c7-455">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e72c7-456">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e72c7-456">Minimum supported server</span></span><br/> | <span data-ttu-id="e72c7-457">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e72c7-457">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e72c7-458">Namespace</span><span class="sxs-lookup"><span data-stu-id="e72c7-458">Namespace</span></span><br/>                | <span data-ttu-id="e72c7-459">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e72c7-459">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e72c7-460">MOF</span><span class="sxs-lookup"><span data-stu-id="e72c7-460">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e72c7-461"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e72c7-461"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e72c7-462">DLL</span><span class="sxs-lookup"><span data-stu-id="e72c7-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e72c7-463"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e72c7-463"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e72c7-464">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e72c7-464">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72c7-465">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e72c7-465">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

