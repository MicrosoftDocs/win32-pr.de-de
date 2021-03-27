---
description: Diese Klasse ist die Ereignistyp Klasse für Lese-und Schreib Ereignisse von Dateien. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: FileIo_ReadWrite-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980368"
---
# <a name="fileio_readwrite-class"></a>Klasse von "fleio" \_

Diese Klasse ist die Ereignistyp Klasse für Lese-und Schreib Ereignisse von Dateien.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a>Member

Die " **fleio \_** "-Klasse "Read Write" enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die " **fleio"- \_ /schreibklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Filekey**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), Zeiger
</dt> </dl>

Um den Dateinamen zu ermitteln, vergleichen Sie den Wert dieser Eigenschaft mit der **FileObject** -Eigenschaft eines [**FileIO- \_ namens**](fileio-name.md) Ereignisses.

</dd> <dt>

**File Object**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Zeiger
</dt> </dl>

Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.

</dd> <dt>

**Ioflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7)
</dt> </dl>

Für diesen Vorgang angegebene e/a-Anforderungs Paketflags.

</dd> <dt>

**Iosize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6)
</dt> </dl>

Anzahl der angeforderten Bytes.

</dd> <dt>

**Unpptr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

E/a-Anforderungspaket. Diese Eigenschaft identifiziert die e/a-Aktivität.

</dd> <dt>

**Offset**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Der Dateioffset für den angeforderten Vorgang wird gestartet.

</dd> <dt>

**TTiD**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Zeiger
</dt> </dl>

Thread Bezeichner des Threads, der den Vorgang ausführt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




