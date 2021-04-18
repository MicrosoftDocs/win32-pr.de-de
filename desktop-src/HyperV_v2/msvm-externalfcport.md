---
description: Stellt einen externen Fibre Channel Anschluss dar.
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Msvm_ExternalFcPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345765"
---
# <a name="msvm_externalfcport-class"></a><span data-ttu-id="a70aa-103">MSVM \_ externalfcport-Klasse</span><span class="sxs-lookup"><span data-stu-id="a70aa-103">Msvm\_ExternalFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="a70aa-104">Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="a70aa-105">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="a70aa-106">Stellt einen externen Fibre Channel Anschluss dar.</span><span class="sxs-lookup"><span data-stu-id="a70aa-106">Represents an external Fibre Channel port.</span></span>

<span data-ttu-id="a70aa-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a70aa-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a70aa-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a><span data-ttu-id="a70aa-109">Member</span><span class="sxs-lookup"><span data-stu-id="a70aa-109">Members</span></span>

<span data-ttu-id="a70aa-110">Die **MSVM \_ externalfcport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a70aa-110">The **Msvm\_ExternalFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a70aa-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a70aa-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a70aa-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a70aa-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a70aa-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="a70aa-113">Methods</span></span>

<span data-ttu-id="a70aa-114">Die **MSVM \_ externalfcport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-114">The **Msvm\_ExternalFcPort** class has these methods.</span></span>



| <span data-ttu-id="a70aa-115">Methode</span><span class="sxs-lookup"><span data-stu-id="a70aa-115">Method</span></span>                                                               | <span data-ttu-id="a70aa-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a70aa-116">Description</span></span>                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="a70aa-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="a70aa-117">**EnableDevice**</span></span>                                                     | <span data-ttu-id="a70aa-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a70aa-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="a70aa-119">**OnlineDevice**</span></span>                                                     | <span data-ttu-id="a70aa-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a70aa-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="a70aa-121">**QuiesceDevice**</span></span>                                                    | <span data-ttu-id="a70aa-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="a70aa-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a70aa-123">**RequestStateChange**</span></span>](msvm-externalfcport-requeststatechange.md) | <span data-ttu-id="a70aa-124">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="a70aa-124">Requests a state change</span></span><br/>       |
| [<span data-ttu-id="a70aa-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="a70aa-125">**Reset**</span></span>](msvm-externalfcport-reset.md)                           | <span data-ttu-id="a70aa-126">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="a70aa-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="a70aa-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="a70aa-127">**RestoreProperties**</span></span>                                                | <span data-ttu-id="a70aa-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a70aa-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="a70aa-129">**SaveProperties**</span></span>                                                   | <span data-ttu-id="a70aa-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a70aa-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a70aa-131">**SetPowerState**</span></span>                                                    | <span data-ttu-id="a70aa-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a70aa-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a70aa-133">Properties</span></span>

<span data-ttu-id="a70aa-134">Die **MSVM \_ externalfcport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a70aa-134">The **Msvm\_ExternalFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-135">**Activecos**</span><span class="sxs-lookup"><span data-stu-id="a70aa-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-136">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-138">Ein Array von ganzen Zahlen, das die aktiven Dienst Klassen angibt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="a70aa-139">Die unterstützten cos werden von der **supportedcos** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a70aa-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="a70aa-140">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="a70aa-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="a70aa-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="a70aa-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-150">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-152">Ein Array von ganzen Zahlen, das die Fibre Channel FC-4-Protokolle angibt, die gerade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="a70aa-153">Eine Liste aller unterstützten Protokolle wird von der **SupportedFC4Types** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a70aa-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="a70aa-154">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="a70aa-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="a70aa-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="a70aa-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="a70aa-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="a70aa-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="a70aa-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="a70aa-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="a70aa-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="a70aa-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="a70aa-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="a70aa-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="a70aa-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="a70aa-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="a70aa-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="a70aa-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="a70aa-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="a70aa-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="a70aa-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="a70aa-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="a70aa-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="a70aa-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="a70aa-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-181">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="a70aa-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-182">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-184">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="a70aa-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-185">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a70aa-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="a70aa-186">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-187">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="a70aa-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-188">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-190">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="a70aa-191">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-192">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="a70aa-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-193">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-195">Gibt an, ob der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="a70aa-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="a70aa-196">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-197">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="a70aa-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-200">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-200">The primary availability and status of the device.</span></span> <span data-ttu-id="a70aa-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-202">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="a70aa-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-203">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-205">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="a70aa-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a70aa-206">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a70aa-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-210">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-210">A short description of the object.</span></span> <span data-ttu-id="a70aa-211">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-212">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="a70aa-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-215">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a70aa-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a70aa-216">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a70aa-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a70aa-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="a70aa-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a70aa-225">)</span><span class="sxs-lookup"><span data-stu-id="a70aa-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-226">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a70aa-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-229">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a70aa-229">The scoping system's creation class name.</span></span> <span data-ttu-id="a70aa-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-231">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a70aa-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-234">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-234">A description of the object.</span></span> <span data-ttu-id="a70aa-235">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a70aa-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-239">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="a70aa-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a70aa-240">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a70aa-241">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a70aa-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="a70aa-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a70aa-250">)</span><span class="sxs-lookup"><span data-stu-id="a70aa-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a70aa-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-254">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="a70aa-255">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a70aa-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-259">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-259">A display name for the object.</span></span> <span data-ttu-id="a70aa-260">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-261">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="a70aa-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-262">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-264">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="a70aa-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="a70aa-265">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a70aa-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-269">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="a70aa-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a70aa-270">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="a70aa-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="a70aa-271">Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="a70aa-272">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a70aa-272">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a70aa-273"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="a70aa-274">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a70aa-275"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="a70aa-276"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="a70aa-277">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-277">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a70aa-278"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="a70aa-279">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a70aa-279">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="a70aa-280"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="a70aa-281">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="a70aa-282"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="a70aa-283">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="a70aa-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="a70aa-284"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="a70aa-285">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="a70aa-286"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="a70aa-287">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="a70aa-287">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="a70aa-288"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="a70aa-289">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="a70aa-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="a70aa-290"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="a70aa-291">Das-Element ist aktiviert, befindet sich jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="a70aa-291">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="a70aa-292">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="a70aa-293">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="a70aa-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="a70aa-294"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="a70aa-295">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="a70aa-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="a70aa-296">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="a70aa-296">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="a70aa-297">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="a70aa-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-298">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-300">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a70aa-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="a70aa-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a70aa-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-305">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="a70aa-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="a70aa-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-307">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="a70aa-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-308">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-310">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a70aa-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="a70aa-311">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a70aa-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-313">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-315">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="a70aa-315">The current health of the element.</span></span> <span data-ttu-id="a70aa-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a70aa-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-318">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-320">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="a70aa-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a70aa-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-323">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a70aa-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-325">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-325">The date and time when the object was installed.</span></span> <span data-ttu-id="a70aa-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="a70aa-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a70aa-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-331">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a70aa-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-332">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a70aa-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a70aa-333">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-334">**Ishypervfähig**</span><span class="sxs-lookup"><span data-stu-id="a70aa-334">**IsHyperVCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-335">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-337">Wenn diese Eigenschaft den Wert **true** hat, kann dieser Fibre Channel Port mit den Switches verbunden werden und somit die Konnektivität zu einem virtuellen Computer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-337">If this property is **True**, this Fibre Channel port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="a70aa-338">Wenn diese Eigenschaft **false** ist, kann dieser Port nicht von der Architektur des virtuellen Computers Fibre Channel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-338">If this property is **False**, then this port cannot be used by the virtual machine Fibre Channel architecture.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a70aa-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-340">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70aa-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-342">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a70aa-342">The last error code reported by the logical device.</span></span> <span data-ttu-id="a70aa-343">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-344">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="a70aa-344">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-345">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-347">Gibt den Typ der Link Technologie für den Port an.</span><span class="sxs-lookup"><span data-stu-id="a70aa-347">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="a70aa-348">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="a70aa-348">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="a70aa-349">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-355"><span id="FDDI"></span><span id="fddi"></span>**F-di** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="a70aa-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**TokenRing** (7)</span><span class="sxs-lookup"><span data-stu-id="a70aa-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="a70aa-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarot** (9)</span><span class="sxs-lookup"><span data-stu-id="a70aa-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="a70aa-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Drahtlos LAN** (11)</span><span class="sxs-lookup"><span data-stu-id="a70aa-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-362">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="a70aa-362">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-363">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-365">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-365">This property has been deprecated.</span></span> <span data-ttu-id="a70aa-366">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-367">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="a70aa-367">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-368">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-370">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="a70aa-370">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-371">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="a70aa-371">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="a70aa-372">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-372">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="a70aa-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-376">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-376">The label by which the object is known.</span></span> <span data-ttu-id="a70aa-377">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-378">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="a70aa-378">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-379">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-381">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a70aa-381">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-382">Ein Array von Zeichen folgen, die die Mac-Adressen für den Port enthalten.</span><span class="sxs-lookup"><span data-stu-id="a70aa-382">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="a70aa-383">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-383">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-384">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="a70aa-384">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-385">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-387">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-387">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a70aa-388">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-388">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a70aa-389">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="a70aa-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="a70aa-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="a70aa-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="a70aa-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="a70aa-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="a70aa-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="a70aa-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="a70aa-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="a70aa-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="a70aa-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="a70aa-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="a70aa-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a70aa-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="a70aa-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a70aa-409">)</span><span class="sxs-lookup"><span data-stu-id="a70aa-409">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-410">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a70aa-410">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-411">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-413">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-413">The current statuses of the object.</span></span> <span data-ttu-id="a70aa-414">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-415">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="a70aa-415">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-416">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-418">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-418">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a70aa-419">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="a70aa-419">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="a70aa-420">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-420">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-421">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a70aa-421">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-422">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-422">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-424">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="a70aa-424">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a70aa-425">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-425">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-426">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="a70aa-426">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-429">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn er auf 1 festgelegt ist (andere).</span><span class="sxs-lookup"><span data-stu-id="a70aa-429">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="a70aa-430">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-431">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="a70aa-431">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-432">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-434">Die Verwendung dieser Eigenschaft wird anstelle der **portType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="a70aa-434">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="a70aa-435">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-435">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-436">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="a70aa-436">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-437">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-439">Beschreibt den Modultyp, wenn **portType** auf 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-439">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="a70aa-440">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-440">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-441">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="a70aa-441">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-444">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a70aa-444">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-445">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-445">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="a70aa-446">Diese hart codierte Adresse kann mithilfe eines Firmware-Upgrades oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-446">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="a70aa-447">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-447">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="a70aa-448">Diese Eigenschaft sollte **null** sein, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-448">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="a70aa-449">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-450">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="a70aa-450">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-451">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-453">Die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="a70aa-453">The port number.</span></span> <span data-ttu-id="a70aa-454">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-454">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-455">**PortType**</span><span class="sxs-lookup"><span data-stu-id="a70aa-455">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-456">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-458">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-458">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="a70aa-459">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige **otherporttype** -Eigenschaft eine Zeichen folgen Beschreibung des Port Typs.</span><span class="sxs-lookup"><span data-stu-id="a70aa-459">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="a70aa-460">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-460">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="a70aa-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="a70aa-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="a70aa-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="a70aa-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="a70aa-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="a70aa-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="a70aa-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="a70aa-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="a70aa-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="a70aa-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="a70aa-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="a70aa-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="a70aa-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="a70aa-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="a70aa-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="a70aa-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="a70aa-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="a70aa-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="a70aa-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="a70aa-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-483">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="a70aa-483">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-484">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-484">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-485">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-486">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-486">The power management capabilities of the device.</span></span> <span data-ttu-id="a70aa-487">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-488">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="a70aa-488">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-489">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-489">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-490">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-491">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a70aa-491">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a70aa-492">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-493">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="a70aa-493">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-494">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-494">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-496">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="a70aa-496">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a70aa-497">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-498">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="a70aa-498">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-499">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-499">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-501">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="a70aa-501">Provides high level status information.</span></span> <span data-ttu-id="a70aa-502">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a70aa-502">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a70aa-503">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a70aa-503">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a70aa-504">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-504">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="a70aa-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a70aa-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="a70aa-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a70aa-511">)</span><span class="sxs-lookup"><span data-stu-id="a70aa-511">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-512">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="a70aa-512">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-513">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-514">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-514">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-515">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="a70aa-515">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-516">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="a70aa-516">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="a70aa-517">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-517">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="a70aa-518">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-518">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-519">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a70aa-519">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-520">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-522">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="a70aa-522">The last requested or desired state for the element.</span></span> <span data-ttu-id="a70aa-523">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-523">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-524">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="a70aa-524">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-525">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-525">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-526">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-526">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-527">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="a70aa-527">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-528">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="a70aa-528">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="a70aa-529">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-529">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-530">**Status**</span><span class="sxs-lookup"><span data-stu-id="a70aa-530">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-531">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-532">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-533">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-533">The current status of the object.</span></span> <span data-ttu-id="a70aa-534">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-535">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="a70aa-535">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-536">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-536">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-537">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-538">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a70aa-538">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a70aa-539">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-539">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-540">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a70aa-540">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-541">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-541">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-543">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a70aa-543">The current state of the logical device.</span></span> <span data-ttu-id="a70aa-544">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-544">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-545">**Supportedcos**</span><span class="sxs-lookup"><span data-stu-id="a70aa-545">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-546">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-546">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-547">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-547">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-548">Ein Array von ganzen Zahlen, das die Fibre Channel unterstützten Klassen von Dienst (COS) angibt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-548">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="a70aa-549">Die aktiven COs werden von der **activecos** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a70aa-549">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="a70aa-550">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-550">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-552"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-552"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-553"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-553"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-554"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-554"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-555"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-555"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-556"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-556"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-557"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="a70aa-557"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-558"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="a70aa-558"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-559">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="a70aa-559">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-560">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a70aa-560">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-561">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-561">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-562">Ein Array von ganzen Zahlen, das die unterstützten Fibre Channel FC-4-Protokolle angibt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-562">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="a70aa-563">Die Protokolle, die aktiv sind und ausgeführt werden, werden von der **ActiveFC4Types** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a70aa-563">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="a70aa-564">Diese Eigenschaft wird von **CIM \_ fcport** geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-564">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a70aa-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="a70aa-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="a70aa-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="a70aa-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="a70aa-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="a70aa-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="a70aa-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="a70aa-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="a70aa-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="a70aa-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="a70aa-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="a70aa-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="a70aa-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="a70aa-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="a70aa-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="a70aa-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="a70aa-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="a70aa-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="a70aa-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="a70aa-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="a70aa-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="a70aa-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="a70aa-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="a70aa-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-591">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="a70aa-591">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-592">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-592">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-593">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-594">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="a70aa-594">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-595">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="a70aa-595">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="a70aa-596">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-596">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-597">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="a70aa-597">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-598">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-599">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-600">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a70aa-600">The scoping system's creation class name.</span></span> <span data-ttu-id="a70aa-601">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-602">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="a70aa-602">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-603">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-604">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-605">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a70aa-605">The scoping system's name.</span></span> <span data-ttu-id="a70aa-606">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-606">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-607">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="a70aa-607">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-608">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a70aa-608">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-609">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-610">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a70aa-610">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a70aa-611">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-611">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-612">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="a70aa-612">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-613">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a70aa-613">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-614">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-615">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="a70aa-615">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a70aa-616">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a70aa-616">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-617">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="a70aa-617">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-618">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-619">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-620">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="a70aa-620">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a70aa-621">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-621">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-622">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="a70aa-622">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-623">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a70aa-623">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-624">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-624">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-625">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-625">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="a70aa-626">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="a70aa-626">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="a70aa-627">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a70aa-627">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="a70aa-628">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a70aa-628">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a70aa-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a70aa-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="a70aa-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="a70aa-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="a70aa-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a70aa-633">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="a70aa-633">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-634">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-635">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-635">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-636">Der World Wide Node Name für diesen Fibre Channel Port.</span><span class="sxs-lookup"><span data-stu-id="a70aa-636">The world wide node name for this Fibre Channel port.</span></span>

</dd> <dt>

<span data-ttu-id="a70aa-637">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="a70aa-637">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70aa-638">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a70aa-638">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70aa-639">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a70aa-639">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70aa-640">Der World Wide Port Name für diesen Fibre Channel Port.</span><span class="sxs-lookup"><span data-stu-id="a70aa-640">The world wide port name for this Fibre Channel port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a70aa-641">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a70aa-641">Requirements</span></span>



| <span data-ttu-id="a70aa-642">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a70aa-642">Requirement</span></span> | <span data-ttu-id="a70aa-643">Wert</span><span class="sxs-lookup"><span data-stu-id="a70aa-643">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70aa-644">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a70aa-644">Minimum supported client</span></span><br/> | <span data-ttu-id="a70aa-645">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a70aa-645">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a70aa-646">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a70aa-646">Minimum supported server</span></span><br/> | <span data-ttu-id="a70aa-647">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a70aa-647">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a70aa-648">Namespace</span><span class="sxs-lookup"><span data-stu-id="a70aa-648">Namespace</span></span><br/>                | <span data-ttu-id="a70aa-649">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a70aa-649">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a70aa-650">MOF</span><span class="sxs-lookup"><span data-stu-id="a70aa-650">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a70aa-651"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-651"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a70aa-652">DLL</span><span class="sxs-lookup"><span data-stu-id="a70aa-652">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a70aa-653"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a70aa-653"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

