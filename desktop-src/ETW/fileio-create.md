---
description: Diese Klasse ist die Ereignistypklasse für das Dateierstellungsereignis. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e0c4085225fe523dcabca87a15bced8bd1f093f0b3da89fa0582b5675cdfbbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829950"
---
# <a name="fileio_create-class"></a>FileIo \_ Create-Klasse

Diese Klasse ist die Ereignistypklasse für das Dateierstellungsereignis.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a>Member

Die **FileIo \_ Create-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ Create-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Createoptions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Werte, die in den *Parametern CreateOptions* und *CreateDispositions* an die [**NtCreateFile-Funktion**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) übergeben werden.

</dd> <dt>

**FileAttributes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Wert, der im *FileAttributes-Parameter* an die [**NtCreateFile-Funktion**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) übergeben wird.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Zeiger
</dt> </dl>

Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Dateiobjektinstanz zwischen Dateierstellungs- und Schließereignissen verwendet werden kann.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

E/A-Anforderungspaket. Diese Eigenschaft identifiziert die E/A-Aktivität.

</dd> <dt>

**OpenPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Pfad zur Datei.

</dd> <dt>

**ShareAccess**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

Wert, der im *ShareAccess-Parameter* an die [**NtCreateFile-Funktion**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) übergeben wird.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Threadbezeichner des Threads, der die Datei erstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 
