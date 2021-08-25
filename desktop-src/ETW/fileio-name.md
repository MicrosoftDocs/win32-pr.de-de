---
description: 'FileIo_Name Klasse: Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: FileIo_Name-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 147e7fd2cb28f7245d8366dc66d7b3859f37586f1bd7c9c0b96d2d7ef57e35d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829712"
---
# <a name="fileio_name-class"></a>\_FileIo-Name-Klasse

Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Member

Die **FileIo \_ Name-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ Name-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Vollständiger Pfad zur Datei, ohne den Laufwerkbuchstaben.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Übereinstimmung mit dem Wert dieses Zeigers auf den **FileObject-Zeigerwert** in einem [**DiskIo \_ TypeGroup1-Ereignis,**](diskio-typegroup1.md) um den Typ des E/A-Vorgangs zu bestimmen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Windows Server 2003:** Um den Laufwerkbuchstaben für den Dateinamenpfad abzurufen, verwenden Sie den **FileObject-Eigenschaftswert,** um dem entsprechenden [DiskIo \_ TypeGroup1-Ereignis zu](diskio-typegroup1.md) zuordnen. Verwenden Sie aus dem DiskIo \_ TypeGroup1-Ereignis die **Eigenschaftswerte DiskNumber** und **ByteOffset,** um dem entsprechenden [SystemConfig \_ LogDisk-Ereignis](systemconfig-logdisk.md) **(ByteOffset** wird **StartOffset** zu zuordnen). Die **DriveLetterString-Eigenschaft** enthält den Laufwerkbuchstaben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




