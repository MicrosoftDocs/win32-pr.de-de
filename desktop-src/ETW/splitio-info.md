---
description: Diese Klasse ist die Ereignistyp Klasse für Split IO-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: SplitIo_Info-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867980"
---
# <a name="splitio_info-class"></a><span data-ttu-id="cbf9c-104">Splitio- \_ Informations Klasse</span><span class="sxs-lookup"><span data-stu-id="cbf9c-104">SplitIo\_Info class</span></span>

<span data-ttu-id="cbf9c-105">Diese Klasse ist die Ereignistyp Klasse für Split IO-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="cbf9c-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="cbf9c-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="cbf9c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf9c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbf9c-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="cbf9c-108">Member</span><span class="sxs-lookup"><span data-stu-id="cbf9c-108">Members</span></span>

<span data-ttu-id="cbf9c-109">Die **splitio \_ Info** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cbf9c-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="cbf9c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbf9c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbf9c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbf9c-111">Properties</span></span>

<span data-ttu-id="cbf9c-112">Die **splitio \_ Info** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cbf9c-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbf9c-113">**Childirp**</span><span class="sxs-lookup"><span data-stu-id="cbf9c-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbf9c-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbf9c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbf9c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbf9c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbf9c-116">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="cbf9c-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cbf9c-117">Untergeordnetes IO-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="cbf9c-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="cbf9c-118">**Paramel**</span><span class="sxs-lookup"><span data-stu-id="cbf9c-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbf9c-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbf9c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbf9c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbf9c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbf9c-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="cbf9c-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cbf9c-122">Übergeordnetes IO-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="cbf9c-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbf9c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbf9c-123">Remarks</span></span>

<span data-ttu-id="cbf9c-124">Gibt an, dass der Volumemanager das Paar in zwei unps aufteilen soll.</span><span class="sxs-lookup"><span data-stu-id="cbf9c-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf9c-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cbf9c-125">Requirements</span></span>



| <span data-ttu-id="cbf9c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbf9c-126">Requirement</span></span> | <span data-ttu-id="cbf9c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cbf9c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cbf9c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbf9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf9c-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbf9c-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cbf9c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbf9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf9c-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbf9c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




