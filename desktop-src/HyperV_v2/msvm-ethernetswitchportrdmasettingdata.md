---
description: Stellt die RDMA-Funktions Einstellungsdaten für den Port dar.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Msvm_EthernetSwitchPortRdmaSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869272"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="874b2-103">MSVM \_ ethernetzwitchportrdmasettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="874b2-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="874b2-104">Stellt die RDMA-Funktions Einstellungsdaten für den Port dar.</span><span class="sxs-lookup"><span data-stu-id="874b2-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="874b2-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="874b2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="874b2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="874b2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="874b2-107">Member</span><span class="sxs-lookup"><span data-stu-id="874b2-107">Members</span></span>

<span data-ttu-id="874b2-108">Die **MSVM \_ ethernetzwitchportrdmasettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="874b2-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="874b2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="874b2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="874b2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="874b2-110">Properties</span></span>

<span data-ttu-id="874b2-111">Die **MSVM \_ ethernetzwitchportrdmasettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="874b2-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="874b2-112">**Rdmaoffloadweight**</span><span class="sxs-lookup"><span data-stu-id="874b2-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="874b2-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="874b2-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="874b2-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="874b2-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="874b2-115">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="874b2-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="874b2-116">Die Gewichtung, die diesem Port für Gast-RDMA zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="874b2-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="874b2-117">Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von RDMA-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="874b2-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="874b2-118">Wenn Sie die **rdmaoffloadweight** -Eigenschaft auf 0 festlegen, wird RDMA auf dem Port deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="874b2-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="874b2-119">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="874b2-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="874b2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="874b2-120">Requirements</span></span>



| <span data-ttu-id="874b2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="874b2-121">Requirement</span></span> | <span data-ttu-id="874b2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="874b2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="874b2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="874b2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="874b2-124">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="874b2-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="874b2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="874b2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="874b2-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="874b2-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="874b2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="874b2-127">Namespace</span></span><br/>                | <span data-ttu-id="874b2-128">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="874b2-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="874b2-129">MOF</span><span class="sxs-lookup"><span data-stu-id="874b2-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="874b2-130"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="874b2-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="874b2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="874b2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="874b2-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="874b2-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="874b2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="874b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="874b2-134">**MSVM \_ ethernetzwitchportfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="874b2-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




