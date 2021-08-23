---
description: 'FileIo_V1_Name-Klasse: Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9a2488bb8f225df94e530e1964f0721c064c256423fe3218feb54adece7d0a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582400"
---
# <a name="fileio_v1_name-class"></a>FileIo \_ V1 \_ Name-Klasse

Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Member

Die **FileIo \_ V1 \_ Name-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ V1 \_ Name-Klasse** verfügt über diese Eigenschaften.

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

**Windows Server 2003:** Um den Laufwerkbuchstaben für den Dateinamenpfad abzurufen, verwenden Sie den **FileObject-Eigenschaftswert,** um dem entsprechenden [DiskIo \_ TypeGroup1-Ereignis](diskio-typegroup1.md) zuzuordnen. Verwenden Sie aus dem DiskIo \_ TypeGroup1-Ereignis die **Eigenschaftswerte DiskNumber** und **ByteOffset,** um dem entsprechenden [SystemConfig \_ LogDisk-Ereignis](systemconfig-logdisk.md) zuzuordnen (**ByteOffset** wird **StartOffset** zugeordnet). Die **DriveLetterString-Eigenschaft** enthält den Laufwerkbuchstaben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




