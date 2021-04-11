---
description: Die CIM \_ PCIController-Klasse stellt die Eigenschaften und die Verwaltung eines PCI-Controllers dar. Die Eigenschaften in dieser Klasse und deren Unterklassen werden in den verschiedenen PCI-Spezifikationen definiert, die von PCI SIG veröffentlicht werden.
ms.assetid: 0f2aec01-362d-49d7-95ea-23487214188c
ms.tgt_platform: multiple
title: CIM_PCIController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCIController
- CIM_PCIController.Availability
- CIM_PCIController.Caption
- CIM_PCIController.ConfigManagerErrorCode
- CIM_PCIController.ConfigManagerUserConfig
- CIM_PCIController.CreationClassName
- CIM_PCIController.Description
- CIM_PCIController.DeviceID
- CIM_PCIController.ErrorCleared
- CIM_PCIController.ErrorDescription
- CIM_PCIController.InstallDate
- CIM_PCIController.LastErrorCode
- CIM_PCIController.MaxNumberControlled
- CIM_PCIController.Name
- CIM_PCIController.PNPDeviceID
- CIM_PCIController.PowerManagementCapabilities
- CIM_PCIController.PowerManagementSupported
- CIM_PCIController.ProtocolSupported
- CIM_PCIController.Status
- CIM_PCIController.StatusInfo
- CIM_PCIController.SystemCreationClassName
- CIM_PCIController.SystemName
- CIM_PCIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4685f55899bf7b133a5039f40d77a2c6ca640d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127529"
---
# <a name="cim_pcicontroller-class"></a><span data-ttu-id="49896-104">CIM \_ PCIController-Klasse</span><span class="sxs-lookup"><span data-stu-id="49896-104">CIM\_PCIController class</span></span>

<span data-ttu-id="49896-105">Die **CIM \_ PCIController** -Klasse stellt die Eigenschaften und die Verwaltung eines PCI-Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="49896-105">The **CIM\_PCIController** class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="49896-106">Die Eigenschaften in dieser Klasse und deren Unterklassen werden in den verschiedenen PCI-Spezifikationen definiert, die von PCI SIG veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="49896-106">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49896-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="49896-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49896-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="49896-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49896-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49896-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="49896-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="49896-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49896-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="49896-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{7BB67AE8-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PCIController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="49896-112">Member</span><span class="sxs-lookup"><span data-stu-id="49896-112">Members</span></span>

<span data-ttu-id="49896-113">Die **CIM \_ PCIController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="49896-113">The **CIM\_PCIController** class has these types of members:</span></span>

-   [<span data-ttu-id="49896-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="49896-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="49896-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49896-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49896-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="49896-116">Methods</span></span>

<span data-ttu-id="49896-117">Die **CIM \_ PCIController** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="49896-117">The **CIM\_PCIController** class has these methods.</span></span>



| <span data-ttu-id="49896-118">Methode</span><span class="sxs-lookup"><span data-stu-id="49896-118">Method</span></span>                                                                   | <span data-ttu-id="49896-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49896-119">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49896-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="49896-120">**Reset**</span></span>](reset-method-in-class-cim-pcicontroller.md)                 | <span data-ttu-id="49896-121">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="49896-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="49896-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="49896-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="49896-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="49896-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcicontroller.md) | <span data-ttu-id="49896-124">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49896-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="49896-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="49896-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49896-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49896-126">Properties</span></span>

<span data-ttu-id="49896-127">Die **CIM \_ PCIController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49896-127">The **CIM\_PCIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49896-128">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="49896-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49896-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49896-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="49896-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="49896-132">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="49896-132">Availability and status of the device.</span></span> <span data-ttu-id="49896-133">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49896-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="49896-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="49896-135">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="49896-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49896-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="49896-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="49896-137">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="49896-137">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="49896-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="49896-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49896-139">Ausführung oder vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="49896-139">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="49896-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="49896-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="49896-141">Warnung.</span><span class="sxs-lookup"><span data-stu-id="49896-141">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="49896-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="49896-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="49896-143">Tests.</span><span class="sxs-lookup"><span data-stu-id="49896-143">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="49896-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="49896-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="49896-145">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="49896-145">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="49896-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="49896-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="49896-147">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="49896-147">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="49896-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="49896-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="49896-149">Offline.</span><span class="sxs-lookup"><span data-stu-id="49896-149">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="49896-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="49896-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="49896-151">Off-Duty.</span><span class="sxs-lookup"><span data-stu-id="49896-151">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="49896-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="49896-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="49896-153">Heruntergestuft.</span><span class="sxs-lookup"><span data-stu-id="49896-153">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="49896-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="49896-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="49896-155">Nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="49896-155">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="49896-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="49896-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="49896-157">Installationsfehler.</span><span class="sxs-lookup"><span data-stu-id="49896-157">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="49896-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="49896-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="49896-159">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status in diesem Modus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="49896-159">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="49896-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="49896-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="49896-161">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="49896-161">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="49896-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="49896-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="49896-163">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="49896-163">Device is not functioning, but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="49896-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="49896-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="49896-165">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="49896-165">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="49896-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="49896-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="49896-167">Das Gerät befindet sich in einem Warn Status und auch in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="49896-167">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="49896-168"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="49896-168"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="49896-169">Angehalten.</span><span class="sxs-lookup"><span data-stu-id="49896-169">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="49896-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="49896-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="49896-171">Nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="49896-171">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="49896-172"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="49896-172"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="49896-173">Nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="49896-173">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="49896-174"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="49896-174"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="49896-175">Der PCI-Controller ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49896-175">The PCI controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49896-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="49896-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-179">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="49896-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="49896-180">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="49896-180">Short textual description of the object.</span></span>

<span data-ttu-id="49896-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-182">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="49896-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49896-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49896-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-185">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="49896-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="49896-186">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="49896-186">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="49896-187">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="49896-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="49896-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="49896-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="49896-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="49896-190">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="49896-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="49896-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="49896-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="49896-192">(1)</span><span class="sxs-lookup"><span data-stu-id="49896-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="49896-193">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="49896-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="49896-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="49896-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="49896-195">(2)</span><span class="sxs-lookup"><span data-stu-id="49896-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="49896-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="49896-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="49896-197">(3)</span><span class="sxs-lookup"><span data-stu-id="49896-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="49896-198">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="49896-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="49896-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="49896-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="49896-200">(4)</span><span class="sxs-lookup"><span data-stu-id="49896-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="49896-201">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="49896-201">Device is not working properly.</span></span> <span data-ttu-id="49896-202">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="49896-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="49896-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="49896-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="49896-204">(5)</span><span class="sxs-lookup"><span data-stu-id="49896-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="49896-205">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="49896-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="49896-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="49896-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="49896-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="49896-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="49896-208">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="49896-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="49896-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="49896-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="49896-210">(7)</span><span class="sxs-lookup"><span data-stu-id="49896-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="49896-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="49896-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="49896-212">(8)</span><span class="sxs-lookup"><span data-stu-id="49896-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="49896-213">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="49896-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="49896-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="49896-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="49896-215">(9)</span><span class="sxs-lookup"><span data-stu-id="49896-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="49896-216">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="49896-216">Device is not working properly.</span></span> <span data-ttu-id="49896-217">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="49896-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="49896-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="49896-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="49896-219">(10)</span><span class="sxs-lookup"><span data-stu-id="49896-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="49896-220">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="49896-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="49896-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="49896-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="49896-222">(11)</span><span class="sxs-lookup"><span data-stu-id="49896-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="49896-223">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="49896-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="49896-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="49896-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="49896-225">(12)</span><span class="sxs-lookup"><span data-stu-id="49896-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="49896-226">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="49896-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="49896-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="49896-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="49896-228">(13)</span><span class="sxs-lookup"><span data-stu-id="49896-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="49896-229">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="49896-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="49896-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="49896-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="49896-231">(14)</span><span class="sxs-lookup"><span data-stu-id="49896-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="49896-232">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="49896-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="49896-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="49896-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="49896-234">(15)</span><span class="sxs-lookup"><span data-stu-id="49896-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="49896-235">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="49896-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="49896-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="49896-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="49896-237">(16)</span><span class="sxs-lookup"><span data-stu-id="49896-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="49896-238">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49896-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="49896-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="49896-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="49896-240">(17)</span><span class="sxs-lookup"><span data-stu-id="49896-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="49896-241">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="49896-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="49896-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="49896-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="49896-243">(18)</span><span class="sxs-lookup"><span data-stu-id="49896-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="49896-244">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="49896-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="49896-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="49896-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="49896-246">(19)</span><span class="sxs-lookup"><span data-stu-id="49896-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="49896-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="49896-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="49896-248">(20)</span><span class="sxs-lookup"><span data-stu-id="49896-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="49896-249">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="49896-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="49896-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="49896-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="49896-251">(21)</span><span class="sxs-lookup"><span data-stu-id="49896-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="49896-252">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="49896-252">System failure.</span></span> <span data-ttu-id="49896-253">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="49896-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="49896-254">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="49896-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="49896-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="49896-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="49896-256">(22)</span><span class="sxs-lookup"><span data-stu-id="49896-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="49896-257">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="49896-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="49896-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="49896-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="49896-259">(23)</span><span class="sxs-lookup"><span data-stu-id="49896-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="49896-260">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="49896-260">System failure.</span></span> <span data-ttu-id="49896-261">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="49896-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="49896-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="49896-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="49896-263">(24)</span><span class="sxs-lookup"><span data-stu-id="49896-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="49896-264">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="49896-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="49896-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="49896-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="49896-266">(25)</span><span class="sxs-lookup"><span data-stu-id="49896-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="49896-267">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="49896-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="49896-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="49896-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="49896-269">(26)</span><span class="sxs-lookup"><span data-stu-id="49896-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="49896-270">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="49896-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="49896-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="49896-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="49896-272">(27)</span><span class="sxs-lookup"><span data-stu-id="49896-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="49896-273">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="49896-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="49896-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="49896-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="49896-275">(28)</span><span class="sxs-lookup"><span data-stu-id="49896-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="49896-276">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="49896-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="49896-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="49896-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="49896-278">(29)</span><span class="sxs-lookup"><span data-stu-id="49896-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="49896-279">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="49896-279">Device is disabled.</span></span> <span data-ttu-id="49896-280">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="49896-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="49896-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="49896-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="49896-282">(30)</span><span class="sxs-lookup"><span data-stu-id="49896-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="49896-283">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49896-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="49896-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="49896-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="49896-285">31,5</span><span class="sxs-lookup"><span data-stu-id="49896-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="49896-286">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="49896-286">Device is not working properly.</span></span> <span data-ttu-id="49896-287">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="49896-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49896-288">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="49896-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-289">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="49896-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49896-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-291">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="49896-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="49896-292">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="49896-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="49896-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-294">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="49896-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-297">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="49896-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="49896-298">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49896-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="49896-299">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="49896-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="49896-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-301">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49896-301">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-304">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="49896-304">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="49896-305">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="49896-305">Textual description of the object.</span></span>

<span data-ttu-id="49896-306">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-307">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="49896-307">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-310">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="49896-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="49896-311">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="49896-311">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="49896-312">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-313">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="49896-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-314">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="49896-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49896-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49896-316">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="49896-316">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="49896-317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="49896-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49896-321">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="49896-321">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="49896-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-323">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="49896-323">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-324">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49896-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49896-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-326">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="49896-326">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="49896-327">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="49896-327">Date and time the object was installed.</span></span> <span data-ttu-id="49896-328">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="49896-328">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="49896-329">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-330">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="49896-330">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-331">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49896-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49896-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49896-333">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="49896-333">Last error code reported by the logical device.</span></span>

<span data-ttu-id="49896-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-335">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="49896-335">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-336">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49896-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49896-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-338">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="49896-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="49896-339">Maximale Anzahl direkt Adressier barer Entitäten, die vom Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="49896-339">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="49896-340">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49896-340">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="49896-341">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-341">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-342">**Name**</span><span class="sxs-lookup"><span data-stu-id="49896-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-345">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="49896-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="49896-346">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="49896-346">Label by which the object is known.</span></span> <span data-ttu-id="49896-347">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="49896-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="49896-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-349">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="49896-349">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-352">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="49896-352">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="49896-353">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="49896-353">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="49896-354">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="49896-355">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="49896-355">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="49896-356">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="49896-356">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-357">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="49896-357">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="49896-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49896-359">Bestimmte energiebezogene Funktionen des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="49896-359">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="49896-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49896-361"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="49896-361"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="49896-362">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="49896-362">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="49896-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="49896-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="49896-364">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49896-364">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="49896-365"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="49896-365"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="49896-366">Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="49896-366">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="49896-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="49896-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49896-368">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49896-368">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="49896-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="49896-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="49896-370">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="49896-370">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="49896-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="49896-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="49896-372">Die [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49896-372">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="49896-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="49896-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="49896-374">Die [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="49896-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="49896-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="49896-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="49896-376">Die [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="49896-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49896-377">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="49896-377">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-378">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="49896-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49896-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49896-380">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="49896-380">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="49896-381">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="49896-381">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="49896-382">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="49896-382">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="49896-383">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="49896-383">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="49896-384">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-385">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="49896-385">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-386">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49896-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49896-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-388">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="49896-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="49896-389">Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49896-389">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="49896-390">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="49896-391">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="49896-391">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49896-392">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="49896-392">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49896-393">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="49896-393">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="49896-394">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="49896-394">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="49896-395">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="49896-395">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="49896-396">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="49896-396">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="49896-397">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="49896-397">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="49896-398">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="49896-398">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="49896-399">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="49896-399">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="49896-400">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="49896-400">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="49896-401">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="49896-401">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="49896-402">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="49896-402">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="49896-403">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="49896-403">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="49896-404">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="49896-404">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="49896-405">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="49896-405">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="49896-406">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="49896-406">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="49896-407">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="49896-407">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="49896-408">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="49896-408">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="49896-409">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="49896-409">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="49896-410">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="49896-410">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="49896-411">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="49896-411">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="49896-412">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="49896-412">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="49896-413">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="49896-413">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="49896-414">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="49896-414">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="49896-415">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="49896-415">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="49896-416">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="49896-416">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="49896-417">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="49896-417">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="49896-418">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="49896-418">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="49896-419">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="49896-419">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="49896-420">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="49896-420">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="49896-421">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="49896-421">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="49896-422">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="49896-422">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="49896-423">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="49896-423">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="49896-424">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="49896-424">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="49896-425">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="49896-425">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="49896-426">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="49896-426">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="49896-427">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="49896-427">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="49896-428">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="49896-428">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="49896-429">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="49896-429">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="49896-430">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="49896-430">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="49896-431">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="49896-431">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="49896-432">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="49896-432">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="49896-433">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="49896-433">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="49896-434">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="49896-434">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="49896-435">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="49896-435">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="49896-436">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="49896-436">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="49896-437">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="49896-437">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="49896-438">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="49896-438">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49896-439">**Status**</span><span class="sxs-lookup"><span data-stu-id="49896-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-440">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-442">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="49896-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="49896-443">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="49896-443">Current status of the object.</span></span> <span data-ttu-id="49896-444">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-444">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="49896-445">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="49896-445">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="49896-446">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="49896-446">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="49896-447">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="49896-447">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="49896-448">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="49896-448">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49896-449">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="49896-449">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="49896-450">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="49896-450">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="49896-451">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="49896-451">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="49896-452">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="49896-452">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="49896-453">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="49896-453">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="49896-454">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="49896-454">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="49896-455">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="49896-455">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="49896-456">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="49896-456">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="49896-457">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="49896-457">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49896-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="49896-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-459">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49896-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49896-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-461">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="49896-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="49896-462">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="49896-462">State of the logical device.</span></span> <span data-ttu-id="49896-463">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49896-463">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="49896-464">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-464">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49896-465">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="49896-465">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49896-466">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="49896-466">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="49896-467">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="49896-467">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="49896-468">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="49896-468">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="49896-469">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="49896-469">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49896-470">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="49896-470">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-471">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-473">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="49896-473">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="49896-474">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="49896-474">Scoping system's creation class name.</span></span>

<span data-ttu-id="49896-475">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-476">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="49896-476">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-477">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49896-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49896-478">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49896-479">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="49896-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="49896-480">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="49896-480">Scoping system's name.</span></span>

<span data-ttu-id="49896-481">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49896-482">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="49896-482">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49896-483">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49896-483">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49896-484">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49896-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49896-485">Datum und Uhrzeit der letzten zurück setzung des Controllers, was bedeutet, dass der Controller heruntergefahren oder neu initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49896-485">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="49896-486">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49896-486">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49896-487">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49896-487">Remarks</span></span>

<span data-ttu-id="49896-488">Die **CIM- \_ PCIController** -Klasse wird vom [**CIM- \_ Controller**](cim-controller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="49896-488">The **CIM\_PCIController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="49896-489">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="49896-489">WMI does not implement this class.</span></span>

<span data-ttu-id="49896-490">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="49896-490">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49896-491">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="49896-491">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49896-492">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49896-492">Requirements</span></span>



| <span data-ttu-id="49896-493">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49896-493">Requirement</span></span> | <span data-ttu-id="49896-494">Wert</span><span class="sxs-lookup"><span data-stu-id="49896-494">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49896-495">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49896-495">Minimum supported client</span></span><br/> | <span data-ttu-id="49896-496">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49896-496">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49896-497">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49896-497">Minimum supported server</span></span><br/> | <span data-ttu-id="49896-498">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49896-498">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49896-499">Namespace</span><span class="sxs-lookup"><span data-stu-id="49896-499">Namespace</span></span><br/>                | <span data-ttu-id="49896-500">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49896-500">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49896-501">MOF</span><span class="sxs-lookup"><span data-stu-id="49896-501">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49896-502"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="49896-502"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49896-503">DLL</span><span class="sxs-lookup"><span data-stu-id="49896-503">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49896-504"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49896-504"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49896-505">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49896-505">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49896-506">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="49896-506">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

