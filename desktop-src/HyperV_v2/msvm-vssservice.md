---
description: Stellt den Gast-VSS-Dienst dar. Sie wird zum Abfragen von Gast Cluster Informationen vom Hyper-V-Host verwendet.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Msvm_VssService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342769"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="8459a-104">MSVM- \_ VssService-Klasse</span><span class="sxs-lookup"><span data-stu-id="8459a-104">Msvm\_VssService class</span></span>

<span data-ttu-id="8459a-105">Stellt den Gast-VSS-Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="8459a-105">Represents the guest VSS service.</span></span> <span data-ttu-id="8459a-106">Sie wird zum Abfragen von Gast Cluster Informationen vom Hyper-V-Host verwendet.</span><span class="sxs-lookup"><span data-stu-id="8459a-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="8459a-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8459a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8459a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8459a-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="8459a-109">Member</span><span class="sxs-lookup"><span data-stu-id="8459a-109">Members</span></span>

<span data-ttu-id="8459a-110">Die **MSVM \_ VssService** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8459a-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="8459a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="8459a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8459a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8459a-112">Methods</span></span>

<span data-ttu-id="8459a-113">Die **MSVM- \_ VssService** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8459a-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="8459a-114">Methode</span><span class="sxs-lookup"><span data-stu-id="8459a-114">Method</span></span>                                                                               | <span data-ttu-id="8459a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8459a-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="8459a-116">**Queryguestclusterinformation**</span><span class="sxs-lookup"><span data-stu-id="8459a-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="8459a-117">Abfragen von Cluster Informationen vom Hyper-V-Host zum Gast.</span><span class="sxs-lookup"><span data-stu-id="8459a-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8459a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8459a-118">Requirements</span></span>



| <span data-ttu-id="8459a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8459a-119">Requirement</span></span> | <span data-ttu-id="8459a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8459a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8459a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8459a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8459a-122">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8459a-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8459a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8459a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8459a-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8459a-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8459a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="8459a-125">Namespace</span></span><br/>                | <span data-ttu-id="8459a-126">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8459a-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8459a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="8459a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8459a-128"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8459a-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8459a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8459a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8459a-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8459a-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8459a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8459a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8459a-132">**MSVM- \_ guestservice**</span><span class="sxs-lookup"><span data-stu-id="8459a-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




