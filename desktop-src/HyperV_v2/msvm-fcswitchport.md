---
description: Stellt einen Port auf dem virtuellen Fibre Channel Switch dar.
ms.assetid: 6b4553b7-2717-4285-9e1a-e2ad22a60997
title: Msvm_FcSwitchPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcSwitchPort
- Msvm_FcSwitchPort.SetPowerState
- Msvm_FcSwitchPort.EnableDevice
- Msvm_FcSwitchPort.OnlineDevice
- Msvm_FcSwitchPort.QuiesceDevice
- Msvm_FcSwitchPort.SaveProperties
- Msvm_FcSwitchPort.RestoreProperties
- Msvm_FcSwitchPort.InstanceID
- Msvm_FcSwitchPort.Caption
- Msvm_FcSwitchPort.Description
- Msvm_FcSwitchPort.ElementName
- Msvm_FcSwitchPort.InstallDate
- Msvm_FcSwitchPort.Name
- Msvm_FcSwitchPort.OperationalStatus
- Msvm_FcSwitchPort.StatusDescriptions
- Msvm_FcSwitchPort.Status
- Msvm_FcSwitchPort.HealthState
- Msvm_FcSwitchPort.CommunicationStatus
- Msvm_FcSwitchPort.DetailedStatus
- Msvm_FcSwitchPort.OperatingStatus
- Msvm_FcSwitchPort.PrimaryStatus
- Msvm_FcSwitchPort.EnabledState
- Msvm_FcSwitchPort.OtherEnabledState
- Msvm_FcSwitchPort.RequestedState
- Msvm_FcSwitchPort.EnabledDefault
- Msvm_FcSwitchPort.TimeOfLastStateChange
- Msvm_FcSwitchPort.AvailableRequestedStates
- Msvm_FcSwitchPort.TransitioningToState
- Msvm_FcSwitchPort.SystemCreationClassName
- Msvm_FcSwitchPort.SystemName
- Msvm_FcSwitchPort.CreationClassName
- Msvm_FcSwitchPort.DeviceID
- Msvm_FcSwitchPort.PowerManagementSupported
- Msvm_FcSwitchPort.PowerManagementCapabilities
- Msvm_FcSwitchPort.Availability
- Msvm_FcSwitchPort.StatusInfo
- Msvm_FcSwitchPort.LastErrorCode
- Msvm_FcSwitchPort.ErrorDescription
- Msvm_FcSwitchPort.ErrorCleared
- Msvm_FcSwitchPort.OtherIdentifyingInfo
- Msvm_FcSwitchPort.PowerOnHours
- Msvm_FcSwitchPort.TotalPowerOnHours
- Msvm_FcSwitchPort.IdentifyingDescriptions
- Msvm_FcSwitchPort.AdditionalAvailability
- Msvm_FcSwitchPort.MaxQuiesceTime
- Msvm_FcSwitchPort.Speed
- Msvm_FcSwitchPort.MaxSpeed
- Msvm_FcSwitchPort.RequestedSpeed
- Msvm_FcSwitchPort.UsageRestriction
- Msvm_FcSwitchPort.PortType
- Msvm_FcSwitchPort.OtherPortType
- Msvm_FcSwitchPort.OtherNetworkPortType
- Msvm_FcSwitchPort.PortNumber
- Msvm_FcSwitchPort.LinkTechnology
- Msvm_FcSwitchPort.OtherLinkTechnology
- Msvm_FcSwitchPort.PermanentAddress
- Msvm_FcSwitchPort.NetworkAddresses
- Msvm_FcSwitchPort.FullDuplex
- Msvm_FcSwitchPort.AutoSense
- Msvm_FcSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_FcSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_FcSwitchPort.SupportedCOS
- Msvm_FcSwitchPort.ActiveCOS
- Msvm_FcSwitchPort.SupportedFC4Types
- Msvm_FcSwitchPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443ae1065b7c7a6a4bb1523a672e388cacb91667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526840"
---
# <a name="msvm_fcswitchport-class"></a><span data-ttu-id="f9b62-103">MSVM \_ fcswitchport-Klasse</span><span class="sxs-lookup"><span data-stu-id="f9b62-103">Msvm\_FcSwitchPort class</span></span>

> [!NOTE]
> <span data-ttu-id="f9b62-104">Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="f9b62-105">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="f9b62-106">Stellt einen Port auf dem virtuellen Fibre Channel Switch dar.</span><span class="sxs-lookup"><span data-stu-id="f9b62-106">Represents a port on the virtual Fibre Channel switch.</span></span>

<span data-ttu-id="f9b62-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9b62-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9b62-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcSwitchPort : CIM_FCPort
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
  uint16   LinkTechnology;
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

## <a name="members"></a><span data-ttu-id="f9b62-109">Member</span><span class="sxs-lookup"><span data-stu-id="f9b62-109">Members</span></span>

<span data-ttu-id="f9b62-110">Die **MSVM \_ fcswitchport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f9b62-110">The **Msvm\_FcSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="f9b62-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f9b62-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9b62-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9b62-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9b62-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f9b62-113">Methods</span></span>

<span data-ttu-id="f9b62-114">Die **MSVM \_ fcswitchport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-114">The **Msvm\_FcSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="f9b62-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f9b62-115">Method</span></span>                                                             | <span data-ttu-id="f9b62-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9b62-116">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="f9b62-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f9b62-117">**EnableDevice**</span></span>                                                   | <span data-ttu-id="f9b62-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f9b62-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="f9b62-119">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="f9b62-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f9b62-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="f9b62-121">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="f9b62-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="f9b62-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f9b62-123">**RequestStateChange**</span></span>](msvm-fcswitchport-requeststatechange.md) | <span data-ttu-id="f9b62-124">fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="f9b62-124">requests a state change.</span></span><br/>      |
| [<span data-ttu-id="f9b62-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="f9b62-125">**Reset**</span></span>](msvm-fcswitchport-reset.md)                           | <span data-ttu-id="f9b62-126">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="f9b62-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="f9b62-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="f9b62-127">**RestoreProperties**</span></span>                                              | <span data-ttu-id="f9b62-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f9b62-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f9b62-129">**SaveProperties**</span></span>                                                 | <span data-ttu-id="f9b62-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f9b62-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f9b62-131">**SetPowerState**</span></span>                                                  | <span data-ttu-id="f9b62-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f9b62-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9b62-133">Properties</span></span>

<span data-ttu-id="f9b62-134">Die **MSVM \_ fcswitchport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9b62-134">The **Msvm\_FcSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-135">**Activecos**</span><span class="sxs-lookup"><span data-stu-id="f9b62-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-136">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-138">Ein Array von ganzen Zahlen, das die aktiven Dienst Klassen angibt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="f9b62-139">Die unterstützten cos werden von der **supportedcos** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9b62-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="f9b62-140">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="f9b62-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="f9b62-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="f9b62-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-150">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-152">Ein Array von ganzen Zahlen, das die Fibre Channel FC-4-Protokolle angibt, die gerade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="f9b62-153">Eine Liste aller unterstützten Protokolle wird von der **SupportedFC4Types** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9b62-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="f9b62-154">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="f9b62-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="f9b62-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="f9b62-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="f9b62-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="f9b62-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="f9b62-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="f9b62-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="f9b62-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="f9b62-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="f9b62-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="f9b62-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="f9b62-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="f9b62-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="f9b62-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="f9b62-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="f9b62-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="f9b62-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="f9b62-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="f9b62-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="f9b62-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="f9b62-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="f9b62-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-181">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="f9b62-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-182">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-184">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="f9b62-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-185">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f9b62-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="f9b62-186">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-187">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="f9b62-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-188">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-190">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="f9b62-191">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-192">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="f9b62-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-193">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f9b62-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-195">Gibt an, ob der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="f9b62-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="f9b62-196">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-197">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="f9b62-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-200">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-200">The primary availability and status of the device.</span></span> <span data-ttu-id="f9b62-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-202">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="f9b62-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-203">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-205">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="f9b62-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f9b62-206">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f9b62-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-210">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-210">A short description of the object.</span></span> <span data-ttu-id="f9b62-211">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-212">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="f9b62-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-215">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f9b62-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f9b62-216">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f9b62-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f9b62-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f9b62-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f9b62-225">)</span><span class="sxs-lookup"><span data-stu-id="f9b62-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-226">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f9b62-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-229">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f9b62-229">The scoping system's creation class name.</span></span> <span data-ttu-id="f9b62-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-231">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9b62-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-234">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-234">A description of the object.</span></span> <span data-ttu-id="f9b62-235">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f9b62-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-239">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="f9b62-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f9b62-240">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f9b62-241">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f9b62-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f9b62-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f9b62-250">)</span><span class="sxs-lookup"><span data-stu-id="f9b62-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f9b62-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-254">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="f9b62-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="f9b62-255">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f9b62-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-259">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-259">A display name for the object.</span></span> <span data-ttu-id="f9b62-260">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-261">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="f9b62-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-262">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-264">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="f9b62-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="f9b62-265">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f9b62-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-269">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="f9b62-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f9b62-270">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="f9b62-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="f9b62-271">Wert</span><span class="sxs-lookup"><span data-stu-id="f9b62-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="f9b62-272">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9b62-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="f9b62-273"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="f9b62-274">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="f9b62-275"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="f9b62-276"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="f9b62-277">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="f9b62-278"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="f9b62-279">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f9b62-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="f9b62-280"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="f9b62-281">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="f9b62-282"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="f9b62-283">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="f9b62-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="f9b62-284"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="f9b62-285">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="f9b62-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="f9b62-286"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="f9b62-287">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="f9b62-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="f9b62-288"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="f9b62-289">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="f9b62-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="f9b62-290"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="f9b62-291">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="f9b62-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="f9b62-292">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="f9b62-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="f9b62-293">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="f9b62-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="f9b62-294"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="f9b62-295">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="f9b62-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="f9b62-296">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="f9b62-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="f9b62-297">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="f9b62-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-298">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f9b62-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-300">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f9b62-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="f9b62-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f9b62-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-305">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="f9b62-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="f9b62-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-307">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="f9b62-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-308">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f9b62-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-310">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f9b62-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="f9b62-311">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f9b62-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-313">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-315">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="f9b62-315">The current health of the element.</span></span> <span data-ttu-id="f9b62-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f9b62-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-318">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-320">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f9b62-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f9b62-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f9b62-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-323">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f9b62-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-325">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-325">The date and time when the object was installed.</span></span> <span data-ttu-id="f9b62-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="f9b62-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f9b62-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-331">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f9b62-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-332">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f9b62-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f9b62-333">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f9b62-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9b62-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-337">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f9b62-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="f9b62-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-339">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="f9b62-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-340">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-342">Gibt den Typ der Link Technologie für den Port an.</span><span class="sxs-lookup"><span data-stu-id="f9b62-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="f9b62-343">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="f9b62-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="f9b62-344">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-350"><span id="FDDI"></span><span id="fddi"></span>**F-di** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="f9b62-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**TokenRing** (7)</span><span class="sxs-lookup"><span data-stu-id="f9b62-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="f9b62-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarot** (9)</span><span class="sxs-lookup"><span data-stu-id="f9b62-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="f9b62-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Drahtlos LAN** (11)</span><span class="sxs-lookup"><span data-stu-id="f9b62-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-357">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="f9b62-357">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-358">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-360">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-360">This property has been deprecated.</span></span> <span data-ttu-id="f9b62-361">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-362">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="f9b62-362">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-363">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-365">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="f9b62-365">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-366">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="f9b62-366">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="f9b62-367">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-367">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-368">**Name**</span><span class="sxs-lookup"><span data-stu-id="f9b62-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-371">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-371">The label by which the object is known.</span></span> <span data-ttu-id="f9b62-372">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-373">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="f9b62-373">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-374">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-374">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-376">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="f9b62-376">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-377">Ein Array von Zeichen folgen, die die Mac-Adressen für den Port enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9b62-377">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="f9b62-378">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-378">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-379">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="f9b62-379">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-380">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-382">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9b62-382">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f9b62-383">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f9b62-384">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="f9b62-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="f9b62-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="f9b62-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="f9b62-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="f9b62-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="f9b62-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="f9b62-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="f9b62-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="f9b62-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="f9b62-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="f9b62-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="f9b62-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f9b62-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f9b62-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f9b62-404">)</span><span class="sxs-lookup"><span data-stu-id="f9b62-404">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-405">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f9b62-405">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-406">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-408">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-408">The current statuses of the object.</span></span> <span data-ttu-id="f9b62-409">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-410">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="f9b62-410">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-411">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-413">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-413">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f9b62-414">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="f9b62-414">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="f9b62-415">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-416">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f9b62-416">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-417">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-417">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-419">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="f9b62-419">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f9b62-420">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-421">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="f9b62-421">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-422">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-424">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn er auf 1 festgelegt ist (andere).</span><span class="sxs-lookup"><span data-stu-id="f9b62-424">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="f9b62-425">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-425">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-426">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="f9b62-426">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-429">Die Verwendung dieser Eigenschaft wird anstelle der **portType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="f9b62-429">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="f9b62-430">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-431">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="f9b62-431">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-432">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-434">Beschreibt den Modultyp, wenn **portType** auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-434">Describes the type of module when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="f9b62-435">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-436">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="f9b62-436">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-437">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-439">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="f9b62-439">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-440">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-440">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="f9b62-441">Diese hart codierte Adresse kann mithilfe eines Firmware-Upgrades oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-441">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="f9b62-442">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-442">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="f9b62-443">Diese Eigenschaft sollte **null** sein, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-443">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="f9b62-444">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-444">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-445">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="f9b62-445">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-446">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-448">Die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="f9b62-448">The port number.</span></span> <span data-ttu-id="f9b62-449">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-450">**PortType**</span><span class="sxs-lookup"><span data-stu-id="f9b62-450">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-451">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-453">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-453">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="f9b62-454">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige **otherporttype** -Eigenschaft eine Zeichen folgen Beschreibung des Port Typs.</span><span class="sxs-lookup"><span data-stu-id="f9b62-454">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="f9b62-455">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-455">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="f9b62-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="f9b62-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="f9b62-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="f9b62-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="f9b62-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="f9b62-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="f9b62-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="f9b62-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="f9b62-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="f9b62-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="f9b62-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="f9b62-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="f9b62-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="f9b62-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="f9b62-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="f9b62-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="f9b62-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="f9b62-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="f9b62-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="f9b62-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-478">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f9b62-478">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-479">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-479">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-480">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-481">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-481">The power management capabilities of the device.</span></span> <span data-ttu-id="f9b62-482">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-482">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-483">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="f9b62-483">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-484">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f9b62-484">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-485">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-486">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9b62-486">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f9b62-487">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-488">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="f9b62-488">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-489">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-489">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-490">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-491">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f9b62-491">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f9b62-492">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-493">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="f9b62-493">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-494">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-496">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="f9b62-496">Provides high level status information.</span></span> <span data-ttu-id="f9b62-497">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9b62-497">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f9b62-498">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b62-498">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f9b62-499">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-499">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="f9b62-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f9b62-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f9b62-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f9b62-506">)</span><span class="sxs-lookup"><span data-stu-id="f9b62-506">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-507">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="f9b62-507">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-508">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-509">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-509">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-510">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="f9b62-510">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-511">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="f9b62-511">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="f9b62-512">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-512">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="f9b62-513">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-513">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-514">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f9b62-514">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-515">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-516">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-517">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="f9b62-517">The last requested or desired state for the element.</span></span> <span data-ttu-id="f9b62-518">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-518">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-519">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="f9b62-519">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-520">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-520">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-522">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="f9b62-522">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-523">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="f9b62-523">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="f9b62-524">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-524">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-525">**Status**</span><span class="sxs-lookup"><span data-stu-id="f9b62-525">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-526">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-527">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-528">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-528">The current status of the object.</span></span> <span data-ttu-id="f9b62-529">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-530">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="f9b62-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-531">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-532">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-533">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f9b62-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f9b62-534">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-535">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f9b62-535">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-536">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-537">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-538">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f9b62-538">The current state of the logical device.</span></span> <span data-ttu-id="f9b62-539">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-539">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-540">**Supportedcos**</span><span class="sxs-lookup"><span data-stu-id="f9b62-540">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-541">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-543">Ein Array von ganzen Zahlen, das die Fibre Channel unterstützten Klassen von Dienst (COS) angibt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-543">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="f9b62-544">Die aktiven COs werden von der **activecos** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9b62-544">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="f9b62-545">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-545">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-547"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-547"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-548"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-548"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-549"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-549"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-550"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-550"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-551"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-551"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-552"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="f9b62-552"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-553"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="f9b62-553"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-554">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="f9b62-554">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-555">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f9b62-555">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-556">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-557">Ein Array von ganzen Zahlen, das die unterstützten Fibre Channel FC-4-Protokolle angibt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-557">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="f9b62-558">Die Protokolle, die aktiv sind und ausgeführt werden, werden von der **ActiveFC4Types** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9b62-558">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="f9b62-559">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-559">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b62-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b62-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="f9b62-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="f9b62-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="f9b62-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="f9b62-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="f9b62-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="f9b62-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="f9b62-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="f9b62-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="f9b62-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="f9b62-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="f9b62-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="f9b62-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="f9b62-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="f9b62-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="f9b62-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="f9b62-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="f9b62-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="f9b62-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="f9b62-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="f9b62-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="f9b62-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="f9b62-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b62-586">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="f9b62-586">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-587">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-587">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-588">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-589">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="f9b62-589">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-590">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="f9b62-590">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="f9b62-591">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-591">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-592">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f9b62-592">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-593">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-593">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-594">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-594">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-595">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f9b62-595">The scoping system's creation class name.</span></span> <span data-ttu-id="f9b62-596">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-596">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-597">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f9b62-597">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-598">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9b62-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-599">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-600">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f9b62-600">The scoping system's name.</span></span> <span data-ttu-id="f9b62-601">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-602">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="f9b62-602">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-603">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f9b62-603">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-604">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-605">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9b62-605">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f9b62-606">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-606">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-607">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="f9b62-607">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-608">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9b62-608">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-609">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-610">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f9b62-610">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f9b62-611">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b62-611">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-612">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="f9b62-612">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-613">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-614">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-615">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="f9b62-615">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f9b62-616">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-616">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f9b62-617">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="f9b62-617">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b62-618">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b62-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-619">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9b62-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b62-620">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-620">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="f9b62-621">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="f9b62-621">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="f9b62-622">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b62-622">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="f9b62-623">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f9b62-623">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f9b62-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f9b62-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b62-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b62-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b62-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b62-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9b62-628">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9b62-628">Requirements</span></span>



| <span data-ttu-id="f9b62-629">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9b62-629">Requirement</span></span> | <span data-ttu-id="f9b62-630">Wert</span><span class="sxs-lookup"><span data-stu-id="f9b62-630">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b62-631">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9b62-631">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b62-632">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9b62-632">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f9b62-633">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9b62-633">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b62-634">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9b62-634">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9b62-635">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9b62-635">Namespace</span></span><br/>                | <span data-ttu-id="f9b62-636">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f9b62-636">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f9b62-637">MOF</span><span class="sxs-lookup"><span data-stu-id="f9b62-637">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9b62-638"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-638"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9b62-639">DLL</span><span class="sxs-lookup"><span data-stu-id="f9b62-639">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9b62-640"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9b62-640"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

