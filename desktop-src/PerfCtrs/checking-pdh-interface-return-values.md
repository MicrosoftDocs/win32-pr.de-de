---
description: Der Rückgabewert von PDH-Funktionen gibt den Erfolg oder Fehler des Funktionsaufrufs an, der sich vom Status der Indikatordaten unterscheidet.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Überprüfen von Statuscodes für Indikatordaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c433e1c45badd3a2211a0e53051ad40d495f63a67b0ca509ae74a5cd99972
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978880"
---
# <a name="checking-counter-data-status-codes"></a>Überprüfen von Statuscodes für Indikatordaten

Der Rückgabewert von PDH-Funktionen gibt den Erfolg oder Fehler des Funktionsaufrufs an, der sich vom Status der Indikatordaten unterscheidet. Überprüfen Sie immer den **CStatus-Member** eines Indikatorwerts, der in den PDH-Strukturen zurückgegeben wird, um sicherzustellen, dass die zurückgegebenen Daten gültig sind, bevor Sie ihn verwenden. Wenn der Wert des **CStatus-Members** keinen Erfolg angibt, verwenden Sie die Daten nicht. Im Folgenden sind die möglichen Statuswerte für Leistungsindikatoren angegeben:



| Wert                              | Bedeutung                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ NO \_ MACHINE          | PDH konnte keine Verbindung mit dem im Indikatorpfad angegebenen Computer herstellen. Wenn dieser Status beim Hinzufügen des Zählers zurückgegeben wird, wird der Zähler nicht vollständig initialisiert. Bei jeder Aktualisierung der Abfrage wird die Verbindung von PDH erneut hergestellt. Wenn die Verbindung hergestellt wird, wird die normale Datensammlung fortgesetzt.                                                                  |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | Der angegebene Computer wurde gefunden, aber das angegebene Leistungsobjekt wurde auf dem Computer gefunden. Wenn dieser Status beim Hinzufügen des Leistungsindikators zurückgegeben wird, wird der angegebene Zähler nicht in die Abfrage eingeschlossen. Wenn dieser Status von einem aktiven Zähler zurückgegeben wird, sind die Daten für diesen Leistungsindikator ungültig. Jedes Mal, wenn die Daten angefordert werden, versucht PDH, diese Indikatordaten abzurufen. |
| PDH \_ CSTATUS \_ NO \_ INSTANCE         | Die angegebene Instanz wurde im -Objekt nicht gefunden. Wenn dieser Status zurückgegeben wird, während der Zähler der Abfrage hinzugefügt wird, wird der Zähler der Abfrage erfolgreich hinzugefügt, aber es sind keine Daten verfügbar, bis die bestimmte Instanz angezeigt wird und ein erfolgreicher Status zurückgegeben wird.                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | Der angegebene Leistungsindikator wurde im angegebenen -Objekt nicht gefunden. Wenn dieser Status beim Hinzufügen des Zählers zurückgegeben wird, wird der Zähler der Abfrage nicht hinzugefügt. Wenn dieser Status nach der Datensammlung zurückgegeben wird, sind die Daten für diesen Leistungsindikator ungültig. Jedes Mal, wenn die Daten angefordert werden, versucht PDH, diese Indikatordaten abzurufen.                                             |
| PDH \_ CSTATUS \_ INVALID \_ DATA        | Der Leistungsindikator wurde erfolgreich gefunden, aber die zurückgegebenen Daten sind ungültig. Dieser Fehler kann auftreten, wenn der Zählerwert kleiner als der vorherige Wert ist. (Da Zählerwerte immer inkrementiert werden, wird für den Zählerwert ein Rollback auf 0 (null) angezeigt, wenn der Maximalwert erreicht wird.) Eine weitere mögliche Ursache ist ein nicht korrekter Systemtimer.                                              |
| PDH \_ CSTATUS \_ VALID \_ DATA          | Die Daten für den Leistungsindikator wurden erfolgreich zurückgegeben, sind jedoch seit dem letzten Lesen des Zählers unverändert.                                                                                                                                                                                                                                                                    |
| PDH \_ CSTATUS \_ NEW \_ DATA            | Die Daten für den Leistungsindikator wurden erfolgreich zurückgegeben und unterscheiden sich vom letzten Lesen des Leistungsindikators. PDH \_ CSTATUS \_ NEW DATA kann für \_ einen Ratenzähler auch dann zurückgegeben werden, wenn die resultierende Rate mit der des letzten Beispiels identisch ist. Dies liegt daran, dass sich der Rohdatenwert, der bei der Ermittlung dieses Statuswerts verwendet wird, geändert hat, nicht die berechnete Rate.                  |
| PDH \_ MORE \_ DATA                    | Der bereitgestellte Puffer war nicht groß genug, um alle Indikatordaten zu speichern. Ordnen Sie einen größeren Puffer zu, und führen Sie die Funktion erneut aus.                                                                                                                                                                                                                                              |
| \_PDH-CSTATUS-ELEMENT \_ \_ NICHT \_ ÜBERPRÜFT | Der Leistungsindikator wurde der Abfrage hinzugefügt, aber weder überprüft noch darauf zugegriffen. Es sind keine zusätzlichen Statusinformationen zu diesem Leistungsindikator verfügbar.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | In der Abfrage wurde kein Indikatorname angegeben.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | Der angegebene Indikatorname wurde nicht gefunden.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | Das angegebene Leistungsobjekt wurde nicht gefunden.                                                                                                                                                                                                                                                                                                                             |
| \_PDH-CALC \_ \_ NEGATIVER NENNER   | Ein Zähler weist einen negativen Nennerwert auf.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CALC \_ NEGATIVE \_ TIMEBASE      | Ein Zähler weist einen negativen Zeitbasiswert auf.                                                                                                                                                                                                                                                                                                                                         |
| NEGATIVER \_ PDH-CALC-WERT \_ \_         | Ein Zähler hat einen negativen Wert.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | Es wurde kein Indikatorpfad angegeben.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ BAD \_ COUNTERNAME     | Das Format des Indikatorpfads ist falsch.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



