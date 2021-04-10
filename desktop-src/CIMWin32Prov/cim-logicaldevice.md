---
description: Die CIM \_ LogicalDevice-Klasse stellt eine Hardware Entität dar, die in physischer Hardware erkannt werden kann oder nicht.
ms.assetid: 4f3d38ff-8080-4b53-ae29-82b68558c550
ms.tgt_platform: multiple
title: CIM_LogicalDevice-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.Caption
- CIM_LogicalDevice.Description
- CIM_LogicalDevice.InstallDate
- CIM_LogicalDevice.Name
- CIM_LogicalDevice.Status
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.ConfigManagerErrorCode
- CIM_LogicalDevice.ConfigManagerUserConfig
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.PNPDeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49974b966e1378350e8e5475ef14bb092b3aaea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126949"
---
# <a name="cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="985cb-103">CIM_LogicalDevice-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="985cb-103">CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="985cb-104">Die **CIM \_ LogicalDevice** -Klasse stellt eine Hardware Entität dar, die in physischer Hardware erkannt werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="985cb-104">The **CIM\_LogicalDevice** class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="985cb-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="985cb-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="985cb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="985cb-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="985cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="985cb-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="985cb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="985cb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="985cb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C529-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDevice : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="985cb-110">Member</span><span class="sxs-lookup"><span data-stu-id="985cb-110">Members</span></span>

<span data-ttu-id="985cb-111">Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="985cb-111">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="985cb-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="985cb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="985cb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="985cb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="985cb-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="985cb-114">Methods</span></span>

<span data-ttu-id="985cb-115">Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="985cb-115">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="985cb-116">Methode</span><span class="sxs-lookup"><span data-stu-id="985cb-116">Method</span></span>                                                                   | <span data-ttu-id="985cb-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="985cb-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="985cb-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="985cb-118">**Reset**</span></span>](reset-method-in-class-cim-logicaldevice.md)                 | <span data-ttu-id="985cb-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="985cb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="985cb-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="985cb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="985cb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="985cb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md) | <span data-ttu-id="985cb-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="985cb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="985cb-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="985cb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="985cb-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="985cb-124">Properties</span></span>

<span data-ttu-id="985cb-125">Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="985cb-125">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="985cb-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="985cb-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="985cb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="985cb-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="985cb-130">Availability and status of the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="985cb-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="985cb-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="985cb-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="985cb-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="985cb-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="985cb-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="985cb-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="985cb-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="985cb-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="985cb-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="985cb-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="985cb-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="985cb-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="985cb-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="985cb-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="985cb-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="985cb-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="985cb-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="985cb-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="985cb-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="985cb-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="985cb-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="985cb-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="985cb-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="985cb-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="985cb-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="985cb-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="985cb-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="985cb-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="985cb-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="985cb-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="985cb-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-148">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="985cb-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="985cb-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="985cb-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="985cb-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="985cb-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="985cb-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="985cb-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="985cb-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="985cb-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="985cb-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="985cb-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="985cb-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="985cb-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="985cb-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="985cb-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="985cb-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="985cb-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="985cb-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="985cb-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-163">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="985cb-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-164">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="985cb-164">A short textual description of the object.</span></span>

<span data-ttu-id="985cb-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="985cb-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="985cb-166">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="985cb-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="985cb-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-169">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="985cb-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-170">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="985cb-170">Win32 Configuration Manager error code.</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="985cb-171">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="985cb-171">**This device is working properly.**</span></span> <span data-ttu-id="985cb-172"> (0)</span><span class="sxs-lookup"><span data-stu-id="985cb-172">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="985cb-173">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="985cb-173">**This device is not configured correctly.**</span></span> <span data-ttu-id="985cb-174">(1)</span><span class="sxs-lookup"><span data-stu-id="985cb-174">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="985cb-175">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="985cb-175">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="985cb-176">(2)</span><span class="sxs-lookup"><span data-stu-id="985cb-176">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="985cb-177">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="985cb-177">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="985cb-178">(3)</span><span class="sxs-lookup"><span data-stu-id="985cb-178">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="985cb-179">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="985cb-179">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="985cb-180">(4)</span><span class="sxs-lookup"><span data-stu-id="985cb-180">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="985cb-181">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="985cb-181">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="985cb-182">(5)</span><span class="sxs-lookup"><span data-stu-id="985cb-182">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="985cb-183">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="985cb-183">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="985cb-184"> (6)</span><span class="sxs-lookup"><span data-stu-id="985cb-184">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="985cb-185">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="985cb-185">**Cannot filter.**</span></span> <span data-ttu-id="985cb-186">(7)</span><span class="sxs-lookup"><span data-stu-id="985cb-186">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="985cb-187">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="985cb-187">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="985cb-188">(8)</span><span class="sxs-lookup"><span data-stu-id="985cb-188">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="985cb-189">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="985cb-189">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="985cb-190">(9)</span><span class="sxs-lookup"><span data-stu-id="985cb-190">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="985cb-191">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="985cb-191">**This device cannot start.**</span></span> <span data-ttu-id="985cb-192">(10)</span><span class="sxs-lookup"><span data-stu-id="985cb-192">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="985cb-193">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="985cb-193">**This device failed.**</span></span> <span data-ttu-id="985cb-194">(11)</span><span class="sxs-lookup"><span data-stu-id="985cb-194">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="985cb-195">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="985cb-195">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="985cb-196">(12)</span><span class="sxs-lookup"><span data-stu-id="985cb-196">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="985cb-197">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="985cb-197">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="985cb-198">(13)</span><span class="sxs-lookup"><span data-stu-id="985cb-198">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="985cb-199">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="985cb-199">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="985cb-200">(14)</span><span class="sxs-lookup"><span data-stu-id="985cb-200">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="985cb-201">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="985cb-201">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="985cb-202">(15)</span><span class="sxs-lookup"><span data-stu-id="985cb-202">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="985cb-203">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="985cb-203">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="985cb-204">(16)</span><span class="sxs-lookup"><span data-stu-id="985cb-204">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="985cb-205">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="985cb-205">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="985cb-206">(17)</span><span class="sxs-lookup"><span data-stu-id="985cb-206">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="985cb-207">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="985cb-207">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="985cb-208">(18)</span><span class="sxs-lookup"><span data-stu-id="985cb-208">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="985cb-209">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="985cb-209">**Failure using the VxD loader.**</span></span> <span data-ttu-id="985cb-210">(19)</span><span class="sxs-lookup"><span data-stu-id="985cb-210">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="985cb-211">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="985cb-211">**Your registry might be corrupted.**</span></span> <span data-ttu-id="985cb-212">(20)</span><span class="sxs-lookup"><span data-stu-id="985cb-212">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="985cb-213">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="985cb-213">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="985cb-214">(21)</span><span class="sxs-lookup"><span data-stu-id="985cb-214">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="985cb-215">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="985cb-215">**This device is disabled.**</span></span> <span data-ttu-id="985cb-216">(22)</span><span class="sxs-lookup"><span data-stu-id="985cb-216">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="985cb-217">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="985cb-217">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="985cb-218">(23)</span><span class="sxs-lookup"><span data-stu-id="985cb-218">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="985cb-219">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="985cb-219">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="985cb-220">(24)</span><span class="sxs-lookup"><span data-stu-id="985cb-220">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="985cb-221">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="985cb-221">**Windows is still setting up this device.**</span></span> <span data-ttu-id="985cb-222">(25)</span><span class="sxs-lookup"><span data-stu-id="985cb-222">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="985cb-223">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="985cb-223">**Windows is still setting up this device.**</span></span> <span data-ttu-id="985cb-224">(26)</span><span class="sxs-lookup"><span data-stu-id="985cb-224">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="985cb-225">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="985cb-225">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="985cb-226">(27)</span><span class="sxs-lookup"><span data-stu-id="985cb-226">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="985cb-227">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="985cb-227">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="985cb-228">(28)</span><span class="sxs-lookup"><span data-stu-id="985cb-228">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="985cb-229">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="985cb-229">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="985cb-230">(29)</span><span class="sxs-lookup"><span data-stu-id="985cb-230">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="985cb-231">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="985cb-231">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="985cb-232">(30)</span><span class="sxs-lookup"><span data-stu-id="985cb-232">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="985cb-233">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="985cb-233">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="985cb-234">31,5</span><span class="sxs-lookup"><span data-stu-id="985cb-234">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="985cb-235">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="985cb-235">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-236">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="985cb-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-238">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="985cb-238">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-239">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="985cb-239">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-240">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="985cb-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-243">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="985cb-243">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="985cb-244">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="985cb-244">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="985cb-245">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-245">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-246">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="985cb-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-249">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="985cb-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-250">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="985cb-250">A textual description of the object.</span></span>

<span data-ttu-id="985cb-251">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="985cb-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="985cb-252">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="985cb-252">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-255">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="985cb-255">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="985cb-256">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="985cb-256">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-257">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="985cb-257">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-258">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="985cb-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985cb-260">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="985cb-260">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-261">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="985cb-261">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985cb-264">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="985cb-264">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="985cb-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-266">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="985cb-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-268">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="985cb-268">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-269">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="985cb-269">Indicates when the object was installed.</span></span> <span data-ttu-id="985cb-270">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="985cb-270">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="985cb-271">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="985cb-271">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="985cb-272">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="985cb-272">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="985cb-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985cb-275">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="985cb-275">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-276">**Name**</span><span class="sxs-lookup"><span data-stu-id="985cb-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-277">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-279">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="985cb-279">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-280">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="985cb-280">Label by which the object is known.</span></span> <span data-ttu-id="985cb-281">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-281">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="985cb-282">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="985cb-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="985cb-283">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="985cb-283">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-286">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="985cb-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-287">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="985cb-287">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="985cb-288">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="985cb-288">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="985cb-289">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="985cb-289">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-290">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="985cb-290">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="985cb-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985cb-292">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="985cb-292">Indicates the specific power-related capabilities of the logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="985cb-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="985cb-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-294">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="985cb-294">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="985cb-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="985cb-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-296">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="985cb-296">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="985cb-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="985cb-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-298">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="985cb-298">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="985cb-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="985cb-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-300">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="985cb-300">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="985cb-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="985cb-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-302">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="985cb-302">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="985cb-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="985cb-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-304">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="985cb-304">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="985cb-305">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-305">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="985cb-306">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="985cb-306">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="985cb-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="985cb-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-308">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="985cb-308">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="985cb-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="985cb-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="985cb-310">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="985cb-310">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="985cb-311">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="985cb-311">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="985cb-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985cb-314">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="985cb-314">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="985cb-315">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="985cb-315">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="985cb-316">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-316">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="985cb-317">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="985cb-317">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-318">**Status**</span><span class="sxs-lookup"><span data-stu-id="985cb-318">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-321">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="985cb-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-322">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="985cb-322">String that indicates the current status of the object.</span></span> <span data-ttu-id="985cb-323">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-323">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="985cb-324">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="985cb-324">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="985cb-325">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="985cb-325">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="985cb-326">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="985cb-326">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="985cb-327">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="985cb-327">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="985cb-328">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="985cb-328">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="985cb-329">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="985cb-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="985cb-330">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="985cb-330">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="985cb-331">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="985cb-331">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="985cb-332">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="985cb-332">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="985cb-333">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="985cb-333">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="985cb-334">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="985cb-334">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="985cb-335">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="985cb-335">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="985cb-336">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="985cb-336">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="985cb-337">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="985cb-337">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="985cb-338">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="985cb-338">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="985cb-339">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="985cb-339">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="985cb-340">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="985cb-340">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="985cb-341">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="985cb-341">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="985cb-342">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="985cb-342">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="985cb-343">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="985cb-343">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="985cb-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-346">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="985cb-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="985cb-347">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="985cb-347">State of the logical device.</span></span> <span data-ttu-id="985cb-348">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="985cb-348">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="985cb-349">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="985cb-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="985cb-350">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="985cb-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="985cb-351">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="985cb-351">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="985cb-352">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="985cb-352">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="985cb-353">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="985cb-353">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="985cb-354">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="985cb-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-357">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="985cb-357">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="985cb-358">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="985cb-358">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="985cb-359">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="985cb-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985cb-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="985cb-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985cb-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="985cb-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985cb-362">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="985cb-362">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="985cb-363">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="985cb-363">The scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="985cb-364">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="985cb-364">Remarks</span></span>

<span data-ttu-id="985cb-365">Merkmale logischer Geräte, die den Manage-Vorgang oder die-Konfiguration enthalten, bzw. die dem **CIM \_ LogicalDevice** -Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="985cb-365">Logical device characteristics that manage operation or configuration are contained in, or associated with, the **CIM\_LogicalDevice** object.</span></span> <span data-ttu-id="985cb-366">Die Betriebseigenschaften des Druckers sind z. b. unterstützte Papiergrößen oder erkannte Fehler.</span><span class="sxs-lookup"><span data-stu-id="985cb-366">Printer operational properties, for example, are supported paper sizes or detected errors.</span></span> <span data-ttu-id="985cb-367">Die Eigenschaften der Sensor Gerätekonfiguration sind z. b. Schwellenwert Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="985cb-367">Sensor device configuration properties, for example, are threshold settings.</span></span> <span data-ttu-id="985cb-368">Für ein logisches Gerät können verschiedene Konfigurationen vorhanden sein, die in den [**CIM- \_ Einstellungs**](cim-setting.md) Objekten enthalten sind, die mit dem logischen Gerät verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="985cb-368">Various configurations can exist for a logical device and are contained in the [**CIM\_Setting**](cim-setting.md) objects, which are associated with the logical device.</span></span>

<span data-ttu-id="985cb-369">Die **CIM \_ LogicalDevice** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="985cb-369">The **CIM\_LogicalDevice** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="985cb-370">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="985cb-370">WMI does not implement this class.</span></span> <span data-ttu-id="985cb-371">Informationen zu Klassen, die von **CIM \_ LogicalDevice** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="985cb-371">For classes derived from **CIM\_LogicalDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="985cb-372">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="985cb-372">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="985cb-373">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="985cb-373">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="985cb-374">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="985cb-374">Requirements</span></span>



| <span data-ttu-id="985cb-375">Anforderung</span><span class="sxs-lookup"><span data-stu-id="985cb-375">Requirement</span></span> | <span data-ttu-id="985cb-376">Wert</span><span class="sxs-lookup"><span data-stu-id="985cb-376">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="985cb-377">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="985cb-377">Minimum supported client</span></span><br/> | <span data-ttu-id="985cb-378">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="985cb-378">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="985cb-379">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="985cb-379">Minimum supported server</span></span><br/> | <span data-ttu-id="985cb-380">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="985cb-380">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="985cb-381">Namespace</span><span class="sxs-lookup"><span data-stu-id="985cb-381">Namespace</span></span><br/>                | <span data-ttu-id="985cb-382">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="985cb-382">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="985cb-383">MOF</span><span class="sxs-lookup"><span data-stu-id="985cb-383">MOF</span></span><br/>                      | <dl> <span data-ttu-id="985cb-384"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="985cb-384"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="985cb-385">DLL</span><span class="sxs-lookup"><span data-stu-id="985cb-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="985cb-386"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="985cb-386"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985cb-387">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="985cb-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985cb-388">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="985cb-388">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

