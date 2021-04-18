---
description: Ordnet die MSVM \_ snapshotcollection den enthaltenen MSVM \_ virtualsystemsettingdata-Objekten zu.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Msvm_CollectedSnapshots-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357424"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="19ea1-103">MSVM \_ collectedshots-Klasse</span><span class="sxs-lookup"><span data-stu-id="19ea1-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="19ea1-104">Ordnet die [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) den enthaltenen [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="19ea1-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="19ea1-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19ea1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ea1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ea1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="19ea1-107">Member</span><span class="sxs-lookup"><span data-stu-id="19ea1-107">Members</span></span>

<span data-ttu-id="19ea1-108">Die **MSVM \_ collectedshots** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="19ea1-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="19ea1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19ea1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19ea1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19ea1-110">Properties</span></span>

<span data-ttu-id="19ea1-111">Die **MSVM \_ collectedshots** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19ea1-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19ea1-112">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="19ea1-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ea1-113">Datentyp: **MSVM \_ snapshotcollection**</span><span class="sxs-lookup"><span data-stu-id="19ea1-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="19ea1-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="19ea1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ea1-115">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="19ea1-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="19ea1-116">Eine [**MSVM- \_ snapshotcollection**](msvm-snapshotcollection.md) -Gruppierung oder ein "Bag"-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="19ea1-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="19ea1-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="19ea1-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ea1-118">Datentyp: **MSVM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="19ea1-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="19ea1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="19ea1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ea1-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="19ea1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="19ea1-121">Ein [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Element, das die Elemente der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="19ea1-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19ea1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19ea1-122">Requirements</span></span>



| <span data-ttu-id="19ea1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19ea1-123">Requirement</span></span> | <span data-ttu-id="19ea1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="19ea1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19ea1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19ea1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19ea1-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19ea1-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="19ea1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19ea1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19ea1-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="19ea1-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="19ea1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="19ea1-129">Namespace</span></span><br/>                | <span data-ttu-id="19ea1-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="19ea1-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19ea1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="19ea1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19ea1-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19ea1-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19ea1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="19ea1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19ea1-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19ea1-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19ea1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19ea1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ea1-136">**CIM \_ collectedmses**</span><span class="sxs-lookup"><span data-stu-id="19ea1-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

