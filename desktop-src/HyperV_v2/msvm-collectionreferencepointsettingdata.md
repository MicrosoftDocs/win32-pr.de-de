---
description: Bietet zusätzliche Informationen, die mit der Methode "kreatereferencepoint" der MSVM \_ collectionreferencepointservice-Klasse verwendet werden können.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Msvm_CollectionReferencePointSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130697"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="0214c-103">MSVM \_ collectionreferencepointsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="0214c-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="0214c-104">Bietet zusätzliche Informationen, die mit der Methode " [**kreatereferencepoint**](msvm-collectionreferencepointservice-createreferencepoint.md) " der [**MSVM \_ collectionreferencepointservice**](msvm-collectionreferencepointservice.md) -Klasse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0214c-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="0214c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0214c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0214c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0214c-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="0214c-107">Member</span><span class="sxs-lookup"><span data-stu-id="0214c-107">Members</span></span>

<span data-ttu-id="0214c-108">Die **MSVM \_ collectionreferencepointsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0214c-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0214c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0214c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0214c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0214c-110">Properties</span></span>

<span data-ttu-id="0214c-111">Die **MSVM \_ collectionreferencepointsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0214c-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0214c-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="0214c-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0214c-113">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0214c-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0214c-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0214c-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0214c-115">Konsistenz Ebene des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="0214c-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0214c-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0214c-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="0214c-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Anwendungs konsistent** (1)</span><span class="sxs-lookup"><span data-stu-id="0214c-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0214c-118">Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Absturz konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="0214c-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="0214c-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Absturz konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="0214c-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0214c-120">Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Anwendungs konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="0214c-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0214c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0214c-121">Requirements</span></span>



| <span data-ttu-id="0214c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0214c-122">Requirement</span></span> | <span data-ttu-id="0214c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0214c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0214c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0214c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0214c-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0214c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0214c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0214c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0214c-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0214c-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0214c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0214c-128">Namespace</span></span><br/>                | <span data-ttu-id="0214c-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0214c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0214c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0214c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0214c-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0214c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0214c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0214c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0214c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0214c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0214c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0214c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0214c-135">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="0214c-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




