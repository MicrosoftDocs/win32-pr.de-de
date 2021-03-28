---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse des Haupt Funktions aufrufdes Treibers. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Drivermajorfunctioncallklasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977144"
---
# <a name="drivermajorfunctioncall-class"></a>Drivermajorfunctioncallklasse

Diese Klasse ist die Ereignistyp Klasse für Ereignisse des Haupt Funktions aufrufdes Treibers.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Member

Die **drivermajorfunctioncallklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **drivermajorfunctioncallklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**File Object**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Zeiger
</dt> </dl>

Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis, um den Typ des e/a-Vorgangs zu bestimmen.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), Zeiger
</dt> </dl>

E/a-Anforderungspaket.

</dd> <dt>

**Majorfunction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Code, der die Hauptfunktion identifiziert, die aufgerufen wird.

</dd> <dt>

**Minorfunction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Code, der die Nebenfunktion, die aufgerufen wird, identifiziert.

</dd> <dt>

**Routineaddr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Zeiger
</dt> </dl>

Adresse der aufgerufenen Treiber Funktion.

</dd> <dt>

**Uniqmatchid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6)
</dt> </dl>

Ein Bezeichner, der die Anforderung eindeutig identifiziert. Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequest**](drivercompleterequest.md) -Ereignis, zu korrelieren.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sowie**](diskio.md)
</dt> </dl>

 

 




