---
description: Die WMI-Klasse des Win32- \_ motherboardgeräts stellt ein Gerät dar, das die zentralen Komponenten des Windows-Computer Systems enthält.
ms.assetid: 2aed5fff-e994-4ce1-8a2e-aadb01adf28d
ms.tgt_platform: multiple
title: Win32_MotherboardDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MotherboardDevice
- Win32_MotherboardDevice.Reset
- Win32_MotherboardDevice.SetPowerState
- Win32_MotherboardDevice.Availability
- Win32_MotherboardDevice.Caption
- Win32_MotherboardDevice.ConfigManagerErrorCode
- Win32_MotherboardDevice.ConfigManagerUserConfig
- Win32_MotherboardDevice.CreationClassName
- Win32_MotherboardDevice.Description
- Win32_MotherboardDevice.DeviceID
- Win32_MotherboardDevice.ErrorCleared
- Win32_MotherboardDevice.ErrorDescription
- Win32_MotherboardDevice.InstallDate
- Win32_MotherboardDevice.LastErrorCode
- Win32_MotherboardDevice.Name
- Win32_MotherboardDevice.PNPDeviceID
- Win32_MotherboardDevice.PowerManagementCapabilities
- Win32_MotherboardDevice.PowerManagementSupported
- Win32_MotherboardDevice.PrimaryBusType
- Win32_MotherboardDevice.RevisionNumber
- Win32_MotherboardDevice.SecondaryBusType
- Win32_MotherboardDevice.Status
- Win32_MotherboardDevice.StatusInfo
- Win32_MotherboardDevice.SystemCreationClassName
- Win32_MotherboardDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6df116d1e4bc4e87d7201deb33f57bc8e91320e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748921"
---
# <a name="win32_motherboarddevice-class"></a><span data-ttu-id="6b2eb-103">Win32- \_ Klasse "motherboarddevice"</span><span class="sxs-lookup"><span data-stu-id="6b2eb-103">Win32\_MotherboardDevice class</span></span>

<span data-ttu-id="6b2eb-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) des **Win32- \_ motherboardgeräts** stellt ein Gerät dar, das die zentralen Komponenten des Windows-Computer Systems enthält.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-104">The **Win32\_MotherboardDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device that contains the central components of the Windows computer system.</span></span>

<span data-ttu-id="6b2eb-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6b2eb-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2eb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_MotherboardDevice : CIM_LogicalDevice
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
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrimaryBusType;
  string   RevisionNumber;
  string   SecondaryBusType;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="6b2eb-108">Member</span><span class="sxs-lookup"><span data-stu-id="6b2eb-108">Members</span></span>

<span data-ttu-id="6b2eb-109">Die Win32-Klasse " **\_ motherboarddevice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b2eb-109">The **Win32\_MotherboardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="6b2eb-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b2eb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6b2eb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b2eb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b2eb-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b2eb-112">Methods</span></span>

<span data-ttu-id="6b2eb-113">Die Win32-Klasse " **\_ motherboarddevice** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-113">The **Win32\_MotherboardDevice** class has these methods.</span></span>



| <span data-ttu-id="6b2eb-114">Methode</span><span class="sxs-lookup"><span data-stu-id="6b2eb-114">Method</span></span>            | <span data-ttu-id="6b2eb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b2eb-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2eb-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-116">**Reset**</span></span>         | <span data-ttu-id="6b2eb-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-117">Not implemented.</span></span> <span data-ttu-id="6b2eb-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6b2eb-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="6b2eb-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-119">**SetPowerState**</span></span> | <span data-ttu-id="6b2eb-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-120">Not implemented.</span></span> <span data-ttu-id="6b2eb-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6b2eb-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6b2eb-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b2eb-122">Properties</span></span>

<span data-ttu-id="6b2eb-123">Die Win32-Klasse " **\_ motherboarddevice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-123">The **Win32\_MotherboardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b2eb-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-127">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-128">Availability and status of the device.</span></span>

<span data-ttu-id="6b2eb-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b2eb-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b2eb-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6b2eb-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="6b2eb-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6b2eb-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6b2eb-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b2eb-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6b2eb-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6b2eb-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6b2eb-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b2eb-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="6b2eb-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6b2eb-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6b2eb-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6b2eb-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6b2eb-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6b2eb-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6b2eb-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6b2eb-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6b2eb-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6b2eb-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6b2eb-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6b2eb-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="6b2eb-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b2eb-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-163">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-164">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="6b2eb-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-166">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-169">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-170">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6b2eb-171">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6b2eb-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6b2eb-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-174">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6b2eb-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6b2eb-176">(1)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-177">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6b2eb-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6b2eb-179">(2)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6b2eb-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6b2eb-181">(3)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-182">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6b2eb-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6b2eb-184">(4)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-185">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-185">Device is not working properly.</span></span> <span data-ttu-id="6b2eb-186">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6b2eb-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6b2eb-188">(5)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-189">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6b2eb-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6b2eb-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-192">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6b2eb-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6b2eb-194">(7)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6b2eb-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6b2eb-196">(8)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-197">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6b2eb-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6b2eb-199">(9)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-200">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-200">Device is not working properly.</span></span> <span data-ttu-id="6b2eb-201">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6b2eb-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6b2eb-203">(10)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-204">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6b2eb-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6b2eb-206">(11)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-207">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6b2eb-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6b2eb-209">(12)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-210">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6b2eb-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6b2eb-212">(13)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-213">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6b2eb-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6b2eb-215">(14)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-216">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6b2eb-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6b2eb-218">(15)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-219">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6b2eb-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6b2eb-221">(16)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-222">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6b2eb-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6b2eb-224">(17)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-225">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6b2eb-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6b2eb-227">(18)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-228">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6b2eb-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6b2eb-230">(19)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6b2eb-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6b2eb-232">(20)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-233">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6b2eb-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6b2eb-235">(21)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-236">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-236">System failure.</span></span> <span data-ttu-id="6b2eb-237">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6b2eb-238">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6b2eb-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6b2eb-240">(22)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-241">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6b2eb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6b2eb-243">(23)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-244">System failure.</span></span> <span data-ttu-id="6b2eb-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6b2eb-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6b2eb-247">(24)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-248">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6b2eb-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6b2eb-250">(25)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-251">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6b2eb-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6b2eb-253">(26)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-254">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6b2eb-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6b2eb-256">(27)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-257">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6b2eb-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6b2eb-259">(28)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-260">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6b2eb-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6b2eb-262">(29)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-263">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-263">Device is disabled.</span></span> <span data-ttu-id="6b2eb-264">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6b2eb-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6b2eb-266">(30)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-267">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6b2eb-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6b2eb-269">31,5</span><span class="sxs-lookup"><span data-stu-id="6b2eb-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-270">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-270">Device is not working properly.</span></span> <span data-ttu-id="6b2eb-271">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b2eb-272">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-273">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b2eb-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-275">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-276">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6b2eb-277">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-278">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-281">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-282">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6b2eb-283">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="6b2eb-284">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-285">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-288">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-289">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-289">Description of the object.</span></span>

<span data-ttu-id="6b2eb-290">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-294">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-295">Eindeutiger Bezeichner dieser Hauptplatine.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-295">Unique identifier of this motherboard.</span></span>

<span data-ttu-id="6b2eb-296">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-297">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-298">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b2eb-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-300">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="6b2eb-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-305">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="6b2eb-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-308">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-310">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-311">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-311">Date and time the object was installed.</span></span> <span data-ttu-id="6b2eb-312">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6b2eb-313">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-315">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-317">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6b2eb-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-322">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-323">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-323">Label by which the object is known.</span></span> <span data-ttu-id="6b2eb-324">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-324">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6b2eb-325">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-325">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-326">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-326">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-329">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-330">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-330">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6b2eb-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6b2eb-332">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6b2eb-332">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-333">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-334">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b2eb-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-336">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-336">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6b2eb-337">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-337">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b2eb-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6b2eb-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b2eb-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b2eb-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-342">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6b2eb-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-344">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6b2eb-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-346">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-346">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6b2eb-347">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-347">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6b2eb-348">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6b2eb-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6b2eb-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-350">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6b2eb-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6b2eb-352">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-352">Timed Power-On Supported</span></span>

<span data-ttu-id="6b2eb-353">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-353">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b2eb-354">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-354">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-355">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b2eb-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-357">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="6b2eb-357">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="6b2eb-358">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-358">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="6b2eb-359">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-360">**PrimaryBusType**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-360">**PrimaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-363">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Hardware \\ \\ Description \\ \\ System \\ \\ multifunctionadapter \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-364">Primärer Bustyp der Hauptplatine.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-364">Primary bus type of the motherboard.</span></span>

<span data-ttu-id="6b2eb-365">Beispiel: "PCI"</span><span class="sxs-lookup"><span data-stu-id="6b2eb-365">Example: "PCI"</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-366">**RevisionNumber**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-366">**RevisionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-369">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Hard \\ \\ Description \\ \\ System")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-370">Die Revisionsnummer der Hauptplatine.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-370">Revision number of the motherboard.</span></span>

<span data-ttu-id="6b2eb-371">Beispiel: "00"</span><span class="sxs-lookup"><span data-stu-id="6b2eb-371">Example: "00"</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-372">**SecondaryBusType**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-372">**SecondaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-375">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Hardware \\ \\ Description \\ \\ System \\ \\ multifunctionadapter \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-376">Der sekundäre Bustyp der Hauptplatine.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-376">Secondary bus type of the motherboard.</span></span>

<span data-ttu-id="6b2eb-377">Beispiel: "ISA"</span><span class="sxs-lookup"><span data-stu-id="6b2eb-377">Example: "ISA"</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-381">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-382">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-382">Current status of the object.</span></span> <span data-ttu-id="6b2eb-383">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6b2eb-384">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="6b2eb-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6b2eb-385">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="6b2eb-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6b2eb-386">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6b2eb-387">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6b2eb-388">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6b2eb-389">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="6b2eb-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6b2eb-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6b2eb-391">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b2eb-392">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b2eb-393">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6b2eb-394">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6b2eb-395">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6b2eb-396">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6b2eb-397">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6b2eb-398">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6b2eb-399">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6b2eb-400">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6b2eb-401">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b2eb-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-403">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-405">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6b2eb-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-406">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-406">State of the logical device.</span></span> <span data-ttu-id="6b2eb-407">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6b2eb-408">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b2eb-409">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b2eb-410">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b2eb-411">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b2eb-412">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b2eb-413">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b2eb-414">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-417">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-418">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="6b2eb-419">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2eb-420">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2eb-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b2eb-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2eb-423">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b2eb-424">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-424">Name of the scoping system.</span></span>

<span data-ttu-id="6b2eb-425">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b2eb-426">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b2eb-426">Remarks</span></span>

<span data-ttu-id="6b2eb-427">Die Win32-Klasse " **\_ motherboarddevice** " ist von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-427">The **Win32\_MotherboardDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6b2eb-428">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b2eb-428">Examples</span></span>

<span data-ttu-id="6b2eb-429">Die folgenden [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) -und [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) -Codebeispiele rufen die Motherboard-Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-429">The following [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) and [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) code samples retrieve motherboard information.</span></span>

<span data-ttu-id="6b2eb-430">Im folgenden VBScript-Codebeispiel werden die Hauptinformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6b2eb-430">The following VBScript code sample retrieves motherboard information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_MotherboardDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Primary Bus Type: " & objItem.PrimaryBusType 
    Wscript.Echo "Secondary Bus Type: " & objItem.SecondaryBusType 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="6b2eb-431">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b2eb-431">Requirements</span></span>



| <span data-ttu-id="6b2eb-432">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b2eb-432">Requirement</span></span> | <span data-ttu-id="6b2eb-433">Wert</span><span class="sxs-lookup"><span data-stu-id="6b2eb-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2eb-434">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-434">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2eb-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b2eb-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b2eb-436">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b2eb-436">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2eb-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b2eb-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b2eb-438">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b2eb-438">Namespace</span></span><br/>                | <span data-ttu-id="6b2eb-439">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b2eb-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b2eb-440">MOF</span><span class="sxs-lookup"><span data-stu-id="6b2eb-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b2eb-441"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6b2eb-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b2eb-442">DLL</span><span class="sxs-lookup"><span data-stu-id="6b2eb-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b2eb-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b2eb-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2eb-444">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b2eb-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2eb-445">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="6b2eb-445">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="6b2eb-446">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="6b2eb-446">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

