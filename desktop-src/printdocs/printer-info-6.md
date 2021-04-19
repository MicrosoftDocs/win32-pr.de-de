---
description: Die Drucker \_ Info \_ 6 gibt den Statuswert eines Druckers an.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: PRINTER_INFO_6 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360825"
---
# <a name="printer_info_6-structure"></a>Drucker \_ Info \_ 6-Struktur

Die **Drucker \_ Info \_ 6** gibt den Statuswert eines Druckers an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a>Member

<dl> <dt>

**dwStatus**
</dt> <dd>

Der Druckerstatus. Dieser Member kann eine beliebige Kombination der folgenden Werte sein.



| Wert                               | Bedeutung                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Drucker \_ Status \_ ausgelastet               | Der Drucker ist ausgelastet.                                                                                          |
| \_ \_ druckerstatustür \_ geöffnet         | Die Drucker Tür ist offen.                                                                                     |
| Drucker \_ Status \_ Fehler              | Nicht verwendet.                                                                                                     |
| Drucker \_ Status wird \_ initialisiert.       | Der Drucker wird zurzeit initialisiert.                                                                                  |
| Drucker Status-e/a \_ \_ \_ aktiv         | Der Drucker befindet sich in einem aktiven Eingabe-/ausgabezustand.                                                                |
| \_manueller Drucker Status- \_ \_ Feed       | Der Drucker befindet sich in einem manuellen Feed-Zustand.                                                                        |
| Drucker \_ Status \_ nicht \_ Toner          | Im Drucker ist kein Toner vorhanden.                                                                                  |
| Drucker \_ Status \_ nicht \_ verfügbar     | Der Drucker ist nicht zum Drucken verfügbar.                                                                    |
| Drucker \_ Status \_ Offline            | Der Drucker ist offline.                                                                                       |
| Drucker \_ Status \_ nicht genügend Arbeits \_ \_ Speicher    | Der Drucker verfügt nicht über genügend Arbeitsspeicher.                                                                            |
| Drucker \_ Status- \_ Ausgabe \_ bin \_ voll  | Das Ausgabefach des Druckers ist voll.                                                                             |
| Drucker \_ Status \_ Seite \_ Punt         | Der Drucker kann die aktuelle Seite nicht drucken.                                                                    |
| Drucker \_ Status \_ Papier \_ Stau         | Das Papier ist im Drucker gejammt.                                                                                |
| Drucker \_ Status \_ Papier \_ out         | Der Drucker ist nicht mehr im Papier.                                                                                  |
| Problem mit dem Drucker \_ Status \_ Papier \_     | Der Drucker hat ein Papier Problem.                                                                              |
| Drucker \_ Status \_ angehalten             | Der Drucker ist angehalten.                                                                                        |
| Drucker \_ Status \_ Ausstehend \_ gelöscht  | Der Drucker steht aufgrund eines Aufrufens der [**deleteprinter**](deleteprinter.md) -Funktion für das Löschen aus. |
| Drucker \_ Status- \_ Energie \_ Spar Speicher        | Der Drucker befindet sich im Energiesparmodus.                                                                            |
| Drucker \_ Status \_ Drucken           | Der Drucker wird gedruckt.                                                                                      |
| Drucker \_ Status \_ Verarbeitung         | Der Drucker verarbeitet einen Befehl aus der Funktion " [**SetPrinter**](setprinter.md) ".                       |
| Drucker \_ Status \_ Server \_ unbekannt    | Der Druckerstatus ist unbekannt.                                                                                |
| Drucker \_ Status- \_ Toner \_ niedrig         | Der Drucker ist niedrig auf dem Toner.                                                                                  |
| Drucker \_ Status \_ Benutzer \_ Eingriff | Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer eine Aktion durchführen kann.                                              |
| Drucker \_ Status \_ wartet            | Der Drucker wartet.                                                                                       |
| Drucker \_ Status \_ \_ Aufwärmphase        | Der Drucker befindet sich in der Aufwärmphase.                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Info \_ 6W** (Unicode) und **\_ Drucker \_ Info \_ 6a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




