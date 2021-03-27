---
description: Diese Klasse ist die Ereignistyp Klasse für Datei Vorgangs Ende-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758430"
---
# <a name="fileio_opend-class"></a>Fleio \_ opend-Klasse

Diese Klasse ist die Ereignistyp Klasse für Datei Vorgangs Ende-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die Klasse " **fleio \_ opend** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **fleio \_ opend** " verfügt über diese Eigenschaften.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

Zusätzliche Informationen, die vom Dateisystem für den Vorgang zurückgegeben werden. Beispielsweise eine Lese Anforderung, die tatsächliche Anzahl von gelesenen Bytes.

</dd> <dt>

**Unpptr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

E/a-Anforderungspaket. Diese Eigenschaft identifiziert die e/a-Aktivität, die beendet wird.

</dd> <dt>

**NTSTATUS**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Rückgabewert des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Am Anfang des Vorgangs werden die [**-Ereignisse des**](fileio.md) -Vorgangs protokolliert. Opend-Ereignisse können separat aktiviert werden, um das Ende dieser Vorgänge anzugeben. Mit "unp" können die BEGIN-und End-Ereignisse korreliert werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




