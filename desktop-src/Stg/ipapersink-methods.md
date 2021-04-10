---
title: Ipapersink-Methoden
description: Copaper macht die IConnectionPointContainer-Schnittstelle verfügbar, damit Clients eine Verbindung mit copaper herstellen können, um Benachrichtigungen über bestimmte Ereignisse zu empfangen, die in copaper auftreten.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8dee615b278c5214ad1efa3c10d22759620103
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209310"
---
# <a name="ipapersink-methods"></a>Ipapersink-Methoden

Copaper macht die [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle verfügbar, damit Clients eine Verbindung mit copaper herstellen können, um Benachrichtigungen über bestimmte Ereignisse zu empfangen, die in copaper auftreten. Wenn Sie diese Schnittstelle verfügbar machen, wird copaper zu einem Verbindungs fähigen Objekt. Ein Client kann [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für diese Schnittstelle aufzurufen und zum Abrufen der Verbindungspunkte des Objekts verwenden. Die Client Teilnahme an diesem Schema wird im zugehörigen **stoclien** -Beispiel behandelt.

Im Grunde implementiert der Client, was als Senke bezeichnet wird, in Form eines Sink-Objekts mit einer Sink-Schnittstelle. Die Senke-Schnittstelle empfängt ausgehende Ereignis Benachrichtigungs Aufrufe von copaper, nachdem die Senke ordnungsgemäß vom Client mit einer copaper-Instanz verbunden ist. Der Client stellt die Verbindung mithilfe eines Verbindungspunkt Objekts her, das von copaper verwaltet wird. Es können zahlreiche Verbindungspunkte auf einem einzelnen Verbindungs fähigen COM-Objekt vorhanden sein. Im **stoservice** -Beispiel verfügt copaper nur über einen Verbindungspunkt, der das Zeichnen von Papier Ereignissen behandelt.

Eine beliebige Anzahl von Clients kann eine Verbindung mit einem einzelnen Verbindungspunkt herstellen. Der \_ Verbindungspunkt für den Verbindungspunkt von Verbindungspunkt in copaper verwaltet eine Gruppe von Verbindungen, die zur Laufzeit dynamisch wachsen können. Die vollständigen Details zur Unterstützung von Verbindungs fähigen-Objekten in copaper sind in Dateien Connect programmiert. H und Connect. Cpp und wird hier nicht behandelt. Die Konstruktion ähnelt sehr der untersuchten Codebeispiele.

Der **stoclien** -Client implementiert geeignete Sink-Objekte für die Verbindungspunkte, die er in copaper finden soll. Im Zusammenhang mit copaper macht das von **stoclien** implementierte wichtige Sink-Objekt die **ipapersink** -Schnittstelle verfügbar. Dies ist die ausgehende Schnittstelle, die von copaper verwendet wird, um **stoclien** verschiedener Ereignisse in copaper zu benachrichtigen.

Im folgenden finden Sie eine Zusammenfassung der Methoden in **itaschen Sink** von iPaper. H im nicht gleich geordneten \\ Verzeichnis.



| Methode   | BESCHREIBUNG                                                   |
|----------|---------------------------------------------------------------|
| Gesperrt   | Ein Client hat das Papier übernommen und gesperrt.           |
| Sperre aufgehoben | Ein Client hat die Kontrolle über das Papier aufgegeben.               |
| Geladen   | Ein Client hat Papier Inhalt aus seiner eigenen Verbund Datei geladen. |
| Gespeichert    | Ein Client hat Papier Inhalt in seiner eigenen Verbund Datei gespeichert.    |
| Inkstart | Ein Client hat eine Color Ink-Zeichnungs Sequenz in das Papier gestartet.   |
| Inkdraw  | Ein Client legt frei Hand Datenpunkte auf der Papieroberfläche ab.     |
| Inkstopps  | Ein Client hat seine frei Hand Zeichnungs Sequenz in das Papier angehalten.   |
| Löschen   | Ein Client hat alle frei Hand Daten aus dem Papier gelöscht.              |
| Geändert  | Ein Client hat die Größe des Papiers geändert.                               |



 

Diese Methoden sind größtenteils selbsterklärend. Obwohl die Senke alle diese Methoden auf irgendeine Weise implementieren muss, werden viele als Stubs implementiert und nicht in den **stoservice**- / **stoclien** -Beispielen verwendet.

Eine wichtige Methode, die in diesen Beispielen verwendet wird, ist die geladene Methode. Wenn copaper vom Client darüber informiert wird, dass eine neue Zeichnung aus einer Datei geladen werden soll, muss der Client benachrichtigt werden, wenn die neuen Daten geladen werden. Zu diesem Zweck ruft copaper **itaschen Sink:: Loaded** in der Client Senke auf. Der Client kann dann [**iPaper:: Redraw**](ipaper--redraw.md) aufrufen, um anzufordern, dass copaper die neuen Daten an den Client zurückgibt. Redraw bewirkt, dass die geladene Zeichnung in der Anzeige des Clients neu gezeichnet wird. Wenn die Auslastung abgeschlossen ist, wird die neu geladene Zeichnung automatisch in dem vom Client bereitgestellten Fenster angezeigt.

Ausführliche Informationen über die Konnektivität dieser iPaper-Methode zu **itaschen Sink** finden Sie unter [**iPaper:: Redraw**](ipaper--redraw.md) .

Die **ipapersink** -Methoden **inkstart**, **inkdraw** und **inkstation** werden verwendet, um einzelne frei Hand Datenpakete an den Client zurückzusenden. Beim Empfang zeichnet der Client diese in der Anzeige auf die gleiche Weise wie bei der ursprünglichen Übermittlung an copaper. Die obige Logik ist allgemein genug, um für mehrere Clients zuzulassen, die alle an demselben Verbindungspunkt für den Verbindungspunkt von Verbindungs Punkten lauschen \_ . Wenn eine gemeinsame copaper-Instanz von diesen Clients gemeinsam genutzt wurde, können alle diese zeichnen, indem eine Verbindung mit diesem Verbindungspunkt hergestellt wird.

 

 