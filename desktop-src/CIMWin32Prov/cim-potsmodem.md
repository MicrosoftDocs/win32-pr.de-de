---
description: Die CIM- \_ Klasse "potsmodem" stellt ein Gerät dar, das binäre Daten in Wellen Modulationen für die Sound basierte Übertragung übersetzt, indem eine Verbindung mit dem reinen Telefon System ("Pots") hergestellt wird.
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: CIM_POTSModem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958435"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="a70c2-103">CIM- \_ Klasse "potsmodem"</span><span class="sxs-lookup"><span data-stu-id="a70c2-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="a70c2-104">Die CIM-Klasse " **\_ potsmodem** " stellt ein Gerät dar, das binäre Daten in Wellen Modulationen für die Sound basierte Übertragung übersetzt, indem eine Verbindung mit dem reinen Telefon System ("Pots") hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a70c2-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a70c2-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a70c2-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a70c2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a70c2-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a70c2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a70c2-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70c2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a70c2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="a70c2-110">Member</span><span class="sxs-lookup"><span data-stu-id="a70c2-110">Members</span></span>

<span data-ttu-id="a70c2-111">Die CIM-Klasse " **\_ potsmodem** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a70c2-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="a70c2-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a70c2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a70c2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a70c2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a70c2-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="a70c2-114">Methods</span></span>

<span data-ttu-id="a70c2-115">Die CIM-Klasse " **\_ potsmodem** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="a70c2-116">Methode</span><span class="sxs-lookup"><span data-stu-id="a70c2-116">Method</span></span>                                                               | <span data-ttu-id="a70c2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a70c2-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a70c2-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="a70c2-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="a70c2-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a70c2-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="a70c2-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a70c2-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a70c2-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="a70c2-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a70c2-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a70c2-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a70c2-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a70c2-124">Properties</span></span>

<span data-ttu-id="a70c2-125">Die CIM-Klasse " **\_ potsmodem** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a70c2-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a70c2-126">**Beantwortungsmodus**</span><span class="sxs-lookup"><span data-stu-id="a70c2-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-129">Aktuelle automatische Antwort-oder Rückruf Einstellung für das Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-130">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-131">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a70c2-132">**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="a70c2-133">**Manuelle Antwort** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="a70c2-134">**Automatische Antwort** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="a70c2-135">**Automatische Antwort mit Rückruf** (5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-136">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="a70c2-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="a70c2-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-140">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-140">Availability and status of the device.</span></span>

<span data-ttu-id="a70c2-141">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a70c2-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a70c2-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a70c2-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a70c2-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="a70c2-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a70c2-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="a70c2-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a70c2-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="a70c2-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a70c2-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a70c2-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a70c2-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="a70c2-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a70c2-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="a70c2-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a70c2-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="a70c2-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a70c2-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="a70c2-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-155">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a70c2-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="a70c2-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-157">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a70c2-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a70c2-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a70c2-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-159">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a70c2-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="a70c2-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a70c2-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="a70c2-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-162">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a70c2-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="a70c2-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-164">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="a70c2-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a70c2-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="a70c2-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-166">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="a70c2-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a70c2-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="a70c2-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-168">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a70c2-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="a70c2-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-170">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="a70c2-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-171">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a70c2-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-174">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a70c2-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-175">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-175">Short textual description of the object.</span></span>

<span data-ttu-id="a70c2-176">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-177">**Compressioninfo**</span><span class="sxs-lookup"><span data-stu-id="a70c2-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-180">Die Eigenschaften der Datenkomprimierung für das Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-181">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-182">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="a70c2-183">**Keine Komprimierung** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="a70c2-184">**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="a70c2-185">**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-186">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="a70c2-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70c2-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-189">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a70c2-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-190">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a70c2-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a70c2-191">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a70c2-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a70c2-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-194">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a70c2-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a70c2-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a70c2-196">(1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-197">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a70c2-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a70c2-199">(2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a70c2-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a70c2-201">(3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-202">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a70c2-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a70c2-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a70c2-204">(4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-205">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a70c2-205">Device is not working properly.</span></span> <span data-ttu-id="a70c2-206">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a70c2-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a70c2-208">(5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-209">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a70c2-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a70c2-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a70c2-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="a70c2-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-212">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="a70c2-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a70c2-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a70c2-214">(7)</span><span class="sxs-lookup"><span data-stu-id="a70c2-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a70c2-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a70c2-216">(8)</span><span class="sxs-lookup"><span data-stu-id="a70c2-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-217">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a70c2-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a70c2-219">(9)</span><span class="sxs-lookup"><span data-stu-id="a70c2-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-220">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a70c2-220">Device is not working properly.</span></span> <span data-ttu-id="a70c2-221">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="a70c2-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a70c2-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a70c2-223">(10)</span><span class="sxs-lookup"><span data-stu-id="a70c2-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-224">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a70c2-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a70c2-226">(11)</span><span class="sxs-lookup"><span data-stu-id="a70c2-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-227">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="a70c2-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a70c2-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a70c2-229">(12)</span><span class="sxs-lookup"><span data-stu-id="a70c2-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-230">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a70c2-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a70c2-232">(13)</span><span class="sxs-lookup"><span data-stu-id="a70c2-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-233">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a70c2-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a70c2-235">(14)</span><span class="sxs-lookup"><span data-stu-id="a70c2-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-236">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a70c2-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a70c2-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a70c2-238">(15)</span><span class="sxs-lookup"><span data-stu-id="a70c2-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-239">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a70c2-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a70c2-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a70c2-241">(16)</span><span class="sxs-lookup"><span data-stu-id="a70c2-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-242">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a70c2-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a70c2-244">(17)</span><span class="sxs-lookup"><span data-stu-id="a70c2-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-245">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="a70c2-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a70c2-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a70c2-247">(18)</span><span class="sxs-lookup"><span data-stu-id="a70c2-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-248">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a70c2-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a70c2-250">(19)</span><span class="sxs-lookup"><span data-stu-id="a70c2-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a70c2-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a70c2-252">(20)</span><span class="sxs-lookup"><span data-stu-id="a70c2-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-253">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a70c2-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a70c2-255">(21)</span><span class="sxs-lookup"><span data-stu-id="a70c2-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-256">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="a70c2-256">System failure.</span></span> <span data-ttu-id="a70c2-257">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a70c2-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a70c2-258">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a70c2-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a70c2-260">(22)</span><span class="sxs-lookup"><span data-stu-id="a70c2-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-261">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a70c2-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a70c2-263">(23)</span><span class="sxs-lookup"><span data-stu-id="a70c2-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-264">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="a70c2-264">System failure.</span></span> <span data-ttu-id="a70c2-265">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a70c2-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a70c2-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a70c2-267">(24)</span><span class="sxs-lookup"><span data-stu-id="a70c2-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-268">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a70c2-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a70c2-270">(25)</span><span class="sxs-lookup"><span data-stu-id="a70c2-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-271">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a70c2-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a70c2-273">(26)</span><span class="sxs-lookup"><span data-stu-id="a70c2-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-274">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a70c2-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a70c2-276">(27)</span><span class="sxs-lookup"><span data-stu-id="a70c2-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-277">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a70c2-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a70c2-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a70c2-279">(28)</span><span class="sxs-lookup"><span data-stu-id="a70c2-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-280">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a70c2-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a70c2-282">(29)</span><span class="sxs-lookup"><span data-stu-id="a70c2-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-283">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-283">Device is disabled.</span></span> <span data-ttu-id="a70c2-284">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a70c2-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a70c2-286">(30)</span><span class="sxs-lookup"><span data-stu-id="a70c2-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-287">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a70c2-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a70c2-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="a70c2-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a70c2-289">31,5</span><span class="sxs-lookup"><span data-stu-id="a70c2-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-290">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a70c2-290">Device is not working properly.</span></span> <span data-ttu-id="a70c2-291">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-292">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="a70c2-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-293">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70c2-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-295">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a70c2-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-296">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a70c2-297">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-298">**Unterstützt**</span><span class="sxs-lookup"><span data-stu-id="a70c2-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-299">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a70c2-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-301">Länder oder Regionen, in denen das Modem betrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a70c2-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-302">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="a70c2-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-305">Das Land oder die Region, für das das Modem aktuell programmiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="a70c2-306">Wenn mehrere Länder oder Regionen unterstützt werden, definiert diese Eigenschaft, welche derzeit zur Verwendung ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-307">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a70c2-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-310">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a70c2-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-311">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a70c2-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a70c2-312">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a70c2-313">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-314">**Currentkennwörter**</span><span class="sxs-lookup"><span data-stu-id="a70c2-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-315">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a70c2-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-317">Aktuell definierte Kenn Wörter für das Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="a70c2-318">Dieses Array kann aus Sicherheitsgründen leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-319">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a70c2-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-322">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a70c2-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-323">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-323">Textual description of the object.</span></span>

<span data-ttu-id="a70c2-324">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-325">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a70c2-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-328">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a70c2-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-329">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="a70c2-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a70c2-330">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-331">**Dialtype**</span><span class="sxs-lookup"><span data-stu-id="a70c2-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-332">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-334">Der Typ des Wählens, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a70c2-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-335">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="a70c2-336">**Ton** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="a70c2-337">**Pulse** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-338">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="a70c2-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-339">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70c2-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-341">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a70c2-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a70c2-342">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-343">**Errorcontrolinfo**</span><span class="sxs-lookup"><span data-stu-id="a70c2-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-346">Fehlerkorrektur Merkmale des Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-347">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-348">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="a70c2-349">**Keine Fehlerkorrektur** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="a70c2-350">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="a70c2-351">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a70c2-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-355">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="a70c2-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a70c2-356">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="a70c2-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-358">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70c2-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-360">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="a70c2-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-361">Das Zeitlimit (in Sekunden) für die automatische Trennung der Telefonleitung, wenn keine Daten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="a70c2-362">Der Wert 0 (null) gibt an, dass dieses Feature vorhanden ist, aber nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a70c2-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-364">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a70c2-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-366">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a70c2-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-367">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-367">Date and time the object was installed.</span></span> <span data-ttu-id="a70c2-368">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a70c2-369">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a70c2-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-371">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70c2-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-373">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a70c2-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a70c2-374">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-375">**Maxbaudratetophon**</span><span class="sxs-lookup"><span data-stu-id="a70c2-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-376">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70c2-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-378">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="a70c2-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-379">Maximale einstellbare Kommunikationsgeschwindigkeit für den Zugriff auf das Telefonsystem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-380">**Maxbaudratetoserialport**</span><span class="sxs-lookup"><span data-stu-id="a70c2-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-381">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70c2-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-383">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="a70c2-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-384">Maximale einstellbare Kommunikationsgeschwindigkeit für den COM-Port für ein externes Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="a70c2-385">Geben Sie 0 (null) ein, wenn Sie nicht zutreffend sind.</span><span class="sxs-lookup"><span data-stu-id="a70c2-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-386">**Maxnumofkennwörter**</span><span class="sxs-lookup"><span data-stu-id="a70c2-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-387">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-389">Maximale Anzahl von Kenn Wörtern, die im Modem selbst definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a70c2-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="a70c2-390">Wenn diese Funktion nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="a70c2-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-391">**Modulationscheme**</span><span class="sxs-lookup"><span data-stu-id="a70c2-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-392">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-394">Das modulmodussystem des Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-395">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-396">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a70c2-397">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="a70c2-398">**Bell 103** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="a70c2-399">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="a70c2-400">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="a70c2-401">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="a70c2-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="a70c2-402">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="a70c2-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="a70c2-403">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="a70c2-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="a70c2-404">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="a70c2-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="a70c2-405">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="a70c2-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="a70c2-406">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="a70c2-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-407">**Name**</span><span class="sxs-lookup"><span data-stu-id="a70c2-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-408">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-410">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a70c2-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-411">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-411">Label by which the object is known.</span></span> <span data-ttu-id="a70c2-412">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a70c2-413">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a70c2-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-417">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a70c2-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-418">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="a70c2-419">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a70c2-420">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a70c2-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-421">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="a70c2-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-422">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70c2-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-424">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a70c2-425">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a70c2-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a70c2-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a70c2-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-430">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a70c2-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a70c2-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-432">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="a70c2-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a70c2-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-434">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a70c2-435">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a70c2-436">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a70c2-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a70c2-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="a70c2-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-438">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a70c2-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="a70c2-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a70c2-440">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a70c2-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-441">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="a70c2-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-442">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70c2-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-444">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a70c2-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a70c2-445">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="a70c2-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a70c2-446">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a70c2-447">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="a70c2-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="a70c2-448">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-449">**Ringsbeforeanswer**</span><span class="sxs-lookup"><span data-stu-id="a70c2-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-450">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a70c2-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-452">Anzahl von Ringen, bevor das Modem einen eingehenden-Rückruf antwortet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-453">**Speakervolumeingefo**</span><span class="sxs-lookup"><span data-stu-id="a70c2-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-454">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-456">Die Volumeebene der akustischen Töne aus dem Modem.</span><span class="sxs-lookup"><span data-stu-id="a70c2-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="a70c2-457">Beispielsweise kann das Volume "hoch", "Mittel" oder "niedrig" gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-458">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70c2-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-459">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a70c2-460">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="a70c2-461">**Hoch** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="a70c2-462">**Mittel** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="a70c2-463">**Niedrig** (5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="a70c2-464">**Aus** (6)</span><span class="sxs-lookup"><span data-stu-id="a70c2-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="a70c2-465">**Automatisch** (7)</span><span class="sxs-lookup"><span data-stu-id="a70c2-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-466">**Status**</span><span class="sxs-lookup"><span data-stu-id="a70c2-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-467">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-469">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a70c2-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-470">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-470">Current status of the object.</span></span> <span data-ttu-id="a70c2-471">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a70c2-472">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a70c2-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a70c2-473">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a70c2-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a70c2-474">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a70c2-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a70c2-475">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a70c2-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-476">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a70c2-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a70c2-477">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a70c2-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a70c2-478">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a70c2-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a70c2-479">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a70c2-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a70c2-480">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a70c2-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a70c2-481">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a70c2-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a70c2-482">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a70c2-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a70c2-483">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a70c2-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a70c2-484">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a70c2-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a70c2-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-486">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70c2-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-488">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a70c2-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-489">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70c2-489">State of the logical device.</span></span> <span data-ttu-id="a70c2-490">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a70c2-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a70c2-491">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a70c2-492">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70c2-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a70c2-493">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a70c2-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a70c2-494">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a70c2-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a70c2-495">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="a70c2-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a70c2-496">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="a70c2-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a70c2-497">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="a70c2-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-498">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70c2-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-500">**True** gibt an, dass das Modem Rückrufe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-501">**Supportssynchronousconnect**</span><span class="sxs-lookup"><span data-stu-id="a70c2-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-502">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70c2-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-504">Wenn **true**, synchron und asynchron, wird die Kommunikation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-505">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="a70c2-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-506">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-508">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a70c2-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-509">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a70c2-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="a70c2-510">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-511">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="a70c2-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-512">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70c2-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-514">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a70c2-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-515">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a70c2-515">Scoping system's name.</span></span>

<span data-ttu-id="a70c2-516">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70c2-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70c2-517">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="a70c2-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70c2-518">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a70c2-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a70c2-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70c2-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70c2-520">Datum und Uhrzeit des letzten zurück Setzens des Controllers.</span><span class="sxs-lookup"><span data-stu-id="a70c2-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="a70c2-521">Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a70c2-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a70c2-522">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a70c2-522">Remarks</span></span>

<span data-ttu-id="a70c2-523">Die CIM-Klasse " **\_ potsmodem** " ist von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a70c2-524">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a70c2-524">WMI does not implement this class.</span></span> <span data-ttu-id="a70c2-525">Informationen zu WMI-Klassen, die von **CIM \_ potsmodem** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="a70c2-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a70c2-526">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a70c2-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a70c2-527">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a70c2-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a70c2-528">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a70c2-528">Requirements</span></span>



| <span data-ttu-id="a70c2-529">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a70c2-529">Requirement</span></span> | <span data-ttu-id="a70c2-530">Wert</span><span class="sxs-lookup"><span data-stu-id="a70c2-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70c2-531">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a70c2-531">Minimum supported client</span></span><br/> | <span data-ttu-id="a70c2-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a70c2-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a70c2-533">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a70c2-533">Minimum supported server</span></span><br/> | <span data-ttu-id="a70c2-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a70c2-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a70c2-535">Namespace</span><span class="sxs-lookup"><span data-stu-id="a70c2-535">Namespace</span></span><br/>                | <span data-ttu-id="a70c2-536">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a70c2-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a70c2-537">MOF</span><span class="sxs-lookup"><span data-stu-id="a70c2-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a70c2-538"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a70c2-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a70c2-539">DLL</span><span class="sxs-lookup"><span data-stu-id="a70c2-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a70c2-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a70c2-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a70c2-541">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a70c2-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70c2-542">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a70c2-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

