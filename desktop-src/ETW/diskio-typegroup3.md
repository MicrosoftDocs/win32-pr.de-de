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
# <a name="diskio_typegroup3-class"></a>Diskio \_ TypeGroup3-Klasse

Diese Klasse ist die Ereignistyp Klasse für Datenträger-e/a-Lösch Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **diskio \_ TypeGroup3** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **diskio \_ TypeGroup3** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

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

**Highresresponse Time**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

CPU-Takt Anzahl vom Beginn des Vorgangs bis zum Ende des Vorgangs.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (4), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

E/a-Anforderungspaket. Diese Eigenschaft identifiziert die e/a-Aktivität.

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

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Der Bezeichner des ausstellenden Threads.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sowie**](diskio.md)
</dt> </dl>

 

 




