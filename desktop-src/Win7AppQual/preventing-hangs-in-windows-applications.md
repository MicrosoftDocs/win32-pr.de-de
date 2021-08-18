---
description: Erfahren Sie, wie Sie das Hängen in Windows Anwendungen für Windows 7- und Windows Server 2008 R2-Plattformen verhindern.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Verhindern von Blockaden in Windows-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5509b8733e45b105694a8bfdadddae0d67096b92c390ed98b3dd937817823b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994822"
---
# <a name="preventing-hangs-in-windows-applications"></a>Verhindern von Blockaden in Windows-Anwendungen

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="description"></a>BESCHREIBUNG

**Hängt – Benutzerperspektive**

Benutzer wie reaktionsfähige Anwendungen. Wenn sie auf ein Menü klicken, soll die Anwendung sofort reagieren, auch wenn sie gerade ihre Arbeit druckt. Wenn sie ein langes Dokument in ihrer bevorzugten Textverarbeitung speichern, möchten sie weiterhin eingeben, während der Datenträger noch rotiert wird. Benutzer werden eher schnell ungeduldig, wenn die Anwendung nicht rechtzeitig auf ihre Eingabe reagiert.

Ein Programmierer erkennt möglicherweise viele legitime Gründe dafür, dass eine Anwendung nicht sofort auf Benutzereingaben reagiert. Möglicherweise ist die Anwendung damit beschäftigt, einige Daten neu zu berechnen, oder sie wartet einfach auf den Abschluss ihrer Datenträger-E/A. Aus der Benutzerforschung wissen wir jedoch, dass Benutzer nach nur wenigen Sekunden nicht reagierender Benutzer verärgert und frustriert werden. Nach 5 Sekunden wird versucht, eine hängende Anwendung zu beenden. Neben Abstürzen sind Anwendungsunterbrechungen die häufigste Ursache für Benutzerunterbrechungen bei der Arbeit mit Win32-Anwendungen.

Es gibt viele verschiedene Ursachen für das Hängen der Anwendung, und nicht alle werden in einer nicht reagierenden Benutzeroberfläche angezeigt. Eine nicht reagierende Benutzeroberfläche ist jedoch eine der gängigsten Hängenderfahrungen, und dieses Szenario erhält derzeit die meisten Betriebssystemunterstützung sowohl für die Erkennung als auch für die Wiederherstellung. Windows erkennt automatisch Debuginformationen und beendet oder startet hängende Anwendungen optional neu. Andernfalls muss der Benutzer den Computer möglicherweise neu starten, um eine hängende Anwendung wiederherzustellen.

**Hängt – Perspektive des Betriebssystems**

Wenn eine Anwendung (oder genauer gesagt ein Thread) ein Fenster auf dem Desktop erstellt, tritt sie in einen impliziten Vertrag mit dem Desktopfenster-Manager (DWM) ein, um Fenstermeldungen rechtzeitig zu verarbeiten. Der DWM sendet Nachrichten (Tastatur-/Mauseingaben und Nachrichten aus anderen Fenstern sowie selbst) in die threadspezifische Nachrichtenwarteschlange. Der Thread ruft diese Nachrichten über seine Nachrichtenwarteschlange ab und verteilt sie. Wenn der Thread die Warteschlange nicht durch Aufrufen von GetMessage() bedient, werden Nachrichten nicht verarbeitet, und das Fenster hängt: Es kann weder neu gezeichnet noch Eingaben vom Benutzer akzeptieren. Das Betriebssystem erkennt diesen Zustand, indem ein Timer an ausstehende Nachrichten in der Nachrichtenwarteschlange angefügt wird. Wenn eine Nachricht nicht innerhalb von 5 Sekunden abgerufen wurde, deklariert der DWM, dass das Fenster hängen bleibt. Sie können diesen bestimmten Fensterzustand über die IsHungAppWindow()-API abfragen.

Die Erkennung ist nur der erste Schritt. An diesem Punkt kann der Benutzer die Anwendung noch nicht einmal beenden. Wenn sie auf die Schaltfläche X (Schließen) klicken, würde dies zu einer WM \_ CLOSE-Nachricht führen, die wie jede andere Nachricht in der Nachrichtenwarteschlange hängen bleibt. Der Desktopfenster-Manager hilft, indem das hängende Fenster nahtlos ausgeblendet und dann durch eine Kopie des "Ghost" ersetzt wird, die eine Bitmap des vorherigen Clientbereichs des ursprünglichen Fensters anzeigt (und der Titelleiste "Nicht reagiert" hinzufügt). Solange der Thread des ursprünglichen Fensters keine Nachrichten abruft, verwaltet dwm beide Fenster gleichzeitig, ermöglicht dem Benutzer jedoch die Interaktion nur mit der inaktiven Kopie. Mithilfe dieses ingedekten Fensters kann der Benutzer die nicht reagierende Anwendung nur verschieben, minimieren und – vor allem – schließen, aber ihren internen Zustand nicht ändern.

Die gesamte Inspenderfahrung sieht wie folgt aus:

![Screenshot: Dialogfeld "Editor reagiert nicht"](images/preventinghangs-ghostwindow.gif)

Der Desktopfenster-Manager führt einen letzten Teil aus: Sie lässt sich in Windows-Fehlerberichterstattung integrieren, sodass der Benutzer die Anwendung nicht nur schließen und optional neu starten kann, sondern auch wertvolle Debugdaten an Microsoft zurücksenden kann. Sie können diese hängen bleibende Daten für Ihre eigenen Anwendungen erhalten, indem Sie sich auf der Winqual-Website anmelden.

Windows 7 wurde dieser Benutzeroberfläche ein neues Feature hinzugefügt. Das Betriebssystem analysiert die hängende Anwendung und gibt dem Benutzer unter bestimmten Umständen die Möglichkeit, einen Blockierungsvorgang abzubrechen und die Anwendung wieder reaktionsfähig zu machen. Die aktuelle Implementierung unterstützt den Abbruch von blockierenden Socketaufrufen. weitere Vorgänge können in zukünftigen Versionen vom Benutzer abgebrochen werden.

Führen Sie die folgenden Schritte aus, um Ihre Anwendung in die Wiederherstellung nach Hängen zu integrieren und die verfügbaren Daten optimal zu nutzen:

-   Stellen Sie sicher, dass sich Ihre Anwendung für Neustart und Wiederherstellung registriert, sodass der Benutzer so problemlos wie möglich hängen bleibt. Eine ordnungsgemäß registrierte Anwendung kann automatisch neu gestartet werden, wobei die meisten nicht gespeicherten Daten intakt sind. Dies funktioniert sowohl bei hängenden anwendungen als auch bei Abstürzen.
-   Abrufen von Informationen zur Häufigkeit und Debuggen von Daten für Ihre hängende und abgestürzte Anwendung von der Winqual-Website. Sie können diese Informationen auch während der Betaphase verwenden, um Ihren Code zu verbessern. Eine kurze Übersicht finden Sie unter "Introducing Windows-Fehlerberichterstattung" (Einführung in Windows-Fehlerberichterstattung).
-   Sie können das Inaktivierungsfeature in Ihrer Anwendung über einen Aufruf von DisableProcessWindowsGhosting () deaktivieren. Dies verhindert jedoch, dass der durchschnittliche Benutzer eine hängende Anwendung schließt und neu startet und häufig mit einem Neustart endet.

**Hängt – Entwicklerperspektive**

Das Betriebssystem definiert, dass eine Anwendung als UI-Thread hängt, der nachrichten seit mindestens 5 Sekunden nicht verarbeitet hat. Offensichtliche Fehler führen dazu, dass einige hängen bleiben, z. B. ein Thread, der auf ein Ereignis wartet, das nie signalisiert wird, und zwei Threads, die jeweils eine Sperre halten und versuchen, die anderen zu erhalten. Sie können diese Fehler ohne zu großen Aufwand beheben. Viele Hängen sind jedoch nicht so klar. Ja, der BENUTZERoberflächenthread ruft keine Nachrichten ab, aber er ist ebenso beschäftigt mit anderen "wichtigen" Arbeiten und wird schließlich zur Verarbeitung von Nachrichten zurückkehren.

Der Benutzer erkennt dies jedoch als Fehler. Der Entwurf sollte den Erwartungen des Benutzers entsprechen. Wenn der Entwurf der Anwendung zu einer nicht reagierenden Anwendung führt, muss sich der Entwurf ändern. Und dies ist wichtig, und schließlich kann die Nichtantwort nicht wie ein Codefehler behoben werden. Dies erfordert Vorlauf während der Entwurfsphase. Der Versuch, die vorhandene Codebasis einer Anwendung so zu gestalten, dass die Benutzeroberfläche reaktionsfähiger wird, ist häufig zu teuer. Die folgenden Entwurfsrichtlinien können hilfreich sein.

-   Machen Sie die Reaktionsfähigkeit der Benutzeroberfläche zu einer Anforderung der obersten Ebene. Der Benutzer sollte immer die Kontrolle über Ihre Anwendung haben.
-   Stellen Sie sicher, dass Benutzer Vorgänge abbrechen können, die länger als eine Sekunde dauern und/oder die Vorgänge im Hintergrund abgeschlossen werden können. Bereitstellen einer geeigneten Statusanzeige bei Bedarf

![Screenshot: Dialogfeld "Elemente kopieren"](images/preventinghangs-progressbar.gif)

-   Zeitintensive oder blockierende Vorgänge als Hintergrundaufgaben in die Warteschlange einreihen (dies erfordert einen gut durchdachten Messagingmechanismus, um den UI-Thread zu informieren, wenn die Arbeit abgeschlossen ist).
-   Halten Sie den Code für Benutzeroberflächenthreads einfach. So viele blockierende API-Aufrufe wie möglich entfernen
-   Fenster und Dialoge nur anzeigen, wenn sie bereit und vollständig betriebsbereit sind. Wenn das Dialogfeld Informationen anzeigen muss, die zu ressourcenintensiv für die Berechnung sind, zeigen Sie zunächst einige generische Informationen an, und aktualisieren Sie sie im laufenden Betrieb, wenn mehr Daten verfügbar sind. Ein gutes Beispiel ist das Dialogfeld "Ordnereigenschaften" aus Windows Explorer. Sie muss die Gesamtgröße des Ordners anzeigen, d. h. Informationen, die im Dateisystem nicht sofort verfügbar sind. Das Dialogfeld wird sofort angezeigt, und das Feld "size" wird von einem Arbeitsthread aktualisiert:

![Screenshot: Seite "Allgemein" Windows Eigenschaften mit eingekreisten Texten "Größe", "Größe auf Datenträger" und "Enthält"](images/preventinghangs-updatingdialog.gif)

Leider gibt es keine einfache Möglichkeit, eine reaktionsfähige Anwendung zu entwerfen und zu schreiben. Windows bietet kein einfaches asynchrones Framework, das eine einfache Planung von blockierenden oder zeitintensiven Vorgängen ermöglichen würde. In den folgenden Abschnitten werden einige der bewährten Methoden zum Verhindern von Hängen vorgestellt, und es werden einige der häufigsten Fallstricke hervorgehoben.

## <a name="best-practices"></a>Empfehlungen

**Benutzeroberflächenthread einfach halten**

Der Ui-Thread ist in erster Linie dafür verantwortlich, Nachrichten abzurufen und zu senden. Jede andere Art von Arbeit birgt das Risiko, dass die Fenster im Besitz dieses Threads hängen.

**tun:**

-   Verschieben von ressourcenintensiven oder ungebundenen Algorithmen, die zu Vorgängen mit langer Ausführungslaufzeit in Arbeitsthreads führen
-   Identifizieren Sie so viele blockierende Funktionsaufrufe wie möglich, und versuchen Sie, sie in Arbeitsthreads zu verschieben. Jede Funktion, die eine andere DLL aufruft, sollte verdächtig sein.
-   Nehmen Sie zusätzlichen Aufwand vor, um alle Datei-E/A- und Netzwerk-API-Aufrufe aus Ihrem Arbeitsthread zu entfernen. Diese Funktionen können für viele Sekunden blockiert werden, wenn es sich nicht um Minuten handelt. Wenn Sie E/A-Vorgänge im UI-Thread durchführen müssen, sollten Sie asynchrone E/A verwenden.
-   Beachten Sie, dass Ihr UI-Thread auch alle STA-COM-Server (Singlethread-Apartment) wartet, die von Ihrem Prozess gehostet werden. Wenn Sie einen blockierenden Aufruf durchführen, reagieren diese COM-Server nicht, bis Sie die Nachrichtenwarteschlange erneut warten.

**Vermeiden Sie Folgendes:**

-   Warten Sie länger als eine sehr kurze Zeit auf ein beliebiges Kernelobjekt (z. B. Event oder Mutex). Wenn Sie überhaupt warten müssen, erwägen Sie die Verwendung von MsgWaitForMultipleObjects(), wodurch die Blockierung aufgehoben wird, wenn eine neue Nachricht eintrifft.
-   Geben Sie die Fenstermeldungswarteschlange eines Threads mithilfe der AttachThreadInput()-Funktion für einen anderen Thread frei. Es ist nicht nur äußerst schwierig, den Zugriff auf die Warteschlange ordnungsgemäß zu synchronisieren, sondern kann auch verhindern, dass das Windows Betriebssystem ein hängendes Fenster ordnungsgemäß erkennt.
-   Verwenden Sie TerminateThread() für einen Ihrer Arbeitsthreads. Durch das Beenden eines Threads auf diese Weise kann er keine Sperren oder Signalereignisse freigeben und kann problemlos zu verwaisten Synchronisierungsobjekten führen.
-   Rufen Sie einen beliebigen "unbekannten" Code aus Ihrem UI-Thread auf. Dies gilt insbesondere, wenn Ihre Anwendung über ein Erweiterbarkeitsmodell verfügt. es gibt keine Garantie dafür, dass Drittanbietercode Ihren Richtlinien zur Reaktionsfähigkeit entspricht.
-   Nehmen Sie eine beliebige Art von blockierenden Broadcastaufruf vor. SendMessage(HWND \_ BROADCAST) versetzt Sie in den Mittelpunkt jeder aktuell ausgeführten falsch geschriebenen Anwendung.

**Implementieren asynchroner Muster**

Zum Entfernen von zeitintensiven oder blockierenden Vorgängen aus dem UI-Thread muss ein asynchrones Framework implementiert werden, das das Auslagern dieser Vorgänge an Arbeitsthreads ermöglicht.

**tun:**

-   Verwenden Sie asynchrone Fenstermeldungs-APIs in Ihrem UI-Thread, insbesondere, indem Sie SendMessage durch einen seiner nicht blockierenden Peers ersetzen: PostMessage, SendNotifyMessage oder SendMessageCallback.
-   Verwenden Sie Hintergrundthreads, um Aufgaben mit langer Ausführung oder Blockierung auszuführen. Verwenden der neuen Threadpool-API zum Implementieren Ihrer Arbeitsthreads
-   Bereitstellen von Abbruchunterstützung für Hintergrundaufgaben mit langer Laufzeit. Verwenden Sie zum Blockieren von E/A-Vorgängen den E/A-Abbruch, aber nur als letzten Ausweg. Es ist nicht einfach, den "richtigen" Vorgang abzubricht.
-   Implementieren eines asynchronen Entwurfs für verwalteten Code mithilfe des IAsyncResult-Musters oder mithilfe von Ereignissen

**Verwenden von Sperren mit Bedacht**

Ihre Anwendung oder DLL benötigt Sperren, um den Zugriff auf ihre internen Datenstrukturen zu synchronisieren. Die Verwendung mehrerer Sperren erhöht die Parallelität und erhöht die Reaktionsfähigkeit Ihrer Anwendung. Durch die Verwendung mehrerer Sperren erhöht sich jedoch auch die Wahrscheinlichkeit, dass diese Sperren in unterschiedlichen Bestellungen verwendet werden und ihre Threads zu einem Deadlock führen. Wenn zwei Threads jeweils eine Sperre halten und dann versuchen, die Sperre des anderen Threads zu erhalten, bilden ihre Vorgänge einen kreisförmigen Wartevorgänge, der jeden Vorwärtsfortschritt für diese Threads blockiert. Sie können diesen Deadlock nur vermeiden, indem Sie sicherstellen, dass alle Threads in der Anwendung immer alle Sperren in der gleichen Reihenfolge erhalten. Es ist jedoch nicht immer einfach, Sperren in der richtigen Reihenfolge zu erhalten. Softwarekomponenten können zusammengestellt werden, Sperrenübernahmen jedoch nicht. Wenn Ihr Code eine andere Komponente aufruft, werden die Sperren dieser Komponente jetzt Teil Ihrer impliziten Sperr reihenfolge – auch wenn Sie keinen Einblick in diese Sperren haben.

Dies wird noch schwieriger, da Sperrvorgänge weit mehr als die üblichen Funktionen für kritische Abschnitte, Mutexe und andere herkömmliche Sperren umfassen. Jeder blockierende Aufruf, der Threadgrenzen überschreitet, verfügt über Synchronisierungseigenschaften, die zu einem Deadlock führen können. Der aufrufende Thread führt einen Vorgang mit "acquire"-Semantik aus und kann die Blockierung erst wieder aufsperren, wenn der Zielthread den Aufruf "freilässt". Einige User32-Funktionen (z. B. SendMessage) sowie viele blockierende COM-Aufrufe fallen in diese Kategorie.

Noch schlechter ist, dass das Betriebssystem über eine eigene interne prozessspezifische Sperre verfügt, die manchmal gehalten wird, während Ihr Code ausgeführt wird. Diese Sperre wird beim Laden von DLLs in den Prozess und daher als "Ladesperre" bezeichnet. Die DllMain-Funktion wird immer unter der Loadersperre ausgeführt. Wenn Sie Sperren in DllMain erhalten (und dies nicht der Fall ist), müssen Sie die Loadersperre als Teil Ihrer Sperr reihenfolge verwenden. Das Aufrufen bestimmter Win32-APIs kann auch die Loadersperre in Ihrem Namen erhalten– Funktionen wie LoadLibraryEx, GetModuleHandle und insbesondere CoCreateInstance.

Sehen Sie sich den folgenden Beispielcode an, um all dies miteinander zu verknüpfen. Diese Funktion übernimmt mehrere Synchronisierungsobjekte und definiert implizit eine Sperr reihenfolge, die bei der Cursorüberprüfung nicht unbedingt offensichtlich ist. Beim Funktionseintrag erhält der Code einen kritischen Abschnitt und gibt ihn erst dann frei, wenn die Funktion beendet wird. Dadurch wird er zum obersten Knoten in unserer Sperrenhierarchie. Der Code ruft dann die Win32-Funktion LoadIcon() auf, die im Untergang möglicherweise das Betriebssystemlader aufruft, um diese Binärdatei zu laden. Dieser Vorgang würde die Loadersperre erhalten, die jetzt auch Teil dieser Sperrhierarchie wird (stellen Sie sicher, dass die DllMain-Funktion die g cs-Sperre \_ nicht erhält). Als Nächstes ruft der Code SendMessage() auf, einen blockierenden threadübergreifenden Vorgang, der nur dann zurück gibt, wenn der UI-Thread antwortet. Stellen Sie erneut sicher, dass der UI-Thread nie g \_ cs erhält.

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

Bei diesem Code scheint klar zu sein, dass wir g cs implizit zur Sperre der obersten Ebene in unserer Sperrhierarchie gemacht haben, auch wenn wir nur den Zugriff auf die Klassenmitgliedsvariablen \_ synchronisieren wollten.

**tun:**

-   Entwerfen Sie eine Sperrhierarchie, und befolgen Sie sie. Fügen Sie alle erforderlichen Sperren hinzu. Es gibt viel mehr Synchronisierungsprimitiven als nur Mutex und CriticalSections. sie müssen alle einbezogen werden. Schließen Sie die Loadersperre in Ihre Hierarchie ein, wenn Sie Sperren in DllMain() verwenden.
-   Stimmen Sie dem Sperrprotokoll mit Ihren Abhängigkeiten zu. Jeder Code, den Ihre Anwendung aufruft oder der Ihre Anwendung aufrufen kann, muss dieselbe Sperrhierarchie verwenden.
-   Sperren Von Datenstrukturen, nicht von Funktionen. Verschieben Sie Sperrkäufe von Funktionseinstiegspunkten weg, und schützen Sie nur den Datenzugriff mit Sperren. Wenn weniger Code unter einer Sperre arbeitet, besteht weniger Wahrscheinlichkeit für Deadlocks.
-   Analysieren Von Sperrenkäufen und -releases in Ihrem Fehlerbehandlungscode. Häufig wird die Sperrhierarchie vergessen, wenn versucht wird, eine Wiederherstellung nach einem Fehlerzustand zu versuchen.
-   Ersetzen Sie geschachtelte Sperren durch Verweiszähler– sie können nicht deadlocken. Einzeln gesperrte Elemente in Listen und Tabellen sind gute Kandidaten
-   Seien Sie vorsichtig, wenn Sie auf ein Threadhand handle aus einer DLL warten. Gehen Sie immer davon aus, dass Ihr Code unter der Loadersperre aufgerufen werden kann. Es ist besser, ihre Ressourcen auf die Verweisanzahl zu verweisen und dem Arbeitsthread eine eigene Bereinigung zu ermöglichen (und dann FreeLibraryAndExitThread zu verwenden, um eine saubere Beendigung zu ermöglichen).
-   Verwenden Sie die Wait Chain Traversal-API, wenn Sie Ihre eigenen Deadlocks diagnostizieren möchten.

**Vermeiden Sie Folgendes:**

-   Machen Sie alles andere als eine sehr einfache Initialisierung in Ihrer DllMain()-Funktion. Weitere Informationen finden Sie unter DllMain-Rückruffunktion. Rufen Sie insbesondere LoadLibraryEx oder CoCreateInstance nicht auf.
-   Schreiben Sie eigene Sperrprimitive. Benutzerdefinierter Synchronisierungscode kann leicht zu feinen Fehlern in Ihrer Codebasis führen. Verwenden Sie stattdessen die umfangreiche Auswahl von Betriebssystemsynchronisierungsobjekten.
-   Führen Sie jede Arbeit in den Konstruktoren und Destruktoren für globale Variablen aus. Sie werden unter der Ladersperre ausgeführt.

**Seien Sie vorsichtig mit Ausnahmen**

Ausnahmen ermöglichen die Trennung des normalen Programmablaufs und der Fehlerbehandlung. Aufgrund dieser Trennung kann es schwierig sein, den genauen Zustand des Programms vor der Ausnahme zu kennen, und der Ausnahmehandler kann wichtige Schritte zum Wiederherstellen eines gültigen Zustands übersehen. Dies gilt insbesondere für Sperrenabkäufe, die im Handler freigegeben werden müssen, um zukünftige Deadlocks zu verhindern.

Der folgende Beispielcode veranschaulicht dieses Problem. Der ungebundene Zugriff auf die Puffervariable führt gelegentlich zu einer Zugriffsverletzung (AV). Diese AV wird vom nativen Ausnahmehandler erfasst, kann jedoch nicht einfach feststellen, ob der kritische Abschnitt zum Zeitpunkt der Ausnahme bereits erfasst wurde (die AV hätte sogar irgendwo im EnterCriticalSection-Code stattfinden können).

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

**tun:**

-   Remove \_ \_ \_ \_ try/except whenever possible; do not use SetUnhandledExceptionFilter
-   Umschließen Sie Ihre Sperren in \_ benutzerdefinierte, automatisch ptr-orientierte Vorlagen, wenn Sie C++-Ausnahmen verwenden. Die Sperre sollte im Destruktor freigegeben werden. Bei nativen Ausnahmen werden die Sperren in Ihrer \_ \_ finally-Anweisung wieder frei.
-   Seien Sie vorsichtig mit dem Code, der in einem nativen Ausnahmehandler ausgeführt wird. Die Ausnahme hat möglicherweise viele Sperren geleert, sodass ihr Handler keines erhalten sollte.

**Vermeiden Sie Folgendes:**

-   Behandeln Sie native Ausnahmen, wenn dies nicht erforderlich ist oder für die Win32-APIs erforderlich ist. Wenn Sie native Ausnahmehandler für die Berichterstellung oder Datenwiederherstellung nach schwerwiegenden Fehlern verwenden, sollten Sie stattdessen den Standardbetriebssystemmechanismus von Windows-Fehlerberichterstattung verwenden.
-   Verwenden Sie C++-Ausnahmen mit beliebigem Benutzeroberflächencode (user32). Eine in einem Rückruf ausgelöste Ausnahme durchfing ebenen von C-Code, der vom Betriebssystem bereitgestellt wird. Dieser Code kennt die C++-Semantik zum Entrollen nicht.

## <a name="links-to-resources"></a>Links zu Ressourcen

-   [Windows-Fehlerberichterstattung](../wer/windows-error-reporting.md)
-   [Asynchroner Entwurf](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [Asynchrone E/A](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**AttachThreadInput-Funktion**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**auto \_ ptr-Klasse**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**DisableProcessWindowsGhosting-Funktion**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**DllMain-Rückruffunktion**](../dlls/dllmain.md)
-   [Ereignisse](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**GetMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [E/A-Abbruch](../fileio/canceling-pending-i-o-operations.md)
-   [**IsHungAppWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Nachrichtenwarteschlange](../winmsg/using-messages-and-message-queues.md)
-   [**MsgWaitForMultipleObjects-Funktion**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Neue Threadpool-API](../procthread/thread-pool-api.md)
-   [**PostMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Neustart und Wiederherstellung](../recovery/registering-for-application-restart.md)
-   [**SendMessageCallback-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**SendNotifyMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Synchronisierungsobjekte](../sync/about-synchronization.md)
-   [**TerminateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Windows-Fehlerberichterstattung](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
