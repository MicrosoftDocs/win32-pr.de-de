---
description: Stellt einen synthetischen Fibre Channel Anschluss dar.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Msvm_SyntheticFcPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128428"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="34d17-103">MSVM \_ syntheticfcport-Klasse</span><span class="sxs-lookup"><span data-stu-id="34d17-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="34d17-104">Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="34d17-105">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="34d17-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="34d17-106">Stellt einen synthetischen Fibre Channel Anschluss dar.</span><span class="sxs-lookup"><span data-stu-id="34d17-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="34d17-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34d17-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d17-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d17-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="34d17-109">Member</span><span class="sxs-lookup"><span data-stu-id="34d17-109">Members</span></span>

<span data-ttu-id="34d17-110">Die **MSVM \_ syntheticfcport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="34d17-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="34d17-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="34d17-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="34d17-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34d17-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34d17-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="34d17-113">Methods</span></span>

<span data-ttu-id="34d17-114">Die **MSVM \_ syntheticfcport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="34d17-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="34d17-115">Methode</span><span class="sxs-lookup"><span data-stu-id="34d17-115">Method</span></span>                                                                | <span data-ttu-id="34d17-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34d17-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="34d17-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="34d17-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="34d17-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d17-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="34d17-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="34d17-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="34d17-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d17-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="34d17-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="34d17-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="34d17-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d17-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="34d17-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="34d17-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="34d17-124">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="34d17-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="34d17-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="34d17-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="34d17-126">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="34d17-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="34d17-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="34d17-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="34d17-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d17-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="34d17-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="34d17-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="34d17-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d17-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="34d17-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="34d17-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="34d17-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d17-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="34d17-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34d17-133">Properties</span></span>

<span data-ttu-id="34d17-134">Die **MSVM \_ syntheticfcport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34d17-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34d17-135">**Activecos**</span><span class="sxs-lookup"><span data-stu-id="34d17-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-136">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-138">Ein Array von ganzen Zahlen, das die aktiven Dienst Klassen angibt.</span><span class="sxs-lookup"><span data-stu-id="34d17-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="34d17-139">Die unterstützten cos werden von der **supportedcos** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="34d17-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="34d17-140">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="34d17-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="34d17-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="34d17-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="34d17-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="34d17-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="34d17-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-150">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-152">Ein Array von ganzen Zahlen, das die Fibre Channel FC-4-Protokolle angibt, die gerade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34d17-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="34d17-153">Eine Liste aller unterstützten Protokolle wird von der **SupportedFC4Types** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="34d17-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="34d17-154">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="34d17-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="34d17-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="34d17-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="34d17-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="34d17-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="34d17-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="34d17-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="34d17-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="34d17-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="34d17-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="34d17-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="34d17-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="34d17-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="34d17-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="34d17-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="34d17-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="34d17-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="34d17-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="34d17-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="34d17-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="34d17-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="34d17-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="34d17-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="34d17-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-181">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="34d17-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-182">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-184">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="34d17-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34d17-185">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="34d17-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="34d17-186">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-187">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="34d17-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-188">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-190">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="34d17-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="34d17-191">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-192">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="34d17-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-193">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-195">Gibt an, ob der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="34d17-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="34d17-196">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-197">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="34d17-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-200">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="34d17-200">The primary availability and status of the device.</span></span> <span data-ttu-id="34d17-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-202">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="34d17-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-203">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-205">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="34d17-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="34d17-206">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d17-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="34d17-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-210">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="34d17-210">A short description of the object.</span></span> <span data-ttu-id="34d17-211">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-212">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="34d17-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-215">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="34d17-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="34d17-216">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34d17-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34d17-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="34d17-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="34d17-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="34d17-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34d17-225">)</span><span class="sxs-lookup"><span data-stu-id="34d17-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-226">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="34d17-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-229">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="34d17-229">The scoping system's creation class name.</span></span> <span data-ttu-id="34d17-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-231">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34d17-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-234">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="34d17-234">A description of the object.</span></span> <span data-ttu-id="34d17-235">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="34d17-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-239">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="34d17-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="34d17-240">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34d17-241">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34d17-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="34d17-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="34d17-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="34d17-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="34d17-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34d17-250">)</span><span class="sxs-lookup"><span data-stu-id="34d17-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="34d17-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-254">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="34d17-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="34d17-255">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="34d17-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-259">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="34d17-259">A display name for the object.</span></span> <span data-ttu-id="34d17-260">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-261">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="34d17-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-262">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-264">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="34d17-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="34d17-265">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d17-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="34d17-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-269">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="34d17-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="34d17-270">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="34d17-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="34d17-271">Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="34d17-272">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="34d17-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="34d17-273"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="34d17-274">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="34d17-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="34d17-275"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="34d17-276"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="34d17-277">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34d17-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="34d17-278"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="34d17-279">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="34d17-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="34d17-280"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="34d17-281">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="34d17-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="34d17-282"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="34d17-283">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="34d17-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="34d17-284"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="34d17-285">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="34d17-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="34d17-286"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="34d17-287">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="34d17-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="34d17-288"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="34d17-289">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="34d17-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="34d17-290"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="34d17-291">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="34d17-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="34d17-292">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="34d17-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="34d17-293">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="34d17-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="34d17-294"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="34d17-295">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="34d17-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="34d17-296">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="34d17-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="34d17-297">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="34d17-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-298">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-300">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="34d17-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="34d17-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="34d17-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-305">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="34d17-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="34d17-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-307">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="34d17-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-308">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-310">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="34d17-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="34d17-311">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="34d17-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-313">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-315">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="34d17-315">The current health of the element.</span></span> <span data-ttu-id="34d17-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="34d17-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-318">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="34d17-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-320">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="34d17-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="34d17-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="34d17-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-323">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="34d17-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-325">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="34d17-325">The date and time when the object was installed.</span></span> <span data-ttu-id="34d17-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="34d17-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="34d17-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-331">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="34d17-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="34d17-332">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="34d17-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="34d17-333">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="34d17-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34d17-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-337">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="34d17-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="34d17-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-339">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="34d17-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-340">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-342">Gibt den Typ der Link Technologie für den Port an.</span><span class="sxs-lookup"><span data-stu-id="34d17-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="34d17-343">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="34d17-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="34d17-344">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="34d17-345">Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="34d17-346">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="34d17-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="34d17-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="34d17-348">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="34d17-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34d17-349">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="34d17-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-350">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-352">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="34d17-352">This property has been deprecated.</span></span> <span data-ttu-id="34d17-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-354">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="34d17-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-355">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-357">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="34d17-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="34d17-358">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="34d17-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="34d17-359">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-360">**Name**</span><span class="sxs-lookup"><span data-stu-id="34d17-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-363">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-363">The label by which the object is known.</span></span> <span data-ttu-id="34d17-364">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-365">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="34d17-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-366">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="34d17-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-368">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="34d17-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="34d17-369">Ein Array von Zeichen folgen, die die Mac-Adressen für den Port enthalten.</span><span class="sxs-lookup"><span data-stu-id="34d17-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="34d17-370">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-371">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="34d17-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-372">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-374">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="34d17-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="34d17-375">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34d17-376">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34d17-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="34d17-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="34d17-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="34d17-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="34d17-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="34d17-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="34d17-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="34d17-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="34d17-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="34d17-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="34d17-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="34d17-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="34d17-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="34d17-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="34d17-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="34d17-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="34d17-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34d17-396">)</span><span class="sxs-lookup"><span data-stu-id="34d17-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="34d17-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-398">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-400">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="34d17-400">The current statuses of the object.</span></span> <span data-ttu-id="34d17-401">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-402">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="34d17-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-405">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="34d17-406">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="34d17-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="34d17-407">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d17-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="34d17-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-409">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="34d17-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-411">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="34d17-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="34d17-412">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-413">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="34d17-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-414">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-416">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn er auf 1 festgelegt ist (andere).</span><span class="sxs-lookup"><span data-stu-id="34d17-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="34d17-417">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-418">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="34d17-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-419">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-421">Die Verwendung dieser Eigenschaft wird anstelle der **portType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="34d17-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="34d17-422">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-423">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="34d17-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-426">Beschreibt den Modultyp, wenn **portType** auf 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="34d17-427">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-428">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="34d17-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-429">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-431">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="34d17-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="34d17-432">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="34d17-433">Diese hart codierte Adresse kann mithilfe eines Firmware-Upgrades oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="34d17-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="34d17-434">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="34d17-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="34d17-435">Diese Eigenschaft sollte **null** sein, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="34d17-436">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-437">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="34d17-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-438">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-440">Die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="34d17-440">The port number.</span></span> <span data-ttu-id="34d17-441">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-442">**PortType**</span><span class="sxs-lookup"><span data-stu-id="34d17-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-443">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-445">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="34d17-446">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige **otherporttype** -Eigenschaft eine Zeichen folgen Beschreibung des Port Typs.</span><span class="sxs-lookup"><span data-stu-id="34d17-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="34d17-447">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="34d17-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="34d17-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="34d17-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="34d17-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="34d17-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="34d17-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="34d17-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="34d17-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="34d17-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="34d17-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="34d17-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="34d17-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="34d17-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="34d17-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="34d17-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="34d17-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="34d17-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="34d17-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="34d17-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="34d17-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="34d17-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-470">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="34d17-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-471">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-473">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="34d17-473">The power management capabilities of the device.</span></span> <span data-ttu-id="34d17-474">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-475">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="34d17-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-476">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-478">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="34d17-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="34d17-479">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-480">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="34d17-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-481">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-483">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="34d17-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="34d17-484">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-485">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="34d17-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-486">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-488">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="34d17-488">Provides high level status information.</span></span> <span data-ttu-id="34d17-489">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="34d17-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="34d17-490">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="34d17-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34d17-491">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34d17-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="34d17-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="34d17-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="34d17-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34d17-498">)</span><span class="sxs-lookup"><span data-stu-id="34d17-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-499">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="34d17-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-500">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-501">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-502">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="34d17-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="34d17-503">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="34d17-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="34d17-504">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="34d17-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="34d17-505">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="34d17-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-507">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-508">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-509">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="34d17-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="34d17-510">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d17-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-511">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="34d17-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-512">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-514">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="34d17-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="34d17-515">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="34d17-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="34d17-516">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-517">**Status**</span><span class="sxs-lookup"><span data-stu-id="34d17-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-518">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-520">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="34d17-520">The current status of the object.</span></span> <span data-ttu-id="34d17-521">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-522">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="34d17-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-523">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="34d17-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-525">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="34d17-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="34d17-526">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="34d17-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-528">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-529">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-530">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="34d17-530">The current state of the logical device.</span></span> <span data-ttu-id="34d17-531">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-532">**Supportedcos**</span><span class="sxs-lookup"><span data-stu-id="34d17-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-533">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-534">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-535">Ein Array von ganzen Zahlen, das die Fibre Channel unterstützten Klassen von Dienst (COS) angibt.</span><span class="sxs-lookup"><span data-stu-id="34d17-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="34d17-536">Die aktiven COs werden von der **activecos** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="34d17-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="34d17-537">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="34d17-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-539"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-540"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="34d17-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-541"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-542"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-543"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="34d17-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-544"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="34d17-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-545"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="34d17-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="34d17-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-547">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34d17-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d17-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-549">Ein Array von ganzen Zahlen, das die unterstützten Fibre Channel FC-4-Protokolle angibt.</span><span class="sxs-lookup"><span data-stu-id="34d17-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="34d17-550">Die Protokolle, die aktiv sind und ausgeführt werden, werden von der **ActiveFC4Types** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="34d17-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="34d17-551">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="34d17-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="34d17-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="34d17-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="34d17-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="34d17-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="34d17-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="34d17-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="34d17-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="34d17-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="34d17-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="34d17-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="34d17-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="34d17-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="34d17-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="34d17-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="34d17-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="34d17-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="34d17-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="34d17-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="34d17-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="34d17-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="34d17-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="34d17-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="34d17-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="34d17-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34d17-578">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="34d17-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-579">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-580">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d17-581">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="34d17-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34d17-582">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="34d17-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="34d17-583">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-584">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="34d17-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-585">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-586">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-587">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="34d17-587">The scoping system's creation class name.</span></span> <span data-ttu-id="34d17-588">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-589">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="34d17-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-590">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34d17-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-591">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-592">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="34d17-592">The scoping system's name.</span></span> <span data-ttu-id="34d17-593">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="34d17-594">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="34d17-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-595">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="34d17-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-596">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-597">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="34d17-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="34d17-598">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d17-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-599">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="34d17-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-600">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34d17-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-601">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-602">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="34d17-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="34d17-603">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d17-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-604">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="34d17-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-605">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-606">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-607">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="34d17-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="34d17-608">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d17-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34d17-609">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="34d17-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d17-610">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d17-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d17-611">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34d17-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d17-612">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="34d17-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="34d17-613">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="34d17-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="34d17-614">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="34d17-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="34d17-615">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="34d17-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="34d17-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34d17-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="34d17-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="34d17-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34d17-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="34d17-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34d17-620">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34d17-620">Requirements</span></span>



| <span data-ttu-id="34d17-621">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34d17-621">Requirement</span></span> | <span data-ttu-id="34d17-622">Wert</span><span class="sxs-lookup"><span data-stu-id="34d17-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34d17-623">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34d17-623">Minimum supported client</span></span><br/> | <span data-ttu-id="34d17-624">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34d17-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34d17-625">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34d17-625">Minimum supported server</span></span><br/> | <span data-ttu-id="34d17-626">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34d17-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34d17-627">Namespace</span><span class="sxs-lookup"><span data-stu-id="34d17-627">Namespace</span></span><br/>                | <span data-ttu-id="34d17-628">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="34d17-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34d17-629">MOF</span><span class="sxs-lookup"><span data-stu-id="34d17-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34d17-630"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34d17-631">DLL</span><span class="sxs-lookup"><span data-stu-id="34d17-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34d17-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34d17-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

