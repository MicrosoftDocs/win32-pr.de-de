---
description: Diese Klasse ist die Ereignistyp Klasse für Datei Vorgangs Ende-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758430"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="e11a7-104">Fleio \_ opend-Klasse</span><span class="sxs-lookup"><span data-stu-id="e11a7-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="e11a7-105">Diese Klasse ist die Ereignistyp Klasse für Datei Vorgangs Ende-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e11a7-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="e11a7-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e11a7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11a7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e11a7-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="e11a7-108">Member</span><span class="sxs-lookup"><span data-stu-id="e11a7-108">Members</span></span>

<span data-ttu-id="e11a7-109">Die Klasse " **fleio \_ opend** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e11a7-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="e11a7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e11a7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e11a7-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e11a7-111">Properties</span></span>

<span data-ttu-id="e11a7-112">Die Klasse " **fleio \_ opend** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e11a7-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e11a7-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="e11a7-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e11a7-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e11a7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e11a7-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e11a7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e11a7-116">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e11a7-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e11a7-117">Zusätzliche Informationen, die vom Dateisystem für den Vorgang zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e11a7-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="e11a7-118">Beispielsweise eine Lese Anforderung, die tatsächliche Anzahl von gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="e11a7-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="e11a7-119">**Unpptr**</span><span class="sxs-lookup"><span data-stu-id="e11a7-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e11a7-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e11a7-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e11a7-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e11a7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e11a7-122">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="e11a7-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e11a7-123">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="e11a7-123">IO request packet.</span></span> <span data-ttu-id="e11a7-124">Diese Eigenschaft identifiziert die e/a-Aktivität, die beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e11a7-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="e11a7-125">**NTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="e11a7-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e11a7-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e11a7-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e11a7-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e11a7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e11a7-128">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="e11a7-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e11a7-129">Rückgabewert des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e11a7-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e11a7-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e11a7-130">Remarks</span></span>

<span data-ttu-id="e11a7-131">Am Anfang des Vorgangs werden die [**-Ereignisse des**](fileio.md) -Vorgangs protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e11a7-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="e11a7-132">Opend-Ereignisse können separat aktiviert werden, um das Ende dieser Vorgänge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e11a7-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="e11a7-133">Mit "unp" können die BEGIN-und End-Ereignisse korreliert werden.</span><span class="sxs-lookup"><span data-stu-id="e11a7-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e11a7-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e11a7-134">Requirements</span></span>



| <span data-ttu-id="e11a7-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e11a7-135">Requirement</span></span> | <span data-ttu-id="e11a7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e11a7-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e11a7-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e11a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e11a7-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e11a7-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e11a7-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e11a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e11a7-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e11a7-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e11a7-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e11a7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11a7-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="e11a7-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




