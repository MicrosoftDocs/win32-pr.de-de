---
description: Die Klasse "fleio \_ v0 \_ Name" ist eine ältere Version der Ereignistyp Klasse für Datei-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758425"
---
# <a name="fileio_v0_name-class"></a>Klasse "fleio \_ v0 \_ Name"

Die Klasse " **fleio \_ v0 \_ Name** " ist eine ältere Version der Ereignistyp Klasse für Datei-e/a-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die Klasse " **fleio \_ v0 \_ Name** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **fleio \_ v0 \_ Name** " verfügt über diese Eigenschaften.

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

**Windows Server 2003:** Zum Abrufen des Laufwerk Buchstabens für den Dateinamen Pfad verwenden Sie den **FileObject** -Eigenschafts Wert, um dem entsprechenden [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis zuzuordnen. Verwenden Sie aus dem **diskio \_ TypeGroup1** -Ereignis die **disknumber** -und **Byteoffset** -Eigenschaftswerte, um das entsprechende [**SystemConfig \_ logdisk**](systemconfig-logdisk.md) -Ereignis zuzuordnen. Die " **driveletterstring** "-Eigenschaft enthält den Laufwerk Buchstaben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"Fleio \_ v0"**](fileio-v0.md)
</dt> </dl>

 

 




