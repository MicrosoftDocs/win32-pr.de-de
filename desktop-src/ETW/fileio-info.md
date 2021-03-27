---
description: Diese Klasse ist die Ereignistyp Klasse für das Datei Informations Ereignis. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980369"
---
# <a name="fileio_info-class"></a>Klasse "fleio \_ Info"

Diese Klasse ist die Ereignistyp Klasse für das Datei Informations Ereignis.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a>Member

Die Klasse " **fleio \_ Info** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **fleio \_ Info** " verfügt über diese Eigenschaften.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), Zeiger
</dt> </dl>

Bei filedispositioninformation-Anforderungen enthält dieses Feld die angeforderte Disposition. Bei fileendoffileinformation-und filezugecationinformation-Anforderungen enthält dieses Feld die angegebene Dateigröße.

</dd> <dt>

**Filekey**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Zeiger
</dt> </dl>

Um den Dateinamen zu ermitteln, vergleichen Sie den Wert dieser Eigenschaft mit der **FileObject** -Eigenschaft eines [**FileIO- \_ namens**](fileio-name.md) Ereignisses.

</dd> <dt>

**File Object**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Zeiger
</dt> </dl>

Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.

</dd> <dt>

**Infoclass**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6)
</dt> </dl>

Die angeforderte Datei Informations Klasse.

</dd> <dt>

**Unpptr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

E/a-Anforderungspaket. Diese Eigenschaft identifiziert die e/a-Aktivität.

</dd> <dt>

**TTiD**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

Thread Bezeichner des Threads, der den Vorgang ausführt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Festlegen von Informationen und Abfrage Informations Ereignissen geben an, dass die Dateiattribute festgelegt oder abgefragt wurden. Wenn ein FSCTL-Befehl ausgegeben wird, wird ein Ereignis für die Dateisystem Steuerung (fscontrol) aufgezeichnet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




