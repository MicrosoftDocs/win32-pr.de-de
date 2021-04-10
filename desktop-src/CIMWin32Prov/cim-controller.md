---
description: Die CIM \_ -Controller Klasse ist eine übergeordnete Klasse zum Gruppieren von verschiedenen Steuerelement bezogenen Geräten. Beispiele für Controller sind SCSI-Controller, USB-Controller und serielle Controller.
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: CIM_Controller-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214126"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="7efbd-104">CIM_Controller-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="7efbd-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7efbd-105">Die **CIM- \_ Controller** Klasse ist eine übergeordnete Klasse zum Gruppieren von verschiedenen Steuerelement bezogenen Geräten.</span><span class="sxs-lookup"><span data-stu-id="7efbd-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="7efbd-106">Beispiele für Controller sind SCSI-Controller, USB-Controller und serielle Controller.</span><span class="sxs-lookup"><span data-stu-id="7efbd-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="7efbd-107">Die **CIM- \_ Controller** Klasse ist eine Abstraktion für Geräte mit einem einzelnen Protokollstapel, die in erster Linie für die Kommunikation und Steuerung oder das Zurücksetzen von Downstream-Geräten ([**CIM \_ controlledby**](cim-controlledby.md)) vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7efbd-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7efbd-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7efbd-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7efbd-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7efbd-110">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7efbd-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7efbd-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7efbd-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7efbd-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="7efbd-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
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
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="7efbd-113">Member</span><span class="sxs-lookup"><span data-stu-id="7efbd-113">Members</span></span>

<span data-ttu-id="7efbd-114">Die **CIM- \_ Controller** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7efbd-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="7efbd-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="7efbd-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="7efbd-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7efbd-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7efbd-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="7efbd-117">Methods</span></span>

<span data-ttu-id="7efbd-118">Die **CIM- \_ Controller** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="7efbd-119">Methode</span><span class="sxs-lookup"><span data-stu-id="7efbd-119">Method</span></span>                                                                | <span data-ttu-id="7efbd-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7efbd-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7efbd-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="7efbd-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="7efbd-122">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="7efbd-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="7efbd-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="7efbd-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="7efbd-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7efbd-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="7efbd-125">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7efbd-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7efbd-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="7efbd-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7efbd-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7efbd-127">Properties</span></span>

<span data-ttu-id="7efbd-128">Die **CIM- \_ Controller** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7efbd-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7efbd-129">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="7efbd-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7efbd-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="7efbd-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-133">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="7efbd-133">Availability and status of the device.</span></span>

<span data-ttu-id="7efbd-134">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7efbd-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7efbd-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7efbd-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7efbd-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7efbd-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="7efbd-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7efbd-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="7efbd-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7efbd-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="7efbd-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7efbd-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="7efbd-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7efbd-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="7efbd-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7efbd-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="7efbd-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7efbd-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="7efbd-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7efbd-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="7efbd-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7efbd-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="7efbd-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7efbd-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="7efbd-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7efbd-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="7efbd-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-148">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7efbd-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="7efbd-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-150">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7efbd-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7efbd-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="7efbd-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-152">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7efbd-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="7efbd-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7efbd-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="7efbd-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-155">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="7efbd-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7efbd-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="7efbd-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-157">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="7efbd-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7efbd-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="7efbd-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-159">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="7efbd-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7efbd-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="7efbd-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-161">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7efbd-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7efbd-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="7efbd-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-163">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="7efbd-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7efbd-164">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7efbd-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-167">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7efbd-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-168">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7efbd-168">A short textual description of the object.</span></span>

<span data-ttu-id="7efbd-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-170">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="7efbd-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7efbd-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-173">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7efbd-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-174">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7efbd-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7efbd-175">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7efbd-176">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-176">**This device is working properly.**</span></span> <span data-ttu-id="7efbd-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="7efbd-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7efbd-178">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="7efbd-179">(1)</span><span class="sxs-lookup"><span data-stu-id="7efbd-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7efbd-180">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7efbd-181">(2)</span><span class="sxs-lookup"><span data-stu-id="7efbd-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7efbd-182">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7efbd-183">(3)</span><span class="sxs-lookup"><span data-stu-id="7efbd-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7efbd-184">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7efbd-185">(4)</span><span class="sxs-lookup"><span data-stu-id="7efbd-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7efbd-186">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7efbd-187">(5)</span><span class="sxs-lookup"><span data-stu-id="7efbd-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7efbd-188">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7efbd-189"> (6)</span><span class="sxs-lookup"><span data-stu-id="7efbd-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7efbd-190">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-190">**Cannot filter.**</span></span> <span data-ttu-id="7efbd-191">(7)</span><span class="sxs-lookup"><span data-stu-id="7efbd-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7efbd-192">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7efbd-193">(8)</span><span class="sxs-lookup"><span data-stu-id="7efbd-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7efbd-194">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7efbd-195">(9)</span><span class="sxs-lookup"><span data-stu-id="7efbd-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7efbd-196">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-196">**This device cannot start.**</span></span> <span data-ttu-id="7efbd-197">(10)</span><span class="sxs-lookup"><span data-stu-id="7efbd-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7efbd-198">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-198">**This device failed.**</span></span> <span data-ttu-id="7efbd-199">(11)</span><span class="sxs-lookup"><span data-stu-id="7efbd-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7efbd-200">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7efbd-201">(12)</span><span class="sxs-lookup"><span data-stu-id="7efbd-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7efbd-202">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7efbd-203">(13)</span><span class="sxs-lookup"><span data-stu-id="7efbd-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7efbd-204">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7efbd-205">(14)</span><span class="sxs-lookup"><span data-stu-id="7efbd-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7efbd-206">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7efbd-207">(15)</span><span class="sxs-lookup"><span data-stu-id="7efbd-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7efbd-208">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7efbd-209">(16)</span><span class="sxs-lookup"><span data-stu-id="7efbd-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7efbd-210">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7efbd-211">(17)</span><span class="sxs-lookup"><span data-stu-id="7efbd-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7efbd-212">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7efbd-213">(18)</span><span class="sxs-lookup"><span data-stu-id="7efbd-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7efbd-214">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="7efbd-215">(19)</span><span class="sxs-lookup"><span data-stu-id="7efbd-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7efbd-216">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="7efbd-217">(20)</span><span class="sxs-lookup"><span data-stu-id="7efbd-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7efbd-218">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7efbd-219">(21)</span><span class="sxs-lookup"><span data-stu-id="7efbd-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7efbd-220">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-220">**This device is disabled.**</span></span> <span data-ttu-id="7efbd-221">(22)</span><span class="sxs-lookup"><span data-stu-id="7efbd-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7efbd-222">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7efbd-223">(23)</span><span class="sxs-lookup"><span data-stu-id="7efbd-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7efbd-224">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7efbd-225">(24)</span><span class="sxs-lookup"><span data-stu-id="7efbd-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7efbd-226">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7efbd-227">(25)</span><span class="sxs-lookup"><span data-stu-id="7efbd-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7efbd-228">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7efbd-229">(26)</span><span class="sxs-lookup"><span data-stu-id="7efbd-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7efbd-230">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7efbd-231">(27)</span><span class="sxs-lookup"><span data-stu-id="7efbd-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7efbd-232">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7efbd-233">(28)</span><span class="sxs-lookup"><span data-stu-id="7efbd-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7efbd-234">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7efbd-235">(29)</span><span class="sxs-lookup"><span data-stu-id="7efbd-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7efbd-236">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7efbd-237">(30)</span><span class="sxs-lookup"><span data-stu-id="7efbd-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7efbd-238">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="7efbd-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7efbd-239">31,5</span><span class="sxs-lookup"><span data-stu-id="7efbd-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7efbd-240">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="7efbd-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-241">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7efbd-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-243">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7efbd-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-244">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="7efbd-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7efbd-245">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-246">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7efbd-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-249">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7efbd-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-250">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7efbd-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7efbd-251">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7efbd-252">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-253">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7efbd-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-256">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7efbd-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-257">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7efbd-257">A textual description of the object.</span></span>

<span data-ttu-id="7efbd-258">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-259">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7efbd-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-262">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7efbd-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-263">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="7efbd-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7efbd-264">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-265">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="7efbd-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-266">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7efbd-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-268">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7efbd-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7efbd-269">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7efbd-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-273">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="7efbd-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7efbd-274">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7efbd-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-276">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7efbd-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-278">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7efbd-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-279">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7efbd-279">Indicates when the object was installed.</span></span> <span data-ttu-id="7efbd-280">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7efbd-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7efbd-281">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-282">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7efbd-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7efbd-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-285">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7efbd-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7efbd-286">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-287">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="7efbd-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-288">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7efbd-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-290">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="7efbd-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-291">Maximale Anzahl von direkt adressierbaren Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="7efbd-292">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-293">**Name**</span><span class="sxs-lookup"><span data-stu-id="7efbd-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-296">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7efbd-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-297">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7efbd-297">Label by which the object is known.</span></span> <span data-ttu-id="7efbd-298">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7efbd-299">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7efbd-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-303">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7efbd-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-304">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="7efbd-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7efbd-305">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7efbd-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="7efbd-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-307">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="7efbd-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-308">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7efbd-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-310">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="7efbd-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="7efbd-311">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7efbd-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7efbd-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-313">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7efbd-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7efbd-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-315">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7efbd-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="7efbd-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-317">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7efbd-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7efbd-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7efbd-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-319">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7efbd-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7efbd-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="7efbd-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-321">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="7efbd-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7efbd-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="7efbd-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-323">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="7efbd-324">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="7efbd-325">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7efbd-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7efbd-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="7efbd-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-327">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="7efbd-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7efbd-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="7efbd-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7efbd-329">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7efbd-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7efbd-330">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="7efbd-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-331">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7efbd-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-333">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7efbd-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7efbd-334">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="7efbd-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7efbd-335">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7efbd-336">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="7efbd-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7efbd-337">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-338">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="7efbd-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-339">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7efbd-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-341">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7efbd-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-342">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7efbd-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7efbd-343">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7efbd-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7efbd-344">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7efbd-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="7efbd-345">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="7efbd-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="7efbd-346">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="7efbd-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="7efbd-347">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="7efbd-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="7efbd-348">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="7efbd-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="7efbd-349">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="7efbd-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="7efbd-350">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="7efbd-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="7efbd-351">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="7efbd-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="7efbd-352">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="7efbd-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="7efbd-353">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="7efbd-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="7efbd-354">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="7efbd-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="7efbd-355">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="7efbd-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="7efbd-356">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="7efbd-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="7efbd-357">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="7efbd-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="7efbd-358">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="7efbd-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="7efbd-359">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="7efbd-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="7efbd-360">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="7efbd-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="7efbd-361">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="7efbd-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="7efbd-362">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="7efbd-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="7efbd-363">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="7efbd-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="7efbd-364">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="7efbd-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="7efbd-365">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="7efbd-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="7efbd-366">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="7efbd-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="7efbd-367">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="7efbd-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="7efbd-368">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="7efbd-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="7efbd-369">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="7efbd-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="7efbd-370">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="7efbd-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="7efbd-371">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="7efbd-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="7efbd-372">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="7efbd-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="7efbd-373">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="7efbd-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="7efbd-374">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="7efbd-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="7efbd-375">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="7efbd-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="7efbd-376">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="7efbd-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="7efbd-377">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="7efbd-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="7efbd-378">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="7efbd-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="7efbd-379">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="7efbd-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="7efbd-380">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="7efbd-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="7efbd-381">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="7efbd-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="7efbd-382">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="7efbd-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="7efbd-383">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="7efbd-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="7efbd-384">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="7efbd-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="7efbd-385">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="7efbd-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="7efbd-386">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="7efbd-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="7efbd-387">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="7efbd-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="7efbd-388">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="7efbd-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="7efbd-389">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="7efbd-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7efbd-390">**Status**</span><span class="sxs-lookup"><span data-stu-id="7efbd-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-393">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7efbd-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-394">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="7efbd-395">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7efbd-396">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7efbd-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7efbd-397">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="7efbd-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7efbd-398">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7efbd-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7efbd-399">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="7efbd-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7efbd-400">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7efbd-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7efbd-401">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7efbd-402">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7efbd-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7efbd-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7efbd-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7efbd-404">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7efbd-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7efbd-405">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7efbd-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7efbd-406">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7efbd-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7efbd-407">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7efbd-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7efbd-408">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7efbd-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7efbd-409">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7efbd-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7efbd-410">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7efbd-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7efbd-411">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7efbd-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7efbd-412">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7efbd-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7efbd-413">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7efbd-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7efbd-414">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7efbd-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7efbd-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7efbd-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-416">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7efbd-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-418">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7efbd-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-419">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7efbd-419">State of the logical device.</span></span> <span data-ttu-id="7efbd-420">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7efbd-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="7efbd-421">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7efbd-422">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7efbd-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7efbd-423">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7efbd-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7efbd-424">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7efbd-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7efbd-425">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="7efbd-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7efbd-426">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="7efbd-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7efbd-427">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7efbd-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-430">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7efbd-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-431">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7efbd-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="7efbd-432">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-433">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="7efbd-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7efbd-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-436">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7efbd-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-437">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7efbd-437">The scoping system's name.</span></span>

<span data-ttu-id="7efbd-438">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7efbd-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7efbd-439">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="7efbd-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efbd-440">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7efbd-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7efbd-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7efbd-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efbd-442">Datum und Uhrzeit der letzten zurück setzung des Controllers (heruntergefahren oder neu initialisiert).</span><span class="sxs-lookup"><span data-stu-id="7efbd-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7efbd-443">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7efbd-443">Remarks</span></span>

<span data-ttu-id="7efbd-444">Die **CIM- \_ Controller** Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7efbd-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7efbd-445">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7efbd-445">WMI does not implement this class.</span></span> <span data-ttu-id="7efbd-446">Informationen zu Klassen, die vom **CIM- \_ Controller** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="7efbd-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7efbd-447">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7efbd-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7efbd-448">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7efbd-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7efbd-449">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7efbd-449">Requirements</span></span>



| <span data-ttu-id="7efbd-450">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7efbd-450">Requirement</span></span> | <span data-ttu-id="7efbd-451">Wert</span><span class="sxs-lookup"><span data-stu-id="7efbd-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7efbd-452">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7efbd-452">Minimum supported client</span></span><br/> | <span data-ttu-id="7efbd-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7efbd-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7efbd-454">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7efbd-454">Minimum supported server</span></span><br/> | <span data-ttu-id="7efbd-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7efbd-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7efbd-456">Namespace</span><span class="sxs-lookup"><span data-stu-id="7efbd-456">Namespace</span></span><br/>                | <span data-ttu-id="7efbd-457">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7efbd-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7efbd-458">MOF</span><span class="sxs-lookup"><span data-stu-id="7efbd-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7efbd-459"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7efbd-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7efbd-460">DLL</span><span class="sxs-lookup"><span data-stu-id="7efbd-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7efbd-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7efbd-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7efbd-462">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7efbd-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efbd-463">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="7efbd-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

