---
description: Diese Klasse ist die Ereignistypklasse für Ereignisse zur Anforderungsrückgabe vom Typ "Driver Complete". Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: DriverCompleteRequestReturn-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: be19cd1a4b8f7cf4957d08f9ccebf01c5e8646ade06cce9708e645c1a7ea2a5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901210"
---
# <a name="drivercompleterequestreturn-class"></a>DriverCompleteRequestReturn-Klasse

Diese Klasse ist die Ereignistypklasse für Ereignisse zur Anforderungsrückgabe vom Typ "Driver Complete".

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Member

Die **DriverCompleteRequestReturn-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DriverCompleteRequestReturn-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

E/A-Anforderungspaket.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Bezeichner, der die Anforderung eindeutig identifiziert. Verwenden Sie diesen Bezeichner, um mit den anderen Treiberereignissen zu korrelieren, z. B. dem [**DriverCompleteRequest-Ereignis.**](drivercompleterequest.md)

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

 

 




