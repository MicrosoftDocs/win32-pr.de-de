---
description: Diese Klasse ist die Ereignistyp Klasse für einfache Datei Vorgangs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: FileIo_SimpleOp-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980361"
---
# <a name="fileio_simpleop-class"></a>Klasse "fleio \_ simpleop"

Diese Klasse ist die Ereignistyp Klasse für einfache Datei Vorgangs Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a>Member

Die Klasse " **fleio \_ simpleop** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **fleio \_ simpleop** " verfügt über diese Eigenschaften.

<dl> <dt>

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

Das Bereinigungs Ereignis wird protokolliert, wenn das letzte Handle der Datei geschlossen wird. Das Close-Ereignis gibt an, dass ein Datei Objekt freigegeben wird. Das Flush-Ereignis gibt an, wann die Datei Puffer vollständig auf den Datenträger geleert werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




