---
description: Stellt eine Zuordnung dar, bei der ein CIM \_ serviceaccesspoint-Objekt Protokoll Dienste von einem CIM \_ protocolendpoint-Objekt anfordert.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: CIM_BindsTo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357852"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="45439-103">CIM \_ bindsto-Klasse</span><span class="sxs-lookup"><span data-stu-id="45439-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="45439-104">Stellt eine Zuordnung dar, bei der ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) -Objekt Protokoll Dienste von einem [**CIM \_ protocolendpoint**](cim-protocolendpoint.md) -Objekt anfordert.</span><span class="sxs-lookup"><span data-stu-id="45439-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="45439-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45439-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="45439-106">Member</span><span class="sxs-lookup"><span data-stu-id="45439-106">Members</span></span>

<span data-ttu-id="45439-107">Die **CIM- \_ bindsto** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="45439-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="45439-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45439-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45439-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45439-109">Properties</span></span>

<span data-ttu-id="45439-110">Die **CIM- \_ bindsto** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45439-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45439-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="45439-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45439-112">Datentyp: **CIM \_ protocolendpoint**</span><span class="sxs-lookup"><span data-stu-id="45439-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="45439-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45439-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45439-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="45439-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="45439-115">Der Endpunkt auf niedrigerer Ebene, auf den der Dienst Zugriffspunkt zugreift.</span><span class="sxs-lookup"><span data-stu-id="45439-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="45439-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="45439-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45439-117">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="45439-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="45439-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45439-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45439-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="45439-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="45439-120">Der Zugriffspunkt oder Protokoll Endpunkt, der vom Endpunkt auf niedrigerer Ebene abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="45439-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45439-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45439-121">Requirements</span></span>



| <span data-ttu-id="45439-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45439-122">Requirement</span></span> | <span data-ttu-id="45439-123">Wert</span><span class="sxs-lookup"><span data-stu-id="45439-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45439-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45439-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45439-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="45439-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="45439-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45439-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45439-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45439-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="45439-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="45439-128">Namespace</span></span><br/>                | <span data-ttu-id="45439-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="45439-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="45439-130">MOF</span><span class="sxs-lookup"><span data-stu-id="45439-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45439-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="45439-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45439-132">DLL</span><span class="sxs-lookup"><span data-stu-id="45439-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45439-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45439-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45439-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45439-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45439-135">**CIM \_ sapsapabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="45439-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

