---
description: Stellt eine generische Zuordnung zwischen zwei verwalteten Elementen dar, die unterschiedliche Aspekte der gleichen zugrunde liegenden Entität darstellen.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: CIM_LogicalIdentity-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346480"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="a4000-103">CIM_LogicalIdentity-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="a4000-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="a4000-104">Stellt eine generische Zuordnung zwischen zwei verwalteten Elementen dar, die unterschiedliche Aspekte der gleichen zugrunde liegenden Entität darstellen.</span><span class="sxs-lookup"><span data-stu-id="a4000-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4000-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4000-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="a4000-106">Member</span><span class="sxs-lookup"><span data-stu-id="a4000-106">Members</span></span>

<span data-ttu-id="a4000-107">Die **CIM \_ logicalidentity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a4000-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="a4000-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4000-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4000-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4000-109">Properties</span></span>

<span data-ttu-id="a4000-110">Die **CIM \_ logicalidentity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4000-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4000-111">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="a4000-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4000-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="a4000-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a4000-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a4000-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4000-114">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a4000-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a4000-115">Der zweite Aspekt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a4000-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a4000-116">**Systemelement**</span><span class="sxs-lookup"><span data-stu-id="a4000-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4000-117">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="a4000-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a4000-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a4000-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4000-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a4000-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a4000-120">Der erste Aspekt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a4000-120">The first aspect in the association.</span></span> <span data-ttu-id="a4000-121">Durch die Verwendung von System im Eigenschaftsnamen wird der Bereich der Zuordnung nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="a4000-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4000-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4000-122">Requirements</span></span>



| <span data-ttu-id="a4000-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4000-123">Requirement</span></span> | <span data-ttu-id="a4000-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a4000-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4000-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4000-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a4000-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4000-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a4000-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4000-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a4000-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a4000-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a4000-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4000-129">Namespace</span></span><br/>                | <span data-ttu-id="a4000-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a4000-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a4000-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a4000-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4000-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a4000-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4000-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a4000-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4000-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4000-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

