---
description: Diese Klasse ist die Ereignistypklasse für Dateivorgang-Endereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: 74042df74f8e128c4d92b6e4f1c886a7bba2f673c1a8a998a4b7f251475c3f93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130590"
---
# <a name="fileio_opend-class"></a>FileIo \_ OpEnd-Klasse

Diese Klasse ist die Ereignistypklasse für Dateivorgang-Endereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>Member

Die **FileIo \_ OpEnd-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **FileIo \_ OpEnd-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Zusätzliche Informationen, die vom Dateisystem für den Vorgang zurückgegeben werden. Beispiel für eine Leseanforderung: die tatsächliche Anzahl der gelesenen Bytes.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

E/A-Anforderungspaket. Diese Eigenschaft identifiziert die E/A-Aktivität, die beendet wird.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Gibt den Wert aus dem Vorgang zurück.

</dd> </dl>

## <a name="remarks"></a>Hinweise

[**FileIo-Ereignisse**](fileio.md) werden zu Beginn des Vorgangs protokolliert. OpEnd-Ereignisse können separat aktiviert werden, um das Ende dieser Vorgänge anzugeben. Irp kann verwendet werden, um die Anfangs- und Endereignisse zu korrelieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




