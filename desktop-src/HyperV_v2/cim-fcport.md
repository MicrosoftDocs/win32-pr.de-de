---
description: Stellt die Funktionen und die Verwaltung eines Fibre Channel-Port Geräts (FC) dar.
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: CIM_FCPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343220"
---
# <a name="cim_fcport-class"></a><span data-ttu-id="22167-103">CIM \_ fcport-Klasse</span><span class="sxs-lookup"><span data-stu-id="22167-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="22167-104">Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="22167-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="22167-105">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="22167-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="22167-106">Stellt die Funktionen und die Verwaltung eines Fibre Channel-Port Geräts (FC) dar.</span><span class="sxs-lookup"><span data-stu-id="22167-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="22167-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22167-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="22167-108">Member</span><span class="sxs-lookup"><span data-stu-id="22167-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="22167-109">Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="22167-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="22167-110">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="22167-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="22167-111">Die **CIM \_ fcport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="22167-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="22167-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22167-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22167-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22167-113">Properties</span></span>

<span data-ttu-id="22167-114">Die **CIM \_ fcport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="22167-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22167-115">**Activecos**</span><span class="sxs-lookup"><span data-stu-id="22167-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22167-116">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22167-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22167-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22167-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22167-118">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ fcport**".**Supportedcos**")</span><span class="sxs-lookup"><span data-stu-id="22167-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="22167-119">Die Active Class of Service (COS)-Einstellungen für den Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="22167-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22167-120">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22167-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="22167-121">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="22167-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="22167-122">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="22167-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="22167-123">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="22167-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="22167-124">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="22167-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="22167-125">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="22167-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="22167-126">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="22167-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="22167-127">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="22167-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22167-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="22167-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22167-129">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22167-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22167-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22167-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22167-131">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ fcport**".**SupportedFC4Types**")</span><span class="sxs-lookup"><span data-stu-id="22167-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="22167-132">Die auf dem Fibre Channel laufenden FC-4-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="22167-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22167-133">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22167-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22167-134">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="22167-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="22167-135">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="22167-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="22167-136">**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="22167-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="22167-137">**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="22167-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="22167-138">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="22167-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="22167-139">**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="22167-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="22167-140">**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="22167-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="22167-141">**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="22167-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="22167-142">**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="22167-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="22167-143">**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="22167-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="22167-144">**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="22167-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="22167-145">**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="22167-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="22167-146">**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="22167-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="22167-147">**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="22167-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="22167-148">**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="22167-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="22167-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="22167-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="22167-150">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="22167-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="22167-151">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="22167-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="22167-152">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="22167-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="22167-153">**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="22167-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="22167-154">**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="22167-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="22167-155">**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="22167-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="22167-156">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="22167-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="22167-157">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="22167-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="22167-158">**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="22167-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22167-159">**PortType**</span><span class="sxs-lookup"><span data-stu-id="22167-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22167-160">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22167-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22167-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22167-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22167-162">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="22167-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="22167-163">Der aktivierte Modus für den Port.</span><span class="sxs-lookup"><span data-stu-id="22167-163">The enabled mode for the port.</span></span> <span data-ttu-id="22167-164">Die portmodi werden durch ANSI-X3-Standards definiert.</span><span class="sxs-lookup"><span data-stu-id="22167-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="22167-165">Wenn der Port angemeldet ist, handelt es sich hierbei um den ausgehandelten Porttyp. andernfalls wird der konfigurierte Porttyp gemeldet.</span><span class="sxs-lookup"><span data-stu-id="22167-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22167-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22167-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22167-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="22167-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="22167-168">Die zugehörige Eigenschaft **otherporttype** enthält eine Zeichen folgen Beschreibung für den Porttyp.</span><span class="sxs-lookup"><span data-stu-id="22167-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="22167-169"><span id="N"></span><span id="n"></span>**N** (10)</span><span class="sxs-lookup"><span data-stu-id="22167-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="22167-170">Knotenport</span><span class="sxs-lookup"><span data-stu-id="22167-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="22167-171"><span id="NL"></span><span id="nl"></span>**Nl** (11)</span><span class="sxs-lookup"><span data-stu-id="22167-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="22167-172">Knotenport Unterstützung für die von FC über eine über-</span><span class="sxs-lookup"><span data-stu-id="22167-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="22167-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span><span class="sxs-lookup"><span data-stu-id="22167-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="22167-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)</span><span class="sxs-lookup"><span data-stu-id="22167-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="22167-175">Der Port kann entweder zu einem knotenport (N) oder zu einem knotenport werden, der die von FC unterstützte Schleife (NL) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22167-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="22167-176"><span id="E"></span><span id="e"></span>**E** (14)</span><span class="sxs-lookup"><span data-stu-id="22167-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="22167-177">Erweiterungsport, der Fabric-Elemente verbindet (z. b. FC-Switches)</span><span class="sxs-lookup"><span data-stu-id="22167-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="22167-178"><span id="F"></span><span id="f"></span>**F** (15)</span><span class="sxs-lookup"><span data-stu-id="22167-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="22167-179">Fabric-Port (Element)</span><span class="sxs-lookup"><span data-stu-id="22167-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="22167-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span><span class="sxs-lookup"><span data-stu-id="22167-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="22167-181">Fabric-Port (Element), der die von der FC-über eine</span><span class="sxs-lookup"><span data-stu-id="22167-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="22167-182"><span id="B"></span><span id="b"></span>**B** (17)</span><span class="sxs-lookup"><span data-stu-id="22167-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="22167-183">Brückenanschluss</span><span class="sxs-lookup"><span data-stu-id="22167-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="22167-184"><span id="G"></span><span id="g"></span>**G** (18)</span><span class="sxs-lookup"><span data-stu-id="22167-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="22167-185">Der Port kann entweder als Erweiterungsanschluss (E) oder als Fabric-Port (F) aushandeln.</span><span class="sxs-lookup"><span data-stu-id="22167-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="22167-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="22167-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22167-187">**Supportedcos**</span><span class="sxs-lookup"><span data-stu-id="22167-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22167-188">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22167-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22167-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22167-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22167-190">Die vom Fibre Channel unterstützten Klassen der Dienst Einstellungen (COS).</span><span class="sxs-lookup"><span data-stu-id="22167-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22167-191">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22167-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="22167-192">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="22167-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="22167-193">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="22167-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="22167-194">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="22167-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="22167-195">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="22167-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="22167-196">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="22167-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="22167-197">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="22167-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="22167-198">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="22167-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22167-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="22167-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22167-200">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22167-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22167-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22167-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22167-202">Die vom Fibre Channel unterstützten FC-4-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="22167-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22167-203">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22167-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22167-204">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="22167-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="22167-205">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="22167-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="22167-206">**IP über FC** (5)</span><span class="sxs-lookup"><span data-stu-id="22167-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="22167-207">**SCSI-f** (8)</span><span class="sxs-lookup"><span data-stu-id="22167-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="22167-208">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="22167-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="22167-209">**IPI-3 Master** (17)</span><span class="sxs-lookup"><span data-stu-id="22167-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="22167-210">**IPI-3-Slave** (18)</span><span class="sxs-lookup"><span data-stu-id="22167-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="22167-211">**IPI-3-Peer** (19)</span><span class="sxs-lookup"><span data-stu-id="22167-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="22167-212">**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="22167-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="22167-213">**CP IPI-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="22167-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="22167-214">**CP IPI-3-Peer** (23)</span><span class="sxs-lookup"><span data-stu-id="22167-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="22167-215">**Sbccs-Kanal** (25)</span><span class="sxs-lookup"><span data-stu-id="22167-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="22167-216">**Sbccs-Steuerungseinheit** (26)</span><span class="sxs-lookup"><span data-stu-id="22167-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="22167-217">**FC-SB-2-Channel** (27)</span><span class="sxs-lookup"><span data-stu-id="22167-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="22167-218">**FC-SB-2-Steuerungseinheit** (28)</span><span class="sxs-lookup"><span data-stu-id="22167-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="22167-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="22167-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="22167-220">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="22167-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="22167-221">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="22167-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="22167-222">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="22167-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="22167-223">**BBL-Steuer** Element (80)</span><span class="sxs-lookup"><span data-stu-id="22167-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="22167-224">**BBL-gekapseltes LAN-PDU** (81)</span><span class="sxs-lookup"><span data-stu-id="22167-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="22167-225">**BBL 802,3 gekapseltes LAN PDU** (82)</span><span class="sxs-lookup"><span data-stu-id="22167-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="22167-226">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="22167-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="22167-227">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="22167-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="22167-228">**Hersteller eindeutig** (255)</span><span class="sxs-lookup"><span data-stu-id="22167-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="22167-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="22167-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="22167-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22167-230">Requirements</span></span>



| <span data-ttu-id="22167-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22167-231">Requirement</span></span> | <span data-ttu-id="22167-232">Wert</span><span class="sxs-lookup"><span data-stu-id="22167-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22167-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22167-233">Minimum supported client</span></span><br/> | <span data-ttu-id="22167-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="22167-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="22167-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22167-235">Minimum supported server</span></span><br/> | <span data-ttu-id="22167-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22167-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="22167-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="22167-237">Namespace</span></span><br/>                | <span data-ttu-id="22167-238">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="22167-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="22167-239">MOF</span><span class="sxs-lookup"><span data-stu-id="22167-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22167-240"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="22167-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22167-241">DLL</span><span class="sxs-lookup"><span data-stu-id="22167-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22167-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22167-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22167-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22167-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22167-244">**CIM- \_ Netzwerkport**</span><span class="sxs-lookup"><span data-stu-id="22167-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

