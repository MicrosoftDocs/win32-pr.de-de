---
description: Ordnet dem virtuellen System eine Momentaufnahme des virtuellen Systems zu.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: CIM_SnapshotOfVirtualSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960167"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="9f9c0-103">CIM \_ snapshodesvirtualsystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="9f9c0-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="9f9c0-104">Ordnet dem virtuellen System eine Momentaufnahme des virtuellen Systems zu.</span><span class="sxs-lookup"><span data-stu-id="9f9c0-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f9c0-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9f9c0-106">Member</span><span class="sxs-lookup"><span data-stu-id="9f9c0-106">Members</span></span>

<span data-ttu-id="9f9c0-107">Die **CIM \_ snapshotofvirtualsystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9f9c0-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="9f9c0-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f9c0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f9c0-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f9c0-109">Properties</span></span>

<span data-ttu-id="9f9c0-110">Die **CIM \_ snapshodesvirtualsystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f9c0-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f9c0-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="9f9c0-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f9c0-112">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="9f9c0-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9f9c0-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f9c0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f9c0-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9f9c0-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9f9c0-115">Ein Verweis auf das Computersystem, das das virtuelle System darstellt.</span><span class="sxs-lookup"><span data-stu-id="9f9c0-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="9f9c0-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="9f9c0-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f9c0-117">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="9f9c0-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="9f9c0-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f9c0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f9c0-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="9f9c0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9f9c0-120">Ein Verweis auf das Einstellungsdaten Objekt, das die Momentaufnahme des virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="9f9c0-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f9c0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f9c0-121">Requirements</span></span>



| <span data-ttu-id="9f9c0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f9c0-122">Requirement</span></span> | <span data-ttu-id="9f9c0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9f9c0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9c0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f9c0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9f9c0-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9f9c0-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9f9c0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f9c0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9f9c0-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f9c0-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9f9c0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f9c0-128">Namespace</span></span><br/>                | <span data-ttu-id="9f9c0-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f9c0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9f9c0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="9f9c0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f9c0-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f9c0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f9c0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9f9c0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f9c0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f9c0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f9c0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f9c0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9c0-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="9f9c0-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

