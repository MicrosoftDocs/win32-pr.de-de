---
description: Die PdhVbGetCounterPathElements-Funktion analysiert eine vollqualifizierte Pfadzeichenfolge des Leistungsindikators in ihre einzelnen Elemente.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: fecd9ecac573ecc1a5afabcfc4a14bf6fd1ca5cee7b44387ea910b0cf1a5820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011328"
---
# <a name="pdhvbgetcounterpathelements-function"></a>PdhVbGetCounterPathElements-Funktion

Die **PdhVbGetCounterPathElements-Funktion** analysiert eine vollqualifizierte Pfadzeichenfolge des Leistungsindikators in ihre einzelnen Elemente. Jede der Zeichenfolgenvariablen muss die gleiche Größe (*BufferSize*) aufweisen und dimensioniert und initialisiert sein, bevor sie in dieser Funktion verwendet wird.

> [!IMPORTANT]
> Die funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der unter [Leistungsindikatorfunktionen beschriebenen Funktionen.](performance-counters-functions.md)

Funktion PdhVbGetCounterPathElements( \_ ByVal PathString as String, \_ ByVal MachineName as String, \_ ByVal ObjectName as String, \_ ByVal InstanceName as String, \_ ByVal ParentInstance as String, \_ ByVal CounterName as String, \_ ByVal BufferSize as long \_ ) so long

## <a name="parameters"></a>Parameter

<dl> <dt>

*PathString* 
</dt> <dd>

Zählerpfadzeichenfolge, die in die einzelnen Elemente zerbrochen werden soll.

</dd> <dt>

*MachineName* 
</dt> <dd>

Die Zeichenfolge, die den Computernamen empfangen soll.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Die Zeichenfolge, die den Objektnamen empfangen soll.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Zeichenfolge zum Empfangen des Instanznamens, sofern verwendet.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Zeichenfolge, die die übergeordnete Instanz empfangen soll, sofern verwendet.

</dd> <dt>

*Countername* 
</dt> <dd>

Die Zeichenfolge, die den Indikatornamen empfangen soll.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Maximale Größe jeder Zeichenfolgenvariablen, die als Parameter für diesen Funktionsaufruf verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird eine lange ganze **Zahl** zurückgegeben, die ERROR \_ SUCCESS entspricht.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehlercode oder](/windows/desktop/Debug/system-error-codes) [ein PDH-Fehlercode.](pdh-error-codes.md) Im Folgenden finden Sie mögliche Werte.



| Rückgabecode                                                                                                     | Beschreibung                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_PDH: UNGÜLTIGES \_ ARGUMENT**</dt> </dl>           | Mindestens einer der Zeichenfolgenpuffer ist nicht die richtige Größe.<br/>                          |
| <dl> <dt>**PDH \_ MORE \_ DATA**</dt> </dl>                  | Mindestens ein Indikatorpfad-Element ist zu groß für die Länge des Rückgabepuffers.<br/> |
| <dl> <dt>**\_ \_ PDH-SPEICHERBELEGUNGSFEHLER \_**</dt> </dl> | Ein temporärer Speicherpuffer konnte nicht zugeordnet werden.<br/>                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

