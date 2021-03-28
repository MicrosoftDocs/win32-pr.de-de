---
description: Diese Klasse ist die Ereignistyp Klasse für Datenträger-e/a-Lösch Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: DiskIo_TypeGroup3-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977145"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="32f51-104">Diskio \_ TypeGroup3-Klasse</span><span class="sxs-lookup"><span data-stu-id="32f51-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="32f51-105">Diese Klasse ist die Ereignistyp Klasse für Datenträger-e/a-Lösch Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="32f51-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="32f51-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="32f51-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f51-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="32f51-107">Syntax</span></span>

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="32f51-108">Member</span><span class="sxs-lookup"><span data-stu-id="32f51-108">Members</span></span>

<span data-ttu-id="32f51-109">Die **diskio \_ TypeGroup3** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="32f51-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="32f51-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f51-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32f51-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f51-111">Properties</span></span>

<span data-ttu-id="32f51-112">Die **diskio \_ TypeGroup3** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="32f51-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32f51-113">**Disknumber**</span><span class="sxs-lookup"><span data-stu-id="32f51-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f51-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f51-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f51-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f51-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f51-116">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="32f51-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="32f51-117">Zahl, die den physischen Datenträger identifiziert.</span><span class="sxs-lookup"><span data-stu-id="32f51-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="32f51-118">**Highresresponse Time**</span><span class="sxs-lookup"><span data-stu-id="32f51-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f51-119">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32f51-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32f51-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f51-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f51-121">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="32f51-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="32f51-122">CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="32f51-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32f51-123">**IRP**</span><span class="sxs-lookup"><span data-stu-id="32f51-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f51-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f51-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f51-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f51-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f51-126">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (4), [**Zeiger**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="32f51-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="32f51-127">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="32f51-127">I/O request packet.</span></span> <span data-ttu-id="32f51-128">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="32f51-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="32f51-129">**Unpflags**</span><span class="sxs-lookup"><span data-stu-id="32f51-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f51-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f51-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f51-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f51-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f51-132">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="32f51-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="32f51-133">Kann mindestens eines der folgenden e/a-Anforderungs Paketflags enthalten (definiert in "ntddk. h", bei dem es sich um eine DDK-Header Datei handelt):</span><span class="sxs-lookup"><span data-stu-id="32f51-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="32f51-134">**"unp \_ NoCache"**</span><span class="sxs-lookup"><span data-stu-id="32f51-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="32f51-135">**Auslagerungs-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32f51-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="32f51-136">**Beendigung der unp- \_ \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="32f51-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="32f51-137">**synchrone unp- \_ \_ API**</span><span class="sxs-lookup"><span data-stu-id="32f51-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="32f51-138">**Mit unp \_ verknüpfte \_ unp**</span><span class="sxs-lookup"><span data-stu-id="32f51-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="32f51-139">**nicht- \_ gepufferte e/a \_**</span><span class="sxs-lookup"><span data-stu-id="32f51-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="32f51-140">**unp- \_ \_ Puffer Freigabe**</span><span class="sxs-lookup"><span data-stu-id="32f51-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="32f51-141">**unp- \_ Eingabe \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="32f51-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="32f51-142">**unp-e/a für \_ synchrone \_ Auslagerung \_**</span><span class="sxs-lookup"><span data-stu-id="32f51-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="32f51-143">**Vorgang zum \_ Erstellen von irren \_**</span><span class="sxs-lookup"><span data-stu-id="32f51-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="32f51-144">**unp- \_ Lese \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="32f51-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="32f51-145">**unp- \_ Schreib \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="32f51-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="32f51-146">**unp-Schließ \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="32f51-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="32f51-147">**e/a- \_ \_ \_ Abschluss der Antwort**</span><span class="sxs-lookup"><span data-stu-id="32f51-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32f51-148">**Issuingthreadid**</span><span class="sxs-lookup"><span data-stu-id="32f51-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f51-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f51-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f51-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f51-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f51-151">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="32f51-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="32f51-152">Der Bezeichner des ausstellenden Threads.</span><span class="sxs-lookup"><span data-stu-id="32f51-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="32f51-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32f51-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32f51-154">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="32f51-154">Requirements</span></span>



| <span data-ttu-id="32f51-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32f51-155">Requirement</span></span> | <span data-ttu-id="32f51-156">Wert</span><span class="sxs-lookup"><span data-stu-id="32f51-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32f51-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32f51-157">Minimum supported client</span></span><br/> | <span data-ttu-id="32f51-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32f51-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32f51-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32f51-159">Minimum supported server</span></span><br/> | <span data-ttu-id="32f51-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32f51-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32f51-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32f51-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f51-162">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="32f51-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




