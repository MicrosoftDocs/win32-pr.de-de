---
description: Ordnet einen transparenten Überbrückungs Dienst einem Eintrag der Weiterleitungs Datenbank zu.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: CIM_TransparentBridgingDynamicForwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360020"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="18769-103">CIM- \_ transparentbridgingdynamicforwarding-Klasse</span><span class="sxs-lookup"><span data-stu-id="18769-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="18769-104">Ordnet einen transparenten Überbrückungs Dienst einem Eintrag der Weiterleitungs Datenbank zu.</span><span class="sxs-lookup"><span data-stu-id="18769-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="18769-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18769-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="18769-106">Member</span><span class="sxs-lookup"><span data-stu-id="18769-106">Members</span></span>

<span data-ttu-id="18769-107">Die CIM-Klasse " **\_ transparentbridgingdynamicforwarding** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18769-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="18769-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18769-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18769-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18769-109">Properties</span></span>

<span data-ttu-id="18769-110">Die CIM-Klasse " **\_ transparentbridgingdynamicforwarding** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18769-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18769-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="18769-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18769-112">Datentyp: **CIM \_ transparentbridgingservice**</span><span class="sxs-lookup"><span data-stu-id="18769-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="18769-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18769-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18769-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="18769-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="18769-115">Ein [**CIM- \_ transparentbridgingservice**](cim-transparentbridgingservice.md) -Verweis auf den transparenten Überbrückungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="18769-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="18769-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="18769-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18769-117">Datentyp: **CIM \_ dynamicforwardingentry**</span><span class="sxs-lookup"><span data-stu-id="18769-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="18769-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18769-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18769-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18769-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18769-120">Ein [**CIM \_ dynamicforwardingentry**](cim-dynamicforwardingentry.md) -Verweis auf den weitergeleiteten Datenbankeintrag.</span><span class="sxs-lookup"><span data-stu-id="18769-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18769-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18769-121">Requirements</span></span>



| <span data-ttu-id="18769-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18769-122">Requirement</span></span> | <span data-ttu-id="18769-123">Wert</span><span class="sxs-lookup"><span data-stu-id="18769-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18769-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18769-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18769-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="18769-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="18769-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18769-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18769-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18769-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="18769-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="18769-128">Namespace</span></span><br/>                | <span data-ttu-id="18769-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="18769-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18769-130">MOF</span><span class="sxs-lookup"><span data-stu-id="18769-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18769-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18769-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18769-132">DLL</span><span class="sxs-lookup"><span data-stu-id="18769-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18769-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18769-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18769-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18769-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18769-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="18769-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

