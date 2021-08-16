---
description: Diese Klasse ist die Ereignistypklasse für Hartseitenfehlerereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: PageFault_HardFault-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdabfab80eadc75fa05ffe148363a85cb5ddefad9abb626cfa4e1c3fa6fe2a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394613"
---
# <a name="pagefault_hardfault-class"></a>PageFault \_ HardFault-Klasse

Diese Klasse ist die Ereignistypklasse für Hartseitenfehlerereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a>Member

Die **PageFault \_ HardFault-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **PageFault \_ HardFault-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

Menge der aus ReadOffset gelesenen Daten, um den Fehler zu erfüllen.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Zeiger
</dt> </dl>

Übereinstimmung mit dem Wert dieses Zeigers mit dem **FileObject-Zeigerwert** in einem [**FileIo \_ Name-Ereignis,**](fileio-name.md) um den Namen der Datei zu bestimmen.

</dd> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Extension("WmiTime")
</dt> </dl>

Startzeitstempel, bei dem ein Seitenfehler aufgetreten ist.

</dd> <dt>

**ReadOffset**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Format("x")
</dt> </dl>

Dateioffset, aus dem Daten gelesen wurden, um den Fehler zu erfüllen.

</dd> <dt>

**TThreadId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Format("x")
</dt> </dl>

Threadbezeichner des Threads, der auf den Seitenfehler gestoßen ist.

</dd> <dt>

**VirtualAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Zeiger
</dt> </dl>

Fehleradresse.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




