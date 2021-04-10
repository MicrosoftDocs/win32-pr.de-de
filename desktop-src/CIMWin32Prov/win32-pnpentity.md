---
description: Ezeigt die Eigenschaften eines Plug & Play Geräts an.
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Win32_PnPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126098"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="f1fce-103">Win32- \_ pnptity-Klasse</span><span class="sxs-lookup"><span data-stu-id="f1fce-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="f1fce-104">Die **Win32 \_ pnptity** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Eigenschaften eines Plug & Play Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="f1fce-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="f1fce-105">Plug & Play Entitäten werden als Einträge in der Device Manager in der Systemsteuerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="f1fce-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1fce-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f1fce-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1fce-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f1fce-109">Member</span><span class="sxs-lookup"><span data-stu-id="f1fce-109">Members</span></span>

<span data-ttu-id="f1fce-110">Die **Win32- \_ pnptity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f1fce-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="f1fce-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1fce-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1fce-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1fce-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1fce-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1fce-113">Methods</span></span>

<span data-ttu-id="f1fce-114">Die **Win32- \_ pnptity** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="f1fce-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f1fce-115">Method</span></span>                                                             | <span data-ttu-id="f1fce-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1fce-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1fce-117">**Ier**</span><span class="sxs-lookup"><span data-stu-id="f1fce-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="f1fce-118">Deaktiviert dieses Plug & Play Gerät.</span><span class="sxs-lookup"><span data-stu-id="f1fce-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="f1fce-119">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="f1fce-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="f1fce-120">Aktiviert dieses Plug & Play Gerät.</span><span class="sxs-lookup"><span data-stu-id="f1fce-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="f1fce-121">**Getdeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="f1fce-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="f1fce-122">Ruft die angegebenen Eigenschaften dieses Plug & Play Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="f1fce-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="f1fce-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="f1fce-123">**Reset**</span></span>                                                          | <span data-ttu-id="f1fce-124">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-124">Not implemented.</span></span> <span data-ttu-id="f1fce-125">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1fce-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="f1fce-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f1fce-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="f1fce-127">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-127">Not implemented.</span></span> <span data-ttu-id="f1fce-128">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1fce-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1fce-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1fce-129">Properties</span></span>

<span data-ttu-id="f1fce-130">Die **Win32- \_ pnptity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1fce-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1fce-131">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="f1fce-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-132">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1fce-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-134">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="f1fce-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-135">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-135">Availability and status of the device.</span></span>

<span data-ttu-id="f1fce-136">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1fce-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f1fce-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1fce-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f1fce-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f1fce-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="f1fce-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-140">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="f1fce-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f1fce-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="f1fce-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f1fce-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="f1fce-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f1fce-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="f1fce-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f1fce-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="f1fce-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f1fce-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="f1fce-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f1fce-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f1fce-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1fce-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="f1fce-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f1fce-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="f1fce-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f1fce-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="f1fce-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f1fce-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="f1fce-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-151">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f1fce-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="f1fce-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-153">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f1fce-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f1fce-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-155">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f1fce-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="f1fce-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f1fce-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="f1fce-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-158">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f1fce-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="f1fce-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-160">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="f1fce-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f1fce-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="f1fce-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-162">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="f1fce-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f1fce-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="f1fce-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-164">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f1fce-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="f1fce-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-166">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="f1fce-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1fce-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1fce-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-170">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f1fce-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-171">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-171">Short description of the object.</span></span>

<span data-ttu-id="f1fce-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-173">**Klassen-GUID**</span><span class="sxs-lookup"><span data-stu-id="f1fce-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-176">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1fce-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-177">GUID (Global Unique Identifier) dieses Plug & Play Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-178">**Compatibleid**</span><span class="sxs-lookup"><span data-stu-id="f1fce-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-179">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f1fce-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-181">Eine Hersteller definierte Identifikations Zeichenfolge, die von Setup verwendet wird, um ein Gerät mit einer INF-Datei abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="f1fce-182">Ein Gerät kann über eine Liste der zugeordneten kompatiblen IDs verfügen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="f1fce-183">Die kompatiblen IDs sollten in der Reihenfolge der absteigenden Eignung aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="f1fce-184">Wenn von Setup keine INF-Datei gefunden werden kann, die mit einer der Hardware-IDs eines Geräts übereinstimmt, werden kompatible IDs verwendet, um nach einer INF-Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="f1fce-185">Eine kompatible ID hat das gleiche Format wie eine **HardwareID**.</span><span class="sxs-lookup"><span data-stu-id="f1fce-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="f1fce-186">Weitere Informationen finden Sie unter [Windows-Treiberkit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="f1fce-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-187">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="f1fce-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-188">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1fce-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-190">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1fce-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-191">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f1fce-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f1fce-192">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f1fce-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f1fce-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="f1fce-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-195">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f1fce-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f1fce-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f1fce-197">(1)</span><span class="sxs-lookup"><span data-stu-id="f1fce-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-198">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1fce-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f1fce-200">(2)</span><span class="sxs-lookup"><span data-stu-id="f1fce-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f1fce-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f1fce-202">(3)</span><span class="sxs-lookup"><span data-stu-id="f1fce-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-203">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f1fce-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f1fce-205">(4)</span><span class="sxs-lookup"><span data-stu-id="f1fce-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-206">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f1fce-206">Device is not working properly.</span></span> <span data-ttu-id="f1fce-207">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f1fce-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f1fce-209">(5)</span><span class="sxs-lookup"><span data-stu-id="f1fce-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-210">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1fce-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f1fce-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f1fce-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="f1fce-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-213">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="f1fce-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f1fce-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f1fce-215">(7)</span><span class="sxs-lookup"><span data-stu-id="f1fce-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f1fce-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f1fce-217">(8)</span><span class="sxs-lookup"><span data-stu-id="f1fce-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-218">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f1fce-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f1fce-220">(9)</span><span class="sxs-lookup"><span data-stu-id="f1fce-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-221">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f1fce-221">Device is not working properly.</span></span> <span data-ttu-id="f1fce-222">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="f1fce-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f1fce-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f1fce-224">(10)</span><span class="sxs-lookup"><span data-stu-id="f1fce-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-225">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f1fce-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f1fce-227">(11)</span><span class="sxs-lookup"><span data-stu-id="f1fce-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-228">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="f1fce-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f1fce-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f1fce-230">(12)</span><span class="sxs-lookup"><span data-stu-id="f1fce-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-231">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f1fce-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f1fce-233">(13)</span><span class="sxs-lookup"><span data-stu-id="f1fce-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-234">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f1fce-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f1fce-236">(14)</span><span class="sxs-lookup"><span data-stu-id="f1fce-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-237">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f1fce-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f1fce-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f1fce-239">(15)</span><span class="sxs-lookup"><span data-stu-id="f1fce-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-240">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f1fce-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f1fce-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f1fce-242">(16)</span><span class="sxs-lookup"><span data-stu-id="f1fce-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-243">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f1fce-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f1fce-245">(17)</span><span class="sxs-lookup"><span data-stu-id="f1fce-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-246">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="f1fce-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1fce-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f1fce-248">(18)</span><span class="sxs-lookup"><span data-stu-id="f1fce-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-249">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f1fce-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f1fce-251">(19)</span><span class="sxs-lookup"><span data-stu-id="f1fce-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f1fce-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f1fce-253">(20)</span><span class="sxs-lookup"><span data-stu-id="f1fce-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-254">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f1fce-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f1fce-256">(21)</span><span class="sxs-lookup"><span data-stu-id="f1fce-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-257">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="f1fce-257">System failure.</span></span> <span data-ttu-id="f1fce-258">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f1fce-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f1fce-259">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f1fce-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f1fce-261">(22)</span><span class="sxs-lookup"><span data-stu-id="f1fce-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-262">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f1fce-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f1fce-264">(23)</span><span class="sxs-lookup"><span data-stu-id="f1fce-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-265">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="f1fce-265">System failure.</span></span> <span data-ttu-id="f1fce-266">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f1fce-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f1fce-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f1fce-268">(24)</span><span class="sxs-lookup"><span data-stu-id="f1fce-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-269">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f1fce-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f1fce-271">(25)</span><span class="sxs-lookup"><span data-stu-id="f1fce-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-272">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f1fce-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f1fce-274">(26)</span><span class="sxs-lookup"><span data-stu-id="f1fce-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-275">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f1fce-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f1fce-277">(27)</span><span class="sxs-lookup"><span data-stu-id="f1fce-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-278">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1fce-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f1fce-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f1fce-280">(28)</span><span class="sxs-lookup"><span data-stu-id="f1fce-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-281">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f1fce-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f1fce-283">(29)</span><span class="sxs-lookup"><span data-stu-id="f1fce-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-284">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-284">Device is disabled.</span></span> <span data-ttu-id="f1fce-285">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f1fce-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f1fce-287">(30)</span><span class="sxs-lookup"><span data-stu-id="f1fce-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-288">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1fce-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1fce-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="f1fce-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f1fce-290">31,5</span><span class="sxs-lookup"><span data-stu-id="f1fce-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-291">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f1fce-291">Device is not working properly.</span></span> <span data-ttu-id="f1fce-292">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1fce-293">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="f1fce-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-294">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f1fce-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-296">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1fce-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-297">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f1fce-298">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-299">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f1fce-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-302">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1fce-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-303">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1fce-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f1fce-304">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f1fce-305">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-306">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1fce-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-309">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f1fce-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-310">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-310">Description of the object.</span></span>

<span data-ttu-id="f1fce-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1fce-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-315">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1fce-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-316">Der Bezeichner des Plug & Play Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="f1fce-317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-318">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="f1fce-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-319">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f1fce-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-321">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f1fce-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="f1fce-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f1fce-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-326">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="f1fce-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-328">**HardwareID**</span><span class="sxs-lookup"><span data-stu-id="f1fce-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-329">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f1fce-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-331">Eine Hersteller definierte Identifikations Zeichenfolge, die von Setup verwendet wird, um ein Gerät mit einer INF-Datei abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="f1fce-332">Normalerweise verfügt ein Gerät über eine zugeordnete Liste von Hardware-IDs.</span><span class="sxs-lookup"><span data-stu-id="f1fce-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="f1fce-333">Eine Ausnahme ist der 1394-Bustreiber, der keine Hardware-IDs verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="f1fce-334">Die erste Hardware-ID in der Liste sollte die Geräte-ID sein.</span><span class="sxs-lookup"><span data-stu-id="f1fce-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="f1fce-335">Die verbleibenden IDs sollten in der Reihenfolge der absteigenden Eignung aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="f1fce-336">Hardware-IDs werden in einem der folgenden Formate angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f1fce-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="f1fce-337">\\enumeratorenumerator-spezifisch-Geräte-ID</span><span class="sxs-lookup"><span data-stu-id="f1fce-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="f1fce-338">Dies ist das gängigste Format für einzelne PNP-Geräte.</span><span class="sxs-lookup"><span data-stu-id="f1fce-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="f1fce-339">Ein Beispiel für einen Enumerator ist das BIOS oder ISAPNP.</span><span class="sxs-lookup"><span data-stu-id="f1fce-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="f1fce-340">\*enumeratorspezifische ID</span><span class="sxs-lookup"><span data-stu-id="f1fce-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="f1fce-341">Ein Sternchen ( \* ) gibt an, dass mehr als ein Enumerator verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1fce-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="f1fce-342">Geräteklassen spezifische ID</span><span class="sxs-lookup"><span data-stu-id="f1fce-342">device-class-specific ID</span></span>

    <span data-ttu-id="f1fce-343">Ein benutzerdefiniertes Format.</span><span class="sxs-lookup"><span data-stu-id="f1fce-343">A custom format.</span></span>

<span data-ttu-id="f1fce-344">Beispiele für Hardware-IDs:</span><span class="sxs-lookup"><span data-stu-id="f1fce-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="f1fce-345">root \\ \* PNPOF08</span><span class="sxs-lookup"><span data-stu-id="f1fce-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="f1fce-346">PC \\ ven \_ 1000&dev \_ 001&Subsys \_ 00000000&Rev \_ 02</span><span class="sxs-lookup"><span data-stu-id="f1fce-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="f1fce-347">Weitere Informationen finden Sie im [Windows-Treiberkit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="f1fce-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1fce-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-349">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1fce-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-351">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f1fce-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-352">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-352">Date and time the object was installed.</span></span> <span data-ttu-id="f1fce-353">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1fce-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f1fce-354">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-355">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f1fce-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-356">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1fce-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-358">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f1fce-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f1fce-359">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-360">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="f1fce-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-363">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1fce-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-364">Der Name des Herstellers des Plug & Play Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="f1fce-365">Beispiel: "Acme"</span><span class="sxs-lookup"><span data-stu-id="f1fce-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-366">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1fce-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-369">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f1fce-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-370">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f1fce-370">Label by which the object is known.</span></span> <span data-ttu-id="f1fce-371">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f1fce-372">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-373">**Pnpclass**</span><span class="sxs-lookup"><span data-stu-id="f1fce-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-376">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1fce-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="f1fce-377">Diese Eigenschaft ist, obwohl Sie in der MOF-Datei aufgelistet ist, in der-Klasse nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="f1fce-378">Die-Eigenschaft wird hier nur aus Gründen der Vollständigkeit beschrieben und um die MOF-Datei selbst zu verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="f1fce-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="f1fce-379">Der Name des Typs dieses Plug & Play Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="f1fce-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft befindet sich nicht in der MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1fce-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1fce-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-384">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1fce-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-385">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f1fce-386">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f1fce-387">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f1fce-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-388">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f1fce-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-389">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f1fce-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-391">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-391">Not implemented.</span></span>

<span data-ttu-id="f1fce-392">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1fce-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f1fce-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-394">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f1fce-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f1fce-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-396">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1fce-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="f1fce-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-398">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f1fce-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f1fce-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-400">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1fce-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f1fce-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="f1fce-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-402">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="f1fce-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f1fce-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="f1fce-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-404">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="f1fce-405">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f1fce-406">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="f1fce-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f1fce-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="f1fce-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-408">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="f1fce-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f1fce-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="f1fce-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f1fce-410">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1fce-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1fce-411">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="f1fce-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-412">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f1fce-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-414">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1fce-414">Not implemented.</span></span>

<span data-ttu-id="f1fce-415">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-416">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="f1fce-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-417">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f1fce-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-419">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1fce-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-420">Gibt an, ob sich dieses Plug & Play Gerät derzeit im System befindet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="f1fce-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-422">**Service**</span><span class="sxs-lookup"><span data-stu-id="f1fce-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-423">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-425">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1fce-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-426">Name des diensdienstanbieter, der dieses Plug & Play Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="f1fce-427">Weitere Informationen finden Sie unter [**Win32 \_ systemdriverpnptity**](win32-systemdriverpnpentity.md).</span><span class="sxs-lookup"><span data-stu-id="f1fce-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="f1fce-428">Beispiel: "ATAPI"</span><span class="sxs-lookup"><span data-stu-id="f1fce-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="f1fce-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-432">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f1fce-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-433">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-433">Current status of the object.</span></span> <span data-ttu-id="f1fce-434">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f1fce-435">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="f1fce-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f1fce-436">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="f1fce-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f1fce-437">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f1fce-438">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f1fce-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f1fce-439">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f1fce-440">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f1fce-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f1fce-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f1fce-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f1fce-442">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f1fce-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1fce-443">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f1fce-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1fce-444">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f1fce-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f1fce-445">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f1fce-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f1fce-446">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f1fce-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f1fce-447">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f1fce-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f1fce-448">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f1fce-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f1fce-449">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f1fce-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f1fce-450">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f1fce-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f1fce-451">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f1fce-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f1fce-452">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f1fce-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1fce-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f1fce-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-454">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1fce-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-456">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f1fce-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-457">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f1fce-457">State of the logical device.</span></span> <span data-ttu-id="f1fce-458">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f1fce-459">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1fce-460">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f1fce-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1fce-461">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f1fce-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f1fce-462">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f1fce-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1fce-463">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="f1fce-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f1fce-464">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="f1fce-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1fce-465">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f1fce-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-466">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-468">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1fce-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-469">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="f1fce-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="f1fce-470">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-471">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f1fce-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fce-472">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1fce-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-473">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1fce-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fce-474">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1fce-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1fce-475">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f1fce-475">Name of the scoping system.</span></span>

<span data-ttu-id="f1fce-476">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1fce-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1fce-477">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1fce-477">Remarks</span></span>

<span data-ttu-id="f1fce-478">Die **Win32- \_ pnptity** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f1fce-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f1fce-479">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1fce-479">Examples</span></span>

<span data-ttu-id="f1fce-480">Das [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell-Beispiel in der TechNet Gallery verwendet zum Abrufen einer Liste mit nicht funktionierenden Hardware mithilfe von WMI den Win32-Wert von **Win32 \_** .</span><span class="sxs-lookup"><span data-stu-id="f1fce-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="f1fce-481">Im folgenden VBScript-Codebeispiel wird eine Verbindung mit einer Gruppe von Remote Computern in derselben Domäne hergestellt, indem ein Array von Remote Computernamen erstellt und dann die Namen der Plug & Play Geräte – Instanzen von Win32 \_ pnptity – auf den einzelnen Computern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f1fce-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="f1fce-482">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1fce-482">Requirements</span></span>



| <span data-ttu-id="f1fce-483">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1fce-483">Requirement</span></span> | <span data-ttu-id="f1fce-484">Wert</span><span class="sxs-lookup"><span data-stu-id="f1fce-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fce-485">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1fce-485">Minimum supported client</span></span><br/> | <span data-ttu-id="f1fce-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1fce-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1fce-487">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1fce-487">Minimum supported server</span></span><br/> | <span data-ttu-id="f1fce-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1fce-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1fce-489">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1fce-489">Namespace</span></span><br/>                | <span data-ttu-id="f1fce-490">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1fce-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1fce-491">MOF</span><span class="sxs-lookup"><span data-stu-id="f1fce-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1fce-492"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f1fce-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1fce-493">DLL</span><span class="sxs-lookup"><span data-stu-id="f1fce-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1fce-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1fce-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1fce-495">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1fce-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fce-496">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="f1fce-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="f1fce-497">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="f1fce-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f1fce-498">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="f1fce-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="f1fce-499">WMI-Tasks: Computer Hardware</span><span class="sxs-lookup"><span data-stu-id="f1fce-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
