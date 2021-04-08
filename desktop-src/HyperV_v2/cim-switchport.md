---
description: Stellt einen Switchport dar, der Datenrahmen sendet und empfängt.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: CIM_SwitchPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959802"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="f7c67-103">CIM \_ Switchport-Klasse</span><span class="sxs-lookup"><span data-stu-id="f7c67-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="f7c67-104">Stellt einen Switchport dar, der Datenrahmen sendet und empfängt.</span><span class="sxs-lookup"><span data-stu-id="f7c67-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7c67-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="f7c67-106">Member</span><span class="sxs-lookup"><span data-stu-id="f7c67-106">Members</span></span>

<span data-ttu-id="f7c67-107">Die **CIM \_ Switchport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f7c67-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="f7c67-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7c67-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7c67-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7c67-109">Properties</span></span>

<span data-ttu-id="f7c67-110">Die **CIM \_ Switchport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f7c67-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7c67-111">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="f7c67-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c67-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7c67-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7c67-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f7c67-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c67-114">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dPort ")</span><span class="sxs-lookup"><span data-stu-id="f7c67-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="f7c67-115">Der numerische Bezeichner für den Switchport.</span><span class="sxs-lookup"><span data-stu-id="f7c67-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7c67-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7c67-116">Requirements</span></span>



| <span data-ttu-id="f7c67-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7c67-117">Requirement</span></span> | <span data-ttu-id="f7c67-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f7c67-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c67-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7c67-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c67-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f7c67-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f7c67-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7c67-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c67-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f7c67-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f7c67-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7c67-123">Namespace</span></span><br/>                | <span data-ttu-id="f7c67-124">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f7c67-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7c67-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f7c67-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7c67-126"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f7c67-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7c67-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c67-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c67-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7c67-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7c67-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7c67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c67-130">**CIM- \_ protocolendpoint**</span><span class="sxs-lookup"><span data-stu-id="f7c67-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

