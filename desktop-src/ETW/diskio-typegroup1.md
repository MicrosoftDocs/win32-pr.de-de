---
description: Diese Klasse ist die Ereignistyp Klasse für Datenträger-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: DiskIo_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526867"
---
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="39d8b-104">Diskio \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="39d8b-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="39d8b-105">Diese Klasse ist die Ereignistyp Klasse für Datenträger-e/a-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="39d8b-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="39d8b-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="39d8b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d8b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d8b-107">Syntax</span></span>

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="39d8b-108">Member</span><span class="sxs-lookup"><span data-stu-id="39d8b-108">Members</span></span>

<span data-ttu-id="39d8b-109">Die **diskio \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="39d8b-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="39d8b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39d8b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39d8b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39d8b-111">Properties</span></span>

<span data-ttu-id="39d8b-112">Die **diskio \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39d8b-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39d8b-113">**Byte Offset**</span><span class="sxs-lookup"><span data-stu-id="39d8b-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-114">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="39d8b-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-116">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="39d8b-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-117">Byte Offset vom Anfang des physischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="39d8b-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-118">**Disknumber**</span><span class="sxs-lookup"><span data-stu-id="39d8b-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-121">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="39d8b-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-122">Zahl, die den physischen Datenträger identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39d8b-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-123">**File Object**</span><span class="sxs-lookup"><span data-stu-id="39d8b-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-126">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (6), [**Zeiger**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="39d8b-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-127">Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**FileIO- \_ namens**](fileio-name.md) Ereignis, um die am e/a-Vorgang beteiligte Datei zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="39d8b-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-128">**Highresresponse Time**</span><span class="sxs-lookup"><span data-stu-id="39d8b-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="39d8b-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-131">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (8)</span><span class="sxs-lookup"><span data-stu-id="39d8b-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-132">Die Zeit zwischen der e/a-Initiierung und dem Abschluss des Partitions-Managers (in den Tick-Einheiten von [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).</span><span class="sxs-lookup"><span data-stu-id="39d8b-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="39d8b-133">**Windows Server 2003:** Diese Eigenschaft verfügt über einen [**wmidataid**](event-tracing-mof-qualifiers.md) -Wert von 7.</span><span class="sxs-lookup"><span data-stu-id="39d8b-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="39d8b-134">**Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39d8b-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-135">**IRP**</span><span class="sxs-lookup"><span data-stu-id="39d8b-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-136">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-138">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (7), [**Zeiger**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="39d8b-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-139">Das e/a-Anforderungspaket, das die e/a-Aktivität identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39d8b-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="39d8b-140">**Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39d8b-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-141">**Unpflags**</span><span class="sxs-lookup"><span data-stu-id="39d8b-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-144">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="39d8b-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-145">Kann mindestens eines der folgenden e/a-Anforderungs Paketflags enthalten (definiert in "ntddk. h", bei dem es sich um eine DDK-Header Datei handelt):</span><span class="sxs-lookup"><span data-stu-id="39d8b-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="39d8b-146">**"unp \_ NoCache"**</span><span class="sxs-lookup"><span data-stu-id="39d8b-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="39d8b-147">**Auslagerungs-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39d8b-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="39d8b-148">**Beendigung der unp- \_ \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="39d8b-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="39d8b-149">**synchrone unp- \_ \_ API**</span><span class="sxs-lookup"><span data-stu-id="39d8b-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="39d8b-150">**Mit unp \_ verknüpfte \_ unp**</span><span class="sxs-lookup"><span data-stu-id="39d8b-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="39d8b-151">**nicht- \_ gepufferte e/a \_**</span><span class="sxs-lookup"><span data-stu-id="39d8b-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="39d8b-152">**unp- \_ \_ Puffer Freigabe**</span><span class="sxs-lookup"><span data-stu-id="39d8b-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="39d8b-153">**unp- \_ Eingabe \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="39d8b-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="39d8b-154">**unp-e/a für \_ synchrone \_ Auslagerung \_**</span><span class="sxs-lookup"><span data-stu-id="39d8b-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="39d8b-155">**Vorgang zum \_ Erstellen von irren \_**</span><span class="sxs-lookup"><span data-stu-id="39d8b-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="39d8b-156">**unp- \_ Lese \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="39d8b-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="39d8b-157">**unp- \_ Schreib \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="39d8b-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="39d8b-158">**unp-Schließ \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="39d8b-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="39d8b-159">**e/a- \_ \_ \_ Abschluss der Antwort**</span><span class="sxs-lookup"><span data-stu-id="39d8b-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39d8b-160">**Issuingthreadid**</span><span class="sxs-lookup"><span data-stu-id="39d8b-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-163">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (9)</span><span class="sxs-lookup"><span data-stu-id="39d8b-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-164">Der Bezeichner des ausstellenden Threads.</span><span class="sxs-lookup"><span data-stu-id="39d8b-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="39d8b-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 mit SP1, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39d8b-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-166">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="39d8b-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-169">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="39d8b-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-170">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="39d8b-170">Reserved.</span></span>

<span data-ttu-id="39d8b-171">**Windows Server 2008 R2, Windows Server 2008 und Windows 7:** Der Name der Eigenschaft ist **queuetiefe**, die die CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="39d8b-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="39d8b-172">Beachten Sie, dass dieser Wert einen Überlauf verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="39d8b-172">Note that this value can overflow.</span></span>

<span data-ttu-id="39d8b-173">**Windows Vista, Windows Server 2003 mit SP1, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Der Name der Eigenschaft ist **Response Time**, die die CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="39d8b-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="39d8b-174">Beachten Sie, dass dieser Wert einen Überlauf verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="39d8b-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="39d8b-175">**TransferSize**</span><span class="sxs-lookup"><span data-stu-id="39d8b-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d8b-176">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39d8b-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39d8b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d8b-178">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="39d8b-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="39d8b-179">Größe der Daten, die vom Datenträger gelesen oder geschrieben werden (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="39d8b-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39d8b-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39d8b-180">Remarks</span></span>

<span data-ttu-id="39d8b-181">Windows Server 2003 verwendet die folgende Definition für die **diskio \_ TypeGroup1** -Ereignistyp Klasse.</span><span class="sxs-lookup"><span data-stu-id="39d8b-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

<span data-ttu-id="39d8b-182">Die **ResponseTime** -Eigenschaft enthält die CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="39d8b-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="39d8b-183">Beachten Sie, dass dieser Wert einen Überlauf verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="39d8b-183">Note that this value can overflow.</span></span>

<span data-ttu-id="39d8b-184">Die **highresresponse Time** -Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39d8b-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="39d8b-185">Windows Server 2003 mit SP1 und Windows Vista verwendet die folgende Definition für die Klasse **diskio \_ TypeGroup1** Event Type.</span><span class="sxs-lookup"><span data-stu-id="39d8b-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

<span data-ttu-id="39d8b-186">Die Eigenschaft " **unp** " ist das e/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="39d8b-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="39d8b-187">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="39d8b-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="39d8b-188">Sie können diese Eigenschaft mit den [**diskio \_ TypeGroup2**](diskio-typegroup2.md) -Ereignissen verwenden, um die Antwortzeit zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="39d8b-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="39d8b-189">Die **highresresponse Time** -Eigenschaft wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39d8b-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="39d8b-190">Die-Eigenschaft enthält die Zeit zwischen der e/a-Initiierung und der Vervollständigung, die von PartitionManager gemessen wird (in den KeQueryPerformanceCounter-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="39d8b-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="39d8b-191">Verwenden Sie diese Eigenschaft anstelle der Response **time** -Eigenschaft, um die Datenträger-e/a-Antwortzeit zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="39d8b-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d8b-192">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="39d8b-192">Requirements</span></span>



| <span data-ttu-id="39d8b-193">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39d8b-193">Requirement</span></span> | <span data-ttu-id="39d8b-194">Wert</span><span class="sxs-lookup"><span data-stu-id="39d8b-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-195">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39d8b-195">Minimum supported client</span></span><br/> | <span data-ttu-id="39d8b-196">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39d8b-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39d8b-197">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39d8b-197">Minimum supported server</span></span><br/> | <span data-ttu-id="39d8b-198">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39d8b-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="39d8b-199">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39d8b-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d8b-200">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="39d8b-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 
