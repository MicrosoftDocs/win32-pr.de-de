---
description: Stellt die Einstellungen für die Auslagerungs Auslagerung dar.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Msvm_EthernetSwitchHardwareOffloadSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350996"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="78727-103">MSVM \_ ethernezwitchhardwareoffloadsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="78727-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="78727-104">Stellt die Einstellungen für die Auslagerungs Auslagerung dar.</span><span class="sxs-lookup"><span data-stu-id="78727-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="78727-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78727-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78727-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="78727-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="78727-107">Member</span><span class="sxs-lookup"><span data-stu-id="78727-107">Members</span></span>

<span data-ttu-id="78727-108">Die **MSVM \_ ethernezwitchhardwareoffloadsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="78727-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="78727-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78727-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78727-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78727-110">Properties</span></span>

<span data-ttu-id="78727-111">Die **MSVM \_ ethernezwitchhardwareoffloadsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78727-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78727-112">**Defaultqueuevmmqaktivierte**</span><span class="sxs-lookup"><span data-stu-id="78727-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78727-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78727-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78727-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78727-115">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-116">Gibt die vmmq-Einstellungen für die Standard Warteschlange des vSwitches an.</span><span class="sxs-lookup"><span data-stu-id="78727-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="78727-117">**Defaultqueuevmmqqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="78727-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78727-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78727-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78727-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78727-120">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-121">Gibt die Anzahl der Warteschlangen für die Standard Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="78727-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="78727-122">**Defaultqueuevrssaktivierte**</span><span class="sxs-lookup"><span data-stu-id="78727-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78727-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78727-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78727-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78727-125">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-126">Gibt die vrss-Einstellungen für die Standard Warteschlange des vSwitches an.</span><span class="sxs-lookup"><span data-stu-id="78727-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="78727-127">**Defaultqueuevrssexcludeprimaryprocessor**</span><span class="sxs-lookup"><span data-stu-id="78727-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78727-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78727-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78727-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78727-130">Qualifizierer: **wmidataid** (6), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-131">Gibt an, ob die primäre VMQ-CPU von der vrss/vmmq-dereferenzierungstabelle ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="78727-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="78727-132">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="78727-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="78727-133">**Defaultqueuevrssindependenthostverteilung**</span><span class="sxs-lookup"><span data-stu-id="78727-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78727-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78727-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78727-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78727-136">Qualifizierer: **wmidataid** (7), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-137">Gibt an, ob die vrss-Verteilung für die Standard Warteschlange unabhängig vom RSS-Status des externen VPORTS immer durchzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="78727-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="78727-138">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="78727-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="78727-139">**Defaultqueuevrssminqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="78727-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78727-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78727-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78727-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78727-142">Qualifizierer: **wmidataid** (4), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-143">Gibt die Mindestanzahl von Warteschlangen an, die für vrss/vmmq verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78727-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="78727-144">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="78727-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="78727-145">**Defaultqueuevrssqueueschedulingmode**</span><span class="sxs-lookup"><span data-stu-id="78727-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78727-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78727-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78727-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78727-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78727-148">Qualifizierer: **wmidataid** (5), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="78727-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="78727-149">Gibt an, wie vrss/vmmq-Warteschlangen an verschiedene Host Prozessoren geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="78727-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="78727-150">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="78727-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78727-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78727-151">Requirements</span></span>



| <span data-ttu-id="78727-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78727-152">Requirement</span></span> | <span data-ttu-id="78727-153">Wert</span><span class="sxs-lookup"><span data-stu-id="78727-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78727-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78727-154">Minimum supported client</span></span><br/> | <span data-ttu-id="78727-155">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78727-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="78727-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78727-156">Minimum supported server</span></span><br/> | <span data-ttu-id="78727-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78727-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="78727-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="78727-158">Namespace</span></span><br/>                | <span data-ttu-id="78727-159">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="78727-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="78727-160">MOF</span><span class="sxs-lookup"><span data-stu-id="78727-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78727-161"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="78727-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78727-162">DLL</span><span class="sxs-lookup"><span data-stu-id="78727-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78727-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78727-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78727-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78727-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78727-165">**MSVM \_ ethernetzwitchfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="78727-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




