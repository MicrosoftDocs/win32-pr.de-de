---
description: Stellt eine Zuordnung dar, bei \_ der ein CIM serviceaccesspoint-oder CIM \_ protocolendpoint-Objekt von einem zugrunde liegenden CIM \_ lanendpoint-Objekt auf demselben System abhängt.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: CIM_BindsToLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353849"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="dc761-103">CIM \_ bindstolanendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="dc761-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="dc761-104">Stellt eine Zuordnung dar, bei der ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) -oder [**CIM \_ protocolendpoint**](cim-protocolendpoint.md) -Objekt von einem zugrunde liegenden [**CIM \_ lanendpoint**](cim-lanendpoint.md) -Objekt auf demselben System abhängt.</span><span class="sxs-lookup"><span data-stu-id="dc761-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc761-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc761-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="dc761-106">Member</span><span class="sxs-lookup"><span data-stu-id="dc761-106">Members</span></span>

<span data-ttu-id="dc761-107">Die **CIM \_ bindstolanendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc761-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="dc761-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc761-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc761-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc761-109">Properties</span></span>

<span data-ttu-id="dc761-110">Die **CIM \_ bindstolanendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc761-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc761-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="dc761-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc761-112">Datentyp: **CIM \_ lanendpoint**</span><span class="sxs-lookup"><span data-stu-id="dc761-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="dc761-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc761-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc761-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="dc761-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dc761-115">Das zugrunde liegende [**CIM \_ lanendpoint**](cim-lanendpoint.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="dc761-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="dc761-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="dc761-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc761-117">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="dc761-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="dc761-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc761-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc761-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="dc761-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="dc761-120">Das [**CIM- \_ serviceaccesspoint**](cim-serviceaccesspoint.md) -oder [**CIM \_ protocolendpoint**](cim-protocolendpoint.md) -Objekt, das vom [**CIM- \_ lanendpoint**](cim-lanendpoint.md)abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="dc761-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc761-121">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="dc761-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc761-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc761-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc761-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc761-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc761-124">Die rahmenmethode für den Dienst Zugriffspunkt oder den Protokoll Endpunkt auf der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="dc761-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="dc761-125">RAW 802.3 ist nur bekannt, dass Sie mit dem IPX-Protokoll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc761-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc761-126">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dc761-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="dc761-127">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="dc761-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="dc761-128">**802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="dc761-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="dc761-129">**Snap** -in (3)</span><span class="sxs-lookup"><span data-stu-id="dc761-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="dc761-130">**RAW 802.3** (4)</span><span class="sxs-lookup"><span data-stu-id="dc761-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="dc761-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc761-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dc761-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc761-132">Requirements</span></span>



| <span data-ttu-id="dc761-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc761-133">Requirement</span></span> | <span data-ttu-id="dc761-134">Wert</span><span class="sxs-lookup"><span data-stu-id="dc761-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc761-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc761-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dc761-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dc761-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dc761-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc761-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dc761-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc761-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dc761-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc761-139">Namespace</span></span><br/>                | <span data-ttu-id="dc761-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dc761-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dc761-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dc761-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc761-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc761-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc761-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dc761-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc761-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc761-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc761-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc761-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc761-146">**CIM- \_ bindsto**</span><span class="sxs-lookup"><span data-stu-id="dc761-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 

