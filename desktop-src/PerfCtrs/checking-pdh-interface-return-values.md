---
description: Der Rückgabewert von PDH-Funktionen gibt den Erfolg oder Misserfolg des Funktions Aufrufes an, der sich vom Status der Leistungsdaten unterscheidet.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Überprüfen der Status Codes der gegen Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7daed51ba6e8df385170b9a23b419267409ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348016"
---
# <a name="checking-counter-data-status-codes"></a>Überprüfen der Status Codes der gegen Daten

Der Rückgabewert von PDH-Funktionen gibt den Erfolg oder Misserfolg des Funktions Aufrufes an, der sich vom Status der Leistungsdaten unterscheidet. Überprüfen Sie immer den **cstatus** -Member eines in den PDH-Strukturen zurückgegebenen Leistungs Zählers, um sicherzustellen, dass die zurückgegebenen Daten gültig sind, bevor Sie Sie verwenden. Wenn der Wert des **cstatus** -Members nicht auf Erfolg hinweist, sollten Sie die Daten nicht verwenden. Im folgenden sind die möglichen Statuswerte für Leistungsindikatoren aufgeführt:



| Wert                              | Bedeutung                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ cstatus \_ kein \_ Computer          | PDH konnte keine Verbindung mit dem Computer herstellen, der im Counter-Pfad angegeben ist. Wenn dieser Status beim Hinzufügen des Zählers zurückgegeben wird, wird der-Counter nicht vollständig initialisiert. Jedes Mal, wenn die Abfrage aktualisiert wird, wiederholt PDH die Verbindung. Wenn die Verbindung hergestellt wird, wird die normale Datensammlung fortgesetzt.                                                                  |
| PDH \_ cstatus \_ No- \_ Objekt           | Der angegebene Computer wurde gefunden, aber das angegebene Leistungs Objekt wurde auf dem Computer gefunden. Wenn dieser Status beim Hinzufügen des Zählers zurückgegeben wird, ist der angegebene Counter nicht in der Abfrage enthalten. Wenn dieser Status von einem aktiven-Wert zurückgegeben wird, sind die Daten für diesen Wert ungültig. Jedes Mal, wenn die Daten angefordert werden, versucht PDH, diese Daten zu erhalten. |
| PDH \_ cstatus \_ keine \_ Instanz         | Die angegebene-Instanz wurde nicht im-Objekt gefunden. Wenn dieser Status zurückgegeben wird, während der-Wert der Abfrage hinzugefügt wird, wird der-Wert der Abfrage erfolgreich hinzugefügt. es sind jedoch keine Daten verfügbar, bis die jeweilige Instanz angezeigt wird und der Status erfolgreich zurückgegeben wurde.                                                                                                  |
| PDH \_ cstatus \_ kein \_ Counter          | Der angegebene Counter wurde im angegebenen Objekt nicht gefunden. Wenn dieser Status beim Hinzufügen des Zählers zurückgegeben wird, wird der-Wert nicht der Abfrage hinzugefügt. Wenn dieser Status nach der Datensammlung zurückgegeben wird, sind die Daten für diesen Wert ungültig. Jedes Mal, wenn die Daten angefordert werden, versucht PDH, diese Daten zu erhalten.                                             |
| PDH \_ cstatus \_ ungültige \_ Daten        | Der Gegenstand wurde gefunden, aber die zurückgegebenen Daten sind ungültig. Dieser Fehler kann auftreten, wenn der Wert des Leistungs Zählers kleiner als der vorherige Wert ist. (Da Leistungswerte immer erhöht werden, wird der Wert des Leistungs Zählers auf 0 (null) gesetzt, wenn er seinen maximalen Wert erreicht.) Eine weitere mögliche Ursache ist ein nicht korrekter System Zeitgeber.                                              |
| gültige PDH \_ cstatus- \_ \_ Daten          | Die Daten für den Gegenstand wurden erfolgreich zurückgegeben, Sie sind jedoch seit dem letzten Lesen des Zählers unverändert.                                                                                                                                                                                                                                                                    |
| PDH \_ cstatus \_ neue \_ Daten            | Die Daten für den Gegenstand wurden erfolgreich zurückgegeben und unterscheiden sich vom Zeitpunkt der letzten Lesevorgang. PDH \_ cstatus \_ neue \_ Daten können für einen Raten Zählers zurückgegeben werden, auch wenn die resultierende Rate mit dem letzten Beispiel übereinstimmt. Dies liegt daran, dass sich der Rohdatenwert, der bei der Ermittlung dieses Status Werts verwendet wird, geändert hat, nicht die berechnete Rate.                  |
| PDH \_ Weitere \_ Daten                    | Der angegebene Puffer war nicht groß genug, um alle gegen Daten zu speichern. Weisen Sie einen größeren Puffer zu, und führen Sie die Funktion erneut aus.                                                                                                                                                                                                                                              |
| PDH- \_ cstatus- \_ Element \_ nicht \_ überprüft | Der-Wert wurde der Abfrage hinzugefügt, wurde jedoch nicht überprüft, und es wurde nicht darauf zugegriffen. Es sind keine zusätzlichen Statusinformationen zu diesem Zählers verfügbar.                                                                                                                                                                                                                                 |
| PDH \_ cstatus \_ kein \_ counterName      | In der Abfrage wurde kein Name des Zählers angegeben.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ cstatus \_ kein \_ Counter          | Der angegebene Name des Zählers konnte nicht gefunden werden.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ cstatus \_ No- \_ Objekt           | Das angegebene Leistungs Objekt konnte nicht gefunden werden.                                                                                                                                                                                                                                                                                                                             |
| PDH \_ calc ( \_ negativer \_ Nenner)   | Ein Leistungs Bewert weist einen negativen nennenwert auf.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ Calc \_ negative \_ Timebase      | Ein Leistungs bemesser hat einen negativen Zeit Basis-Wert.                                                                                                                                                                                                                                                                                                                                         |
| negativer PDH \_ Calc- \_ \_ Wert         | Ein Leistungswert weist einen negativen Wert auf.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ cstatus \_ kein \_ counterName      | Es wurde kein Counter-Pfad angegeben.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ cstatus ungültiger \_ \_ counterName     | Das Format des Counter-path ist falsch.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



