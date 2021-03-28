---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse, die vom Treiber erfüllt werden. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Drivercompleterequest-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977152"
---
# <a name="drivercompleterequest-class"></a>Drivercompleterequest-Klasse

Diese Klasse ist die Ereignistyp Klasse für Ereignisse, die vom Treiber erfüllt werden.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Member

Die Klasse " **drivercompleterequest** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **drivercompleterequest** " verfügt über diese Eigenschaften.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

E/a-Anforderungspaket.

</dd> <dt>

**Routineaddr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Adresse der aufgerufenen Treiber Funktion.

</dd> <dt>

**Uniqmatchid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Ein Bezeichner, der die Anforderung eindeutig identifiziert. Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequestreturn**](drivercompleterequestreturn.md) -Ereignis, zu korrelieren.

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

 

 




