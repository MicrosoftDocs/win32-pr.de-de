---
description: Bietet zusätzliche Informationen, die mit der Methode "kreatereferencepoint" der Klasse "MSVM \_ virtualsystemreferencepointservice" verwendet werden können.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Msvm_VirtualSystemReferencePointSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366359"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="311a1-103">MSVM \_ virtualsystemreferencepointsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="311a1-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="311a1-104">Bietet zusätzliche Informationen, die mit der Methode " [**kreatereferencepoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) " der Klasse " [**MSVM \_ virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md) " verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="311a1-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="311a1-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="311a1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="311a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="311a1-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="311a1-107">Member</span><span class="sxs-lookup"><span data-stu-id="311a1-107">Members</span></span>

<span data-ttu-id="311a1-108">Die **MSVM \_ virtualsystemreferencepointsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="311a1-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="311a1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="311a1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="311a1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="311a1-110">Properties</span></span>

<span data-ttu-id="311a1-111">Die **MSVM \_ virtualsystemreferencepointsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="311a1-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="311a1-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="311a1-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311a1-113">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="311a1-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="311a1-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="311a1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311a1-115">Die Konsistenz Ebene des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="311a1-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="311a1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="311a1-116">Requirements</span></span>



| <span data-ttu-id="311a1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="311a1-117">Requirement</span></span> | <span data-ttu-id="311a1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="311a1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="311a1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="311a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="311a1-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="311a1-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="311a1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="311a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="311a1-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="311a1-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="311a1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="311a1-123">Namespace</span></span><br/>                | <span data-ttu-id="311a1-124">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="311a1-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="311a1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="311a1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="311a1-126"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="311a1-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="311a1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="311a1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="311a1-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="311a1-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="311a1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="311a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311a1-130">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="311a1-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




