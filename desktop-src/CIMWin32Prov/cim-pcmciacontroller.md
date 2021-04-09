---
description: Die CIM \_ PCMCIAController-Klasse stellt die Funktionen und die Verwaltung eines PCMCIA-Controllers (private Computer Memory Card International Association) dar.
ms.assetid: 341cbc6c-dd25-4dea-bcce-cd4e3f4d5324
ms.tgt_platform: multiple
title: CIM_PCMCIAController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController
- CIM_PCMCIAController.Availability
- CIM_PCMCIAController.Caption
- CIM_PCMCIAController.ConfigManagerErrorCode
- CIM_PCMCIAController.ConfigManagerUserConfig
- CIM_PCMCIAController.CreationClassName
- CIM_PCMCIAController.Description
- CIM_PCMCIAController.DeviceID
- CIM_PCMCIAController.ErrorCleared
- CIM_PCMCIAController.ErrorDescription
- CIM_PCMCIAController.InstallDate
- CIM_PCMCIAController.LastErrorCode
- CIM_PCMCIAController.Manufacturer
- CIM_PCMCIAController.MaxNumberControlled
- CIM_PCMCIAController.Name
- CIM_PCMCIAController.PNPDeviceID
- CIM_PCMCIAController.PowerManagementCapabilities
- CIM_PCMCIAController.PowerManagementSupported
- CIM_PCMCIAController.ProtocolSupported
- CIM_PCMCIAController.Status
- CIM_PCMCIAController.StatusInfo
- CIM_PCMCIAController.SystemCreationClassName
- CIM_PCMCIAController.SystemName
- CIM_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95d05e11dd0c439708c477e3ec776bc7a2c333d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126536"
---
# <a name="cim_pcmciacontroller-class"></a><span data-ttu-id="c4cfe-103">CIM \_ PCMCIAController-Klasse</span><span class="sxs-lookup"><span data-stu-id="c4cfe-103">CIM\_PCMCIAController class</span></span>

<span data-ttu-id="c4cfe-104">Die **CIM \_ PCMCIAController** -Klasse stellt die Funktionen und die Verwaltung eines PCMCIA-Controllers (private Computer Memory Card International Association) dar.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-104">The **CIM\_PCMCIAController** class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4cfe-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c4cfe-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c4cfe-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c4cfe-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c4cfe-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cfe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4cfe-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PCMCIAController : cim_controller
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="c4cfe-110">Member</span><span class="sxs-lookup"><span data-stu-id="c4cfe-110">Members</span></span>

<span data-ttu-id="c4cfe-111">Die **CIM- \_ PCMCIAController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c4cfe-111">The **CIM\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="c4cfe-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4cfe-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4cfe-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4cfe-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4cfe-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4cfe-114">Methods</span></span>

<span data-ttu-id="c4cfe-115">Die **CIM- \_ PCMCIAController** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-115">The **CIM\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="c4cfe-116">Methode</span><span class="sxs-lookup"><span data-stu-id="c4cfe-116">Method</span></span>                                                                      | <span data-ttu-id="c4cfe-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4cfe-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4cfe-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-118">**Reset**</span></span>](reset-method-in-class-cim-pcmciacontroller.md)                 | <span data-ttu-id="c4cfe-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c4cfe-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c4cfe-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcmciacontroller.md) | <span data-ttu-id="c4cfe-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c4cfe-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4cfe-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4cfe-124">Properties</span></span>

<span data-ttu-id="c4cfe-125">Die **CIM- \_ PCMCIAController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-125">The **CIM\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4cfe-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-130">Availability and status of the device.</span></span> <span data-ttu-id="c4cfe-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4cfe-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-133">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="c4cfe-133">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4cfe-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-135">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-135">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c4cfe-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-137">Ausführung oder vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-137">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c4cfe-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-139">Warnung.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-139">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c4cfe-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-141">Tests.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-141">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c4cfe-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-143">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c4cfe-143">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c4cfe-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-145">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-145">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c4cfe-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-147">Offline.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-147">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c4cfe-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-149">Off-Duty.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-149">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c4cfe-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="c4cfe-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-151">Heruntergestuft.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-151">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c4cfe-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-153">Nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-153">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c4cfe-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-155">Installationsfehler.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-155">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c4cfe-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-157">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status in diesem Modus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-157">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c4cfe-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-159">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-159">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c4cfe-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-161">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-161">Device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c4cfe-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-163">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-163">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c4cfe-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-165">Das Gerät befindet sich in einem Warn Status und auch in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-165">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c4cfe-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-167">Angehalten.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-167">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c4cfe-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-169">Nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-169">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c4cfe-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-171">Nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="c4cfe-171">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c4cfe-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="c4cfe-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-173">Der PCMCIA-Controller ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-173">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c4cfe-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-177">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-178">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-178">Short textual description of the object.</span></span>

<span data-ttu-id="c4cfe-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-180">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-181">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-183">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-184">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c4cfe-185">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c4cfe-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c4cfe-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-188">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c4cfe-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c4cfe-190">(1)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-191">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c4cfe-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c4cfe-193">(2)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c4cfe-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c4cfe-195">(3)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-196">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c4cfe-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c4cfe-198">(4)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-199">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-199">Device is not working properly.</span></span> <span data-ttu-id="c4cfe-200">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c4cfe-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c4cfe-202">(5)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-203">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c4cfe-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c4cfe-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-206">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c4cfe-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c4cfe-208">(7)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c4cfe-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c4cfe-210">(8)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-211">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c4cfe-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c4cfe-213">(9)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-214">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-214">Device is not working properly.</span></span> <span data-ttu-id="c4cfe-215">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c4cfe-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c4cfe-217">(10)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-218">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c4cfe-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c4cfe-220">(11)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-221">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c4cfe-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c4cfe-223">(12)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-224">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c4cfe-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c4cfe-226">(13)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-227">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c4cfe-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c4cfe-229">(14)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-230">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c4cfe-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c4cfe-232">(15)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-233">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c4cfe-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c4cfe-235">(16)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-236">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c4cfe-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c4cfe-238">(17)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-239">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c4cfe-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c4cfe-241">(18)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-242">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c4cfe-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c4cfe-244">(19)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c4cfe-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c4cfe-246">(20)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-247">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c4cfe-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c4cfe-249">(21)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-250">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-250">System failure.</span></span> <span data-ttu-id="c4cfe-251">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c4cfe-252">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c4cfe-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c4cfe-254">(22)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-255">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c4cfe-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c4cfe-257">(23)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-258">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-258">System failure.</span></span> <span data-ttu-id="c4cfe-259">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c4cfe-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c4cfe-261">(24)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-262">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c4cfe-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c4cfe-264">(25)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-265">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c4cfe-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c4cfe-267">(26)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-268">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c4cfe-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c4cfe-270">(27)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-271">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c4cfe-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c4cfe-273">(28)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-274">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c4cfe-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c4cfe-276">(29)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-277">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-277">Device is disabled.</span></span> <span data-ttu-id="c4cfe-278">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c4cfe-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c4cfe-280">(30)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-281">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c4cfe-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c4cfe-283">31,5</span><span class="sxs-lookup"><span data-stu-id="c4cfe-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-284">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-284">Device is not working properly.</span></span> <span data-ttu-id="c4cfe-285">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c4cfe-286">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-287">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c4cfe-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-289">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-290">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c4cfe-291">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-292">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-295">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-296">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c4cfe-297">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c4cfe-298">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-299">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-302">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-303">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-303">Textual description of the object.</span></span>

<span data-ttu-id="c4cfe-304">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-308">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-309">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c4cfe-310">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-311">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c4cfe-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-314">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c4cfe-315">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-319">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c4cfe-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-322">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-324">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-325">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-325">Date and time the object was installed.</span></span> <span data-ttu-id="c4cfe-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c4cfe-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-329">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-331">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c4cfe-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-333">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-333">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-336">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-337">Der Name des Herstellers des PCMCIA-Controllers.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-337">Name of the PCMCIA controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-338">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-338">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-339">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-341">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-342">Maximale Anzahl direkt Adressier barer Entitäten, die vom Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-342">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="c4cfe-343">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-343">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="c4cfe-344">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-344">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-345">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-345">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-348">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-349">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-349">Label by which the object is known.</span></span> <span data-ttu-id="c4cfe-350">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-350">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c4cfe-351">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-351">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-355">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-356">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-356">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="c4cfe-357">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c4cfe-358">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c4cfe-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-359">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-360">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c4cfe-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-362">Bestimmte energiebezogene Funktionen des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-362">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c4cfe-363">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4cfe-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-365">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-365">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c4cfe-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-367">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-367">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c4cfe-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-369">Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-369">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c4cfe-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-371">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-371">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c4cfe-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-373">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-373">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c4cfe-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-375">Die [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-375">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c4cfe-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-377">Die [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="c4cfe-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c4cfe-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c4cfe-379">Die [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c4cfe-380">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-381">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c4cfe-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-383">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c4cfe-384">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c4cfe-385">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c4cfe-386">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="c4cfe-387">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-388">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-388">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-389">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-391">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-392">Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-392">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="c4cfe-393">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-393">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="c4cfe-394">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="c4cfe-394">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4cfe-395">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4cfe-396">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="c4cfe-397">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-397">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="c4cfe-398">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-398">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="c4cfe-399">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-399">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="c4cfe-400">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-400">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="c4cfe-401">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-401">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="c4cfe-402">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-402">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="c4cfe-403">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-403">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="c4cfe-404">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-404">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="c4cfe-405">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-405">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="c4cfe-406">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-406">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="c4cfe-407">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-407">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="c4cfe-408">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-408">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="c4cfe-409">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-409">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="c4cfe-410">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-410">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="c4cfe-411">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-411">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="c4cfe-412">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-412">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="c4cfe-413">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-413">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="c4cfe-414">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-414">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c4cfe-415">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-415">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="c4cfe-416">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-416">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="c4cfe-417">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-417">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="c4cfe-418">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-418">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="c4cfe-419">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-419">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="c4cfe-420">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-420">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="c4cfe-421">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-421">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="c4cfe-422">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-422">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="c4cfe-423">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-423">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="c4cfe-424">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-424">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="c4cfe-425">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-425">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="c4cfe-426">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-426">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="c4cfe-427">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-427">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="c4cfe-428">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-428">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="c4cfe-429">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-429">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="c4cfe-430">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-430">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="c4cfe-431">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-431">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="c4cfe-432">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-432">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="c4cfe-433">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-433">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="c4cfe-434">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-434">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="c4cfe-435">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-435">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="c4cfe-436">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-436">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="c4cfe-437">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-437">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="c4cfe-438">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-438">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="c4cfe-439">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-439">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="c4cfe-440">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-440">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="c4cfe-441">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-441">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4cfe-442">**Status**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-442">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-443">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-445">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-445">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-446">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-446">Current status of the object.</span></span> <span data-ttu-id="c4cfe-447">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c4cfe-448">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c4cfe-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c4cfe-449">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c4cfe-450">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c4cfe-451">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4cfe-452">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c4cfe-453">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c4cfe-454">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c4cfe-455">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c4cfe-456">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c4cfe-457">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c4cfe-458">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c4cfe-459">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c4cfe-460">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4cfe-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-462">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-464">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c4cfe-464">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-465">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-465">State of the logical device.</span></span> <span data-ttu-id="c4cfe-466">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c4cfe-467">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4cfe-468">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4cfe-469">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c4cfe-470">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c4cfe-471">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c4cfe-472">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4cfe-473">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-476">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-477">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-477">Scoping system's creation class name.</span></span>

<span data-ttu-id="c4cfe-478">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-479">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-480">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-482">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-482">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-483">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-483">Scoping system's name.</span></span>

<span data-ttu-id="c4cfe-484">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4cfe-485">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-485">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4cfe-486">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-486">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4cfe-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4cfe-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4cfe-488">Datum und Uhrzeit der letzten zurück Setzung dieses Controllers, was bedeutet, dass der Controller heruntergefahren oder neu initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-488">Date and time this controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="c4cfe-489">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-489">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4cfe-490">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4cfe-490">Remarks</span></span>

<span data-ttu-id="c4cfe-491">Die **CIM- \_ PCMCIAController** -Klasse wird vom [**CIM- \_ Controller**](cim-controller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-491">The **CIM\_PCMCIAController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="c4cfe-492">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-492">WMI does not implement this class.</span></span> <span data-ttu-id="c4cfe-493">Informationen zu WMI-Klassen, die von **CIM- \_ PCMCIAController** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4cfe-493">For WMI classes that are derived from **CIM\_PCMCIAController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c4cfe-494">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c4cfe-495">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c4cfe-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4cfe-496">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4cfe-496">Requirements</span></span>



| <span data-ttu-id="c4cfe-497">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4cfe-497">Requirement</span></span> | <span data-ttu-id="c4cfe-498">Wert</span><span class="sxs-lookup"><span data-stu-id="c4cfe-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cfe-499">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-499">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cfe-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4cfe-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4cfe-501">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4cfe-501">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cfe-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4cfe-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4cfe-503">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4cfe-503">Namespace</span></span><br/>                | <span data-ttu-id="c4cfe-504">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c4cfe-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c4cfe-505">MOF</span><span class="sxs-lookup"><span data-stu-id="c4cfe-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4cfe-506"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4cfe-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4cfe-507">DLL</span><span class="sxs-lookup"><span data-stu-id="c4cfe-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4cfe-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4cfe-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4cfe-509">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4cfe-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cfe-510">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="c4cfe-510">**cim\_controller**</span></span>](cim-controller.md)
</dt> </dl>

 

