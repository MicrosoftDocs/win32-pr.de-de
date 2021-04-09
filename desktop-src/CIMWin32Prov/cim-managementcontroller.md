---
description: Die CIM \_ Managementcontroller-Klasse bezieht sich auf die Funktionen und die Verwaltung eines Verwaltungs Controllers.
ms.assetid: 47ad29d1-5021-4469-87c0-bd9403faa70c
ms.tgt_platform: multiple
title: CIM_ManagementController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagementController
- CIM_ManagementController.Availability
- CIM_ManagementController.Caption
- CIM_ManagementController.ConfigManagerErrorCode
- CIM_ManagementController.ConfigManagerUserConfig
- CIM_ManagementController.CreationClassName
- CIM_ManagementController.Description
- CIM_ManagementController.DeviceID
- CIM_ManagementController.ErrorCleared
- CIM_ManagementController.ErrorDescription
- CIM_ManagementController.InstallDate
- CIM_ManagementController.LastErrorCode
- CIM_ManagementController.MaxNumberControlled
- CIM_ManagementController.Name
- CIM_ManagementController.PNPDeviceID
- CIM_ManagementController.PowerManagementCapabilities
- CIM_ManagementController.PowerManagementSupported
- CIM_ManagementController.ProtocolSupported
- CIM_ManagementController.Status
- CIM_ManagementController.StatusInfo
- CIM_ManagementController.SystemCreationClassName
- CIM_ManagementController.SystemName
- CIM_ManagementController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c5eab51a8c8a370086f5cd5ac9215948fcd2e2f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958400"
---
# <a name="cim_managementcontroller-class"></a><span data-ttu-id="b25c3-103">CIM- \_ Managementcontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="b25c3-103">CIM\_ManagementController class</span></span>

<span data-ttu-id="b25c3-104">Die **CIM \_ Managementcontroller** -Klasse bezieht sich auf die Funktionen und die Verwaltung eines Verwaltungs Controllers.</span><span class="sxs-lookup"><span data-stu-id="b25c3-104">The **CIM\_ManagementController** class relates to the capabilities and management of a management controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b25c3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b25c3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b25c3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b25c3-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b25c3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b25c3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25c3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b25c3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7250D62E-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ManagementController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="b25c3-110">Member</span><span class="sxs-lookup"><span data-stu-id="b25c3-110">Members</span></span>

<span data-ttu-id="b25c3-111">Die **CIM- \_ Managementcontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b25c3-111">The **CIM\_ManagementController** class has these types of members:</span></span>

-   [<span data-ttu-id="b25c3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b25c3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b25c3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b25c3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b25c3-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="b25c3-114">Methods</span></span>

<span data-ttu-id="b25c3-115">Die **CIM \_ Managementcontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-115">The **CIM\_ManagementController** class has these methods.</span></span>



| <span data-ttu-id="b25c3-116">Methode</span><span class="sxs-lookup"><span data-stu-id="b25c3-116">Method</span></span>                                                                          | <span data-ttu-id="b25c3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b25c3-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b25c3-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="b25c3-118">**Reset**</span></span>](reset-method-in-class-cim-managementcontroller.md)                 | <span data-ttu-id="b25c3-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="b25c3-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b25c3-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b25c3-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b25c3-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-managementcontroller.md) | <span data-ttu-id="b25c3-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b25c3-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b25c3-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b25c3-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b25c3-124">Properties</span></span>

<span data-ttu-id="b25c3-125">Die **CIM \_ Managementcontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b25c3-125">The **CIM\_ManagementController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b25c3-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="b25c3-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b25c3-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="b25c3-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-130">Availability and status of the device.</span></span>

<span data-ttu-id="b25c3-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b25c3-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b25c3-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b25c3-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b25c3-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b25c3-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="b25c3-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b25c3-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="b25c3-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b25c3-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="b25c3-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b25c3-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="b25c3-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b25c3-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="b25c3-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b25c3-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="b25c3-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b25c3-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b25c3-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b25c3-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="b25c3-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b25c3-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="b25c3-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b25c3-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="b25c3-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b25c3-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="b25c3-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b25c3-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="b25c3-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b25c3-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b25c3-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b25c3-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b25c3-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="b25c3-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b25c3-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="b25c3-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b25c3-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="b25c3-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="b25c3-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b25c3-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="b25c3-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="b25c3-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b25c3-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="b25c3-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b25c3-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="b25c3-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="b25c3-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b25c3-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b25c3-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-164">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b25c3-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-165">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-165">Short textual description of the object.</span></span>

<span data-ttu-id="b25c3-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-167">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="b25c3-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b25c3-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-170">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b25c3-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-171">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b25c3-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b25c3-172">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b25c3-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b25c3-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="b25c3-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-175">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b25c3-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b25c3-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b25c3-177">(1)</span><span class="sxs-lookup"><span data-stu-id="b25c3-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-178">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b25c3-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b25c3-180">(2)</span><span class="sxs-lookup"><span data-stu-id="b25c3-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b25c3-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b25c3-182">(3)</span><span class="sxs-lookup"><span data-stu-id="b25c3-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-183">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b25c3-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b25c3-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b25c3-185">(4)</span><span class="sxs-lookup"><span data-stu-id="b25c3-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-186">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b25c3-186">Device is not working properly.</span></span> <span data-ttu-id="b25c3-187">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b25c3-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b25c3-189">(5)</span><span class="sxs-lookup"><span data-stu-id="b25c3-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-190">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b25c3-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b25c3-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b25c3-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="b25c3-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-193">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="b25c3-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b25c3-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b25c3-195">(7)</span><span class="sxs-lookup"><span data-stu-id="b25c3-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b25c3-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b25c3-197">(8)</span><span class="sxs-lookup"><span data-stu-id="b25c3-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-198">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b25c3-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b25c3-200">(9)</span><span class="sxs-lookup"><span data-stu-id="b25c3-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-201">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="b25c3-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b25c3-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b25c3-203">(10)</span><span class="sxs-lookup"><span data-stu-id="b25c3-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-204">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b25c3-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b25c3-206">(11)</span><span class="sxs-lookup"><span data-stu-id="b25c3-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-207">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="b25c3-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b25c3-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b25c3-209">(12)</span><span class="sxs-lookup"><span data-stu-id="b25c3-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-210">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b25c3-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b25c3-212">(13)</span><span class="sxs-lookup"><span data-stu-id="b25c3-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-213">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b25c3-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b25c3-215">(14)</span><span class="sxs-lookup"><span data-stu-id="b25c3-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-216">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b25c3-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b25c3-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b25c3-218">(15)</span><span class="sxs-lookup"><span data-stu-id="b25c3-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-219">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b25c3-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b25c3-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b25c3-221">(16)</span><span class="sxs-lookup"><span data-stu-id="b25c3-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-222">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b25c3-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b25c3-224">(17)</span><span class="sxs-lookup"><span data-stu-id="b25c3-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-225">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="b25c3-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b25c3-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b25c3-227">(18)</span><span class="sxs-lookup"><span data-stu-id="b25c3-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-228">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b25c3-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b25c3-230">(19)</span><span class="sxs-lookup"><span data-stu-id="b25c3-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b25c3-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b25c3-232">(20)</span><span class="sxs-lookup"><span data-stu-id="b25c3-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-233">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b25c3-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b25c3-235">(21)</span><span class="sxs-lookup"><span data-stu-id="b25c3-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-236">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="b25c3-236">System failure.</span></span> <span data-ttu-id="b25c3-237">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b25c3-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b25c3-238">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b25c3-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b25c3-240">(22)</span><span class="sxs-lookup"><span data-stu-id="b25c3-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-241">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b25c3-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b25c3-243">(23)</span><span class="sxs-lookup"><span data-stu-id="b25c3-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="b25c3-244">System failure.</span></span> <span data-ttu-id="b25c3-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b25c3-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b25c3-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b25c3-247">(24)</span><span class="sxs-lookup"><span data-stu-id="b25c3-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-248">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b25c3-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b25c3-250">(25)</span><span class="sxs-lookup"><span data-stu-id="b25c3-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-251">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b25c3-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b25c3-253">(26)</span><span class="sxs-lookup"><span data-stu-id="b25c3-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-254">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b25c3-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b25c3-256">(27)</span><span class="sxs-lookup"><span data-stu-id="b25c3-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-257">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b25c3-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b25c3-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b25c3-259">(28)</span><span class="sxs-lookup"><span data-stu-id="b25c3-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-260">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b25c3-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b25c3-262">(29)</span><span class="sxs-lookup"><span data-stu-id="b25c3-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-263">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b25c3-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b25c3-265">(30)</span><span class="sxs-lookup"><span data-stu-id="b25c3-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-266">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b25c3-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b25c3-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b25c3-268">31,5</span><span class="sxs-lookup"><span data-stu-id="b25c3-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-269">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b25c3-270">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="b25c3-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-271">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b25c3-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-273">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b25c3-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-274">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b25c3-275">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-276">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b25c3-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-277">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-279">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b25c3-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-280">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b25c3-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b25c3-281">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b25c3-282">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-283">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b25c3-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-286">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b25c3-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-287">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-287">Textual description of the object.</span></span>

<span data-ttu-id="b25c3-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b25c3-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-292">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b25c3-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-293">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="b25c3-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b25c3-294">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-295">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="b25c3-295">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-296">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b25c3-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-298">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b25c3-298">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b25c3-299">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-300">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b25c3-300">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-303">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="b25c3-303">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b25c3-304">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b25c3-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-306">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b25c3-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-308">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="b25c3-308">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-309">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-309">Date and time the object was installed.</span></span> <span data-ttu-id="b25c3-310">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b25c3-310">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b25c3-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-312">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b25c3-312">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-313">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b25c3-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-315">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b25c3-315">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b25c3-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-317">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="b25c3-317">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-318">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b25c3-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-320">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="b25c3-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-321">Maximale Anzahl direkt Adressier barer Entitäten, die vom Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-321">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="b25c3-322">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-322">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="b25c3-323">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-323">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-324">**Name**</span><span class="sxs-lookup"><span data-stu-id="b25c3-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-327">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b25c3-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-328">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b25c3-328">Label by which the object is known.</span></span> <span data-ttu-id="b25c3-329">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-329">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b25c3-330">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-331">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b25c3-331">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-332">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-334">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b25c3-334">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-335">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-335">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b25c3-336">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b25c3-337">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b25c3-337">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-338">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="b25c3-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-339">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b25c3-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-341">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-341">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b25c3-342">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-342">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b25c3-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b25c3-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b25c3-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b25c3-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b25c3-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="b25c3-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b25c3-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b25c3-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-347">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b25c3-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b25c3-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="b25c3-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-349">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="b25c3-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b25c3-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="b25c3-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-351">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b25c3-352">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b25c3-353">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b25c3-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b25c3-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="b25c3-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-355">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b25c3-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b25c3-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="b25c3-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b25c3-357">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b25c3-357">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b25c3-358">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="b25c3-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-359">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b25c3-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-361">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b25c3-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b25c3-362">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="b25c3-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b25c3-363">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b25c3-364">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="b25c3-364">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b25c3-365">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-366">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="b25c3-366">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-367">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b25c3-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-369">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b25c3-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-370">Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b25c3-370">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="b25c3-371">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-371">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="b25c3-372">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="b25c3-372">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b25c3-373">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b25c3-373">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b25c3-374">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b25c3-374">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="b25c3-375">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="b25c3-375">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="b25c3-376">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="b25c3-376">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="b25c3-377">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="b25c3-377">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="b25c3-378">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="b25c3-378">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="b25c3-379">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="b25c3-379">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="b25c3-380">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="b25c3-380">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="b25c3-381">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="b25c3-381">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="b25c3-382">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="b25c3-382">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="b25c3-383">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="b25c3-383">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="b25c3-384">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="b25c3-384">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="b25c3-385">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="b25c3-385">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="b25c3-386">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="b25c3-386">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="b25c3-387">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="b25c3-387">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="b25c3-388">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="b25c3-388">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="b25c3-389">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="b25c3-389">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="b25c3-390">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="b25c3-390">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="b25c3-391">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="b25c3-391">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="b25c3-392">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="b25c3-392">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="b25c3-393">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="b25c3-393">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="b25c3-394">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="b25c3-394">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="b25c3-395">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="b25c3-395">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="b25c3-396">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="b25c3-396">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="b25c3-397">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="b25c3-397">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="b25c3-398">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="b25c3-398">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="b25c3-399">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="b25c3-399">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="b25c3-400">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="b25c3-400">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="b25c3-401">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="b25c3-401">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="b25c3-402">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="b25c3-402">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="b25c3-403">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="b25c3-403">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="b25c3-404">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="b25c3-404">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="b25c3-405">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="b25c3-405">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="b25c3-406">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="b25c3-406">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="b25c3-407">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="b25c3-407">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="b25c3-408">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="b25c3-408">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="b25c3-409">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="b25c3-409">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="b25c3-410">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="b25c3-410">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="b25c3-411">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="b25c3-411">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="b25c3-412">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="b25c3-412">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="b25c3-413">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="b25c3-413">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="b25c3-414">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="b25c3-414">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="b25c3-415">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="b25c3-415">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="b25c3-416">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="b25c3-416">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="b25c3-417">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="b25c3-417">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="b25c3-418">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="b25c3-418">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="b25c3-419">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="b25c3-419">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b25c3-420">**Status**</span><span class="sxs-lookup"><span data-stu-id="b25c3-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-423">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b25c3-423">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-424">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-424">Current status of the object.</span></span>

<span data-ttu-id="b25c3-425">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b25c3-426">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="b25c3-426">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b25c3-427">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b25c3-427">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b25c3-428">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="b25c3-428">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b25c3-429">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="b25c3-429">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b25c3-430">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b25c3-430">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b25c3-431">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b25c3-431">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b25c3-432">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="b25c3-432">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b25c3-433">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="b25c3-433">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b25c3-434">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="b25c3-434">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b25c3-435">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="b25c3-435">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b25c3-436">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="b25c3-436">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b25c3-437">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="b25c3-437">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b25c3-438">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="b25c3-438">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b25c3-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b25c3-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-440">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b25c3-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-442">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b25c3-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-443">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b25c3-443">State of the logical device.</span></span> <span data-ttu-id="b25c3-444">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b25c3-444">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b25c3-445">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b25c3-446">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b25c3-446">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b25c3-447">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b25c3-447">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b25c3-448">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b25c3-448">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b25c3-449">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="b25c3-449">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b25c3-450">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="b25c3-450">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b25c3-451">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b25c3-451">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-452">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-454">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b25c3-454">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-455">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="b25c3-455">Scoping system's creation class name.</span></span>

<span data-ttu-id="b25c3-456">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-457">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="b25c3-457">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-458">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b25c3-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-460">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b25c3-460">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-461">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="b25c3-461">Scoping system's name.</span></span>

<span data-ttu-id="b25c3-462">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-462">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25c3-463">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="b25c3-463">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25c3-464">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b25c3-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b25c3-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b25c3-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25c3-466">Datum und Uhrzeit des letzten zurück Setzens des Controllers.</span><span class="sxs-lookup"><span data-stu-id="b25c3-466">Date and time this controller was last reset.</span></span> <span data-ttu-id="b25c3-467">Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b25c3-467">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="b25c3-468">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b25c3-468">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b25c3-469">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b25c3-469">Remarks</span></span>

<span data-ttu-id="b25c3-470">Die **CIM- \_ Managementcontroller** -Klasse wird vom [**CIM- \_ Controller**](cim-controller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-470">The **CIM\_ManagementController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="b25c3-471">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b25c3-471">WMI does not implement this class.</span></span>

<span data-ttu-id="b25c3-472">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b25c3-472">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b25c3-473">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b25c3-473">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b25c3-474">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b25c3-474">Requirements</span></span>



| <span data-ttu-id="b25c3-475">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b25c3-475">Requirement</span></span> | <span data-ttu-id="b25c3-476">Wert</span><span class="sxs-lookup"><span data-stu-id="b25c3-476">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b25c3-477">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b25c3-477">Minimum supported client</span></span><br/> | <span data-ttu-id="b25c3-478">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b25c3-478">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b25c3-479">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b25c3-479">Minimum supported server</span></span><br/> | <span data-ttu-id="b25c3-480">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b25c3-480">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b25c3-481">Namespace</span><span class="sxs-lookup"><span data-stu-id="b25c3-481">Namespace</span></span><br/>                | <span data-ttu-id="b25c3-482">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b25c3-482">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b25c3-483">MOF</span><span class="sxs-lookup"><span data-stu-id="b25c3-483">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b25c3-484"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b25c3-484"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b25c3-485">DLL</span><span class="sxs-lookup"><span data-stu-id="b25c3-485">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25c3-486"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25c3-486"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b25c3-487">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b25c3-487">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25c3-488">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="b25c3-488">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

