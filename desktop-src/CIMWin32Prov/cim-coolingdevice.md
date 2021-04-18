---
description: Die CIM \_ coolingdevice-Klasse stellt die Funktionen und die Verwaltung von Kühlgeräten dar.
ms.assetid: ac0f0df4-c174-4306-9325-eaa316ee820a
ms.tgt_platform: multiple
title: CIM_CoolingDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CoolingDevice
- CIM_CoolingDevice.Caption
- CIM_CoolingDevice.Description
- CIM_CoolingDevice.InstallDate
- CIM_CoolingDevice.Name
- CIM_CoolingDevice.Status
- CIM_CoolingDevice.Availability
- CIM_CoolingDevice.ConfigManagerErrorCode
- CIM_CoolingDevice.ConfigManagerUserConfig
- CIM_CoolingDevice.CreationClassName
- CIM_CoolingDevice.DeviceID
- CIM_CoolingDevice.PowerManagementCapabilities
- CIM_CoolingDevice.ErrorCleared
- CIM_CoolingDevice.ErrorDescription
- CIM_CoolingDevice.LastErrorCode
- CIM_CoolingDevice.PNPDeviceID
- CIM_CoolingDevice.PowerManagementSupported
- CIM_CoolingDevice.StatusInfo
- CIM_CoolingDevice.SystemCreationClassName
- CIM_CoolingDevice.SystemName
- CIM_CoolingDevice.ActiveCooling
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f6c480e910cf72a319856942fda28d2139d0a6ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343599"
---
# <a name="cim_coolingdevice-class"></a><span data-ttu-id="50745-103">CIM \_ coolingdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="50745-103">CIM\_CoolingDevice class</span></span>

<span data-ttu-id="50745-104">Die **CIM \_ coolingdevice** -Klasse stellt die Funktionen und die Verwaltung von Kühlgeräten dar.</span><span class="sxs-lookup"><span data-stu-id="50745-104">The **CIM\_CoolingDevice** class represents the capabilities and management of cooling devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50745-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="50745-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="50745-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="50745-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="50745-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="50745-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="50745-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="50745-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="50745-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="50745-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979A-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_CoolingDevice : CIM_LogicalDevice
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
  boolean  ActiveCooling;
};
```

## <a name="members"></a><span data-ttu-id="50745-110">Member</span><span class="sxs-lookup"><span data-stu-id="50745-110">Members</span></span>

<span data-ttu-id="50745-111">Die **CIM \_ coolingdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="50745-111">The **CIM\_CoolingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="50745-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="50745-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="50745-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50745-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="50745-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="50745-114">Methods</span></span>

<span data-ttu-id="50745-115">Die **CIM \_ coolingdevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="50745-115">The **CIM\_CoolingDevice** class has these methods.</span></span>



| <span data-ttu-id="50745-116">Methode</span><span class="sxs-lookup"><span data-stu-id="50745-116">Method</span></span>                                                                   | <span data-ttu-id="50745-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50745-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50745-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="50745-118">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                    | <span data-ttu-id="50745-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="50745-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="50745-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="50745-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="50745-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="50745-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-coolingdevice.md) | <span data-ttu-id="50745-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50745-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="50745-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="50745-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="50745-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50745-124">Properties</span></span>

<span data-ttu-id="50745-125">Die **CIM \_ coolingdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50745-125">The **CIM\_CoolingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50745-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="50745-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50745-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50745-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50745-129">**True** gibt an, dass das kühl Gerät aktiv (im Gegensatz zur passiven) Kühlung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="50745-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

</dd> <dt>

<span data-ttu-id="50745-130">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="50745-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50745-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50745-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="50745-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="50745-134">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="50745-134">Availability and status of the device.</span></span>

<span data-ttu-id="50745-135">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50745-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="50745-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50745-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="50745-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="50745-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="50745-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="50745-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="50745-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="50745-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="50745-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="50745-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="50745-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="50745-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="50745-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="50745-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="50745-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="50745-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="50745-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="50745-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="50745-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="50745-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="50745-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="50745-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="50745-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="50745-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="50745-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="50745-149">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="50745-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="50745-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="50745-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="50745-151">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="50745-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="50745-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="50745-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="50745-153">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="50745-153">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="50745-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="50745-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="50745-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="50745-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="50745-156">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="50745-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="50745-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="50745-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="50745-158">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="50745-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="50745-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="50745-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="50745-160">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="50745-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="50745-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="50745-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="50745-162">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="50745-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="50745-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="50745-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="50745-164">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="50745-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="50745-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="50745-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-168">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="50745-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="50745-169">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="50745-169">A short textual description of the object.</span></span>

<span data-ttu-id="50745-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-171">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="50745-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50745-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50745-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-174">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="50745-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="50745-175">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="50745-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="50745-176">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="50745-177">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="50745-177">**This device is working properly.**</span></span> <span data-ttu-id="50745-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="50745-178">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="50745-179">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="50745-179">**This device is not configured correctly.**</span></span> <span data-ttu-id="50745-180">(1)</span><span class="sxs-lookup"><span data-stu-id="50745-180">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="50745-181">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="50745-181">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="50745-182">(2)</span><span class="sxs-lookup"><span data-stu-id="50745-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="50745-183">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="50745-183">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="50745-184">(3)</span><span class="sxs-lookup"><span data-stu-id="50745-184">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="50745-185">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="50745-185">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="50745-186">(4)</span><span class="sxs-lookup"><span data-stu-id="50745-186">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="50745-187">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="50745-187">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="50745-188">(5)</span><span class="sxs-lookup"><span data-stu-id="50745-188">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="50745-189">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="50745-189">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="50745-190"> (6)</span><span class="sxs-lookup"><span data-stu-id="50745-190">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="50745-191">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="50745-191">**Cannot filter.**</span></span> <span data-ttu-id="50745-192">(7)</span><span class="sxs-lookup"><span data-stu-id="50745-192">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="50745-193">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="50745-193">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="50745-194">(8)</span><span class="sxs-lookup"><span data-stu-id="50745-194">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="50745-195">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="50745-195">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="50745-196">(9)</span><span class="sxs-lookup"><span data-stu-id="50745-196">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="50745-197">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="50745-197">**This device cannot start.**</span></span> <span data-ttu-id="50745-198">(10)</span><span class="sxs-lookup"><span data-stu-id="50745-198">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="50745-199">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="50745-199">**This device failed.**</span></span> <span data-ttu-id="50745-200">(11)</span><span class="sxs-lookup"><span data-stu-id="50745-200">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="50745-201">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="50745-201">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="50745-202">(12)</span><span class="sxs-lookup"><span data-stu-id="50745-202">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="50745-203">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="50745-203">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="50745-204">(13)</span><span class="sxs-lookup"><span data-stu-id="50745-204">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="50745-205">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="50745-205">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="50745-206">(14)</span><span class="sxs-lookup"><span data-stu-id="50745-206">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="50745-207">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="50745-207">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="50745-208">(15)</span><span class="sxs-lookup"><span data-stu-id="50745-208">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="50745-209">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="50745-209">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="50745-210">(16)</span><span class="sxs-lookup"><span data-stu-id="50745-210">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="50745-211">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="50745-211">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="50745-212">(17)</span><span class="sxs-lookup"><span data-stu-id="50745-212">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="50745-213">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="50745-213">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="50745-214">(18)</span><span class="sxs-lookup"><span data-stu-id="50745-214">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="50745-215">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="50745-215">**Failure using the VxD loader.**</span></span> <span data-ttu-id="50745-216">(19)</span><span class="sxs-lookup"><span data-stu-id="50745-216">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="50745-217">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="50745-217">**Your registry might be corrupted.**</span></span> <span data-ttu-id="50745-218">(20)</span><span class="sxs-lookup"><span data-stu-id="50745-218">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="50745-219">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="50745-219">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="50745-220">(21)</span><span class="sxs-lookup"><span data-stu-id="50745-220">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="50745-221">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="50745-221">**This device is disabled.**</span></span> <span data-ttu-id="50745-222">(22)</span><span class="sxs-lookup"><span data-stu-id="50745-222">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="50745-223">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="50745-223">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="50745-224">(23)</span><span class="sxs-lookup"><span data-stu-id="50745-224">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="50745-225">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="50745-225">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="50745-226">(24)</span><span class="sxs-lookup"><span data-stu-id="50745-226">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="50745-227">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="50745-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="50745-228">(25)</span><span class="sxs-lookup"><span data-stu-id="50745-228">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="50745-229">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="50745-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="50745-230">(26)</span><span class="sxs-lookup"><span data-stu-id="50745-230">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="50745-231">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="50745-231">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="50745-232">(27)</span><span class="sxs-lookup"><span data-stu-id="50745-232">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="50745-233">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="50745-233">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="50745-234">(28)</span><span class="sxs-lookup"><span data-stu-id="50745-234">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="50745-235">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="50745-235">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="50745-236">(29)</span><span class="sxs-lookup"><span data-stu-id="50745-236">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="50745-237">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="50745-237">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="50745-238">(30)</span><span class="sxs-lookup"><span data-stu-id="50745-238">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="50745-239">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="50745-239">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="50745-240">31,5</span><span class="sxs-lookup"><span data-stu-id="50745-240">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50745-241">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="50745-241">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-242">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50745-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50745-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-244">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="50745-244">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="50745-245">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="50745-245">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="50745-246">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-246">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-247">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="50745-247">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-250">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="50745-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="50745-251">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50745-251">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="50745-252">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="50745-252">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="50745-253">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-253">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-254">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50745-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-257">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="50745-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="50745-258">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="50745-258">A textual description of the object.</span></span>

<span data-ttu-id="50745-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-260">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="50745-260">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-263">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="50745-263">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="50745-264">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="50745-264">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="50745-265">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-266">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="50745-266">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-267">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50745-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50745-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50745-269">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="50745-269">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="50745-270">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-271">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="50745-271">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50745-274">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="50745-274">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="50745-275">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="50745-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-277">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="50745-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="50745-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-279">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="50745-279">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="50745-280">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="50745-280">Indicates when the object was installed.</span></span> <span data-ttu-id="50745-281">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="50745-281">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="50745-282">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-283">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="50745-283">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-284">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50745-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50745-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50745-286">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="50745-286">Last error code reported by the logical device.</span></span>

<span data-ttu-id="50745-287">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-288">**Name**</span><span class="sxs-lookup"><span data-stu-id="50745-288">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-291">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="50745-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="50745-292">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="50745-292">Label by which the object is known.</span></span> <span data-ttu-id="50745-293">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="50745-293">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="50745-294">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-295">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="50745-295">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-298">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="50745-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="50745-299">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="50745-299">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="50745-300">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="50745-300">Example: "\*PNP030b"</span></span>

<span data-ttu-id="50745-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-302">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="50745-302">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-303">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="50745-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="50745-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50745-305">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="50745-305">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="50745-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50745-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="50745-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="50745-308">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="50745-308">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="50745-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="50745-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="50745-310">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50745-310">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="50745-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="50745-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="50745-312">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="50745-312">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="50745-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="50745-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="50745-314">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50745-314">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="50745-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="50745-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="50745-316">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="50745-316">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="50745-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="50745-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="50745-318">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50745-318">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="50745-319">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="50745-319">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="50745-320">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="50745-320">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="50745-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="50745-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="50745-322">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="50745-322">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="50745-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="50745-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="50745-324">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="50745-324">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="50745-325">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="50745-325">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-326">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="50745-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50745-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50745-328">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="50745-328">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="50745-329">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="50745-329">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="50745-330">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50745-330">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="50745-331">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="50745-331">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="50745-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-333">**Status**</span><span class="sxs-lookup"><span data-stu-id="50745-333">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-336">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="50745-336">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="50745-337">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="50745-337">String that indicates the current status of the object.</span></span> <span data-ttu-id="50745-338">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="50745-338">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="50745-339">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="50745-339">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="50745-340">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="50745-340">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="50745-341">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="50745-341">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="50745-342">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="50745-342">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="50745-343">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="50745-343">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="50745-344">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="50745-345">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="50745-345">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="50745-346">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="50745-346">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="50745-347">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="50745-347">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="50745-348">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="50745-348">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50745-349">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="50745-349">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="50745-350">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="50745-350">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="50745-351">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="50745-351">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="50745-352">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="50745-352">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="50745-353">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="50745-353">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="50745-354">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="50745-354">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="50745-355">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="50745-355">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="50745-356">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="50745-356">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="50745-357">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="50745-357">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50745-358">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="50745-358">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-359">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50745-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50745-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-361">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="50745-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="50745-362">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="50745-362">State of the logical device.</span></span> <span data-ttu-id="50745-363">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50745-363">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="50745-364">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50745-365">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="50745-365">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50745-366">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="50745-366">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="50745-367">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="50745-367">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="50745-368">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="50745-368">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="50745-369">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="50745-369">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50745-370">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="50745-370">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-371">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-373">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="50745-373">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="50745-374">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="50745-374">The scoping system's creation class name.</span></span>

<span data-ttu-id="50745-375">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="50745-376">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="50745-376">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50745-377">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50745-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50745-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50745-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50745-379">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="50745-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="50745-380">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="50745-380">The scoping system's name.</span></span>

<span data-ttu-id="50745-381">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="50745-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50745-382">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50745-382">Remarks</span></span>

<span data-ttu-id="50745-383">Die **CIM \_ coolingdevice** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="50745-383">The **CIM\_CoolingDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="50745-384">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="50745-384">WMI does not implement this class.</span></span> <span data-ttu-id="50745-385">Informationen zu Klassen, die von **CIM \_ coolingdevice** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="50745-385">For classes derived from **CIM\_CoolingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="50745-386">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="50745-386">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="50745-387">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="50745-387">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="50745-388">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50745-388">Requirements</span></span>



| <span data-ttu-id="50745-389">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50745-389">Requirement</span></span> | <span data-ttu-id="50745-390">Wert</span><span class="sxs-lookup"><span data-stu-id="50745-390">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50745-391">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50745-391">Minimum supported client</span></span><br/> | <span data-ttu-id="50745-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50745-392">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50745-393">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50745-393">Minimum supported server</span></span><br/> | <span data-ttu-id="50745-394">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50745-394">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50745-395">Namespace</span><span class="sxs-lookup"><span data-stu-id="50745-395">Namespace</span></span><br/>                | <span data-ttu-id="50745-396">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="50745-396">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50745-397">MOF</span><span class="sxs-lookup"><span data-stu-id="50745-397">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50745-398"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="50745-398"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50745-399">DLL</span><span class="sxs-lookup"><span data-stu-id="50745-399">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50745-400"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50745-400"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50745-401">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50745-401">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50745-402">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="50745-402">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

