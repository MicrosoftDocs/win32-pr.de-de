---
description: Diese Klasse ist die Ereignistyp Klasse für Datei-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: a25c96a8a3db11f577e7780d9f12448a8a0039dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977520"
---
# <a name="fileio_name-class"></a>\_Klasse "Klasse Name"

Diese Klasse ist die Ereignistyp Klasse für Datei-e/a-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die Klasse " **fleio \_ Name** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **fleio \_ Name** " verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Vollständiger Pfad zur Datei, ohne den Laufwerk Buchstaben.

</dd> <dt>

File Object
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis, um den Typ des e/a-Vorgangs zu bestimmen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Windows Server 2003:** Zum Abrufen des Laufwerk Buchstabens für den Dateinamen Pfad verwenden Sie den **FileObject** -Eigenschafts Wert, um dem entsprechenden [diskio \_ TypeGroup1](diskio-typegroup1.md) -Ereignis zuzuordnen. Verwenden Sie aus dem diskio \_ TypeGroup1-Ereignis **die disknumber** -und **Byteoffset** -Eigenschaftswerte, um das entsprechende [SystemConfig \_ logdisk](systemconfig-logdisk.md) -Ereignis zuzuordnen (**Byteoffset** wird **Startoffset** zugeordnet). Die " **driveletterstring** "-Eigenschaft enthält den Laufwerk Buchstaben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




