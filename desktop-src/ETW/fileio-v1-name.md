---
description: 'FileIo_V1_Name Klasse: Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: 62069f8a462499dfbfd9cfa368b9f5985d4775e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106548"
---
# <a name="fileio_v1_name-class"></a>FileIo \_ V1 \_ Name-Klasse

Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

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

Die **FileIo \_ V1 \_ Name-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ V1 \_ Name-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

## <a name="remarks"></a>Bemerkungen

**Windows Server 2003:** Um den Laufwerkbuchstaben für den Dateinamenpfad abzurufen, verwenden Sie den **FileObject-Eigenschaftswert,** um dem entsprechenden [DiskIo \_ TypeGroup1-Ereignis zu](diskio-typegroup1.md) zuordnen. Verwenden Sie aus dem DiskIo \_ TypeGroup1-Ereignis die **Eigenschaftswerte DiskNumber** und **ByteOffset,** um dem entsprechenden [SystemConfig \_ LogDisk-Ereignis](systemconfig-logdisk.md) **(ByteOffset** wird **StartOffset** zu zuordnen). Die **DriveLetterString-Eigenschaft** enthält den Laufwerkbuchstaben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




