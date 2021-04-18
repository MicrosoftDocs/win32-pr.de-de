---
description: Stellt eine Zuordnung dar, in der ein Eintrag einer Weiterleitungs Datenbank auf einen Switchport angewendet wird.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: CIM_SwitchPortDynamicForwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368247"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="96daa-103">CIM \_ switchportdynamicforwarding-Klasse</span><span class="sxs-lookup"><span data-stu-id="96daa-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="96daa-104">Stellt eine Zuordnung dar, in der ein Eintrag einer Weiterleitungs Datenbank auf einen Switchport angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="96daa-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="96daa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96daa-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="96daa-106">Member</span><span class="sxs-lookup"><span data-stu-id="96daa-106">Members</span></span>

<span data-ttu-id="96daa-107">Die **CIM \_ switchportdynamicforwarding** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="96daa-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="96daa-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96daa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96daa-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96daa-109">Properties</span></span>

<span data-ttu-id="96daa-110">Die **CIM \_ switchportdynamicforwarding** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96daa-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96daa-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="96daa-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96daa-112">Datentyp: **CIM \_ Switchport**</span><span class="sxs-lookup"><span data-stu-id="96daa-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="96daa-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="96daa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96daa-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="96daa-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="96daa-115">Ein [**CIM- \_ switchportverweis auf den Switchport**](cim-switchport.md) .</span><span class="sxs-lookup"><span data-stu-id="96daa-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="96daa-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="96daa-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96daa-117">Datentyp: **CIM \_ dynamicforwardingentry**</span><span class="sxs-lookup"><span data-stu-id="96daa-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="96daa-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="96daa-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96daa-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="96daa-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="96daa-120">Ein [**CIM \_ dynamicforwardingentry**](cim-dynamicforwardingentry.md) -Verweis auf den Eintrag der Weiterleitungs Datenbank.</span><span class="sxs-lookup"><span data-stu-id="96daa-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96daa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96daa-121">Requirements</span></span>



| <span data-ttu-id="96daa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96daa-122">Requirement</span></span> | <span data-ttu-id="96daa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="96daa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96daa-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96daa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="96daa-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="96daa-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="96daa-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96daa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="96daa-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96daa-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="96daa-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="96daa-128">Namespace</span></span><br/>                | <span data-ttu-id="96daa-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="96daa-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="96daa-130">MOF</span><span class="sxs-lookup"><span data-stu-id="96daa-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96daa-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="96daa-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96daa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="96daa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96daa-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96daa-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="96daa-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96daa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96daa-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="96daa-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

