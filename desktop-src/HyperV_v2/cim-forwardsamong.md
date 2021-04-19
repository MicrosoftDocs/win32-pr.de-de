---
description: Stellt eine Zuordnung dar, in der Protokoll Endpunkte von einem Weiterleitungs Dienst zum Weiterleiten von Daten abhängen.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: CIM_ForwardsAmong-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339732"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="c0f7a-103">CIM \_ forwardsamong-Klasse</span><span class="sxs-lookup"><span data-stu-id="c0f7a-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="c0f7a-104">Stellt eine Zuordnung dar, in der Protokoll Endpunkte von einem Weiterleitungs Dienst zum Weiterleiten von Daten abhängen.</span><span class="sxs-lookup"><span data-stu-id="c0f7a-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0f7a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c0f7a-106">Member</span><span class="sxs-lookup"><span data-stu-id="c0f7a-106">Members</span></span>

<span data-ttu-id="c0f7a-107">Die **CIM \_ forwardsamong** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0f7a-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="c0f7a-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0f7a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0f7a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0f7a-109">Properties</span></span>

<span data-ttu-id="c0f7a-110">Die **CIM \_ forwardsamong** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0f7a-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0f7a-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="c0f7a-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f7a-112">Datentyp: **CIM \_ protocolendpoint**</span><span class="sxs-lookup"><span data-stu-id="c0f7a-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="c0f7a-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0f7a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f7a-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="c0f7a-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c0f7a-115">Die Protokoll Endpunkte senden und empfangen die weitergeleiteten Daten.</span><span class="sxs-lookup"><span data-stu-id="c0f7a-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="c0f7a-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="c0f7a-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f7a-117">Datentyp: **CIM \_ forwardingservice**</span><span class="sxs-lookup"><span data-stu-id="c0f7a-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="c0f7a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0f7a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f7a-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="c0f7a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c0f7a-120">Der Weiterleitungs Dienst, der die Daten weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="c0f7a-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0f7a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f7a-121">Requirements</span></span>



| <span data-ttu-id="c0f7a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0f7a-122">Requirement</span></span> | <span data-ttu-id="c0f7a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f7a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f7a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0f7a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f7a-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c0f7a-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c0f7a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0f7a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f7a-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c0f7a-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c0f7a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0f7a-128">Namespace</span></span><br/>                | <span data-ttu-id="c0f7a-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0f7a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0f7a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c0f7a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0f7a-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c0f7a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0f7a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f7a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f7a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0f7a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0f7a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0f7a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f7a-135">**CIM \_ servicesapabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="c0f7a-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

