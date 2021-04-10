---
description: Die Win32- \_ WMI-Klasse "potsmodem" stellt die Dienste und Merkmale eines Modem-Modem (Plain Old Telefon Service) auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Win32_POTSModem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861183"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="21940-103">Win32- \_ Klasse "potsmodem"</span><span class="sxs-lookup"><span data-stu-id="21940-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="21940-104">Die Win32- [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **\_ potsmodem** " stellt die Dienste und Merkmale eines Modem-Modem (Plain Old Telefon Service) auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="21940-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21940-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="21940-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="21940-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="21940-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21940-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="21940-108">Member</span><span class="sxs-lookup"><span data-stu-id="21940-108">Members</span></span>

<span data-ttu-id="21940-109">Die Win32-Klasse " **\_ potsmodem** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="21940-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="21940-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="21940-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="21940-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21940-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="21940-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="21940-112">Methods</span></span>

<span data-ttu-id="21940-113">Die Win32-Klasse " **\_ potsmodem** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="21940-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="21940-114">Methode</span><span class="sxs-lookup"><span data-stu-id="21940-114">Method</span></span>            | <span data-ttu-id="21940-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21940-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21940-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="21940-116">**Reset**</span></span>         | <span data-ttu-id="21940-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="21940-117">Not implemented.</span></span> <span data-ttu-id="21940-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ potsmodem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="21940-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="21940-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="21940-119">**SetPowerState**</span></span> | <span data-ttu-id="21940-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="21940-120">Not implemented.</span></span> <span data-ttu-id="21940-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ potsmodem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="21940-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="21940-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21940-122">Properties</span></span>

<span data-ttu-id="21940-123">Die Win32-Klasse " **\_ potsmodem** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21940-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21940-124">**Beantwortungsmodus**</span><span class="sxs-lookup"><span data-stu-id="21940-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-127">Aktuelle automatische Antwort oder Rückruf Einstellung für das Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="21940-128">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-129">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-130">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21940-131">**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="21940-132">**Manuelle Antwort** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="21940-133">**Automatische Antwort** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="21940-134">**Automatische Antwort mit Rückruf** (5)</span><span class="sxs-lookup"><span data-stu-id="21940-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="21940-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-138">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| AttachedTo")</span><span class="sxs-lookup"><span data-stu-id="21940-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="21940-139">Der Port, an den das POTS-Modem angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="21940-140">Beispiel: "COM1"</span><span class="sxs-lookup"><span data-stu-id="21940-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="21940-141">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="21940-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-144">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="21940-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="21940-145">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="21940-145">Availability and status of the device.</span></span>

<span data-ttu-id="21940-146">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="21940-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21940-150">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="21940-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="21940-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="21940-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="21940-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21940-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="21940-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="21940-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="21940-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="21940-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="21940-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="21940-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="21940-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21940-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="21940-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="21940-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="21940-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="21940-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="21940-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="21940-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="21940-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="21940-161">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="21940-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="21940-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="21940-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="21940-163">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="21940-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="21940-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="21940-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="21940-165">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="21940-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="21940-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="21940-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="21940-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="21940-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="21940-168">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="21940-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="21940-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="21940-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="21940-170">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="21940-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="21940-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="21940-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="21940-172">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="21940-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="21940-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="21940-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="21940-174">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="21940-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="21940-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="21940-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="21940-176">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="21940-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-177">**BlindOff**</span><span class="sxs-lookup"><span data-stu-id="21940-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-180">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOff")</span><span class="sxs-lookup"><span data-stu-id="21940-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="21940-181">Befehls Zeichenfolge, mit der ein Wählton vor dem einwählen erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="21940-182">Beispiel: "X4"</span><span class="sxs-lookup"><span data-stu-id="21940-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="21940-183">**Blinker**</span><span class="sxs-lookup"><span data-stu-id="21940-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-186">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOn")</span><span class="sxs-lookup"><span data-stu-id="21940-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="21940-187">Befehls Zeichenfolge, die verwendet wird, um zu wählen, ob ein Wählton vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="21940-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="21940-188">Beispiel: "X3"</span><span class="sxs-lookup"><span data-stu-id="21940-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="21940-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="21940-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-192">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="21940-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="21940-193">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21940-193">Short description of the object.</span></span>

<span data-ttu-id="21940-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="21940-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-198">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| compatibilityflags")</span><span class="sxs-lookup"><span data-stu-id="21940-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="21940-199">Alle Modem Verbindungsprotokolle, mit denen dieses Modem Gerät kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="21940-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="21940-200">**Compressioninfo**</span><span class="sxs-lookup"><span data-stu-id="21940-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-201">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-203">Die Eigenschaften der Datenkomprimierung für das Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="21940-204">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="21940-207">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="21940-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="21940-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Keine Komprimierung** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="21940-209">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="21940-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="21940-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21940-211">Keine Komprimierung</span><span class="sxs-lookup"><span data-stu-id="21940-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="21940-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="21940-213">MNP 5</span><span class="sxs-lookup"><span data-stu-id="21940-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="21940-214"><span id="5"></span>**5@@**</span><span class="sxs-lookup"><span data-stu-id="21940-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="21940-215">V. 42 bis</span><span class="sxs-lookup"><span data-stu-id="21940-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-216">**Komprimierbar**</span><span class="sxs-lookup"><span data-stu-id="21940-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-219">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Compression \_ Off")</span><span class="sxs-lookup"><span data-stu-id="21940-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="21940-220">Befehls Zeichenfolge zum Deaktivieren der Hardware Datenkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="21940-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="21940-221">Beispiel: "S46 = 136"</span><span class="sxs-lookup"><span data-stu-id="21940-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="21940-222">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="21940-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-225">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Compression \_ on")</span><span class="sxs-lookup"><span data-stu-id="21940-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="21940-226">Befehls Zeichenfolge zum Aktivieren der Hardware Datenkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="21940-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="21940-227">Beispiel: "S46 = 138"</span><span class="sxs-lookup"><span data-stu-id="21940-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="21940-228">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="21940-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-229">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21940-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21940-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-231">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="21940-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="21940-232">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="21940-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="21940-233">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="21940-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="21940-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="21940-235"> (0)</span><span class="sxs-lookup"><span data-stu-id="21940-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="21940-236">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="21940-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="21940-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="21940-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="21940-238">(1)</span><span class="sxs-lookup"><span data-stu-id="21940-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="21940-239">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="21940-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="21940-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="21940-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="21940-241">(2)</span><span class="sxs-lookup"><span data-stu-id="21940-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="21940-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="21940-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="21940-243">(3)</span><span class="sxs-lookup"><span data-stu-id="21940-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="21940-244">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="21940-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="21940-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="21940-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="21940-246">(4)</span><span class="sxs-lookup"><span data-stu-id="21940-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="21940-247">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="21940-247">Device is not working properly.</span></span> <span data-ttu-id="21940-248">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="21940-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="21940-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="21940-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="21940-250">(5)</span><span class="sxs-lookup"><span data-stu-id="21940-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="21940-251">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="21940-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="21940-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="21940-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="21940-253"> (6)</span><span class="sxs-lookup"><span data-stu-id="21940-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="21940-254">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="21940-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="21940-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="21940-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="21940-256">(7)</span><span class="sxs-lookup"><span data-stu-id="21940-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="21940-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="21940-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="21940-258">(8)</span><span class="sxs-lookup"><span data-stu-id="21940-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="21940-259">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="21940-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="21940-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="21940-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="21940-261">(9)</span><span class="sxs-lookup"><span data-stu-id="21940-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="21940-262">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="21940-262">Device is not working properly.</span></span> <span data-ttu-id="21940-263">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="21940-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="21940-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="21940-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="21940-265">(10)</span><span class="sxs-lookup"><span data-stu-id="21940-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="21940-266">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="21940-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="21940-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="21940-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="21940-268">(11)</span><span class="sxs-lookup"><span data-stu-id="21940-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="21940-269">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="21940-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="21940-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="21940-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="21940-271">(12)</span><span class="sxs-lookup"><span data-stu-id="21940-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="21940-272">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="21940-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="21940-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="21940-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="21940-274">(13)</span><span class="sxs-lookup"><span data-stu-id="21940-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="21940-275">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="21940-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="21940-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="21940-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="21940-277">(14)</span><span class="sxs-lookup"><span data-stu-id="21940-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="21940-278">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="21940-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="21940-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="21940-280">(15)</span><span class="sxs-lookup"><span data-stu-id="21940-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="21940-281">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="21940-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="21940-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="21940-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="21940-283">(16)</span><span class="sxs-lookup"><span data-stu-id="21940-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="21940-284">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21940-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="21940-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="21940-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="21940-286">(17)</span><span class="sxs-lookup"><span data-stu-id="21940-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="21940-287">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="21940-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="21940-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="21940-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="21940-289">(18)</span><span class="sxs-lookup"><span data-stu-id="21940-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="21940-290">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="21940-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="21940-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="21940-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="21940-292">(19)</span><span class="sxs-lookup"><span data-stu-id="21940-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="21940-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="21940-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="21940-294">(20)</span><span class="sxs-lookup"><span data-stu-id="21940-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="21940-295">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="21940-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="21940-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="21940-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="21940-297">(21)</span><span class="sxs-lookup"><span data-stu-id="21940-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="21940-298">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="21940-298">System failure.</span></span> <span data-ttu-id="21940-299">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="21940-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="21940-300">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="21940-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="21940-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="21940-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="21940-302">(22)</span><span class="sxs-lookup"><span data-stu-id="21940-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="21940-303">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="21940-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="21940-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="21940-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="21940-305">(23)</span><span class="sxs-lookup"><span data-stu-id="21940-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="21940-306">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="21940-306">System failure.</span></span> <span data-ttu-id="21940-307">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="21940-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="21940-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="21940-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="21940-309">(24)</span><span class="sxs-lookup"><span data-stu-id="21940-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="21940-310">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="21940-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="21940-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="21940-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="21940-312">(25)</span><span class="sxs-lookup"><span data-stu-id="21940-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="21940-313">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="21940-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="21940-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="21940-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="21940-315">(26)</span><span class="sxs-lookup"><span data-stu-id="21940-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="21940-316">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="21940-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="21940-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="21940-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="21940-318">(27)</span><span class="sxs-lookup"><span data-stu-id="21940-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="21940-319">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="21940-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="21940-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="21940-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="21940-321">(28)</span><span class="sxs-lookup"><span data-stu-id="21940-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="21940-322">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="21940-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="21940-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="21940-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="21940-324">(29)</span><span class="sxs-lookup"><span data-stu-id="21940-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="21940-325">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="21940-325">Device is disabled.</span></span> <span data-ttu-id="21940-326">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="21940-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="21940-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="21940-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="21940-328">(30)</span><span class="sxs-lookup"><span data-stu-id="21940-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="21940-329">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="21940-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="21940-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="21940-331">31,5</span><span class="sxs-lookup"><span data-stu-id="21940-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="21940-332">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="21940-332">Device is not working properly.</span></span> <span data-ttu-id="21940-333">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="21940-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-334">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="21940-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-335">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21940-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21940-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-337">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="21940-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="21940-338">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="21940-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="21940-339">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-340">**ConfigurationDialog**</span><span class="sxs-lookup"><span data-stu-id="21940-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-341">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-343">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ConfigDialog")</span><span class="sxs-lookup"><span data-stu-id="21940-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="21940-344">Die Modem Initialisierungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="21940-344">Modem initialization string.</span></span> <span data-ttu-id="21940-345">Diese Eigenschaft besteht aus Befehls Zeichenfolgen aus anderen Eigenschaften dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="21940-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="21940-346">**Unterstützt**</span><span class="sxs-lookup"><span data-stu-id="21940-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-347">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="21940-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="21940-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-349">Array von Ländern/Regionen, in denen das Modem betrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="21940-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="21940-350">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-351">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="21940-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-354">Das Land bzw. die Region, für das das Modem aktuell programmiert ist.</span><span class="sxs-lookup"><span data-stu-id="21940-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="21940-355">Wenn mehrere Länder/Regionen unterstützt werden, definiert diese Eigenschaft, welche derzeit zur Verwendung ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="21940-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="21940-356">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-357">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="21940-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-360">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="21940-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="21940-361">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="21940-362">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="21940-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="21940-363">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-364">**Currentkennwörter**</span><span class="sxs-lookup"><span data-stu-id="21940-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-365">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="21940-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="21940-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-367">Liste der aktuell definierten Kenn Wörter für das Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="21940-368">Dieses Array kann aus Sicherheitsgründen leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="21940-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="21940-369">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="21940-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-371">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="21940-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="21940-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-373">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span><span class="sxs-lookup"><span data-stu-id="21940-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="21940-374">Steuerungseinstellungen für ein serielles Kommunikationsgerät, in diesem Fall das Modem Gerät.</span><span class="sxs-lookup"><span data-stu-id="21940-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="21940-375">**Standard**</span><span class="sxs-lookup"><span data-stu-id="21940-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-376">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="21940-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="21940-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-378">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| default")</span><span class="sxs-lookup"><span data-stu-id="21940-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="21940-379">**True** gibt an, dass dieses Modem Modem das Standard Modem auf dem Computersystem ist, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="21940-380">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21940-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-383">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="21940-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="21940-384">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21940-384">Description of the object.</span></span>

<span data-ttu-id="21940-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-386">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="21940-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-389">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="21940-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="21940-390">Eindeutiger Bezeichner dieses POTS-Modem von anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="21940-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="21940-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-392">**DeviceLoader**</span><span class="sxs-lookup"><span data-stu-id="21940-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-393">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-395">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DevLoader")</span><span class="sxs-lookup"><span data-stu-id="21940-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="21940-396">Der Name des Geräte Lade Moduls für das Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="21940-397">Ein Geräte Lade Modul lädt und verwaltet Gerätetreiber und Enumeratoren für ein bestimmtes Gerät.</span><span class="sxs-lookup"><span data-stu-id="21940-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="21940-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="21940-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-401">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DeviceType")</span><span class="sxs-lookup"><span data-stu-id="21940-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="21940-402">Physischer Typ des Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-402">Physical type of the modem.</span></span>

<span data-ttu-id="21940-403">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="21940-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="21940-404">"Null Modem"</span><span class="sxs-lookup"><span data-stu-id="21940-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="21940-405">"Internes Modem"</span><span class="sxs-lookup"><span data-stu-id="21940-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="21940-406">"Externes Modem"</span><span class="sxs-lookup"><span data-stu-id="21940-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="21940-407">"PCMCIA-Modem"</span><span class="sxs-lookup"><span data-stu-id="21940-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="21940-408">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="21940-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="21940-409">**Null Modem** ("Null Modem")</span><span class="sxs-lookup"><span data-stu-id="21940-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="21940-410">**Internes Modem** ("internes Modem")</span><span class="sxs-lookup"><span data-stu-id="21940-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="21940-411">**Externes Modem** ("externes Modem")</span><span class="sxs-lookup"><span data-stu-id="21940-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="21940-412">**PCMCIA-Modem** ("PCMCIA-Modem")</span><span class="sxs-lookup"><span data-stu-id="21940-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-413">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="21940-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-414">**Dialtype**</span><span class="sxs-lookup"><span data-stu-id="21940-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-415">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-417">Der Typ der verwendeten Wähl Methode.</span><span class="sxs-lookup"><span data-stu-id="21940-417">Type of dialing method used.</span></span>

<span data-ttu-id="21940-418">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-419">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="21940-420">**Ton** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="21940-421">**Pulse** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-422">**Driverdate**</span><span class="sxs-lookup"><span data-stu-id="21940-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-423">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="21940-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="21940-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-425">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| driverdate")</span><span class="sxs-lookup"><span data-stu-id="21940-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="21940-426">Das Datum des Modem Treibers.</span><span class="sxs-lookup"><span data-stu-id="21940-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="21940-427">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="21940-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-428">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21940-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21940-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-430">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="21940-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="21940-431">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-432">**ErrorControlForced**</span><span class="sxs-lookup"><span data-stu-id="21940-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-435">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ Forced")</span><span class="sxs-lookup"><span data-stu-id="21940-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="21940-436">Befehls Zeichenfolge, die beim Herstellen einer Verbindung zum Aktivieren der Fehlerkorrektur Steuerung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="21940-437">Dies erhöht die Zuverlässigkeit der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="21940-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="21940-438">Beispiel: "+ Q5S36 = 4s48 = 7"</span><span class="sxs-lookup"><span data-stu-id="21940-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="21940-439">**Errorcontrolinfo**</span><span class="sxs-lookup"><span data-stu-id="21940-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-440">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-442">Fehlerkorrektur Merkmale des Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="21940-443">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-444">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-445">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="21940-446">**Keine Fehlerkorrektur** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="21940-447">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="21940-448">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-449">**ErrorControlOff**</span><span class="sxs-lookup"><span data-stu-id="21940-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-450">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-452">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ Off")</span><span class="sxs-lookup"><span data-stu-id="21940-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="21940-453">Befehls Zeichenfolge zum Deaktivieren der Fehler Steuerung.</span><span class="sxs-lookup"><span data-stu-id="21940-453">Command string used to disable error control.</span></span>

<span data-ttu-id="21940-454">Beispiel: "+ Q6S36 = 3s48 = 128"</span><span class="sxs-lookup"><span data-stu-id="21940-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="21940-455">**ErrorControlOn**</span><span class="sxs-lookup"><span data-stu-id="21940-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-456">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-458">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ on")</span><span class="sxs-lookup"><span data-stu-id="21940-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="21940-459">Befehls Zeichenfolge zum Aktivieren der Fehler Steuerung.</span><span class="sxs-lookup"><span data-stu-id="21940-459">Command string used to enable error control.</span></span>

<span data-ttu-id="21940-460">Beispiel: "+ Q5S36 = 7s48 = 7"</span><span class="sxs-lookup"><span data-stu-id="21940-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="21940-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="21940-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-462">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-464">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. getroffenen Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="21940-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="21940-465">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-466">**FlowControlHard**</span><span class="sxs-lookup"><span data-stu-id="21940-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-467">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-469">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Hard")</span><span class="sxs-lookup"><span data-stu-id="21940-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="21940-470">Befehls Zeichenfolge, mit der die Hardware Fluss Steuerung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="21940-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="21940-471">Die Fluss Steuerung besteht aus Signalen, die zwischen Computern gesendet werden, die sicherstellen, dass beide Computer zum übertragen oder empfangen von Daten bereit sind</span><span class="sxs-lookup"><span data-stu-id="21940-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="21940-472">Beispiel: "&K1"</span><span class="sxs-lookup"><span data-stu-id="21940-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="21940-473">**FlowControlOff**</span><span class="sxs-lookup"><span data-stu-id="21940-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-476">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Off")</span><span class="sxs-lookup"><span data-stu-id="21940-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="21940-477">Befehls Zeichenfolge zum Deaktivieren der Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="21940-477">Command string used to disable flow control.</span></span> <span data-ttu-id="21940-478">Die Fluss Steuerung besteht aus Signalen, die zwischen Computern gesendet werden, die sicherstellen, dass beide Computer zum übertragen oder empfangen von Daten bereit sind</span><span class="sxs-lookup"><span data-stu-id="21940-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="21940-479">Beispiel: "&K0"</span><span class="sxs-lookup"><span data-stu-id="21940-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="21940-480">**Flowcontrolsoft**</span><span class="sxs-lookup"><span data-stu-id="21940-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-483">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Soft")</span><span class="sxs-lookup"><span data-stu-id="21940-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="21940-484">Befehls Zeichenfolge zum Aktivieren der Software Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="21940-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="21940-485">Die Fluss Steuerung besteht aus Signalen, die zwischen Computern gesendet werden, die sicherstellen, dass beide Computer zum übertragen oder empfangen von Daten bereit sind</span><span class="sxs-lookup"><span data-stu-id="21940-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="21940-486">Beispiel: "&K2"</span><span class="sxs-lookup"><span data-stu-id="21940-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="21940-487">**Inactivityscale**</span><span class="sxs-lookup"><span data-stu-id="21940-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-488">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-490">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| inactivityscale")</span><span class="sxs-lookup"><span data-stu-id="21940-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="21940-491">Multiplikator, der mit der **InactivityTimeout** -Eigenschaft verwendet wird, um den Timeout Zeitraum einer Verbindung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="21940-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="21940-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="21940-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-493">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21940-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21940-494">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-495">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="21940-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="21940-496">Das Zeitlimit (in Sekunden) für die automatische Trennung der Telefonleitung, wenn keine Daten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="21940-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="21940-497">Der Wert 0 (null) gibt an, dass dieses Feature vorhanden ist, aber nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="21940-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="21940-498">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="21940-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-500">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21940-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21940-501">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-502">Index Nummer für dieses Modem Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="21940-503">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="21940-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="21940-504">**Indexex**</span><span class="sxs-lookup"><span data-stu-id="21940-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-505">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-506">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-507">Die Geräte Instanz-ID für dieses Modem Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="21940-508">Beispiel: "1&08"</span><span class="sxs-lookup"><span data-stu-id="21940-508">Example: "1&08"</span></span>

<span data-ttu-id="21940-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist ab Windows Server 2016 und Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21940-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="21940-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="21940-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-511">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="21940-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="21940-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-513">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="21940-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="21940-514">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="21940-514">Date and time the object was installed.</span></span> <span data-ttu-id="21940-515">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="21940-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="21940-516">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-517">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="21940-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-518">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21940-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21940-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-520">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="21940-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="21940-521">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-522">**Maxbaudratetophon**</span><span class="sxs-lookup"><span data-stu-id="21940-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-523">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21940-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21940-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-525">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="21940-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="21940-526">Maximale einstellbare Kommunikationsgeschwindigkeit für den Zugriff auf das Telefonsystem.</span><span class="sxs-lookup"><span data-stu-id="21940-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="21940-527">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-528">**Maxbaudratetoserialport**</span><span class="sxs-lookup"><span data-stu-id="21940-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-529">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21940-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21940-530">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-531">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="21940-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="21940-532">Maximale einstellbare Kommunikationsgeschwindigkeit für den COM-Port für ein externes Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="21940-533">Geben Sie 0 (null) ein, wenn Sie nicht zutreffend sind.</span><span class="sxs-lookup"><span data-stu-id="21940-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="21940-534">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-535">**Maxnumofkennwörter**</span><span class="sxs-lookup"><span data-stu-id="21940-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-536">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-537">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-538">Anzahl der Kenn Wörter, die im Modem selbst definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="21940-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="21940-539">Wenn diese Funktion nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="21940-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="21940-540">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-541">**Modell**</span><span class="sxs-lookup"><span data-stu-id="21940-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-542">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-543">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-544">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Model")</span><span class="sxs-lookup"><span data-stu-id="21940-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="21940-545">Modell dieses Töpfe-Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-545">Model of this POTS modem.</span></span>

<span data-ttu-id="21940-546">Beispiel: "Sport-56K extern"</span><span class="sxs-lookup"><span data-stu-id="21940-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="21940-547">**Modeminspath**</span><span class="sxs-lookup"><span data-stu-id="21940-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-548">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-549">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-550">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| INFPath")</span><span class="sxs-lookup"><span data-stu-id="21940-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="21940-551">Der Pfad zur INF-Datei dieses Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="21940-552">Diese Datei enthält Initialisierungs Informationen für das Modem und den Treiber.</span><span class="sxs-lookup"><span data-stu-id="21940-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="21940-553">Beispiel: "C: \\ Windows \\ INF"</span><span class="sxs-lookup"><span data-stu-id="21940-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="21940-554">**Modeminf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="21940-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-555">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-556">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-557">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="21940-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="21940-558">Der Name des Abschnitts in der INF-Datei des Modem, der Informationen zum Modem enthält.</span><span class="sxs-lookup"><span data-stu-id="21940-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="21940-559">**ModulationBell**</span><span class="sxs-lookup"><span data-stu-id="21940-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-560">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-561">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-562">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Modulation \_ Bell")</span><span class="sxs-lookup"><span data-stu-id="21940-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="21940-563">Befehls Zeichenfolge, die das Modem anweist, Glocken Modulationen für 300 und 1200 bit/s zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="21940-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="21940-564">Beispiel: "B1"</span><span class="sxs-lookup"><span data-stu-id="21940-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="21940-565">**ModulationCCITT**</span><span class="sxs-lookup"><span data-stu-id="21940-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-566">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-567">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-568">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Modulation \_ CCITT")</span><span class="sxs-lookup"><span data-stu-id="21940-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="21940-569">Befehls Zeichenfolge, die das Modem anweist, die CCITT-Modulationen für 300 und 1200 bit/s zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="21940-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="21940-570">Beispiel: "B0"</span><span class="sxs-lookup"><span data-stu-id="21940-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="21940-571">**Modulationscheme**</span><span class="sxs-lookup"><span data-stu-id="21940-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-572">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-573">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-574">Das modulmodussystem des Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="21940-575">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-576">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-577">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21940-578">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="21940-579">**Bell 103** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="21940-580">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="21940-581">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="21940-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="21940-582">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="21940-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="21940-583">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="21940-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="21940-584">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="21940-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="21940-585">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="21940-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="21940-586">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="21940-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="21940-587">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="21940-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-588">**Name**</span><span class="sxs-lookup"><span data-stu-id="21940-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-589">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-590">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-591">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="21940-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="21940-592">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="21940-592">Label by which the object is known.</span></span> <span data-ttu-id="21940-593">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="21940-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="21940-594">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="21940-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-596">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-597">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-598">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="21940-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="21940-599">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="21940-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="21940-600">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="21940-601">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="21940-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="21940-602">**Portsubclass**</span><span class="sxs-lookup"><span data-stu-id="21940-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-603">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-604">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-605">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| portsubclass"), **value** ("Parallel Port", "Serial Port", "Modem")</span><span class="sxs-lookup"><span data-stu-id="21940-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="21940-606">Die Definition des für dieses Modem verwendeten Ports.</span><span class="sxs-lookup"><span data-stu-id="21940-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="21940-607">("00")</span><span class="sxs-lookup"><span data-stu-id="21940-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="21940-608">Paralleler Port</span><span class="sxs-lookup"><span data-stu-id="21940-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="21940-609">("01")</span><span class="sxs-lookup"><span data-stu-id="21940-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="21940-610">Serieller Port</span><span class="sxs-lookup"><span data-stu-id="21940-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="21940-611">("02")</span><span class="sxs-lookup"><span data-stu-id="21940-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="21940-612">Modem</span><span class="sxs-lookup"><span data-stu-id="21940-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-613">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="21940-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-614">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="21940-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21940-615">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-616">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="21940-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="21940-617">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21940-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21940-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="21940-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21940-622">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21940-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="21940-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="21940-624">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="21940-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="21940-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="21940-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="21940-626">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21940-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="21940-627">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="21940-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="21940-628">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="21940-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="21940-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="21940-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="21940-630">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="21940-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="21940-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="21940-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="21940-632">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="21940-632">Timed Power-On Supported</span></span>

<span data-ttu-id="21940-633">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="21940-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-634">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="21940-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-635">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21940-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21940-636">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-637">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="21940-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="21940-638">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="21940-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="21940-639">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-640">**Präfix**</span><span class="sxs-lookup"><span data-stu-id="21940-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-641">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-642">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-643">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| prefix")</span><span class="sxs-lookup"><span data-stu-id="21940-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="21940-644">Ein Präfix, das für den Zugriff auf eine externe Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="21940-645">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="21940-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-646">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="21940-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="21940-647">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-648">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Properties")</span><span class="sxs-lookup"><span data-stu-id="21940-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="21940-649">Liste aller Eigenschaften (und ihrer Werte) für dieses Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="21940-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="21940-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-651">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-652">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-653">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| providerName")</span><span class="sxs-lookup"><span data-stu-id="21940-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="21940-654">Netzwerkpfad zu dem Computer, der die Modem Dienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="21940-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="21940-655">**Puls**</span><span class="sxs-lookup"><span data-stu-id="21940-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-656">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-657">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-658">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Pulse")</span><span class="sxs-lookup"><span data-stu-id="21940-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="21940-659">Befehls Zeichenfolge, die das Modem anweist, den Pulsmodus für die Wahl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="21940-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="21940-660">Pulse-Wähl ist für Telefon Zeilen erforderlich, die keine Unterschiede in der Ton Behandlung verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="21940-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="21940-661">Beispiel: "P"</span><span class="sxs-lookup"><span data-stu-id="21940-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="21940-662">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="21940-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-663">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-664">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-665">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) (Reset), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Reset")</span><span class="sxs-lookup"><span data-stu-id="21940-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="21940-666">Befehls Zeichenfolge, mit der das Modem für den nächsten-Befehl zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="21940-667">Beispiel: "at&F"</span><span class="sxs-lookup"><span data-stu-id="21940-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="21940-668">**ResponsesKeyName**</span><span class="sxs-lookup"><span data-stu-id="21940-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-669">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-670">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-671">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ResponsesKeyName")</span><span class="sxs-lookup"><span data-stu-id="21940-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="21940-672">Antwort: dieses Modem meldet möglicherweise während des Verbindungs Vorgangs an das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="21940-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="21940-673">Die ersten beiden Zeichen geben den Typ der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="21940-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="21940-674">Die beiden zweiten Zeichen geben Informationen über die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="21940-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="21940-675">Die beiden zweiten Zeichen werden nur für den Aushandlungs Status oder Verbindungs Antwort Codes verwendet.</span><span class="sxs-lookup"><span data-stu-id="21940-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="21940-676">Mit den nächsten acht Zeichen wird die in Bits pro Sekunde (Bit/s) ausgehandelte Modem-zu-Modem-Zeilen Geschwindigkeit angegeben.</span><span class="sxs-lookup"><span data-stu-id="21940-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="21940-677">Die Zeichen stellen ein 32-Bit-Format ohne Vorzeichen ohne Vorzeichen dar (Byte und Wort umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="21940-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="21940-678">Die letzten acht Zeichen zeigen an, dass das Modem zu einer anderen Port-oder DTE-Geschwindigkeit (Data Terminal Equipment) wechselt.</span><span class="sxs-lookup"><span data-stu-id="21940-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="21940-679">Normalerweise wird dieses Feld nicht verwendet, da Modems Verbindungen mit gesperrter Port Geschwindigkeit unabhängig von der Geschwindigkeit von Modem zu Modem oder DCE (Data Communications Equipment) herstellen.</span><span class="sxs-lookup"><span data-stu-id="21940-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="21940-680">**Ringsbeforeanswer**</span><span class="sxs-lookup"><span data-stu-id="21940-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-681">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="21940-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="21940-682">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-683">Anzahl von Ringen, bevor das Modem einen eingehenden-Rückruf antwortet.</span><span class="sxs-lookup"><span data-stu-id="21940-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="21940-684">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-685">**Speakermudedial**</span><span class="sxs-lookup"><span data-stu-id="21940-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-686">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-687">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-688">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| speakermudedial")</span><span class="sxs-lookup"><span data-stu-id="21940-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="21940-689">Befehls Zeichenfolge, die verwendet wird, um den Modem Sprecher nach dem einblenden einer Zahl zu aktivieren und den Sprecher zu deaktivieren, wenn eine Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="21940-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="21940-690">Beispiel: "M1"</span><span class="sxs-lookup"><span data-stu-id="21940-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="21940-691">**SpeakerModeOff**</span><span class="sxs-lookup"><span data-stu-id="21940-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-692">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-693">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-694">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOff")</span><span class="sxs-lookup"><span data-stu-id="21940-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="21940-695">Befehls Zeichenfolge, mit der der Modem Sprecher ausgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="21940-696">Beispiel: "M0"</span><span class="sxs-lookup"><span data-stu-id="21940-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="21940-697">**Speakermudeon**</span><span class="sxs-lookup"><span data-stu-id="21940-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-698">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-699">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-700">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| speakermudeon")</span><span class="sxs-lookup"><span data-stu-id="21940-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="21940-701">Befehls Zeichenfolge, die zum Einschalten des Modem spreches verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21940-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="21940-702">Beispiel: "m2"</span><span class="sxs-lookup"><span data-stu-id="21940-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="21940-703">**SpeakerModeSetup**</span><span class="sxs-lookup"><span data-stu-id="21940-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-704">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-705">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-706">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeSetup")</span><span class="sxs-lookup"><span data-stu-id="21940-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="21940-707">Befehls Zeichenfolge, die verwendet wird, um das Modem anzuweisen, den Sprecher zu aktivieren (bis eine Verbindung hergestellt ist).</span><span class="sxs-lookup"><span data-stu-id="21940-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="21940-708">Beispiel: "M3"</span><span class="sxs-lookup"><span data-stu-id="21940-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="21940-709">**SpeakerVolumeHigh**</span><span class="sxs-lookup"><span data-stu-id="21940-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-710">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-711">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-712">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| speakervolume \_ High")</span><span class="sxs-lookup"><span data-stu-id="21940-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="21940-713">Befehls Zeichenfolge, mit der der Modem Sprecher auf das höchste Volume festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="21940-714">Beispiel: "L3"</span><span class="sxs-lookup"><span data-stu-id="21940-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="21940-715">**Speakervolumeingefo**</span><span class="sxs-lookup"><span data-stu-id="21940-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-716">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-717">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-718">Beschreibt die Volumeebene der akustischen Töne aus dem Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="21940-719">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-720">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21940-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-721">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21940-722">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="21940-723">**Hoch** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="21940-724">**Mittel** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="21940-725">**Niedrig** (5)</span><span class="sxs-lookup"><span data-stu-id="21940-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="21940-726">**Aus** (6)</span><span class="sxs-lookup"><span data-stu-id="21940-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="21940-727">**Automatisch** (7)</span><span class="sxs-lookup"><span data-stu-id="21940-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-728">**SpeakerVolumeLow**</span><span class="sxs-lookup"><span data-stu-id="21940-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-729">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-730">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-731">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| speakervolume \_ Low")</span><span class="sxs-lookup"><span data-stu-id="21940-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="21940-732">Befehls Zeichenfolge, mit der der Modem Sprecher auf das niedrigste Volume festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="21940-733">Beispiel: "L1"</span><span class="sxs-lookup"><span data-stu-id="21940-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="21940-734">**SpeakerVolumeMed**</span><span class="sxs-lookup"><span data-stu-id="21940-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-735">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-736">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-737">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| speakervolume \_ Med")</span><span class="sxs-lookup"><span data-stu-id="21940-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="21940-738">Befehls Zeichenfolge, mit der der Modem Sprecher auf ein mittleres Volume festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="21940-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="21940-739">Beispiel: "L2"</span><span class="sxs-lookup"><span data-stu-id="21940-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="21940-740">**Status**</span><span class="sxs-lookup"><span data-stu-id="21940-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-741">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-742">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-743">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="21940-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="21940-744">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21940-744">Current status of the object.</span></span> <span data-ttu-id="21940-745">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="21940-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="21940-746">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="21940-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="21940-747">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="21940-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="21940-748">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="21940-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="21940-749">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="21940-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="21940-750">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="21940-751">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="21940-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="21940-752">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="21940-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="21940-753">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="21940-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21940-754">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="21940-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-755">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="21940-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="21940-756">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="21940-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="21940-757">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="21940-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="21940-758">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="21940-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="21940-759">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="21940-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="21940-760">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="21940-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="21940-761">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="21940-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="21940-762">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="21940-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="21940-763">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="21940-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="21940-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-765">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21940-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21940-766">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-767">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="21940-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="21940-768">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="21940-768">State of the logical device.</span></span> <span data-ttu-id="21940-769">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21940-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="21940-770">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21940-771">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21940-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21940-772">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="21940-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="21940-773">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="21940-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21940-774">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="21940-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21940-775">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="21940-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="21940-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-777">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-778">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-779">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API-Zeilen- \| gerätestrukturen \| linedevcaps \| dwstringformat")</span><span class="sxs-lookup"><span data-stu-id="21940-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="21940-780">Typ der Zeichen, die für Text verwendet werden, der über das Modem durchlaufen</span><span class="sxs-lookup"><span data-stu-id="21940-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="21940-781">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="21940-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="21940-782">"ASCII-Zeichen folgen Format"</span><span class="sxs-lookup"><span data-stu-id="21940-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="21940-783">"DBCS-Zeichen folgen Format"</span><span class="sxs-lookup"><span data-stu-id="21940-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="21940-784">"Unicode-Zeichen folgen Format"</span><span class="sxs-lookup"><span data-stu-id="21940-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="21940-785">**ASCII-Zeichen folgen Format** ("ASCII-Zeichen folgen Format")</span><span class="sxs-lookup"><span data-stu-id="21940-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="21940-786">**DBCS-Zeichen folgen Format** ("DBCS-Zeichen folgen Format")</span><span class="sxs-lookup"><span data-stu-id="21940-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="21940-787">**Unicode-Zeichen folgen Format** ("Unicode-Zeichen folgen Format")</span><span class="sxs-lookup"><span data-stu-id="21940-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21940-788">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="21940-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-789">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21940-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21940-790">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-791">**True** gibt an, dass das Modem den Rückruf unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21940-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="21940-792">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-793">**Supportssynchronousconnect**</span><span class="sxs-lookup"><span data-stu-id="21940-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-794">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21940-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21940-795">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-796">Wenn **true**, synchron und asynchron, wird die Kommunikation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21940-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="21940-797">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-798">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="21940-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-799">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-800">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-801">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="21940-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="21940-802">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="21940-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="21940-803">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-804">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="21940-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-805">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-806">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-807">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="21940-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="21940-808">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="21940-808">Name of the scoping system.</span></span>

<span data-ttu-id="21940-809">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-810">**Abschlusszeichen**</span><span class="sxs-lookup"><span data-stu-id="21940-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-811">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-812">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-813">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Terminator")</span><span class="sxs-lookup"><span data-stu-id="21940-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="21940-814">Eine Zeichenfolge, die das Ende einer Befehls Zeichenfolge markiert.</span><span class="sxs-lookup"><span data-stu-id="21940-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="21940-815">Beispiel: "<CR"</span><span class="sxs-lookup"><span data-stu-id="21940-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="21940-816">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="21940-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-817">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="21940-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="21940-818">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21940-819">Datum und Uhrzeit der letzten zurück setzung des Modem.</span><span class="sxs-lookup"><span data-stu-id="21940-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="21940-820">Diese Eigenschaft wird von [**CIM \_ potsmodem**](cim-potsmodem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21940-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="21940-821">**Ton**</span><span class="sxs-lookup"><span data-stu-id="21940-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-822">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-823">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-824">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Tone")</span><span class="sxs-lookup"><span data-stu-id="21940-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="21940-825">Befehls Zeichenfolge, die das Modem anweist, den Tonmodus für die Wahl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="21940-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="21940-826">Die Telefonleitung muss die Unterstützung von Ton Einwähl Unterstützung</span><span class="sxs-lookup"><span data-stu-id="21940-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="21940-827">Beispiel: "T"</span><span class="sxs-lookup"><span data-stu-id="21940-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="21940-828">**VoiceSwitchFeature**</span><span class="sxs-lookup"><span data-stu-id="21940-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21940-829">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21940-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21940-830">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21940-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21940-831">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| VoiceSwitchFeature")</span><span class="sxs-lookup"><span data-stu-id="21940-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="21940-832">Befehls Zeichenfolgen, die zum Aktivieren der Sprachfunktionen eines Sprachmodem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21940-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="21940-833">Beispiel: "at + V"</span><span class="sxs-lookup"><span data-stu-id="21940-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21940-834">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21940-834">Remarks</span></span>

<span data-ttu-id="21940-835">Die Win32-Klasse " **\_ potsmodem** " ist von [**CIM \_ potsmodem**](cim-potsmodem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="21940-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21940-836">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21940-836">Requirements</span></span>



| <span data-ttu-id="21940-837">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21940-837">Requirement</span></span> | <span data-ttu-id="21940-838">Wert</span><span class="sxs-lookup"><span data-stu-id="21940-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21940-839">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21940-839">Minimum supported client</span></span><br/> | <span data-ttu-id="21940-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21940-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21940-841">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21940-841">Minimum supported server</span></span><br/> | <span data-ttu-id="21940-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21940-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21940-843">Namespace</span><span class="sxs-lookup"><span data-stu-id="21940-843">Namespace</span></span><br/>                | <span data-ttu-id="21940-844">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="21940-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21940-845">MOF</span><span class="sxs-lookup"><span data-stu-id="21940-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21940-846"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="21940-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21940-847">DLL</span><span class="sxs-lookup"><span data-stu-id="21940-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21940-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21940-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21940-849">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21940-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21940-850">**CIM- \_ potsmodem**</span><span class="sxs-lookup"><span data-stu-id="21940-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="21940-851">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="21940-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
