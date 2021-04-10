---
description: Die CIM \_ pointingdevice-Klasse stellt ein Gerät dar, das auf die Bereiche auf der Anzeige zeigt. Jedes Gerät, das einen Zeiger bearbeitet oder auf Bereiche in einer visuellen Anzeige zeigt, ist ein Member dieser Klasse. Beispielsweise eine Maus, einen Tablettstift, ein Touchpad oder ein Tablet.
ms.assetid: b093134a-534a-4680-8fce-d96baff26139
ms.tgt_platform: multiple
title: CIM_PointingDevice-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.Availability
- CIM_PointingDevice.Caption
- CIM_PointingDevice.ConfigManagerErrorCode
- CIM_PointingDevice.ConfigManagerUserConfig
- CIM_PointingDevice.CreationClassName
- CIM_PointingDevice.Description
- CIM_PointingDevice.DeviceID
- CIM_PointingDevice.ErrorCleared
- CIM_PointingDevice.ErrorDescription
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.InstallDate
- CIM_PointingDevice.IsLocked
- CIM_PointingDevice.LastErrorCode
- CIM_PointingDevice.Name
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.PNPDeviceID
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.PowerManagementCapabilities
- CIM_PointingDevice.PowerManagementSupported
- CIM_PointingDevice.Resolution
- CIM_PointingDevice.Status
- CIM_PointingDevice.StatusInfo
- CIM_PointingDevice.SystemCreationClassName
- CIM_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3f0a52ac11d927f5cabf171f49fee3a5febaa6a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214252"
---
# <a name="cim_pointingdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="df32f-105">CIM_PointingDevice-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="df32f-105">CIM_PointingDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="df32f-106">Die **CIM \_ pointingdevice** -Klasse stellt ein Gerät dar, das auf die Bereiche auf der Anzeige zeigt.</span><span class="sxs-lookup"><span data-stu-id="df32f-106">The **CIM\_PointingDevice** class represents a device that points to regions on the display.</span></span> <span data-ttu-id="df32f-107">Jedes Gerät, das einen Zeiger bearbeitet oder auf Bereiche in einer visuellen Anzeige zeigt, ist ein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="df32f-107">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="df32f-108">Beispielsweise eine Maus, einen Tablettstift, ein Touchpad oder ein Tablet.</span><span class="sxs-lookup"><span data-stu-id="df32f-108">For example, a mouse, stylus, touch pad, or tablet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df32f-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="df32f-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="df32f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="df32f-111">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="df32f-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="df32f-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="df32f-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="df32f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="df32f-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C535-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="df32f-114">Member</span><span class="sxs-lookup"><span data-stu-id="df32f-114">Members</span></span>

<span data-ttu-id="df32f-115">Die **CIM \_ pointingdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="df32f-115">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="df32f-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="df32f-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="df32f-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df32f-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df32f-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="df32f-118">Methods</span></span>

<span data-ttu-id="df32f-119">Die **CIM \_ pointingdevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="df32f-119">The **CIM\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="df32f-120">Methode</span><span class="sxs-lookup"><span data-stu-id="df32f-120">Method</span></span>                                                                    | <span data-ttu-id="df32f-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df32f-121">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df32f-122">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="df32f-122">**Reset**</span></span>](reset-method-in-class-cim-pointingdevice.md)                 | <span data-ttu-id="df32f-123">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="df32f-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="df32f-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="df32f-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="df32f-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="df32f-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pointingdevice.md) | <span data-ttu-id="df32f-126">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df32f-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="df32f-127">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="df32f-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df32f-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df32f-128">Properties</span></span>

<span data-ttu-id="df32f-129">Die **CIM \_ pointingdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="df32f-129">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df32f-130">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="df32f-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df32f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="df32f-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-134">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="df32f-134">Availability and status of the device.</span></span>

<span data-ttu-id="df32f-135">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df32f-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="df32f-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df32f-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="df32f-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="df32f-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="df32f-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="df32f-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="df32f-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="df32f-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="df32f-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="df32f-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="df32f-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="df32f-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="df32f-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="df32f-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="df32f-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="df32f-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="df32f-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="df32f-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="df32f-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="df32f-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="df32f-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="df32f-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="df32f-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="df32f-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="df32f-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-149">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="df32f-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="df32f-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="df32f-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-151">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="df32f-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="df32f-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="df32f-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-153">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="df32f-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="df32f-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="df32f-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="df32f-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-156">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="df32f-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="df32f-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="df32f-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-158">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="df32f-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="df32f-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="df32f-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-160">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="df32f-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="df32f-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="df32f-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-162">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="df32f-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="df32f-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="df32f-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-164">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="df32f-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="df32f-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-168">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="df32f-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-169">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="df32f-169">Short textual description of the object.</span></span>

<span data-ttu-id="df32f-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-171">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="df32f-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df32f-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-174">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="df32f-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-175">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="df32f-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="df32f-176">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="df32f-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="df32f-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="df32f-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="df32f-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-179">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="df32f-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="df32f-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="df32f-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="df32f-181">(1)</span><span class="sxs-lookup"><span data-stu-id="df32f-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-182">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="df32f-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="df32f-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="df32f-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="df32f-184">(2)</span><span class="sxs-lookup"><span data-stu-id="df32f-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="df32f-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="df32f-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="df32f-186">(3)</span><span class="sxs-lookup"><span data-stu-id="df32f-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-187">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="df32f-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="df32f-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="df32f-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="df32f-189">(4)</span><span class="sxs-lookup"><span data-stu-id="df32f-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-190">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="df32f-190">Device is not working properly.</span></span> <span data-ttu-id="df32f-191">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="df32f-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="df32f-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="df32f-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="df32f-193">(5)</span><span class="sxs-lookup"><span data-stu-id="df32f-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-194">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df32f-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="df32f-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="df32f-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="df32f-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="df32f-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-197">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="df32f-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="df32f-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="df32f-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="df32f-199">(7)</span><span class="sxs-lookup"><span data-stu-id="df32f-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="df32f-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="df32f-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="df32f-201">(8)</span><span class="sxs-lookup"><span data-stu-id="df32f-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-202">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="df32f-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="df32f-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="df32f-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="df32f-204">(9)</span><span class="sxs-lookup"><span data-stu-id="df32f-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-205">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="df32f-205">Device is not working properly.</span></span> <span data-ttu-id="df32f-206">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="df32f-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="df32f-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="df32f-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="df32f-208">(10)</span><span class="sxs-lookup"><span data-stu-id="df32f-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-209">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="df32f-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="df32f-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="df32f-211">(11)</span><span class="sxs-lookup"><span data-stu-id="df32f-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-212">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="df32f-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="df32f-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="df32f-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="df32f-214">(12)</span><span class="sxs-lookup"><span data-stu-id="df32f-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-215">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="df32f-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="df32f-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="df32f-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="df32f-217">(13)</span><span class="sxs-lookup"><span data-stu-id="df32f-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-218">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="df32f-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="df32f-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="df32f-220">(14)</span><span class="sxs-lookup"><span data-stu-id="df32f-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-221">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="df32f-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="df32f-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="df32f-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="df32f-223">(15)</span><span class="sxs-lookup"><span data-stu-id="df32f-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-224">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="df32f-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="df32f-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="df32f-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="df32f-226">(16)</span><span class="sxs-lookup"><span data-stu-id="df32f-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-227">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="df32f-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="df32f-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="df32f-229">(17)</span><span class="sxs-lookup"><span data-stu-id="df32f-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-230">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="df32f-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="df32f-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="df32f-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="df32f-232">(18)</span><span class="sxs-lookup"><span data-stu-id="df32f-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-233">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="df32f-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="df32f-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="df32f-235">(19)</span><span class="sxs-lookup"><span data-stu-id="df32f-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="df32f-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="df32f-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="df32f-237">(20)</span><span class="sxs-lookup"><span data-stu-id="df32f-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-238">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="df32f-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="df32f-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="df32f-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="df32f-240">(21)</span><span class="sxs-lookup"><span data-stu-id="df32f-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-241">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="df32f-241">System failure.</span></span> <span data-ttu-id="df32f-242">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="df32f-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="df32f-243">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="df32f-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="df32f-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="df32f-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="df32f-245">(22)</span><span class="sxs-lookup"><span data-stu-id="df32f-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-246">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="df32f-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="df32f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="df32f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="df32f-248">(23)</span><span class="sxs-lookup"><span data-stu-id="df32f-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-249">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="df32f-249">System failure.</span></span> <span data-ttu-id="df32f-250">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="df32f-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="df32f-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="df32f-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="df32f-252">(24)</span><span class="sxs-lookup"><span data-stu-id="df32f-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-253">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="df32f-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="df32f-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="df32f-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="df32f-255">(25)</span><span class="sxs-lookup"><span data-stu-id="df32f-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-256">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="df32f-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="df32f-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="df32f-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="df32f-258">(26)</span><span class="sxs-lookup"><span data-stu-id="df32f-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-259">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="df32f-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="df32f-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="df32f-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="df32f-261">(27)</span><span class="sxs-lookup"><span data-stu-id="df32f-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-262">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="df32f-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="df32f-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="df32f-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="df32f-264">(28)</span><span class="sxs-lookup"><span data-stu-id="df32f-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-265">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="df32f-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="df32f-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="df32f-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="df32f-267">(29)</span><span class="sxs-lookup"><span data-stu-id="df32f-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-268">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="df32f-268">Device is disabled.</span></span> <span data-ttu-id="df32f-269">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="df32f-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="df32f-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="df32f-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="df32f-271">(30)</span><span class="sxs-lookup"><span data-stu-id="df32f-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-272">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df32f-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="df32f-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="df32f-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="df32f-274">31,5</span><span class="sxs-lookup"><span data-stu-id="df32f-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-275">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="df32f-275">Device is not working properly.</span></span> <span data-ttu-id="df32f-276">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-277">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="df32f-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-278">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="df32f-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-280">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="df32f-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-281">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="df32f-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="df32f-282">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-283">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="df32f-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-286">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df32f-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df32f-287">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df32f-287">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="df32f-288">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-288">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="df32f-289">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-290">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df32f-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-291">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-293">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="df32f-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-294">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="df32f-294">Textual description of the object.</span></span>

<span data-ttu-id="df32f-295">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="df32f-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-299">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df32f-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df32f-300">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="df32f-300">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="df32f-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-302">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="df32f-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-303">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="df32f-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-305">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="df32f-305">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="df32f-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="df32f-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-310">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="df32f-310">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="df32f-311">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-312">**Händigkeit**</span><span class="sxs-lookup"><span data-stu-id="df32f-312">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-313">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df32f-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-315">Konfiguration des Zeige Geräts für den rechten oder linken Vorgang.</span><span class="sxs-lookup"><span data-stu-id="df32f-315">Configuration of the pointing device for right-hand or left-hand operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df32f-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="df32f-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="df32f-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (1)</span><span class="sxs-lookup"><span data-stu-id="df32f-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="df32f-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Rechter übergebenen Vorgang** (2)</span><span class="sxs-lookup"><span data-stu-id="df32f-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-319">Rechter Vorgang</span><span class="sxs-lookup"><span data-stu-id="df32f-319">Right-hand operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="df32f-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Linker Vorgang** (3)</span><span class="sxs-lookup"><span data-stu-id="df32f-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-321">Linker Vorgang</span><span class="sxs-lookup"><span data-stu-id="df32f-321">Left-hand operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="df32f-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-323">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="df32f-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-325">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="df32f-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-326">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="df32f-326">Date and time the object was installed.</span></span> <span data-ttu-id="df32f-327">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="df32f-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="df32f-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-329">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="df32f-329">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-330">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="df32f-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-332">**True** gibt an, dass das Gerät gesperrt ist und Benutzereingaben oder-Ausgaben verhindert.</span><span class="sxs-lookup"><span data-stu-id="df32f-332">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="df32f-333">Diese Eigenschaft wird von [**CIM \_ userdevice**](cim-userdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-333">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="df32f-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df32f-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-337">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="df32f-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="df32f-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-339">**Name**</span><span class="sxs-lookup"><span data-stu-id="df32f-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-342">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="df32f-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-343">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="df32f-343">Label by which the object is known.</span></span> <span data-ttu-id="df32f-344">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-344">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="df32f-345">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-345">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-346">**Anzahl von Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="df32f-346">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-347">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="df32f-347">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-349">Anzahl der Schaltflächen auf dem Zeigegerät.</span><span class="sxs-lookup"><span data-stu-id="df32f-349">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="df32f-350">Beispiel: "2"</span><span class="sxs-lookup"><span data-stu-id="df32f-350">Example: "2"</span></span>

</dd> <dt>

<span data-ttu-id="df32f-351">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="df32f-351">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-354">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="df32f-354">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-355">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="df32f-355">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="df32f-356">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="df32f-357">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="df32f-357">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="df32f-358">**Pointingtype**</span><span class="sxs-lookup"><span data-stu-id="df32f-358">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-359">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df32f-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-361">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| zeigt Gerät \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="df32f-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-362">Der Typ des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="df32f-362">Type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df32f-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="df32f-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df32f-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="df32f-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="df32f-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Maus** (3)</span><span class="sxs-lookup"><span data-stu-id="df32f-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="df32f-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Ball verfolgen** (4)</span><span class="sxs-lookup"><span data-stu-id="df32f-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-367">Trackballunterstützung</span><span class="sxs-lookup"><span data-stu-id="df32f-367">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="df32f-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>Verfolgungs **Punkt** (5)</span><span class="sxs-lookup"><span data-stu-id="df32f-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="df32f-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Gleitspunkt** (6)</span><span class="sxs-lookup"><span data-stu-id="df32f-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="df32f-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touchpad** (7)</span><span class="sxs-lookup"><span data-stu-id="df32f-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="df32f-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touchscreen** (8)</span><span class="sxs-lookup"><span data-stu-id="df32f-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="df32f-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Maus optischer Sensor** (9)</span><span class="sxs-lookup"><span data-stu-id="df32f-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-373">Optischer Sensor Sensor</span><span class="sxs-lookup"><span data-stu-id="df32f-373">Mouse   optical sensor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-374">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="df32f-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-375">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="df32f-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df32f-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-377">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="df32f-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="df32f-378">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df32f-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="df32f-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="df32f-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="df32f-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df32f-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="df32f-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df32f-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="df32f-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-383">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df32f-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="df32f-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="df32f-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-385">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="df32f-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="df32f-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="df32f-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-387">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df32f-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="df32f-388">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="df32f-389">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="df32f-389">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="df32f-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="df32f-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-391">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df32f-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="df32f-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="df32f-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="df32f-393">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df32f-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-394">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="df32f-394">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-395">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="df32f-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df32f-397">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="df32f-397">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="df32f-398">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="df32f-398">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="df32f-399">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-399">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="df32f-400">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="df32f-400">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="df32f-401">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-402">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="df32f-402">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-403">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df32f-403">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-405">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zählungen pro Zoll")</span><span class="sxs-lookup"><span data-stu-id="df32f-405">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-406">Nach Verfolgungs Auflösung.</span><span class="sxs-lookup"><span data-stu-id="df32f-406">Tracking resolution.</span></span>

<span data-ttu-id="df32f-407">Beispiel: "0"</span><span class="sxs-lookup"><span data-stu-id="df32f-407">Example: "0"</span></span>

</dd> <dt>

<span data-ttu-id="df32f-408">**Status**</span><span class="sxs-lookup"><span data-stu-id="df32f-408">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-409">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-411">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="df32f-411">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-412">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="df32f-412">Current status of the object.</span></span> <span data-ttu-id="df32f-413">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="df32f-414">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="df32f-414">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="df32f-415">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="df32f-415">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="df32f-416">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="df32f-416">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="df32f-417">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="df32f-417">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df32f-418">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="df32f-418">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="df32f-419">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="df32f-419">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="df32f-420">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="df32f-420">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="df32f-421">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="df32f-421">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="df32f-422">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="df32f-422">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="df32f-423">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="df32f-423">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="df32f-424">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="df32f-424">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="df32f-425">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="df32f-425">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="df32f-426">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="df32f-426">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-427">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="df32f-427">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-428">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df32f-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-430">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="df32f-430">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="df32f-431">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="df32f-431">State of the logical device.</span></span> <span data-ttu-id="df32f-432">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df32f-432">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="df32f-433">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df32f-434">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="df32f-434">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df32f-435">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="df32f-435">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df32f-436">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="df32f-436">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df32f-437">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="df32f-437">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="df32f-438">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="df32f-438">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df32f-439">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="df32f-439">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-440">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-442">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df32f-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df32f-443">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="df32f-443">Scoping system's creation class name.</span></span>

<span data-ttu-id="df32f-444">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df32f-445">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="df32f-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df32f-446">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df32f-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df32f-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df32f-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df32f-448">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df32f-448">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df32f-449">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="df32f-449">Scoping system's name.</span></span>

<span data-ttu-id="df32f-450">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="df32f-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df32f-451">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df32f-451">Remarks</span></span>

<span data-ttu-id="df32f-452">Die **CIM- \_ pointingdevice** -Klasse wird von [**CIM \_ userdevice**](cim-userdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="df32f-452">The **CIM\_PointingDevice** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="df32f-453">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="df32f-453">WMI does not implement this class.</span></span> <span data-ttu-id="df32f-454">Informationen zu WMI-Klassen, die von **CIM \_ pointingdevice** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df32f-454">For WMI classes derived from **CIM\_PointingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="df32f-455">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="df32f-455">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="df32f-456">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="df32f-456">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="df32f-457">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df32f-457">Requirements</span></span>



| <span data-ttu-id="df32f-458">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df32f-458">Requirement</span></span> | <span data-ttu-id="df32f-459">Wert</span><span class="sxs-lookup"><span data-stu-id="df32f-459">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df32f-460">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df32f-460">Minimum supported client</span></span><br/> | <span data-ttu-id="df32f-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df32f-461">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df32f-462">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df32f-462">Minimum supported server</span></span><br/> | <span data-ttu-id="df32f-463">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df32f-463">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df32f-464">Namespace</span><span class="sxs-lookup"><span data-stu-id="df32f-464">Namespace</span></span><br/>                | <span data-ttu-id="df32f-465">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="df32f-465">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df32f-466">MOF</span><span class="sxs-lookup"><span data-stu-id="df32f-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df32f-467"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="df32f-467"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df32f-468">DLL</span><span class="sxs-lookup"><span data-stu-id="df32f-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df32f-469"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df32f-469"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df32f-470">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df32f-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df32f-471">**CIM- \_ userdevice**</span><span class="sxs-lookup"><span data-stu-id="df32f-471">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

