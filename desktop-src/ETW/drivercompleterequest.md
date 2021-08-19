---
description: Diese Klasse ist die Ereignistypklasse für Ereignisse zum Abschließen von Treiberanforderungen. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: DriverCompleteRequest-Klasse
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
ms.openlocfilehash: 2ef20d7bf097c35e03e94ee9bb80e7fd74ad93d3f28830c66b155b3cacf400b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151631"
---
# <a name="drivercompleterequest-class"></a>DriverCompleteRequest-Klasse

Diese Klasse ist die Ereignistypklasse für Ereignisse zum Abschließen von Treiberanforderungen.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **DriverCompleteRequest-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DriverCompleteRequest-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

E/A-Anforderungspaket.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Adresse der aufgerufenen Treiberfunktion.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Bezeichner, der die Anforderung eindeutig identifiziert. Verwenden Sie diesen Bezeichner, um mit den anderen Treiberereignissen zu korrelieren, z. B. dem [**DriverCompleteRequestReturn-Ereignis.**](drivercompleterequestreturn.md)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




