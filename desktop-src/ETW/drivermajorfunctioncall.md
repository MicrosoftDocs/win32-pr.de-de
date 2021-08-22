---
description: Diese Klasse ist die Ereignistypklasse für Treiber-Hauptfunktionsaufrufereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: DriverMajorFunctionCall-Klasse
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
ms.openlocfilehash: b69012ae3d9dd46d2dd54c3859895288b9113fa89c772172e3f66a730b058d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070240"
---
# <a name="drivermajorfunctioncall-class"></a>DriverMajorFunctionCall-Klasse

Diese Klasse ist die Ereignistypklasse für Treiber-Hauptfunktionsaufrufereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **DriverMajorFunctionCall-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DriverMajorFunctionCall-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Zeiger
</dt> </dl>

Stimmen Sie den Wert dieses Zeigers mit dem **FileObject-Zeigerwert** in einem [**DiskIo \_ TypeGroup1-Ereignis**](diskio-typegroup1.md) ab, um den Typ des E/A-Vorgangs zu bestimmen.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Zeiger
</dt> </dl>

E/A-Anforderungspaket.

</dd> <dt>

**MajorFunction**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Code, der die aufgerufene Hauptfunktion identifiziert.

</dd> <dt>

**MinorFunction**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Code, der die aufgerufene Nebenfunktion initialisiert.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Zeiger
</dt> </dl>

Adresse der aufgerufenen Treiberfunktion.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
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

 

 




