---
description: Die pdhvbgetcounterpathelements-Funktion analysiert eine voll qualifizierte Zeichenfolge für den Leistungsindikator Pfad in die einzelnen Elemente.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Pdhvbgetcounterpathelements-Funktion
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
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368748"
---
# <a name="pdhvbgetcounterpathelements-function"></a>Pdhvbgetcounterpathelements-Funktion

Die **pdhvbgetcounterpathelements** -Funktion analysiert eine voll qualifizierte Zeichenfolge für den Leistungsindikator Pfad in die einzelnen Elemente. Jede der Zeichen folgen Variablen muss dieselbe Größe aufweisen (*bufferSize*) und dimensioniert und initialisiert werden, bevor Sie in dieser Funktion verwendet wird.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion pdhvbgetcounterpathelements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal instanceName As String, \_ ByVal Parameter instance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ )

## <a name="parameters"></a>Parameter

<dl> <dt>

*PathString* 
</dt> <dd>

Die Zeichenfolge für den Counter-Pfad, die in die einzelnen Elemente aufgeteilt werden soll.

</dd> <dt>

*MachineName* 
</dt> <dd>

Zeichenfolge, die den Computernamen empfängt.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Zeichenfolge, die den Objektnamen empfängt.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Zeichenfolge, die den Instanznamen empfängt, falls verwendet.

</dd> <dt>

*Parametriinstance* 
</dt> <dd>

Zeichenfolge, die die übergeordnete Instanz empfängt, sofern Sie verwendet wird.

</dd> <dt>

*CounterName* 
</dt> <dd>

Zeichenfolge, die den Namen des Zählers empfängt.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Maximale Größe der einzelnen Zeichen folgen Variablen, die als Parameter für diesen Funktions Aufrufsatz verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie eine **Long** -Ganzzahl zurück, die dem Fehler \_ Erfolg entspricht.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md). Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                     | Beschreibung                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ungültiges PDH- \_ \_ Argument**</dt> </dl>           | Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.<br/>                          |
| <dl> <dt>**PDH \_ Weitere \_ Daten**</dt> </dl>                  | Mindestens eines der Counter-Pfad Elemente ist zu groß für die Rückgabe Pufferlänge.<br/> |
| <dl> <dt>**PDH-Speicher Belegungs \_ \_ \_ Fehler**</dt> </dl> | Ein temporärer Speicherpuffer konnte nicht zugeordnet werden.<br/>                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**Pdhvbgetcounterpathfromlist**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**Pdhvbgetonecounterpath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

