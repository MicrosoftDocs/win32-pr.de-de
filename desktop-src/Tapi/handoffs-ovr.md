---
description: Wenn eine Anwendung Besitzer Berechtigungen für eine Kommunikationssitzung hat, kann die Anwendung den Besitz an eine andere Anwendung übergeben.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Handoffs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343815e35f1fc331c57c4aa2d9d311697cab7022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345793"
---
# <a name="handoffs"></a>Handoffs

Wenn eine Anwendung Besitzer [Berechtigungen](privilege-ovr.md) für eine Kommunikationssitzung hat, kann die Anwendung den Besitz an eine andere Anwendung übergeben. Der Übergabe-Vorgang wird normalerweise verwendet, um zuzulassen, dass der Medientyp des Aufrufes geändert wird. Die Anwendung mit der höchsten Priorität für den neuen Medientyp sollte den-Befehl übernehmen und verarbeiten. Der Medientyp wird in der Regel aus einem der folgenden Gründe geändert.

**Benutzer Befehl:** Über eine Benutzeroberfläche oder über Fenster Meldungen erfährt die Anwendung, dass der lokale Benutzer den Medientyp ändern möchte. Der Benutzer hat z. b. die neue Zielanwendung (die noch nicht Besitzer ist) aufgefordert, einen vorhandenen Sprachanruf zum Übertragen von Daten zu erhalten. Die Zielanwendung muss nun die Kontrolle über den-Befehl übernehmen. In diesem Fall bemerkt der aktuelle Besitzer, dass die Anzahl der Besitzer zunimmt, und gibt dann seine Kontrolle über den-Befehl aus. Alternativ könnte der Benutzer den aktuellen Besitzer des Aufrufes anweisen, ihn an eine Anwendung zu übergeben, die den neuen Medientyp verarbeiten kann.

**Medientyp Änderung:** Der Dienstanbieter kann eine Änderung des Medientyps erkennen. Beispielsweise gibt die lokale Anwendung eine aufgezeichnete Sprachnachricht an den Aufrufer aus. Während dieser Nachricht beschließt der Aufrufer spontan, einen Faxanruf zu übertragen, und die lokale Anwendung kann entsprechend reagieren, indem der Medientyp in Fax geändert und ggf. der Aufruf an eine Faxanwendung übergeben wird. Eine andere Möglichkeit besteht darin, dass eine Überwachungsanwendung die Medientyp Überwachung aktiviert, und wenn der Medientyp, in dem Sie interessiert ist, bei einem-Rückruf erkannt wird, kann er den Besitz des Aufrufes anfordern. Mit diesem Mechanismus ist es für jede Anwendung unnötig, jeden beliebigen einzelnen Anrufe für jeden Medientyp zu überwachen.

**Remote Partei Befehl:** Die Remote Partei kann während eines vorhandenen Aufrufers interaktiv eine Änderung der Medientypen angeben, z. b. wenn die lokale Anwendung die DTMF-Eingabe vom Remote Aufrufer überwacht. Durch diese Überwachung gibt der Aufrufer beispielsweise an, dass ein Fax gesendet werden soll. Andere Möglichkeiten, wie der Aufrufer lokale Anwendungen steuern kann, sind Befehle, die auf anderen Datenverbindungen und über die ISDN-Benutzer-/benutzerinformationsnachrichten

Eine Telefon Übergabe hat eines der folgenden Ergebnisse:

-   Der-Rückruf wird an eine andere Anwendung übergeben (Erfolg).
-   Die Übergabe Anwendung ist selbst das Ziel (targetSelf).
-   Die Übergabe schlägt fehl (targetnotfound).

Wenn die Anwendung, die den übergebenen-Befehl empfängt, bereits über ein Telefon Handle für den-Befehl verfügt, wird dieses alte-Rückruf Handle verwendet. Andernfalls wird ein neues-Rückruf Handle erstellt. In beiden Fällen erhält die Anwendung Besitzer Berechtigungen für den-Befehl. Wenn die ausgabdeanwendung nicht mit der Zielanwendung identisch ist, wird das Ziel über die Übergabe in einer Sitzungs Zustands Meldung informiert, als ob ein neuer Aufruf empfangen würde.

Wenn die aktuelle Besitzer Anwendung angewiesen wird, die Medientypen zu ändern, erfolgt dies durch das Übergeben des Aufrufes einer Anwendung, die für den Ziel Medientyp verwendet wird. Die zwei Arten von-aufrufungshandeilen werden in [gerichteten Hand](#directed-handoffs) eilen und [Medientyp Handoffs](#media-type-handoffs)beschrieben.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linehandoff**](/windows/win32/api/tapi/nf-tapi-linehandoff), wobei *lpszfilename* auf den Anwendungsnamen für eine direkte Übergabe oder *dwmediamode* auf einen Medientyp für eine indirekte Übergabe festgelegt ist.

**TAPI 3. x:** Siehe [**itbasiccallcontrol:: handoffdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**itbasiccallcontrol:: handoffindirekte**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Gerichtete Handgriffe

Eine *gesteuerte Übergabe* erfolgt, wenn die Zielanwendung nach dem Namen der ursprünglichen Anwendung bekannt ist. Diese Situation tritt beispielsweise bei einem Satz von Anwendungen auf, die vom gleichen Hersteller geschrieben wurden. Der Benutzer kann die Steuerung von gerichteten Hand eilen in der Regel konfigurieren. Bei dieser Übergabe wird der-Befehl an die angegebene Anwendung übergeben, wenn Sie die Zeile geöffnet hat, in der der-Rückruf vorhanden ist. Der Medientyp, der zum Zeitpunkt des Öffnens der Anwendung in der Zeile angegeben wurde, wird ignoriert. Ein gängiges Beispiel ist ein Sprachanruf, gefolgt von einer Faxübertragung im gleichen Anruf. Die gesteuerte Übergabe wird am häufigsten von Anwendungen desselben Entwicklers verwendet, die auch auf andere Weise miteinander verknüpft sind.

Die gesteuerte Übergabe kann auch in zukünftigen Versionen verwendet werden, um mehrere Anwendungen zu übernehmen, die auf eingehende Aufrufe desselben Medientyps warten, wobei die Anwendung zur Behandlung des Aufrufs verwendet wird, der auf der Protokoll Erkennung auf Daten oder einer höheren Ebene statt auf dem Medientyp basiert. Ein Beispiel für seine Verwendung wäre eine eingehende Datenmodem Linie mit Anwendungen wie der Remote Übernahme, dem Bulletin Board, dem Remote Netzwerk Zugriff und dem Remote-e-Mail-Zugriff, die alle auf Aufrufe gleichzeitig warten.

## <a name="media-type-handoffs"></a>Medientyp Handler

Eine *Medientyp Übergabe* findet statt, wenn ein neuer, gezielter Medientyp vorhanden ist, in der Regel, wenn die besitzende Anwendung ermittelt, dass der für den-Befehl benötigte Medientyp nicht vorhanden ist oder gerade geändert wird.

Der Prozess für eine Medien abhängige Übergabe kann ein Überprüfungsprozess sein, wenn der Medientyp unbekanntes Bit auf on ist. Es liegt in der Verantwortung der besitzenden Anwendung, die Medientypen zu durchlaufen, um die Anwendung mit der höchsten Priorität zu suchen. TAPI führt dies nur für den ersten eingehenden Rückruf aus, um den ersten Besitzer zu suchen. Dies erfolgt nicht bei einem Übergabe-Vorgang. Andernfalls ist eine Übergabe praktisch identisch mit der anfänglichen Zuweisung eines Aufrufes für eine Anwendung. Der Unterschied besteht darin, dass nur ein Medientyp für einen indirekten (Medientyp) Handoff festgelegt werden kann.

Da nur ein einzelnes Medientyp angegeben werden kann, wird der-Befehl der Anwendung mit der höchsten Priorität für den Medientyp zugewiesen. Es ist jedoch möglich, dass mehr als ein Medientyp für die Übergabe berücksichtigt wird. In diesem Fall sollte die aushandende Anwendung die höchste Priorität der möglichen Medientypen als Parameter angeben.

Wenn eine Anwendung das unbekannte Bit beim Ausführen eines Medientyp Übergabe angibt und die Übergabe fehlschlägt, bedeutet dies, dass eine unbekannte Anwendung, die eine Medientyp Bestimmung ausführen kann, zurzeit nicht ausgeführt wird. Die Anwendung, die die Übergabe durchläuft, sollte dann versuchen, den-Rückruf an die Anwendung mit der höchsten Priorität zu übergeben, die für den nächsten Medientyp registriert ist.

Die empfangende Anwendung ist nun für den-Befehl verantwortlich. Er prüft jetzt den tatsächlichen Medientyp des Aufrufes. Wenn die Anwendung den Medientyp des Aufrufes verarbeiten kann, muss sichergestellt werden, dass es sich um die Anwendung mit der höchsten Priorität handelt, die für diesen Medientyp registriert ist. Wenn dies der Fall ist, wird der-Rückruf beibehalten und normal verarbeitet. Wenn dies nicht der Fall ist, wird der Aufrufvorgang an eine andere Anwendung, die für diesen Medientyp registriert ist

Wenn der Test für diesen Medientyp jedoch fehlschlägt, führt die Anwendung erneut eine Überprüfung durch, und es wird versucht, die verbleibenden Möglichkeiten im Medien Modus auszuführen. Zuerst muss das aktuelle Medientyp Bit ausgeschaltet werden, und anschließend wird ein anderer Handler mit einem anderen Typ ausprobiert.

Dieser Prozess der Überprüfung und Übergabe wird fortgesetzt, und die verbleibenden Medientypen werden nacheinander entfernt. Auf diese Weise kann eine der Anwendungen sehen, dass der Medientyp, den er verarbeitet, den-Befehl aufruft und die Übergabe erfolgreich ist.

Die Anwendung sollte dann den richtigen Medientyp festlegen und alle anderen Medientyp Bits löschen. Dadurch werden andere interessierte Anwendungen über den richtigen Medientyp informiert. Diese anderen Anwendungen erhalten eine Ereignis Benachrichtigungs Meldung, die besagt, dass der Medientyp des Aufrufes geändert hat.

 

 
