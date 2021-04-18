---
description: Stellt eine Beziehung dar, in der über ein Medien Zugriffsgerät auf einen Speicherblock zugegriffen werden muss.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: CIM_MediaPresent-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354899"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="39829-103">CIM_MediaPresent-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="39829-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="39829-104">Stellt eine Beziehung dar, in der über ein Medien Zugriffsgerät auf einen Speicherblock zugegriffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="39829-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="39829-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39829-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="39829-106">Member</span><span class="sxs-lookup"><span data-stu-id="39829-106">Members</span></span>

<span data-ttu-id="39829-107">Die **CIM \_ mediapresent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="39829-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="39829-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39829-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39829-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39829-109">Properties</span></span>

<span data-ttu-id="39829-110">Die **CIM \_ mediapresent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39829-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39829-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="39829-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39829-112">Datentyp: **CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="39829-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="39829-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39829-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39829-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="39829-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="39829-115">Das Medien Zugriffsgerät.</span><span class="sxs-lookup"><span data-stu-id="39829-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="39829-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="39829-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39829-117">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="39829-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="39829-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39829-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39829-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="39829-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="39829-120">Der Speicherblock, auf den zugegriffen wird, wenn das Medien Zugriffsgerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39829-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="39829-121">**Fixedmedia**</span><span class="sxs-lookup"><span data-stu-id="39829-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39829-122">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="39829-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39829-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39829-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39829-124">**true** , wenn der Speicherblock im Medien Zugriffsgerät korrigiert wurde und nicht ausgewiesen werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="39829-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39829-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39829-125">Requirements</span></span>



| <span data-ttu-id="39829-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39829-126">Requirement</span></span> | <span data-ttu-id="39829-127">Wert</span><span class="sxs-lookup"><span data-stu-id="39829-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39829-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39829-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39829-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="39829-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="39829-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39829-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39829-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39829-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="39829-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="39829-132">Namespace</span></span><br/>                | <span data-ttu-id="39829-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="39829-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="39829-134">MOF</span><span class="sxs-lookup"><span data-stu-id="39829-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39829-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="39829-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39829-136">DLL</span><span class="sxs-lookup"><span data-stu-id="39829-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39829-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39829-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39829-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39829-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39829-139">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="39829-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

