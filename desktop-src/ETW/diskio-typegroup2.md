---
description: Diese Klasse ist die Ereignistyp Klasse, die den Anfang der Datenträger-e/a-Lese-, Schreib-und Lösch Ereignisse markiert. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525262"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="12f97-104">Diskio \_ TypeGroup2-Klasse</span><span class="sxs-lookup"><span data-stu-id="12f97-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="12f97-105">Diese Klasse ist die Ereignistyp Klasse, die den Anfang der Datenträger-e/a-Lese-, Schreib-und Lösch Ereignisse markiert.</span><span class="sxs-lookup"><span data-stu-id="12f97-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="12f97-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="12f97-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f97-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12f97-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="12f97-108">Member</span><span class="sxs-lookup"><span data-stu-id="12f97-108">Members</span></span>

<span data-ttu-id="12f97-109">Die **diskio \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="12f97-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="12f97-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12f97-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12f97-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12f97-111">Properties</span></span>

<span data-ttu-id="12f97-112">Die **diskio \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12f97-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12f97-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="12f97-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f97-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12f97-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12f97-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12f97-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12f97-116">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1), [**Zeiger**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="12f97-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="12f97-117">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="12f97-117">I/O request packet.</span></span> <span data-ttu-id="12f97-118">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="12f97-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="12f97-119">**Issuingthreadid**</span><span class="sxs-lookup"><span data-stu-id="12f97-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f97-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12f97-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12f97-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12f97-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12f97-122">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="12f97-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="12f97-123">Der Bezeichner des ausstellenden Threads.</span><span class="sxs-lookup"><span data-stu-id="12f97-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="12f97-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12f97-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12f97-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="12f97-125">Requirements</span></span>



| <span data-ttu-id="12f97-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12f97-126">Requirement</span></span> | <span data-ttu-id="12f97-127">Wert</span><span class="sxs-lookup"><span data-stu-id="12f97-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12f97-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12f97-128">Minimum supported client</span></span><br/> | <span data-ttu-id="12f97-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12f97-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12f97-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12f97-130">Minimum supported server</span></span><br/> | <span data-ttu-id="12f97-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12f97-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12f97-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="12f97-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f97-133">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="12f97-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




