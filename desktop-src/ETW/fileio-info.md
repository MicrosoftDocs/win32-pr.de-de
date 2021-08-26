---
description: Diese Klasse ist die Ereignistypklasse für das Dateiinformationsereignis. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: 8a77d135fa5140f5d8d51a26164cd96009f06bacee654d13bec8dbaa9dcd76a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042000"
---
# <a name="fileio_info-class"></a>FileIo \_ Info-Klasse

Diese Klasse ist die Ereignistypklasse für das Dateiinformationsereignis.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **FileIo \_ Info-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ Info-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Zeiger
</dt> </dl>

Für FileDispositionInformation-Anforderungen enthält dieses Feld die angeforderte Disposition. Für FileEndOfFileInformation- und FileAllocationInformation-Anforderungen enthält dieses Feld die angegebene Dateigröße.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Zeiger
</dt> </dl>

Um den Dateinamen zu bestimmen, passen Sie den Wert dieser Eigenschaft mit der **FileObject-Eigenschaft** eines [**FileIo \_ Name-Ereignisses**](fileio-name.md) an.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Zeiger
</dt> </dl>

Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Dateiobjektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.

</dd> <dt>

**InfoClass**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

Angeforderte Dateiinformationsklasse.

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

**TTID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Threadbezeichner des Threads, der den Vorgang ausgeführt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ereignisse zum Festlegen von Informationen und Abfrageinformationen geben an, dass die Dateiattribute festgelegt oder abgefragt wurden. Ein Ereignis der Dateisystemsteuerung (FILE SYSTEM Control, FSControl) wird aufgezeichnet, wenn ein FSCTL-Befehl ausgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




