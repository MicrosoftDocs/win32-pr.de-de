---
description: Die PdhVbAddCounter-Funktion erstellt einen Indikatoreintrag im angegebenen Abfrageobjekt und gibt nach erfolgreichem Abschluss ein Handle für diesen Indikator zurück.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6605e2fb02edad23831b22334b960eaa2e89f23206673608500f248452094ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061148"
---
# <a name="pdhvbaddcounter-function"></a>PdhVbAddCounter-Funktion

Die **PdhVbAddCounter-Funktion** erstellt einen Indikatoreintrag im angegebenen Abfrageobjekt und gibt nach erfolgreichem Abschluss ein Handle für diesen Indikator zurück.

> [!IMPORTANT]
> Die in diesem Thema beschriebene Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der in [Leistungsindikatorfunktionen beschriebenen](performance-counters-functions.md)Funktionen.

Funktion PdhVbAddCounter( \_ ByVal QueryHandle as Long, \_ ByVal CounterPath as String, \_ ByVal CounterHandle as Long \_ ) As Long

## <a name="parameters"></a>Parameter

<dl> <dt>

*QueryHandle* 
</dt> <dd>

ID der Abfrage, der dieser Leistungsindikator zugewiesen werden soll. Dieser Wert wird von der [**PdhVbOpenQuery-Funktion**](pdhvbopenquery.md) zurückgegeben.

</dd> <dt>

*CounterPath* 
</dt> <dd>

Textzeichenfolge, die den Namen des Indikatorpfads angibt, der der Abfrage hinzugefügt werden soll. Der Inhalt dieser Zeichenfolge muss ein gültiger Indikatorpfad sein, der aus dem Indikatorbrowser oder einer anderen Quelle abgerufen wird.

</dd> <dt>

*CounterHandle* 
</dt> <dd>

Eindeutiger Verweis, der diesen Leistungsindikator in der Abfrage identifiziert. Diese Variable muss mit 0 (null) initialisiert werden, bevor die Funktion aufgerufen wird. Sie enthält bei der Rückgabe nur dann einen gültigen Wert, wenn die Funktion erfolgreich abgeschlossen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie eine **Long-Ganzzahl** zurück, die error success \_ entspricht, und ein neues Handle in der *CounterHandle-Variablen.*

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehlercode](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode.](pdh-error-codes.md) Im Folgenden sind mögliche Werte angegeben.



| Rückgabecode                                                                                                     | Beschreibung                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_UNGÜLTIGES \_ PDH-ARGUMENT**</dt> </dl>           | Mindestens ein Argument ist ungültig oder falsch.<br/>              |
| <dl> <dt>**\_ \_ \_ PDH-SPEICHERBELEGUNGSFEHLER**</dt> </dl> | Ein Speicherpuffer konnte nicht zugeordnet werden.<br/>                            |
| <dl> <dt>**\_UNGÜLTIGES \_ PDH-HANDLE**</dt> </dl>             | Das Abfragehandle ist ungültig.<br/>                                     |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ COUNTER**</dt> </dl>        | Der angegebene Indikator wurde nicht gefunden.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ OBJECT**</dt> </dl>         | Das angegebene Objekt konnte nicht gefunden werden.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ MACHINE**</dt> </dl>        | Ein Computereintrag konnte nicht erstellt werden.<br/>                             |
| <dl> <dt>**PDH \_ CSTATUS \_ BAD \_ COUNTERNAME**</dt> </dl>   | Eine leere Pfadzeichenfolge für den Indikatornamen wurde übergeben.<br/>                   |
| <dl> <dt>**\_PDH-FUNKTION \_ NICHT \_ GEFUNDEN**</dt> </dl>        | Die Berechnungsfunktion für diesen Indikator konnte nicht bestimmt werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

