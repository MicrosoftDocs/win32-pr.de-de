---
description: Die FileIo \_ V0 \_ Name-Klasse ist eine ältere Version der Ereignistypklasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 11a85c182511a866d3fb76f291b0a73ed0541fdee34b7e6f74c036b5446792db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041860"
---
# <a name="fileio_v0_name-class"></a>FileIo \_ V0 \_ Name-Klasse

Die **FileIo \_ V0 \_ Name-Klasse** ist eine ältere Version der Ereignistypklasse für Datei-E/A-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Member

Die **FileIo \_ V0 \_ Name-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ V0 \_ Name-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Vollständiger Pfad zur Datei, ohne laufwerksbuchstabe.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Stimmen Sie den Wert dieses Zeigers mit dem **FileObject-Zeigerwert** in einem [**DiskIo \_ TypeGroup1-Ereignis**](diskio-typegroup1.md) ab, um den Typ des E/A-Vorgangs zu bestimmen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Windows Server 2003:** Um den Laufwerkbuchstaben für den Dateinamenpfad abzurufen, verwenden Sie den **FileObject-Eigenschaftswert,** um dem entsprechenden [**DiskIo \_ TypeGroup1-Ereignis**](diskio-typegroup1.md) zuzuordnen. Verwenden Sie aus dem **DiskIo \_ TypeGroup1-Ereignis** die Eigenschaftswerte **DiskNumber** und **ByteOffset,** um dem entsprechenden [**SystemConfig \_ LogDisk-Ereignis**](systemconfig-logdisk.md) zuzuordnen. Die **DriveLetterString-Eigenschaft** enthält den Laufwerkbuchstaben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> </dl>

 

 




