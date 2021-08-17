---
description: Diese Klasse ist die Ereignistypklasse für Datenträger-E/A-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: 3a69643602a59fa7be8cd844f3f2908c92e2e08545f7444d1002ec1542b36730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814976"
---
# <a name="diskio_typegroup1-class"></a>DiskIo \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Datenträger-E/A-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **DiskIo \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DiskIo \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Byteoffset vom Anfang des physischen Datenträgers.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Zahl, die den physischen Datenträger identifiziert.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Übereinstimmung mit dem Wert dieses Zeigers auf den **FileObject-Zeigerwert** in einem [**FileIo \_ Name-Ereignis,**](fileio-name.md) um die am E/A-Vorgang beteiligte Datei zu bestimmen.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Die Vom Partitions-Manager gemessene Zeit zwischen der E/A-Initiierung und dem Abschluss (in den [**Tick-Einheiten von KeQueryPerformanceCounter).**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter)

**Windows Server 2003:** Diese Eigenschaft hat den [**WmiDataId-Wert**](event-tracing-mof-qualifiers.md) 7.

**Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Das E/A-Anforderungspaket, das die E/A-Aktivität identifiziert.

**Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Kann mindestens eines der folgenden E/A-Anforderungspaketflags enthalten (definiert in Ntddk.h, einer DDK-Headerdatei):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOCACHE**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **\_ \_ IRP-PAGING-E/A**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **ABSCHLUSS DER \_ \_ IRP-BEREITSTELLUNG**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **SYNCHRONE \_ \_ IRP-API**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **\_IRP-ZUGEORDNETES \_ IRP**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **IRP \_ BUFFERED \_ IO**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**IRP \_ DEALLOCATE \_ BUFFER**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **\_IRP-EINGABEVORGANG \_**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **SYNCHRONE \_ \_ IRP-PAGING-E/A \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **\_ \_ IRP-ERSTELLUNGSVORGANG**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**\_IRP-LESEVORGANG \_**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **\_IRP-SCHREIBVORGANG \_**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **IRP- \_ \_ CLOSE-VORGANG**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **IRP \_ DEFER \_ IO \_ COMPLETION**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Der Bezeichner des ausstellenden Threads.

**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 mit SP1, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Reserviert.

**Windows Server 2008 R2, Windows Server 2008 und Windows 7:** Der Name der Eigenschaft ist **QueueDepth,** die die CPU-Tickanzahl vom Anfang des Vorgangs bis zum Ende des Vorgangs enthält. Beachten Sie, dass dieser Wert überlaufen kann.

**Windows Vista, Windows Server 2003 mit SP1, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Der Name der Eigenschaft ist **ResponseTime,** die die CPU-Tickanzahl vom Anfang des Vorgangs bis zum Ende des Vorgangs enthält. Beachten Sie, dass dieser Wert überlaufen kann.

</dd> <dt>

**TransferSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Größe der auf den Datenträger gelesenen oder von diesem geschriebenen Daten in Bytes.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Windows Server 2003 verwendet die folgende Definition für die **DiskIo \_ TypeGroup1-Ereignistypklasse.**

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

Die **ResponseTime-Eigenschaft** enthält die CPU-Tickanzahl vom Anfang des Vorgangs bis zum Ende des Vorgangs. Beachten Sie, dass dieser Wert überlaufen kann.

Die **HighResResponseTime-Eigenschaft** wird nicht unterstützt.

Windows Server 2003 mit SP1 und Windows Vista verwendet die folgende Definition für die **DiskIo \_ TypeGroup1-Ereignistypklasse.**

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

Die **Irp-Eigenschaft** ist das E/A-Anforderungspaket. Diese Eigenschaft identifiziert die E/A-Aktivität. Sie können diese Eigenschaft mit den [**DiskIo \_ TypeGroup2-Ereignissen**](diskio-typegroup2.md) verwenden, um die Antwortzeit zu korrelieren.

Die **HighResResponseTime-Eigenschaft** wird unterstützt. Die -Eigenschaft enthält die Zeit zwischen der E/A-Initiierung und dem Abschluss, die von PartitionManager gemessen wird (in den KeQueryPerformanceCounter-Einheiten). Verwenden Sie diese Eigenschaft anstelle der **ResponseTime-Eigenschaft,** um die E/A-Antwortzeit des Datenträgers zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 
