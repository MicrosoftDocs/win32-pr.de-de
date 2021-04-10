---
description: Die WMI-Klasse für den Win32- \_ Bus stellt einen physischen Bus dar, der von einem Computer mit Windows-Betriebssystem angezeigt wird. Jede Instanz eines Windows-Busses ist ein Nachfolger (oder Mitglied) dieser Klasse.
ms.assetid: 76ba15f4-8c7b-4713-b5a2-e444fbab064a
ms.tgt_platform: multiple
title: Win32_Bus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Bus
- Win32_Bus.Reset
- Win32_Bus.SetPowerState
- Win32_Bus.Availability
- Win32_Bus.BusNum
- Win32_Bus.BusType
- Win32_Bus.Caption
- Win32_Bus.ConfigManagerErrorCode
- Win32_Bus.ConfigManagerUserConfig
- Win32_Bus.CreationClassName
- Win32_Bus.Description
- Win32_Bus.DeviceID
- Win32_Bus.ErrorCleared
- Win32_Bus.ErrorDescription
- Win32_Bus.InstallDate
- Win32_Bus.LastErrorCode
- Win32_Bus.Name
- Win32_Bus.PNPDeviceID
- Win32_Bus.PowerManagementCapabilities
- Win32_Bus.PowerManagementSupported
- Win32_Bus.Status
- Win32_Bus.StatusInfo
- Win32_Bus.SystemCreationClassName
- Win32_Bus.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac31a2187ee7e4974e1ddedbf084efd482748753
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860828"
---
# <a name="win32_bus-class"></a><span data-ttu-id="3b802-104">Win32- \_ Busklasse</span><span class="sxs-lookup"><span data-stu-id="3b802-104">Win32\_Bus class</span></span>

<span data-ttu-id="3b802-105">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für den **Win32- \_ Bus** stellt einen physischen Bus dar, der von einem Computer mit Windows-Betriebssystem angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b802-105">The **Win32\_Bus** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical bus as seen by a computer running a Windows operating system.</span></span> <span data-ttu-id="3b802-106">Jede Instanz eines Windows-Busses ist ein Nachfolger (oder Mitglied) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="3b802-106">Any instance of a Windows bus is a descendant (or member) of this class.</span></span>

<span data-ttu-id="3b802-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3b802-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b802-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b802-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Bus : CIM_LogicalDevice
{
  uint16   Availability;
  uint32   BusNum;
  uint32   BusType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="3b802-109">Member</span><span class="sxs-lookup"><span data-stu-id="3b802-109">Members</span></span>

<span data-ttu-id="3b802-110">Die **Win32- \_ Busklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3b802-110">The **Win32\_Bus** class has these types of members:</span></span>

-   [<span data-ttu-id="3b802-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="3b802-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3b802-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b802-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3b802-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="3b802-113">Methods</span></span>

<span data-ttu-id="3b802-114">Die **Win32- \_ Busklasse** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3b802-114">The **Win32\_Bus** class has these methods.</span></span>



| <span data-ttu-id="3b802-115">Methode</span><span class="sxs-lookup"><span data-stu-id="3b802-115">Method</span></span>            | <span data-ttu-id="3b802-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b802-116">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b802-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="3b802-117">**Reset**</span></span>         | <span data-ttu-id="3b802-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3b802-118">Not implemented.</span></span> <span data-ttu-id="3b802-119">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDevice**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="3b802-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="3b802-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3b802-120">**SetPowerState**</span></span> | <span data-ttu-id="3b802-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3b802-121">Not implemented.</span></span> <span data-ttu-id="3b802-122">Informationen zur Implementierung dieser Methode finden Sie in der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDevice**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="3b802-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3b802-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b802-123">Properties</span></span>

<span data-ttu-id="3b802-124">Die **Win32- \_ Busklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3b802-124">The **Win32\_Bus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b802-125">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="3b802-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b802-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="3b802-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-129">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="3b802-129">Availability and status of the device.</span></span>

<span data-ttu-id="3b802-130">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b802-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3b802-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b802-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="3b802-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3b802-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="3b802-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-134">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="3b802-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3b802-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="3b802-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3b802-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="3b802-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3b802-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="3b802-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3b802-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="3b802-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3b802-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="3b802-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3b802-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="3b802-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3b802-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="3b802-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3b802-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="3b802-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3b802-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="3b802-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3b802-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="3b802-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="3b802-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3b802-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="3b802-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3b802-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3b802-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="3b802-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3b802-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="3b802-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3b802-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="3b802-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="3b802-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3b802-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="3b802-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="3b802-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3b802-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="3b802-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="3b802-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3b802-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="3b802-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3b802-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3b802-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="3b802-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="3b802-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b802-161">**Busnum**</span><span class="sxs-lookup"><span data-stu-id="3b802-161">**BusNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b802-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-164">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3b802-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-165">Die dem physischen Bus zugewiesene logische Nummer.</span><span class="sxs-lookup"><span data-stu-id="3b802-165">Logical number assigned to the physical bus.</span></span>

<span data-ttu-id="3b802-166">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="3b802-166">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="3b802-167">**BusType**</span><span class="sxs-lookup"><span data-stu-id="3b802-167">**BusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b802-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-170">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| chwres \| Interface \_ Type")</span><span class="sxs-lookup"><span data-stu-id="3b802-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|cHwRes\|INTERFACE\_TYPE")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-171">Der Typ des physischen Busses.</span><span class="sxs-lookup"><span data-stu-id="3b802-171">Type of the physical bus.</span></span> <span data-ttu-id="3b802-172">Dieser Wert ist einer der Werte in der **\_ Schnittstellentyp** -Enumeration, die in "Bus. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b802-172">This value will be one of the values in the **INTERFACE\_TYPE** enumeration defined in Bus.h.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3b802-173">Nicht **definiert** (-1)</span><span class="sxs-lookup"><span data-stu-id="3b802-173">**Undefined** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="3b802-174">**Intern** (0)</span><span class="sxs-lookup"><span data-stu-id="3b802-174">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="3b802-175">**ISA** (1)</span><span class="sxs-lookup"><span data-stu-id="3b802-175">**ISA** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="3b802-176">**EISA** (2)</span><span class="sxs-lookup"><span data-stu-id="3b802-176">**EISA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MicroChannel"></span><span id="microchannel"></span><span id="MICROCHANNEL"></span>

<span data-ttu-id="3b802-177">**Mikrochannel** (3)</span><span class="sxs-lookup"><span data-stu-id="3b802-177">**MicroChannel** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboChannel"></span><span id="turbochannel"></span><span id="TURBOCHANNEL"></span>

<span data-ttu-id="3b802-178">**TURBOchannel** (4)</span><span class="sxs-lookup"><span data-stu-id="3b802-178">**TurboChannel** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Bus"></span><span id="pci_bus"></span><span id="PCI_BUS"></span>

<span data-ttu-id="3b802-179">**PCI-Bus** (5)</span><span class="sxs-lookup"><span data-stu-id="3b802-179">**PCI Bus** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="3b802-180">**VME-Bus** (6)</span><span class="sxs-lookup"><span data-stu-id="3b802-180">**VME Bus** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="3b802-181">**NuBus** (7)</span><span class="sxs-lookup"><span data-stu-id="3b802-181">**NuBus** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Bus"></span><span id="pcmcia_bus"></span><span id="PCMCIA_BUS"></span>

<span data-ttu-id="3b802-182">**PCMCIA-Bus** (8)</span><span class="sxs-lookup"><span data-stu-id="3b802-182">**PCMCIA Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="C_Bus"></span><span id="c_bus"></span><span id="C_BUS"></span>

<span data-ttu-id="3b802-183">**C-Bus** (9)</span><span class="sxs-lookup"><span data-stu-id="3b802-183">**C Bus** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MPI_Bus"></span><span id="mpi_bus"></span><span id="MPI_BUS"></span>

<span data-ttu-id="3b802-184">**MPI-Bus** (10)</span><span class="sxs-lookup"><span data-stu-id="3b802-184">**MPI Bus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MPSA_Bus"></span><span id="mpsa_bus"></span><span id="MPSA_BUS"></span>

<span data-ttu-id="3b802-185">**MPSA-Bus** (11)</span><span class="sxs-lookup"><span data-stu-id="3b802-185">**MPSA Bus** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Processor"></span><span id="internal_processor"></span><span id="INTERNAL_PROCESSOR"></span>

<span data-ttu-id="3b802-186">**Interner Prozessor** (12)</span><span class="sxs-lookup"><span data-stu-id="3b802-186">**Internal Processor** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Power_Bus"></span><span id="internal_power_bus"></span><span id="INTERNAL_POWER_BUS"></span>

<span data-ttu-id="3b802-187">**Interner Netzteil** (13)</span><span class="sxs-lookup"><span data-stu-id="3b802-187">**Internal Power Bus** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_ISA_Bus"></span><span id="pnp_isa_bus"></span><span id="PNP_ISA_BUS"></span>

<span data-ttu-id="3b802-188">**PnP ISA Bus** (14)</span><span class="sxs-lookup"><span data-stu-id="3b802-188">**PNP ISA Bus** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_Bus"></span><span id="pnp_bus"></span><span id="PNP_BUS"></span>

<span data-ttu-id="3b802-189">**PnP-Bus** (15)</span><span class="sxs-lookup"><span data-stu-id="3b802-189">**PNP Bus** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum_Interface_Type"></span><span id="maximum_interface_type"></span><span id="MAXIMUM_INTERFACE_TYPE"></span>

<span data-ttu-id="3b802-190">**Maximaler Schnittstellentyp** (16)</span><span class="sxs-lookup"><span data-stu-id="3b802-190">**Maximum Interface Type** (16)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b802-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3b802-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-194">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3b802-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-195">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3b802-195">Short description of the object a one-line string.</span></span>

<span data-ttu-id="3b802-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-197">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="3b802-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-198">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b802-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-200">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3b802-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-201">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3b802-201">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="3b802-202">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3b802-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="3b802-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3b802-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="3b802-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-205">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3b802-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3b802-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="3b802-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3b802-207">(1)</span><span class="sxs-lookup"><span data-stu-id="3b802-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-208">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3b802-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3b802-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="3b802-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3b802-210">(2)</span><span class="sxs-lookup"><span data-stu-id="3b802-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3b802-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="3b802-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3b802-212">(3)</span><span class="sxs-lookup"><span data-stu-id="3b802-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-213">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3b802-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3b802-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="3b802-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3b802-215">(4)</span><span class="sxs-lookup"><span data-stu-id="3b802-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-216">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3b802-216">Device is not working properly.</span></span> <span data-ttu-id="3b802-217">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="3b802-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3b802-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="3b802-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3b802-219">(5)</span><span class="sxs-lookup"><span data-stu-id="3b802-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-220">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b802-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3b802-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="3b802-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3b802-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="3b802-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-223">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="3b802-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3b802-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="3b802-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3b802-225">(7)</span><span class="sxs-lookup"><span data-stu-id="3b802-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3b802-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="3b802-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3b802-227">(8)</span><span class="sxs-lookup"><span data-stu-id="3b802-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-228">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="3b802-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3b802-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="3b802-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3b802-230">(9)</span><span class="sxs-lookup"><span data-stu-id="3b802-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-231">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3b802-231">Device is not working properly.</span></span> <span data-ttu-id="3b802-232">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="3b802-232">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3b802-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="3b802-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3b802-234">(10)</span><span class="sxs-lookup"><span data-stu-id="3b802-234">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-235">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-235">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3b802-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="3b802-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3b802-237">(11)</span><span class="sxs-lookup"><span data-stu-id="3b802-237">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-238">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="3b802-238">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3b802-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="3b802-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3b802-240">(12)</span><span class="sxs-lookup"><span data-stu-id="3b802-240">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-241">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="3b802-241">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3b802-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="3b802-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3b802-243">(13)</span><span class="sxs-lookup"><span data-stu-id="3b802-243">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-244">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-244">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3b802-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="3b802-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3b802-246">(14)</span><span class="sxs-lookup"><span data-stu-id="3b802-246">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-247">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3b802-247">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3b802-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="3b802-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3b802-249">(15)</span><span class="sxs-lookup"><span data-stu-id="3b802-249">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-250">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3b802-250">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3b802-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="3b802-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3b802-252">(16)</span><span class="sxs-lookup"><span data-stu-id="3b802-252">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-253">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-253">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3b802-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="3b802-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3b802-255">(17)</span><span class="sxs-lookup"><span data-stu-id="3b802-255">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-256">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="3b802-256">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3b802-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="3b802-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3b802-258">(18)</span><span class="sxs-lookup"><span data-stu-id="3b802-258">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-259">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-259">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3b802-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="3b802-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3b802-261">(19)</span><span class="sxs-lookup"><span data-stu-id="3b802-261">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3b802-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="3b802-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3b802-263">(20)</span><span class="sxs-lookup"><span data-stu-id="3b802-263">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-264">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="3b802-264">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3b802-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="3b802-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3b802-266">(21)</span><span class="sxs-lookup"><span data-stu-id="3b802-266">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-267">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="3b802-267">System failure.</span></span> <span data-ttu-id="3b802-268">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3b802-268">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3b802-269">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b802-269">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3b802-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="3b802-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3b802-271">(22)</span><span class="sxs-lookup"><span data-stu-id="3b802-271">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-272">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b802-272">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3b802-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="3b802-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3b802-274">(23)</span><span class="sxs-lookup"><span data-stu-id="3b802-274">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-275">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="3b802-275">System failure.</span></span> <span data-ttu-id="3b802-276">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3b802-276">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3b802-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="3b802-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3b802-278">(24)</span><span class="sxs-lookup"><span data-stu-id="3b802-278">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-279">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="3b802-279">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3b802-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="3b802-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3b802-281">(25)</span><span class="sxs-lookup"><span data-stu-id="3b802-281">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-282">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3b802-282">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3b802-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="3b802-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3b802-284">(26)</span><span class="sxs-lookup"><span data-stu-id="3b802-284">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-285">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3b802-285">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3b802-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="3b802-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3b802-287">(27)</span><span class="sxs-lookup"><span data-stu-id="3b802-287">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-288">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b802-288">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3b802-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="3b802-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3b802-290">(28)</span><span class="sxs-lookup"><span data-stu-id="3b802-290">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-291">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="3b802-291">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3b802-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="3b802-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3b802-293">(29)</span><span class="sxs-lookup"><span data-stu-id="3b802-293">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-294">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b802-294">Device is disabled.</span></span> <span data-ttu-id="3b802-295">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3b802-295">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3b802-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="3b802-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3b802-297">(30)</span><span class="sxs-lookup"><span data-stu-id="3b802-297">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-298">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b802-298">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3b802-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="3b802-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3b802-300">31,5</span><span class="sxs-lookup"><span data-stu-id="3b802-300">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-301">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3b802-301">Device is not working properly.</span></span> <span data-ttu-id="3b802-302">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-302">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b802-303">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="3b802-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-304">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3b802-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-306">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3b802-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-307">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b802-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3b802-308">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-309">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="3b802-309">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-312">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b802-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b802-313">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b802-313">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3b802-314">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-314">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="3b802-315">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-316">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b802-316">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-319">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3b802-319">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-320">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3b802-320">Description of the object.</span></span>

<span data-ttu-id="3b802-321">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-322">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3b802-322">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-325">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3b802-325">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-326">Eindeutiger Name, der den Bus identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b802-326">Unique name that identifies the bus.</span></span>

<span data-ttu-id="3b802-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-328">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="3b802-328">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-329">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3b802-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b802-331">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3b802-331">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="3b802-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-333">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3b802-333">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b802-336">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. getroffenen Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="3b802-336">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="3b802-337">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b802-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-339">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b802-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-341">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="3b802-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-342">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3b802-342">Date and time the object was installed.</span></span> <span data-ttu-id="3b802-343">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b802-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3b802-344">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3b802-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-346">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b802-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b802-348">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3b802-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3b802-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-350">**Name**</span><span class="sxs-lookup"><span data-stu-id="3b802-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-351">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-353">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3b802-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-354">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3b802-354">Label by which the object is known.</span></span> <span data-ttu-id="3b802-355">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3b802-356">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-357">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3b802-357">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-360">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3b802-360">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-361">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3b802-361">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3b802-362">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3b802-363">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3b802-363">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3b802-364">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="3b802-364">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-365">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="3b802-365">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b802-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b802-367">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3b802-367">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3b802-368">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-368">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b802-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3b802-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3b802-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3b802-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3b802-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="3b802-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3b802-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3b802-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-373">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b802-373">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3b802-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="3b802-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-375">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="3b802-375">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3b802-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="3b802-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-377">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b802-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3b802-378">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-378">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="3b802-379">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="3b802-379">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3b802-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="3b802-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-381">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState*-Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3b802-381">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3b802-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="3b802-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3b802-383">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="3b802-383">Timed Power-On Supported</span></span>

<span data-ttu-id="3b802-384">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3b802-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b802-385">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="3b802-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-386">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3b802-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b802-388">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="3b802-388">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="3b802-389">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3b802-389">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3b802-390">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-391">**Status**</span><span class="sxs-lookup"><span data-stu-id="3b802-391">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-392">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-394">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3b802-394">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-395">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3b802-395">Current status of the object.</span></span> <span data-ttu-id="3b802-396">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-396">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3b802-397">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="3b802-397">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3b802-398">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="3b802-398">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3b802-399">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-399">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3b802-400">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="3b802-400">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3b802-401">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3b802-402">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3b802-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3b802-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3b802-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3b802-404">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3b802-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3b802-405">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3b802-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b802-406">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3b802-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3b802-407">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3b802-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3b802-408">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3b802-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3b802-409">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="3b802-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3b802-410">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3b802-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3b802-411">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="3b802-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3b802-412">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="3b802-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3b802-413">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="3b802-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3b802-414">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="3b802-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b802-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3b802-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-416">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b802-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-418">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="3b802-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3b802-419">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3b802-419">State of the logical device.</span></span> <span data-ttu-id="3b802-420">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b802-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3b802-421">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b802-422">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3b802-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b802-423">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="3b802-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3b802-424">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3b802-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3b802-425">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="3b802-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3b802-426">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="3b802-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b802-427">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="3b802-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-430">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b802-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b802-431">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="3b802-431">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="3b802-432">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b802-433">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="3b802-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b802-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3b802-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b802-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3b802-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b802-436">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b802-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b802-437">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="3b802-437">Name of the scoping system.</span></span>

<span data-ttu-id="3b802-438">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3b802-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b802-439">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b802-439">Remarks</span></span>

<span data-ttu-id="3b802-440">Die **Win32- \_ Busklasse** wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3b802-440">The **Win32\_Bus** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b802-441">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b802-441">Requirements</span></span>



| <span data-ttu-id="3b802-442">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b802-442">Requirement</span></span> | <span data-ttu-id="3b802-443">Wert</span><span class="sxs-lookup"><span data-stu-id="3b802-443">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b802-444">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b802-444">Minimum supported client</span></span><br/> | <span data-ttu-id="3b802-445">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b802-445">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b802-446">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b802-446">Minimum supported server</span></span><br/> | <span data-ttu-id="3b802-447">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b802-447">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b802-448">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b802-448">Namespace</span></span><br/>                | <span data-ttu-id="3b802-449">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3b802-449">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b802-450">MOF</span><span class="sxs-lookup"><span data-stu-id="3b802-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b802-451"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3b802-451"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b802-452">DLL</span><span class="sxs-lookup"><span data-stu-id="3b802-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b802-453"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b802-453"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b802-454">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b802-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b802-455">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3b802-455">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="3b802-456">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="3b802-456">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

