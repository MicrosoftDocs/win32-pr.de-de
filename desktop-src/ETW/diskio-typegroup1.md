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
# <a name="diskio_typegroup1-class"></a>Diskio \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistyp Klasse für Datenträger-e/a-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **diskio \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **diskio \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Byte Offset**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Byte Offset vom Anfang des physischen Datenträgers.

</dd> <dt>

**Disknumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Zahl, die den physischen Datenträger identifiziert.

</dd> <dt>

**File Object**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (6), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**FileIO- \_ namens**](fileio-name.md) Ereignis, um die am e/a-Vorgang beteiligte Datei zu bestimmen.

</dd> <dt>

**Highresresponse Time**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Die Zeit zwischen der e/a-Initiierung und dem Abschluss des Partitions-Managers (in den Tick-Einheiten von [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).

**Windows Server 2003:** Diese Eigenschaft verfügt über einen [**wmidataid**](event-tracing-mof-qualifiers.md) -Wert von 7.

**Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (7), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Das e/a-Anforderungspaket, das die e/a-Aktivität identifiziert.

**Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**Unpflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Kann mindestens eines der folgenden e/a-Anforderungs Paketflags enthalten (definiert in "ntddk. h", bei dem es sich um eine DDK-Header Datei handelt):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **"unp \_ NoCache"**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **Auslagerungs-e/a \_ \_**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **Beendigung der unp- \_ \_ Einstellung**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **synchrone unp- \_ \_ API**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **Mit unp \_ verknüpfte \_ unp**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **nicht- \_ gepufferte e/a \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**unp- \_ \_ Puffer Freigabe**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **unp- \_ Eingabe \_ Vorgang**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **unp-e/a für \_ synchrone \_ Auslagerung \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **Vorgang zum \_ Erstellen von irren \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**unp- \_ Lese \_ Vorgang**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **unp- \_ Schreib \_ Vorgang**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **unp-Schließ \_ \_ Vorgang**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **e/a- \_ \_ \_ Abschluss der Antwort**
</dt> </dl>

</dd> <dt>

**Issuingthreadid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Der Bezeichner des ausstellenden Threads.

**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 mit SP1, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Diese Eigenschaft wird nicht unterstützt.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Reserviert.

**Windows Server 2008 R2, Windows Server 2008 und Windows 7:** Der Name der Eigenschaft ist **queuetiefe**, die die CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs enthält. Beachten Sie, dass dieser Wert einen Überlauf verursachen kann.

**Windows Vista, Windows Server 2003 mit SP1, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:** Der Name der Eigenschaft ist **Response Time**, die die CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs enthält. Beachten Sie, dass dieser Wert einen Überlauf verursachen kann.

</dd> <dt>

**TransferSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Größe der Daten, die vom Datenträger gelesen oder geschrieben werden (in Bytes).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Windows Server 2003 verwendet die folgende Definition für die **diskio \_ TypeGroup1** -Ereignistyp Klasse.

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

Die **ResponseTime** -Eigenschaft enthält die CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs. Beachten Sie, dass dieser Wert einen Überlauf verursachen kann.

Die **highresresponse Time** -Eigenschaft wird nicht unterstützt.

Windows Server 2003 mit SP1 und Windows Vista verwendet die folgende Definition für die Klasse **diskio \_ TypeGroup1** Event Type.

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

Die Eigenschaft " **unp** " ist das e/a-Anforderungspaket. Diese Eigenschaft identifiziert die e/a-Aktivität. Sie können diese Eigenschaft mit den [**diskio \_ TypeGroup2**](diskio-typegroup2.md) -Ereignissen verwenden, um die Antwortzeit zu korrelieren.

Die **highresresponse Time** -Eigenschaft wird unterstützt. Die-Eigenschaft enthält die Zeit zwischen der e/a-Initiierung und der Vervollständigung, die von PartitionManager gemessen wird (in den KeQueryPerformanceCounter-Einheiten). Verwenden Sie diese Eigenschaft anstelle der Response **time** -Eigenschaft, um die Datenträger-e/a-Antwortzeit zu bestimmen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sowie**](diskio.md)
</dt> </dl>

 

 
