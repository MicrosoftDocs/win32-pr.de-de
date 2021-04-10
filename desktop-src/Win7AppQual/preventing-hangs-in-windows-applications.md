---
description: Erfahren Sie, wie Sie Abstürze in Windows-Anwendungen für Windows 7-und Windows Server 2008 R2-Plattformen vermeiden.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Verhindern von Blockaden in Windows-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a2d8fac95039f20c8c684c50138933c54750c3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104050656"
---
# <a name="preventing-hangs-in-windows-applications"></a>Verhindern von Blockaden in Windows-Anwendungen

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="description"></a>BESCHREIBUNG

**Nicht mehr Benutzer Perspektive**

Benutzer wie reaktionsfähige Anwendungen. Wenn Sie auf ein Menü klicken, soll die Anwendung sofort reagieren, auch wenn Sie gerade Ihre Arbeit druckt. Wenn Sie ein langes Dokument in Ihrem bevorzugten Textprozessor speichern, möchten Sie die Eingabe fortsetzen, während der Datenträger immer noch spinnt. Wenn die Anwendung nicht rechtzeitig auf Ihre Eingaben reagiert, treten die Benutzer ungeduldig auf.

Ein Programmierer könnte viele legitime Gründe erkennen, wenn eine Anwendung nicht sofort auf Benutzereingaben reagiert. Die Anwendung ist möglicherweise ausgelastet, um einige Daten neu zu berechnen oder einfach darauf zu warten, dass die Datenträger-e/a vollständig ist. Aus der Benutzer Recherche wissen wir jedoch, dass Benutzer nach wenigen Sekunden nicht mehr Reaktionsfähigkeit verärgert sind und frustriert werden. Nach 5 Sekunden versuchen Sie, eine nicht reagierende Anwendung zu beenden. Neben abstürzen sind Anwendungs Abstürze bei der Arbeit mit Win32-Anwendungen die häufigste Quelle für die Benutzer Unterbrechung.

Es gibt viele verschiedene Hauptursachen für Anwendungs Abstürze, nicht alle, die sich in einer nicht reagierenden Benutzeroberfläche selbst manifestieren. Eine nicht reagierende Benutzeroberfläche ist jedoch eine der gängigsten Abstürze, und dieses Szenario erhält derzeit die meisten Betriebssystemunterstützung sowohl für die Erkennung als auch für die Wiederherstellung. Windows erkennt automatisch Debuginformationen, sammelt Sie und beendet oder startet nicht reagierende Anwendungen. Andernfalls muss der Benutzer den Computer möglicherweise neu starten, um eine nicht reagierende Anwendung wiederherzustellen.

**Abstürze: Betriebs System Perspektive**

Wenn eine Anwendung (oder genauer, ein Thread) ein Fenster auf dem Desktop erstellt, wechselt Sie in einen impliziten Vertrag mit dem Desktopfenster-Manager (DWM), um Fenster Meldungen rechtzeitig zu verarbeiten. Der DWM stellt Nachrichten (Tastatur-/Maus-Eingaben und Meldungen von anderen Fenstern sowie selbst) in die Thread spezifische Nachrichten Warteschlange. Der Thread ruft diese Nachrichten über die Nachrichten Warteschlange ab und sendet Sie. Wenn der Thread die Warteschlange nicht durch den Aufruf von getMessage () verarbeitet, werden die Nachrichten nicht verarbeitet, und das Fenster hängt nicht aus: die Warteschlange kann nicht neu gezeichnet werden, und es kann keine Eingabe vom Benutzer akzeptiert werden. Das Betriebssystem erkennt diesen Zustand durch Anfügen eines Timers an ausstehende Nachrichten in der Nachrichten Warteschlange. Wenn eine Nachricht nicht innerhalb von 5 Sekunden abgerufen wurde, deklariert die DWM das Fenster, das nicht mehr reagiert. Sie können diesen speziellen Fenster Zustand über die ishungappwindow ()-API Abfragen.

Die Erkennung ist nur der erste Schritt. An diesem Punkt kann der Benutzer die Anwendung immer noch nicht beenden. Wenn Sie auf die Schaltfläche "X (schließen)" klicken, wird eine "WM Close"- \_ Meldung angezeigt, die genau wie jede andere Nachricht in der Nachrichten Warteschlange hängen bleibt. Der Desktopfenster-Manager unterstützt durch das nahtlose ausblenden und anschließende ersetzen des angehängten Fensters durch eine "inaktive" Kopie, die eine Bitmap des vorherigen Client Bereichs des ursprünglichen Fensters anzeigt (und das Hinzufügen von "antwortet nicht" zur Titelleiste). Solange der Thread des ursprünglichen Fensters keine Nachrichten abruft, verwaltet der DWM beide Fenster gleichzeitig, ermöglicht aber nur die Interaktion mit der inaktiven Kopie. Mithilfe dieses inaktiven Fensters kann der Benutzer die nicht reagierende Anwendung nur verschieben, minimieren und am wichtigsten schließen, aber seinen internen Zustand nicht ändern.

Die gesamte Ghost-Darstellung sieht wie folgt aus:

![Screenshot, der das Dialogfeld "Notepad antwortet nicht" anzeigt](images/preventinghangs-ghostwindow.gif)

Der Desktopfenster-Manager führt ein letztes Ergebnis aus. Sie wird in Windows-Fehlerberichterstattung integriert, sodass der Benutzer die Anwendung nicht nur schließen und optional neu starten kann, sondern auch wertvolle Debugdaten an Microsoft senden kann. Sie können diese systemstillstanddaten für Ihre eigenen Anwendungen erhalten, indem Sie sich auf der winqual-Website anmelden.

Windows 7 hat diesem Vorgang ein neues Feature hinzugefügt. Das Betriebssystem analysiert die nicht reagierende Anwendung und erteilt dem Benutzer unter bestimmten Umständen die Möglichkeit, einen blockierenden Vorgang abzubrechen und die Anwendung wieder in Reaktion zu nehmen. Die aktuelle Implementierung unterstützt den Abbruch von blockierenden socketaufrufen. weitere Vorgänge werden in zukünftigen Versionen vom Benutzer abgebrochen.

Führen Sie die folgenden Schritte aus, um Ihre Anwendung in die Benutzeroberflächen-Wiederherstellung zu integrieren und die verfügbaren Daten optimal zu nutzen:

-   Stellen Sie sicher, dass Ihre Anwendung für Neustart und Wiederherstellung registriert wird, sodass Sie für den Benutzer so einfach wie möglich ist. Eine ordnungsgemäß registrierte Anwendung kann automatisch neu gestartet werden, wenn die meisten nicht gespeicherten Daten intakt sind. Dies funktioniert sowohl für den Anwendungs Absturz als auch für Abstürze.
-   Erhalten Sie Informationen zu Häufigkeit und zum Debuggen von Daten für Ihre nicht abgestürzten und abgestürzten Anwendungen von der winqual-Website. Diese Informationen können auch während der Beta Version verwendet werden, um Ihren Code zu verbessern. Eine kurze Übersicht finden Sie unter "Einführung in Windows-Fehlerberichterstattung".
-   Sie können das Ghosting-Feature in der Anwendung mithilfe eines Aufrufens von disableprocesswindowsghosting () deaktivieren. Dadurch wird jedoch verhindert, dass der durchschnittliche Benutzer eine nicht reagierende Anwendung schließt und neu startet und häufig einen Neustart beendet.

**Hängt von der Entwickler Perspektive ab**

Das Betriebssystem definiert einen Anwendungs Absturz als Benutzeroberflächen-Thread, der Nachrichten mindestens 5 Sekunden lang nicht verarbeitet hat. Offensichtliche Fehler verursachen einige Probleme, z. b. einen Thread, der auf ein Ereignis wartet, das nie signalisiert wird, und zwei Threads, die jeweils eine Sperre haben und versuchen, die anderen zu erhalten. Sie können diese Fehler ohne zu viel Aufwand beheben. Viele Abstürze sind jedoch nicht so klar. Ja, der UI-Thread ruft keine Nachrichten ab, aber er ist gleichermaßen ausgelastet, um andere "wichtige" Aufgaben zu erledigen, und wird schließlich zur Verarbeitung von Nachrichten zurückkehren.

Der Benutzer erkennt dies jedoch als Fehler. Der Entwurf sollte den Erwartungen des Benutzers entsprechen. Wenn der Entwurf der Anwendung zu einer nicht reagierenden Anwendung führt, muss sich der Entwurf ändern. Und das ist wichtig, und die Reaktionsfähigkeit kann nicht wie ein Code Fehler korrigiert werden. Hierfür müssen Sie während der Entwurfsphase vorab arbeiten durcharbeiten. Wenn Sie versuchen, die vorhandene Codebasis einer Anwendung zu reaktivieren, um die Benutzeroberfläche reaktionsfähiger zu machen, ist oft zu teuer. Die folgenden Entwurfs Richtlinien können hilfreich sein.

-   Stellen Sie die UI-Reaktionsfähigkeit zu einer Anforderung der obersten Ebene. der Benutzer sollte sich immer die Kontrolle über Ihre Anwendung fühlen.
-   Stellen Sie sicher, dass Benutzer Vorgänge abbrechen können, die länger als eine Sekunde dauern und/oder der Vorgang im Hintergrund ausgeführt werden kann. Bereitstellen der entsprechenden Fortschritts Benutzeroberfläche bei Bedarf

![Screenshot, der das Dialogfeld "Elemente kopieren" anzeigt.](images/preventinghangs-progressbar.gif)

-   Lange Ausführungs-oder Blockierungs Vorgänge als Hintergrundaufgaben in die Warteschlange stellen (hierfür ist ein wohl gedachte Messaging Mechanismus erforderlich, um den UI-Thread zu informieren, wenn die Arbeit abgeschlossen wurde)
-   Den Code für UI-Threads einfach aufbewahren; so viele blockierende API-Aufrufe wie möglich entfernen
-   Fenster und Dialogfelder nur anzeigen, wenn Sie bereit und voll funktionstüchtig sind. Wenn im Dialogfeld Informationen angezeigt werden sollen, die zu viel ressourcenintensiv sind, zeigen Sie zuerst einige generische Informationen an, und aktualisieren Sie Sie im laufenden Betrieb, wenn weitere Daten verfügbar werden. Ein gutes Beispiel ist das Dialogfeld mit den Ordnereigenschaften aus Windows-Explorer. Es muss die Gesamtgröße des Ordners, Informationen, die nicht im Dateisystem verfügbar sind, anzeigen. Das Dialogfeld wird sofort angezeigt, und das Feld "size" wird von einem Arbeits Thread aktualisiert:

![Screenshot, der die Seite "Allgemein" der Windows-Eigenschaften mit dem Text "size", "size on Disk" und "enthält" enthält.](images/preventinghangs-updatingdialog.gif)

Leider gibt es keine einfache Möglichkeit, eine reaktionsfähige Anwendung zu entwerfen und zu schreiben. Windows bietet kein einfaches asynchrones Framework, das eine einfache Planung von Blockierungen oder lang andauernden Vorgängen ermöglicht. In den folgenden Abschnitten werden einige bewährte Methoden zum Verhindern von Abstürzen und zum Hervorheben einiger häufig verwendeter Fehler vorgestellt.

## <a name="best-practices"></a>Bewährte Methoden

**UI-Thread einfach halten**

Die primäre Aufgabe der UI-Thread ist das Abrufen und Verteilen von Nachrichten. Jede andere Art von Arbeit stellt das Risiko dar, das Fenster zu hängen, das im Besitz dieses Threads ist.

**Können**

-   Verschieben Sie ressourcenintensive oder unbegrenzte Algorithmen, die zu Vorgängen mit langer Laufzeit in Arbeitsthreads führen.
-   Identifizieren Sie beliebig viele blockierende Funktionsaufrufe, und versuchen Sie, Sie in die Arbeitsthreads zu verschieben. jede Funktion, die eine andere DLL aufrufen, sollte verdächtig sein.
-   Führen Sie einen zusätzlichen Aufwand aus, um alle Datei-e/a-und Netzwerk-API-Aufrufe aus Ihrem Arbeits Thread zu entfernen. Diese Funktionen können viele Sekunden blockieren, wenn nicht Minuten. Wenn Sie im UI-Thread eine beliebige Art von e/a ausführen müssen, sollten Sie die Verwendung asynchroner e/a-Vorgänge in Erwägung ziehen.
-   Beachten Sie, dass der UI-Thread auch alle von Ihrem Prozess gehosteten STA-COM-Server (Single-Threaded Apartment) bedient. Wenn Sie einen blockierenden Rückruf ausführen, werden diese com-Server erst wieder reagiert, wenn Sie die Nachrichten Warteschlange erneut bedienen.

**Vermeiden Sie Folgendes:**

-   Warten Sie auf ein beliebiges Kernel Objekt (z. b. Ereignis oder Mutex), der länger als eine sehr kurze Zeitspanne ist. Wenn Sie überhaupt warten müssen, empfiehlt es sich, MsgWaitForMultipleObjects () zu verwenden, wodurch die Blockierung beim Eintreffen einer neuen Nachricht blockiert wird.
-   Freigeben der Fenster Nachrichten Warteschlange eines Threads mit einem anderen Thread mithilfe der attachthreadinput ()-Funktion. Es ist nicht nur äußerst schwierig, den Zugriff auf die Warteschlange ordnungsgemäß zu synchronisieren, sondern kann auch verhindern, dass das Windows-Betriebssystem ein nicht reagierendes Fenster ordnungsgemäß erkennt
-   Verwenden Sie TerminateThread () für alle Arbeitsthreads. Das Beenden eines Threads auf diese Weise lässt nicht zu, dass Sperren oder Signalereignisse freigegeben werden, und kann problemlos zu verwaisten Synchronisierungs Objekten führen.
-   Einen "unbekannten" Code aus dem UI-Thread aufzurufen. Dies trifft vor allem dann zu, wenn Ihre Anwendung über ein Erweiterbarkeits Modell verfügt. Es gibt keine Garantie, dass Code von Drittanbietern ihren Reaktions Richtlinien folgt.
-   Alle blockierenden Broadcast Aufrufe durchführen SendMessage (HWND- \_ Broadcast) versetzt Sie in die Gnade aller nicht geschriebenen Anwendungen, die zurzeit ausgeführt werden.

**Implementieren von asynchronen Mustern**

Zum Entfernen von Vorgängen mit langer Ausführungszeit oder Blockierung aus dem UI-Thread muss ein asynchrones Framework implementiert werden, das das Auslagern dieser Vorgänge an Arbeitsthreads ermöglicht.

**Können**

-   Verwenden Sie asynchrone Fenster Nachrichten-APIs in Ihrem UI-Thread, insbesondere, indem Sie SendMessage durch einen der nicht blockierenden Peers ersetzen: PostMessage, sendnotifymess oder sendmessagecallback.
-   Verwenden Sie Hintergrundthreads zum Ausführen von Aufgaben mit langer Ausführungszeit oder Blockierung. Verwenden der neuen Thread Pool-API zum Implementieren von Arbeitsthreads
-   Bereitstellen von Abbruch Unterstützung für Hintergrundaufgaben mit langer Ausführungszeit. Für blockierende e/a-Vorgänge verwenden Sie den e/a-Abbruch, aber nur als letzten Ausweg. Es ist nicht einfach, den "Right"-Vorgang abzubrechen.
-   Implementieren eines asynchronen Entwurfs für verwalteten Code mithilfe des iasynkresult-Musters oder mithilfe von Ereignissen

**Verwenden von Sperren**

Die Anwendung oder dll benötigt sperren, um den Zugriff auf die internen Datenstrukturen zu synchronisieren. Die Verwendung mehrerer Sperren erhöht die Parallelität und sorgt für eine reaktionsfähigere Anwendung. Wenn Sie jedoch mehrere Sperren verwenden, erhöht sich auch die Wahrscheinlichkeit, dass diese Sperren in verschiedenen Reihen folgen abgerufen werden, sodass Ihre Threads Deadlock werden. Wenn zwei Threads jeweils eine Sperre aufweisen und dann versuchen, die Sperre des anderen Threads abzurufen, bilden Ihre Vorgänge eine zirkuläre Wartezeit, die den Fortschritt für diese Threads blockiert. Sie können diesen Deadlock nur vermeiden, indem Sie sicherstellen, dass alle Threads in der Anwendung immer alle Sperren in derselben Reihenfolge abrufen. Es ist jedoch nicht immer einfach, Sperren in der Reihenfolge "Right" zu erhalten. Software Komponenten können zusammengesetzt werden, aber Sperr Übernahmen sind nicht möglich. Wenn Ihr Code eine andere Komponente aufruft, werden die Sperren dieser Komponente nun Teil der impliziten Sperr Reihenfolge, selbst wenn Sie keine Einblicke in diese Sperren haben.

Es ist sogar noch schwieriger, da Sperr Vorgänge weit mehr als die üblichen Funktionen für kritische Abschnitte, Mutexen und andere herkömmliche Sperren enthalten. Alle blockierenden Aufrufe, die Thread Grenzen überschreiten, verfügen über Synchronisierungs Eigenschaften, die zu einem Deadlock führen können. Der aufrufende Thread führt einen Vorgang mit der Semantik "abrufen" aus und kann die Blockierung erst wieder entsperren, wenn der Ziel Thread "Releases" aufruft. Eine Reihe von User32-Funktionen (z. b. SendMessage) sowie viele blockierende com-Aufrufe fallen in diese Kategorie.

Noch schlimmer ist, dass das Betriebssystem über eine eigene interne prozessspezifische Sperre verfügt, die bei der Ausführung des Codes manchmal angehalten wird. Diese Sperre wird abgerufen, wenn DLLs in den Prozess geladen werden, und wird daher als "Loadersperre" bezeichnet. Die DllMain-Funktion wird immer unter der Loadersperre ausgeführt. Wenn Sie Sperren in DllMain erwerben (was nicht der Grund ist), müssen Sie das Lade Modul in der Sperr Reihenfolge sperren. Wenn Sie bestimmte Win32-APIs aufrufen, erhalten Sie möglicherweise auch die Loadersperre in ihren Namen, wie z. b. LoadLibraryEx, GetModuleHandle und vor allem CoCreateInstance.

Um dies zu verknüpfen, sehen Sie sich den unten stehenden Beispielcode an. Diese Funktion ruft mehrere Synchronisierungs Objekte ab und definiert implizit eine Sperr Reihenfolge, was bei der flüchtigen Überprüfung nicht unbedingt offensichtlich ist. Bei einem Funktions Eintrag erhält der Code einen kritischen Abschnitt und gibt ihn nicht bis zum Beenden der Funktion frei. Dadurch wird der Code zum obersten Knoten in unserer Sperr Hierarchie. Der Code ruft dann die Win32-Funktion "LoadIcon ()" auf, die unter den überdecken den Ladevorgang des Betriebssystems aufrufen kann, um diese Binärdatei zu laden. Dieser Vorgang würde die Loadersperre abrufen, die jetzt auch Teil dieser Sperr Hierarchie wird (stellen Sie sicher, dass die DllMain-Funktion die g CS-Sperre nicht erhält \_ ). Als Nächstes ruft der Code SendMessage () auf, einen blockierenden Thread übergreifenden Vorgang, der nicht zurückgegeben wird, wenn der UI-Thread antwortet. Stellen Sie erneut sicher, dass der UI-Thread niemals g \_ CS erhält.

```
bool foo::bar (char* buffer)  
{  
      EnterCriticalSection(&g_cs);  
      // Get 'new data' icon  
      this.m_Icon = LoadIcon(hInst, MAKEINTRESOURCE(5));  
      // Let UI thread know to update icon SendMessage(hWnd,WM_COMMAND,IDM_ICON,NULL);  
      this.m_Params = GetParams(buffer);  
      LeaveCriticalSection(&g_cs);
      return true;  
}  
```

Wenn Sie diesen Code betrachten, ist es offensichtlich, dass wir g \_ cs in der Sperr Hierarchie implizit die Sperre der obersten Ebene erstellt haben, auch wenn wir nur den Zugriff auf die Klassenmember-Variablen synchronisieren wollten.

**Können**

-   Entwerfen Sie eine Sperr Hierarchie, und befolgen Sie Sie. Fügen Sie alle erforderlichen Sperren hinzu. Es gibt viele weitere Synchronisierungs primitive als nur Mutex und criticalabschnitts; Sie müssen alle eingeschlossen werden. Einschließen der Loadersperre in ihre Hierarchie, wenn Sie Sperren in DllMain () verwenden
-   Stimmen Sie dem Sperrprotokoll mit ihren Abhängigkeiten zu. Sämtlicher Code, der von der Anwendung aufgerufen wird oder der die Anwendung aufrufen kann, muss dieselbe Sperr Hierarchie verwenden.
-   Lock Data Structures not Functions. Verschieben Sie Sperr Käufe von Funktions Einstiegspunkten, und schützen Sie nur den Datenzugriff mit Sperren. Wenn weniger Code unter einer Sperre betrieben wird, besteht weniger Wahrscheinlichkeit für Deadlocks.
-   Analysieren Sie die Übernahmen und Releases von Sperren im Fehler Behandlungs Code. Häufig die Sperr Hierarchie, wenn Sie bei der Wiederherstellung nach einem Fehlerzustand vergessen wird
-   Ersetzen Sie die durch den Verweis Zähler erfallenen sperren, sodass Sie keinen Deadlock haben. Einzeln gesperrte Elemente in Listen und Tabellen sind gute Kandidaten.
-   Seien Sie vorsichtig, wenn Sie auf ein Thread Handle von einer DLL warten. Nehmen Sie immer an, dass der Code unter der Loadersperre aufgerufen werden kann. Es ist besser, auf Ihre Ressourcen zu verweisen, und der Arbeits Thread kann eine eigene Bereinigung durchführen (und dann FreeLibraryAndExitThread verwenden, um die Bereinigung zu beenden).
-   Verwenden Sie die Wait Chain Traversal-API, wenn Sie Ihre eigenen Deadlocks diagnostizieren möchten.

**Vermeiden Sie Folgendes:**

-   Führen Sie in der DllMain ()-Funktion etwas anderes als die sehr einfache Initialisierung aus. Weitere Informationen finden Sie unter DllMain-Rückruffunktion. Insbesondere nicht "LoadLibraryEx" oder "cokreateinstance" aufrufen
-   Schreiben Sie eigene Sperr primitive. Mit benutzerdefiniertem Synchronisierungs Code können Sie problemlos einfache Fehler in die Codebasis einbringen. Verwenden Sie stattdessen die umfangreiche Auswahl von Betriebssystem-Synchronisierungs Objekten.
-   Arbeiten in den Konstruktoren und Debuggern für globale Variablen, Sie werden unter der Loadersperre ausgeführt.

**Vorsicht bei Ausnahmen**

Ausnahmen ermöglichen die Trennung des normalen Programmflusses und der Fehlerbehandlung. Aufgrund dieser Trennung ist es möglicherweise schwierig, den genauen Zustand des Programms vor der Ausnahme zu erkennen, und der Ausnahmehandler könnte wichtige Schritte bei der Wiederherstellung eines gültigen Zustands übersehen. Dies gilt insbesondere für Sperr Käufe, die im Handler freigegeben werden müssen, um zukünftige Deadlocks zu verhindern.

Der folgende Beispielcode veranschaulicht dieses Problem. Der unbegrenzte Zugriff auf die Variable "Buffer" führt gelegentlich zu einer Zugriffsverletzung (AV). Diese AV-Datei wird vom systemeigenen Ausnahmehandler abgefangen, aber es ist nicht einfach zu bestimmen, ob der kritische Abschnitt zum Zeitpunkt der Ausnahme bereits abgerufen wurde (die AV könnte sogar irgendwo im Code von EnterCriticalSection stattgefunden haben).

```
 BOOL bar (char* buffer)  
{  
   BOOL rc = FALSE;  
   __try {  
      EnterCriticalSection(&cs);  
      while (*buffer++ != '&') ;  
      rc = GetParams(buffer);  
      LeaveCriticalSection(&cs);  
   } __except (EXCEPTION_EXECUTE_HANDLER)  
   {  
      return FALSE;  
   } 
   return rc;  
}  
```

**Können**

-   " \_ \_ Try/" entfernen \_ \_ , wenn dies möglich ist. verwenden Sie "Set-Filter" nicht.
-   Umschließen Sie Ihre Sperren in benutzerdefinierten automatischen \_ ptr-ähnlichen Vorlagen, wenn Sie C++-Ausnahmen verwenden. Die Sperre sollte im Dekonstruktor freigegeben werden. Freigabe der Sperren in der letzten Anweisung für Native Ausnahmen \_ \_
-   Seien Sie vorsichtig mit dem Code, der in einem nativen Ausnahmehandler ausgeführt wird. die Ausnahme hat möglicherweise viele Sperren kompromittiert, sodass der Handler keine

**Vermeiden Sie Folgendes:**

-   Behandeln Sie Native Ausnahmen, wenn dies nicht erforderlich oder für die Win32-APIs erforderlich ist. Wenn Sie Native Ausnahmehandler für die Berichterstellung oder die Datenwiederherstellung nach einem schwerwiegenden Fehler verwenden, sollten Sie stattdessen den standardmäßigen Betriebssystem Mechanismus von Windows-Fehlerberichterstattung verwenden.
-   Verwenden Sie C++-Ausnahmen mit beliebigen Arten von UI-Code (User32). eine Ausnahme, die in einem Rückruf ausgelöst wird, durchläuft die Ebenen des C-Codes, die vom Betriebssystem bereitgestellt werden. Dieser Code kennt die Semantik "C++ auflösen" nicht.

## <a name="links-to-resources"></a>Links zu Ressourcen

-   [Windows-Fehlerberichterstattung](../wer/windows-error-reporting.md)
-   [Asynchroner Entwurf](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [Asynchrone e/a](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**Attachthreadinput-Funktion**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**Auto \_ ptr-Klasse**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**Disableprocesswindowsghosting-Funktion**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**DllMain-Rückruffunktion**](../dlls/dllmain.md)
-   [Ereignisse](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**GetMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [E/a-Abbruch](../fileio/canceling-pending-i-o-operations.md)
-   [**Ishungappwindow-Funktion**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Nachrichten Warteschlange](../winmsg/using-messages-and-message-queues.md)
-   [**MsgWaitForMultipleObjects-Funktion**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Neue Thread Pool-API](../procthread/thread-pool-api.md)
-   [**PostMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Neustart und Wiederherstellung](../recovery/registering-for-application-restart.md)
-   [**Sendmessagecallback-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**Sendnotisymess Age-Funktion**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Synchronisierungs Objekte](../sync/about-synchronization.md)
-   [**TerminateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Windows-Fehlerberichterstattung](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
