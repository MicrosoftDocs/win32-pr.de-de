---
description: Die CIM \_ BinarySensor-Klasse stellt eine boolesche Ausgabe bereit.
ms.assetid: 51396a51-78ea-4c49-8dcc-7fb815f334ae
ms.tgt_platform: multiple
title: CIM_BinarySensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor
- CIM_BinarySensor.Caption
- CIM_BinarySensor.Description
- CIM_BinarySensor.InstallDate
- CIM_BinarySensor.Name
- CIM_BinarySensor.Status
- CIM_BinarySensor.Availability
- CIM_BinarySensor.ConfigManagerErrorCode
- CIM_BinarySensor.ConfigManagerUserConfig
- CIM_BinarySensor.CreationClassName
- CIM_BinarySensor.DeviceID
- CIM_BinarySensor.PowerManagementCapabilities
- CIM_BinarySensor.ErrorCleared
- CIM_BinarySensor.ErrorDescription
- CIM_BinarySensor.LastErrorCode
- CIM_BinarySensor.PNPDeviceID
- CIM_BinarySensor.PowerManagementSupported
- CIM_BinarySensor.StatusInfo
- CIM_BinarySensor.SystemCreationClassName
- CIM_BinarySensor.SystemName
- CIM_BinarySensor.CurrentReading
- CIM_BinarySensor.ExpectedReading
- CIM_BinarySensor.InterpretationOfFalse
- CIM_BinarySensor.InterpretationOfTrue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0d795f98473c09937571d415e34cf6fcb7f3486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345624"
---
# <a name="cim_binarysensor-class"></a><span data-ttu-id="40ab7-103">CIM \_ BinarySensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="40ab7-103">CIM\_BinarySensor class</span></span>

<span data-ttu-id="40ab7-104">Die **CIM \_ BinarySensor** -Klasse stellt eine boolesche Ausgabe bereit.</span><span class="sxs-lookup"><span data-stu-id="40ab7-104">The **CIM\_BinarySensor** class provides a Boolean output.</span></span> <span data-ttu-id="40ab7-105">Die Eigenschaften " **CurrentState** " und " **possiblestates** " wurden für die sensorung hinzugefügt, sodass die **CIM- \_ BinarySensor** -Unterklasse nicht mehr benötigt wird, obwohl Sie aus Gründen der Abwärtskompatibilität beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="40ab7-105">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="40ab7-106">Ein binärer Sensor kann erstellt werden, indem ein Sensor mit zwei möglichen Zuständen instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="40ab7-106">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40ab7-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="40ab7-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="40ab7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="40ab7-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="40ab7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="40ab7-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="40ab7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ab7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="40ab7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{11140D44-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_BinarySensor : CIM_Sensor
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
  boolean  CurrentReading;
  boolean  ExpectedReading;
  string   InterpretationOfFalse;
  string   InterpretationOfTrue;
};
```

## <a name="members"></a><span data-ttu-id="40ab7-112">Member</span><span class="sxs-lookup"><span data-stu-id="40ab7-112">Members</span></span>

<span data-ttu-id="40ab7-113">Die **CIM \_ BinarySensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="40ab7-113">The **CIM\_BinarySensor** class has these types of members:</span></span>

-   [<span data-ttu-id="40ab7-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="40ab7-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="40ab7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40ab7-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40ab7-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="40ab7-116">Methods</span></span>

<span data-ttu-id="40ab7-117">Die **CIM \_ BinarySensor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-117">The **CIM\_BinarySensor** class has these methods.</span></span>



| <span data-ttu-id="40ab7-118">Methode</span><span class="sxs-lookup"><span data-stu-id="40ab7-118">Method</span></span>                                                                  | <span data-ttu-id="40ab7-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40ab7-119">Description</span></span>                                                                                                                                |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40ab7-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="40ab7-120">**Reset**</span></span>](reset-method-in-class-cim-binarysensor.md)                 | <span data-ttu-id="40ab7-121">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="40ab7-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="40ab7-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="40ab7-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="40ab7-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="40ab7-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-binarysensor.md) | <span data-ttu-id="40ab7-124">Definiert den gewünschten Energiezustand für ein logisches Gerät und den Zeitpunkt, zu dem das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40ab7-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="40ab7-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="40ab7-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="40ab7-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40ab7-126">Properties</span></span>

<span data-ttu-id="40ab7-127">Die **CIM \_ BinarySensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="40ab7-127">The **CIM\_BinarySensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40ab7-128">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="40ab7-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40ab7-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="40ab7-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-132">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="40ab7-132">Availability and status of the device.</span></span>

<span data-ttu-id="40ab7-133">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40ab7-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="40ab7-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40ab7-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="40ab7-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="40ab7-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="40ab7-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="40ab7-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="40ab7-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="40ab7-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="40ab7-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="40ab7-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="40ab7-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="40ab7-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="40ab7-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="40ab7-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="40ab7-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="40ab7-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="40ab7-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40ab7-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="40ab7-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="40ab7-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="40ab7-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="40ab7-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="40ab7-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="40ab7-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="40ab7-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-147">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="40ab7-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="40ab7-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-149">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="40ab7-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="40ab7-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="40ab7-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-151">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="40ab7-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="40ab7-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="40ab7-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="40ab7-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-154">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="40ab7-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="40ab7-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="40ab7-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-156">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="40ab7-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="40ab7-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="40ab7-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-158">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="40ab7-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="40ab7-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="40ab7-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-160">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="40ab7-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="40ab7-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="40ab7-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-162">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="40ab7-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40ab7-163">**Caption**</span><span class="sxs-lookup"><span data-stu-id="40ab7-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-166">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="40ab7-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-167">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="40ab7-167">A short textual description of the object.</span></span>

<span data-ttu-id="40ab7-168">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-169">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="40ab7-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40ab7-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-172">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="40ab7-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-173">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="40ab7-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="40ab7-174">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="40ab7-175">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-175">**This device is working properly.**</span></span> <span data-ttu-id="40ab7-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="40ab7-176">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="40ab7-177">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-177">**This device is not configured correctly.**</span></span> <span data-ttu-id="40ab7-178">(1)</span><span class="sxs-lookup"><span data-stu-id="40ab7-178">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="40ab7-179">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-179">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="40ab7-180">(2)</span><span class="sxs-lookup"><span data-stu-id="40ab7-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="40ab7-181">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-181">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="40ab7-182">(3)</span><span class="sxs-lookup"><span data-stu-id="40ab7-182">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="40ab7-183">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-183">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="40ab7-184">(4)</span><span class="sxs-lookup"><span data-stu-id="40ab7-184">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="40ab7-185">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-185">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="40ab7-186">(5)</span><span class="sxs-lookup"><span data-stu-id="40ab7-186">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="40ab7-187">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-187">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="40ab7-188"> (6)</span><span class="sxs-lookup"><span data-stu-id="40ab7-188">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="40ab7-189">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-189">**Cannot filter.**</span></span> <span data-ttu-id="40ab7-190">(7)</span><span class="sxs-lookup"><span data-stu-id="40ab7-190">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="40ab7-191">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-191">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="40ab7-192">(8)</span><span class="sxs-lookup"><span data-stu-id="40ab7-192">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="40ab7-193">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-193">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="40ab7-194">(9)</span><span class="sxs-lookup"><span data-stu-id="40ab7-194">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="40ab7-195">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-195">**This device cannot start.**</span></span> <span data-ttu-id="40ab7-196">(10)</span><span class="sxs-lookup"><span data-stu-id="40ab7-196">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="40ab7-197">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-197">**This device failed.**</span></span> <span data-ttu-id="40ab7-198">(11)</span><span class="sxs-lookup"><span data-stu-id="40ab7-198">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="40ab7-199">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-199">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="40ab7-200">(12)</span><span class="sxs-lookup"><span data-stu-id="40ab7-200">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="40ab7-201">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-201">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="40ab7-202">(13)</span><span class="sxs-lookup"><span data-stu-id="40ab7-202">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="40ab7-203">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-203">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="40ab7-204">(14)</span><span class="sxs-lookup"><span data-stu-id="40ab7-204">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="40ab7-205">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-205">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="40ab7-206">(15)</span><span class="sxs-lookup"><span data-stu-id="40ab7-206">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="40ab7-207">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-207">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="40ab7-208">(16)</span><span class="sxs-lookup"><span data-stu-id="40ab7-208">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="40ab7-209">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-209">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="40ab7-210">(17)</span><span class="sxs-lookup"><span data-stu-id="40ab7-210">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="40ab7-211">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-211">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="40ab7-212">(18)</span><span class="sxs-lookup"><span data-stu-id="40ab7-212">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="40ab7-213">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-213">**Failure using the VxD loader.**</span></span> <span data-ttu-id="40ab7-214">(19)</span><span class="sxs-lookup"><span data-stu-id="40ab7-214">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="40ab7-215">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-215">**Your registry might be corrupted.**</span></span> <span data-ttu-id="40ab7-216">(20)</span><span class="sxs-lookup"><span data-stu-id="40ab7-216">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="40ab7-217">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-217">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="40ab7-218">(21)</span><span class="sxs-lookup"><span data-stu-id="40ab7-218">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="40ab7-219">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-219">**This device is disabled.**</span></span> <span data-ttu-id="40ab7-220">(22)</span><span class="sxs-lookup"><span data-stu-id="40ab7-220">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="40ab7-221">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-221">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="40ab7-222">(23)</span><span class="sxs-lookup"><span data-stu-id="40ab7-222">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="40ab7-223">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-223">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="40ab7-224">(24)</span><span class="sxs-lookup"><span data-stu-id="40ab7-224">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="40ab7-225">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-225">**Windows is still setting up this device.**</span></span> <span data-ttu-id="40ab7-226">(25)</span><span class="sxs-lookup"><span data-stu-id="40ab7-226">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="40ab7-227">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="40ab7-228">(26)</span><span class="sxs-lookup"><span data-stu-id="40ab7-228">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="40ab7-229">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-229">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="40ab7-230">(27)</span><span class="sxs-lookup"><span data-stu-id="40ab7-230">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="40ab7-231">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-231">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="40ab7-232">(28)</span><span class="sxs-lookup"><span data-stu-id="40ab7-232">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="40ab7-233">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-233">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="40ab7-234">(29)</span><span class="sxs-lookup"><span data-stu-id="40ab7-234">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="40ab7-235">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-235">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="40ab7-236">(30)</span><span class="sxs-lookup"><span data-stu-id="40ab7-236">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="40ab7-237">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="40ab7-237">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="40ab7-238">31,5</span><span class="sxs-lookup"><span data-stu-id="40ab7-238">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40ab7-239">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="40ab7-239">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-240">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40ab7-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-242">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="40ab7-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-243">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="40ab7-243">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="40ab7-244">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-244">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-245">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="40ab7-245">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-248">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40ab7-248">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-249">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40ab7-249">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="40ab7-250">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-250">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="40ab7-251">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-251">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-252">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="40ab7-252">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-253">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40ab7-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-255">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40ab7-255">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-256">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40ab7-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-259">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="40ab7-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-260">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="40ab7-260">A textual description of the object.</span></span>

<span data-ttu-id="40ab7-261">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="40ab7-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-265">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40ab7-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-266">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="40ab7-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="40ab7-267">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-268">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="40ab7-268">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-269">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40ab7-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-271">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="40ab7-271">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="40ab7-272">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-273">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="40ab7-273">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-276">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="40ab7-276">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="40ab7-277">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-278">**ExpectedReading**</span><span class="sxs-lookup"><span data-stu-id="40ab7-278">**ExpectedReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-279">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40ab7-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-281">Der "normale" Wert für den Sensor.</span><span class="sxs-lookup"><span data-stu-id="40ab7-281">'Normal' value for the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40ab7-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-283">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="40ab7-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-285">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="40ab7-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-286">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="40ab7-286">Indicates when the object was installed.</span></span> <span data-ttu-id="40ab7-287">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="40ab7-287">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="40ab7-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-289">**InterpretationOfFalse**</span><span class="sxs-lookup"><span data-stu-id="40ab7-289">**InterpretationOfFalse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-292">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="40ab7-292">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-293">Die Beschreibung eines ' false '-Werts aus dem binären Sensor.</span><span class="sxs-lookup"><span data-stu-id="40ab7-293">Description of a 'False' value from the binary sensor.</span></span> <span data-ttu-id="40ab7-294">Diese Informationen können einem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-294">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-295">**Interpretationoftrue**</span><span class="sxs-lookup"><span data-stu-id="40ab7-295">**InterpretationOfTrue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-298">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="40ab7-298">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-299">Die Beschreibung eines ' true '-Werts aus dem binären Sensor.</span><span class="sxs-lookup"><span data-stu-id="40ab7-299">Description of a 'True' value from the binary sensor.</span></span> <span data-ttu-id="40ab7-300">Diese Informationen können einem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-300">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-301">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="40ab7-301">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-302">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40ab7-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-304">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="40ab7-304">Last error code reported by the logical device.</span></span>

<span data-ttu-id="40ab7-305">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-306">**Name**</span><span class="sxs-lookup"><span data-stu-id="40ab7-306">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-309">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="40ab7-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-310">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="40ab7-310">Label by which the object is known.</span></span> <span data-ttu-id="40ab7-311">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-311">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="40ab7-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-313">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="40ab7-313">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-316">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="40ab7-316">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-317">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="40ab7-317">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="40ab7-318">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="40ab7-318">Example: "\*PNP030b"</span></span>

<span data-ttu-id="40ab7-319">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-320">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="40ab7-320">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-321">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="40ab7-321">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-323">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="40ab7-323">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="40ab7-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40ab7-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="40ab7-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-326">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-326">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="40ab7-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="40ab7-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-328">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-328">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="40ab7-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="40ab7-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-330">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="40ab7-330">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="40ab7-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="40ab7-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-332">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40ab7-332">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="40ab7-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="40ab7-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-334">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="40ab7-334">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="40ab7-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="40ab7-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-336">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-336">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="40ab7-337">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-337">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="40ab7-338">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="40ab7-338">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="40ab7-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="40ab7-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-340">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="40ab7-340">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="40ab7-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="40ab7-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="40ab7-342">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40ab7-342">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40ab7-343">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="40ab7-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-344">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40ab7-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-346">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="40ab7-346">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="40ab7-347">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="40ab7-347">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="40ab7-348">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-348">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="40ab7-349">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="40ab7-349">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="40ab7-350">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-351">**Status**</span><span class="sxs-lookup"><span data-stu-id="40ab7-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-354">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="40ab7-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-355">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-355">String that indicates the current status of the object.</span></span> <span data-ttu-id="40ab7-356">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-356">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="40ab7-357">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="40ab7-357">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="40ab7-358">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="40ab7-358">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="40ab7-359">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="40ab7-359">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="40ab7-360">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="40ab7-360">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="40ab7-361">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="40ab7-361">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="40ab7-362">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="40ab7-363">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="40ab7-363">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="40ab7-364">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="40ab7-364">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="40ab7-365">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="40ab7-365">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40ab7-366">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="40ab7-366">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40ab7-367">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="40ab7-367">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="40ab7-368">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="40ab7-368">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="40ab7-369">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="40ab7-369">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="40ab7-370">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="40ab7-370">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="40ab7-371">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="40ab7-371">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="40ab7-372">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="40ab7-372">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="40ab7-373">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="40ab7-373">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="40ab7-374">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="40ab7-374">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="40ab7-375">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="40ab7-375">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40ab7-376">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="40ab7-376">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-377">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40ab7-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-379">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="40ab7-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-380">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="40ab7-380">State of the logical device.</span></span> <span data-ttu-id="40ab7-381">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40ab7-381">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="40ab7-382">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40ab7-383">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="40ab7-383">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40ab7-384">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="40ab7-384">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="40ab7-385">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="40ab7-385">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="40ab7-386">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="40ab7-386">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="40ab7-387">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="40ab7-387">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40ab7-388">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="40ab7-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-389">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-391">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40ab7-391">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-392">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="40ab7-392">The scoping system's creation class name.</span></span>

<span data-ttu-id="40ab7-393">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ab7-394">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="40ab7-394">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40ab7-395">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40ab7-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40ab7-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40ab7-397">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40ab7-397">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40ab7-398">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="40ab7-398">The scoping system's name.</span></span>

<span data-ttu-id="40ab7-399">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40ab7-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40ab7-400">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40ab7-400">Remarks</span></span>

<span data-ttu-id="40ab7-401">Die **CIM \_ BinarySensor** -Klasse wird vom [**CIM- \_ Sensor**](cim-sensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="40ab7-401">The **CIM\_BinarySensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="40ab7-402">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="40ab7-402">WMI does not implement this class.</span></span>

<span data-ttu-id="40ab7-403">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="40ab7-403">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="40ab7-404">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="40ab7-404">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ab7-405">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40ab7-405">Requirements</span></span>



| <span data-ttu-id="40ab7-406">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40ab7-406">Requirement</span></span> | <span data-ttu-id="40ab7-407">Wert</span><span class="sxs-lookup"><span data-stu-id="40ab7-407">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ab7-408">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40ab7-408">Minimum supported client</span></span><br/> | <span data-ttu-id="40ab7-409">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40ab7-409">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40ab7-410">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40ab7-410">Minimum supported server</span></span><br/> | <span data-ttu-id="40ab7-411">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40ab7-411">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40ab7-412">Namespace</span><span class="sxs-lookup"><span data-stu-id="40ab7-412">Namespace</span></span><br/>                | <span data-ttu-id="40ab7-413">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40ab7-413">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40ab7-414">MOF</span><span class="sxs-lookup"><span data-stu-id="40ab7-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40ab7-415"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="40ab7-415"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40ab7-416">DLL</span><span class="sxs-lookup"><span data-stu-id="40ab7-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40ab7-417"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ab7-417"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ab7-418">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40ab7-418">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ab7-419">**CIM- \_ Sensor**</span><span class="sxs-lookup"><span data-stu-id="40ab7-419">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

