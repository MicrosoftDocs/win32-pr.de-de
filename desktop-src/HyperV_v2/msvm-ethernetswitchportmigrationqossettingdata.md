---
description: Stellt die VFP-QoS-Einstellungen dar.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Msvm_EthernetSwitchPortMigrationQosSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363543"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="506d0-103">MSVM \_ ethernetzwitchportmigrationqossettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="506d0-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="506d0-104">Stellt die VFP-QoS-Einstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="506d0-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="506d0-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="506d0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="506d0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="506d0-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="506d0-107">Member</span><span class="sxs-lookup"><span data-stu-id="506d0-107">Members</span></span>

<span data-ttu-id="506d0-108">Die **MSVM \_ ethernetzwitchportmigrationqossettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="506d0-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="506d0-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="506d0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="506d0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="506d0-110">Properties</span></span>

<span data-ttu-id="506d0-111">Die **MSVM \_ ethernetzwitchportmigrationqossettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="506d0-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="506d0-112">**Inboundmaximummbit/s**</span><span class="sxs-lookup"><span data-stu-id="506d0-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-113">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="506d0-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-115">Qualifizierer: **wmidataid** (10), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-116">Der Wert der Bandbreiten Abdeckung für eingehenden Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="506d0-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-117">**Outboundmaximummbit/s**</span><span class="sxs-lookup"><span data-stu-id="506d0-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-118">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="506d0-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-120">Qualifizierer: **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-121">Der Wert der Bandbreiten Abdeckung für ausgehenden Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="506d0-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-122">**Outboundreservedvalue**</span><span class="sxs-lookup"><span data-stu-id="506d0-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-123">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="506d0-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-125">Qualifizierer: **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-126">Der Wert für die Bandbreiten Reservierung.</span><span class="sxs-lookup"><span data-stu-id="506d0-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-127">**QueueID**</span><span class="sxs-lookup"><span data-stu-id="506d0-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="506d0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-131">Die ID der QoS-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="506d0-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-132">**Wechseln von \_ defaultreservation**</span><span class="sxs-lookup"><span data-stu-id="506d0-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="506d0-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-135">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-136">Der Standard Reservierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="506d0-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-137">**Schalter \_ enablehardwarelimits**</span><span class="sxs-lookup"><span data-stu-id="506d0-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="506d0-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-140">Qualifizierer: **wmidataid** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-141">Gibt an, ob bei der Verfügbarkeit Hardware Abladungen für Grenzwerte versucht werden.</span><span class="sxs-lookup"><span data-stu-id="506d0-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-142">**Schalter \_ enablehardwarereservations**</span><span class="sxs-lookup"><span data-stu-id="506d0-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="506d0-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-145">Qualifizierer: **wmidataid** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-146">Gibt an, ob Hardware Abladungen für Reservierungen versucht werden, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="506d0-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-147">**Switch \_ enablesoftwarereservations**</span><span class="sxs-lookup"><span data-stu-id="506d0-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="506d0-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-150">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-151">Gibt an, ob die softwarebasierte Reservierung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="506d0-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-152">**\_Linkspeedprozentsatz wechseln**</span><span class="sxs-lookup"><span data-stu-id="506d0-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-153">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="506d0-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-155">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-156">Der Prozentsatz der Verbindungsgeschwindigkeit, der für die Reservierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="506d0-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="506d0-157">**\_Reservierungs Modus wechseln**</span><span class="sxs-lookup"><span data-stu-id="506d0-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="506d0-158">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="506d0-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="506d0-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="506d0-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="506d0-160">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="506d0-161">Der QoS-Reservierungs Modus auf dem Switch.</span><span class="sxs-lookup"><span data-stu-id="506d0-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="506d0-162">**Absolut** (0)</span><span class="sxs-lookup"><span data-stu-id="506d0-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="506d0-163">**Gewichtung** (1)</span><span class="sxs-lookup"><span data-stu-id="506d0-163">**Weight** (1)</span></span>


<span data-ttu-id="506d0-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="506d0-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="506d0-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="506d0-165">Requirements</span></span>



| <span data-ttu-id="506d0-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="506d0-166">Requirement</span></span> | <span data-ttu-id="506d0-167">Wert</span><span class="sxs-lookup"><span data-stu-id="506d0-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="506d0-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="506d0-168">Minimum supported client</span></span><br/> | <span data-ttu-id="506d0-169">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="506d0-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="506d0-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="506d0-170">Minimum supported server</span></span><br/> | <span data-ttu-id="506d0-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="506d0-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="506d0-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="506d0-172">Namespace</span></span><br/>                | <span data-ttu-id="506d0-173">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="506d0-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="506d0-174">MOF</span><span class="sxs-lookup"><span data-stu-id="506d0-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="506d0-175"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="506d0-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="506d0-176">DLL</span><span class="sxs-lookup"><span data-stu-id="506d0-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="506d0-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="506d0-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="506d0-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="506d0-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506d0-179">**MSVM \_ ethernetzwitchportfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="506d0-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

