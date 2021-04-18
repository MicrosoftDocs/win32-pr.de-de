---
title: Erstellen eines Laufwerks Bereinigungs Handlers
description: Ein Grundsatz bewährter Zeitpunkt und wieder in der Welt der Computer ist, dass Sie, unabhängig von der Größe der Speicherkapazität Ihres Computers, ihn schließlich Auffüllen werden.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- Laufwerks Bereinigungs Handler
- Datenträgerbereinigung
- Datadrivencleaner
- registrieren, Datenträger Bereinigungs Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30584439ae2c38ae8a9b7106dae96f69eea5df37
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106337686"
---
# <a name="creating-a-disk-cleanup-handler"></a>Erstellen eines Laufwerks Bereinigungs Handlers

Ein Grundsatz bewährter Zeitpunkt und wieder in der Welt der Computer ist, dass Sie, unabhängig von der Größe der Speicherkapazität Ihres Computers, ihn schließlich Auffüllen werden. Obwohl die durchschnittliche Größe der Festplatte eines Computers im Laufe der Zeit drastisch zugenommen hat, wurden die Anwendungen ebenfalls entsprechend vergrößert, sodass die Benutzer nach Möglichkeiten suchten, mehr freien Festplattenspeicher zu schaffen. Der verfügbare Speicherplatz wird auch durch die zahlreichen temporären Dateien reduziert, die von Anwendungen aus Sicherungs-oder Leistungsgründen erstellt werden. Wenn der Speicherplatz auf dem Datenträger gering ist, ist es erforderlich, den von Anwendungen genutzten Speicherplatz zu reduzieren. Der Speicherplatz kann auf verschiedene Weise freigegeben werden, einschließlich der folgenden:

-   Dateien werden gelöscht.
-   Dateien werden komprimiert.
-   Verschieben von Dateien auf ein Sicherungsmedium.
-   Dateien werden auf einen Remote Server übertragen.

Zu den Dateien, die für die Bereinigung geeignet sind, gehören:

-   Dateien, die der Benutzer nie erneut benötigt.
-   Temporäre Dateien, die nur aus Leistungsgründen vorhanden sind.
-   Dateien, die bei Bedarf von einer Installations-CD wieder hergestellt werden können.
-   Datendateien, die möglicherweise durch neuere Versionen abgelöst wurden, z. b. alte Sicherungsdateien.
-   Ältere Dateien, die in längerer Zeit nicht verwendet wurden.

Das Löschen eignet sich besonders für Dateien, die der Benutzer nie erneut benötigt, z. b. Dateien, die aus Leistungsgründen vorübergehend zwischengespeichert werden. Das Löschen eignet sich auch für Dateien, die problemlos wieder hergestellt werden können, z. b. Grafikdateien, die von einer Installations-CD neu geladen werden können. Dateien, die der Benutzer möglicherweise später benötigt oder die schwierig zu rekonstruieren wäre, sind bessere Kandidaten für die Komprimierung oder Sicherung.

Es ist nicht empfehlenswert, das Dateisystem manuell zu bereinigen. Der Benutzer weiß möglicherweise nicht, wo sich viele Dateien befinden, oder wie Sie erkennen können, welche Dateien sicher entfernt werden können. Außerdem besteht das Risiko, dass der Benutzer wichtige Dateien löscht.

In diesem Thema werden die folgenden Facetten des datenträgercleanupdienstprogramms erläutert.

-   [Das Hilfsprogramm zur Windows-Datenträger Bereinigung](#the-windows-disk-cleanup-utility)
-   [Implementierungs Grundlagen](#implementation-basics)
    -   [Initialisieren/initializeex](#initializeinitializeex)
    -   [Getspaceused](#getspaceused)
    -   [ShowProperties](#showproperties)
    -   [Bereinigen](#purge)
    -   [Deaktivieren](#deactivate)
-   [Registrieren eines Laufwerks Bereinigungs Handlers](#registering-a-disk-cleanup-handler)
    -   [Registrieren der CLSID eines Handlers](#registering-a-handlers-clsid)
    -   [Registrieren eines Handlers beim datenträgercleanupmanager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registrieren eines Handlers beim datenträgercleanupmanager: Windows 2000 oder höher](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Verwenden des datadrivencleaner-Objekts](#using-the-datadrivencleaner-object)
    -   [Beispiel Registrierung eines Laufwerks Bereinigungs Handlers](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>Das Hilfsprogramm zur Windows-Datenträger Bereinigung

Ab Windows 98 umfasst das Windows-Betriebssystem eine Datenträger Bereinigung, ein Dienstprogramm, mit dem der Benutzer den verfügbaren Festplatten Speicherplatz leichter verwalten kann. Das Hilfsprogramm für die Datenträger Bereinigung ist so konzipiert, dass so viel Speicherplatz wie möglich freigegeben und das Risiko verringert wird, dass der Benutzer wesentliche Dateien versehentlich löscht.

Die Datenträger Bereinigung kann auf drei Arten initiiert werden.

-   Der Benutzer kann die Datenträger Bereinigung durch Klicken auf **Start starten**. zeigen auf **Alle Programme**, **Zubehör** und **System Tools**; und klicken Sie dann auf Datenträger **Bereinigung**.
-   Das System benachrichtigt den Benutzer mit einem Meldungs Feld, dass nicht verwendeter Speicherplatz den kritischen Modus erreicht hat. Der Schwellenwert für den kritischen Modus für ein Laufwerk, das größer als 2,25 Gigabyte (GB) ist, beträgt 200 Megabyte (MB). Nachfolgende Warnungen werden bei 80, 50 und 1 MB angegeben. Der Benutzer hat die Möglichkeit, den Speicherplatz manuell freizugeben oder das Hilfsprogramm zum Bereinigen des Datenträgers zu starten.
-   Der Benutzer kann den Assistenten für geplante Aufgaben in Windows (als Wartungs-Assistent auf älteren Systemen bezeichnet) ausführen, um das Hilfsprogramm für die Datenträger Bereinigung automatisch zu den geplanten Zeiten auszuführen.

Die grundlegende Herausforderung in der Datenträger Bereinigung besteht darin, so viel Speicherplatz wie möglich freizugeben, ohne wichtige Dateien zu löschen. Da keine Standardmethode zum Markieren von Dateien für die Bereinigung vorhanden ist, kann keine einzelne Anwendung alle nicht wichtigen Dateien zuverlässig erkennen und bereinigen. Das Hilfsprogramm zur Datenträger Bereinigung löst dieses Problem, indem der Bereinigungs Vorgang zwischen einem einzelnen Datenträger *Bereinigungs Manager* und einer Sammlung von Datenträger *Bereinigungs Handlern* aufgeteilt wird.

Wenn das Hilfsprogramm zum Bereinigen des Datenträgers ausgeführt wird, wird dem Benutzer das folgende Dialogfeld angezeigt. (Wenn auf dem Computer mehr als ein Datenträger oder eine Datenträger Partition vorhanden ist, wird der Benutzer zuerst aufgefordert, ein Laufwerk auszuwählen, bevor dieses Dialogfeld angezeigt wird.)

![Screenshot des Dialog Felds "bereinigen"](images/cleanup1.png)

Der datenträgercleanupmanager ist Teil des Betriebssystems. Daraufhin wird das Dialogfeld angezeigt, das in der obigen Abbildung angezeigt wird, Benutzereingaben behandelt und den Cleanupvorgang verwaltet. Die tatsächliche Auswahl und Bereinigung nicht benötigter Dateien erfolgt durch die einzelnen Datenträger Bereinigungs Handler, die im Listenfeld Datenträgerbereinigungs-Manager angezeigt werden. Der Benutzer hat die Möglichkeit, einzelne Handler zu aktivieren oder zu deaktivieren, indem er in der Benutzeroberfläche des Datenträger Bereinigungs-Managers das entsprechende Kontrollkästchen aktiviert oder deaktiviert.

Jeder Handler ist für einen klar definierten Satz von Dateien verantwortlich. Beispielsweise ist der ausgewählte Handler in der Abbildung für das Bereinigen heruntergeladener Programmdateien zuständig. Der in der Abbildung ausgewählte Handler bietet auch eine Schaltfläche **Dateien anzeigen** . Durch Klicken auf die Schaltfläche kann der Benutzer anfordern, dass der Handler eine Benutzeroberfläche anzeigt, in der Regel ein Windows-Explorer-Fenster, in dem der Benutzer angeben kann, welche Dateien oder Klassen von Dateien bereinigt werden sollen.

Obwohl Windows eine Reihe von Datenträger Bereinigungs Handlern enthält, sind Sie nicht für die Verarbeitung von Dateien konzipiert, die von anderen Anwendungen erstellt wurden. Stattdessen ist der datenträgercleanupmanager so konzipiert, dass er flexibel und erweiterbar ist, indem jeder Entwickler einen eigenen Datenträger Bereinigungs Handler implementieren und registrieren kann. Alle Entwickler können die verfügbaren Datenträger Bereinigungs Dienste durch Implementieren und Registrieren eines Laufwerks Bereinigungs Handlers erweitern.

Alle Anwendungen, die temporäre Dateien entwickeln, können einen Datenträger Bereinigungs Handler implementieren und registrieren. Auf diese Weise erhalten Benutzer eine bequeme und zuverlässige Möglichkeit, die temporären Dateien der Anwendung zu verwalten. Wenn Sie den Handler implementieren, können Sie entscheiden, welche Dateien betroffen sind, und bestimmen, wie der tatsächliche Bereinigung ausgeführt wird.

## <a name="implementation-basics"></a>Implementierungs Grundlagen

Bereinigungs Handler sind in-Process-Server Component Object Model (com)-Objekten. Windows stellt ein vorhandenes Handlerobjekt mit dem Namen datadrivencleaner zur Verwendung zur Verfügung. Sie können auch selbst einen Handler implementieren, um mehr Flexibilität zu erzielen. Mit diesen Objekten können Sie angeben, wie Dateien ausgewählt und Speicherplatz freigegeben werden. im Fall eines implementierten Handlers wird die optionale Benutzeroberfläche für eine präzisetere Steuerung angezeigt. In diesem Abschnitt wird das Implementieren eines eigenen Handlers behandelt. Ausführliche Informationen zur Verwendung des datadrivencleaner-Objekts finden Sie unter [Verwenden des datadrivencleaner-Objekts](#using-the-datadrivencleaner-object).

Ein Datenträger Bereinigungs Handler sollte diese fünf grundlegenden Aufgaben ausführen.

-   Initialisieren Sie das Handlerobjekt.
-   Scannen Sie den Datenträger, um zu ermitteln, wie viel Speicherplatz freigegeben werden kann.
-   Zeigen Sie die Benutzeroberfläche an, um Benutzer Feedback zu den zu bereinigen Dateien zu erhalten. (Optional)
-   Führen Sie die Bereinigung durch.
-   Herunterfahren.

Damit der Datenträger Bereinigungs-Manager diese Aufgaben verwalten kann, muss ein Handler entweder [**iemptyvolumecache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) für Windows 98 oder [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) for Windows Millennium Edition (Windows Me), Windows 2000 und Windows XP exportieren. Da **IEmptyVolumeCache2** von **iemptyvolumecache** erbt und nur die zusätzliche **initializeex**-Methode hinzufügt, ist relativ wenig zusätzlicher Arbeitsaufwand erforderlich, um beides zu implementieren. Wenn der Handler nur für eines dieser Betriebssysteme vorgesehen ist, sollte er beide Schnittstellen exportieren.

Um diese Schnittstellen zu exportieren, müssen Sie diese Methoden implementieren, die den fünf grundlegenden Aufgaben entsprechen.

-   [Initialisieren/initializeex](#initializeinitializeex)
-   [Getspaceused](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Bereinigen](#purge)
-   [Deaktivieren](#deactivate)

### <a name="initializeinitializeex"></a>Initialisieren/initializeex

Die beiden Initialisierungs Methoden, die sehr ähnlich sind, werden aufgerufen, wenn das Hilfsprogramm für die Datenträger Bereinigung ausgeführt wird. Der Windows 98 Disk Bereinigung Manager ruft die [**iemptyvolumecache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) -Methode eines Handlers auf. Bei der Windows Millennium Edition (Windows Me), Windows 2000 oder dem Windows XP-Datenträger Bereinigungs-Manager wird jedoch zunächst versucht, [**IEmptyVolumeCache2:: initializeex**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) aufrufend und nur **iemptyvolumecache:: Initialize** zu verwenden, wenn [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) vom Handler nicht verfügbar gemacht wird. Der datenträgercleanupmanager übergibt Informationen an die-Methode, z. b. den Registrierungsschlüssel des Handlers und das Datenträger Volume, das bereinigt werden soll.

Beide Methoden können verschiedene Anzeige Zeichenfolgen zurückgeben und ein oder mehrere Flags festlegen. Der Hauptunterschied zwischen den beiden Methoden besteht darin, wie der im Datenträger Bereinigungs-Manager angezeigte Text behandelt wird. Die folgenden drei Zeichen folgen sind betroffen.



| String       | Zweck                                                                            | Initialisieren                                                                           | Initializeex                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Anzeigename | Der Name des Handlers, der im Listenfeld Datenträgerbereinigungs-Manager angezeigt wird.               | Wenn *ppwszdisplayname* **null** ist, wird der Standardwert aus der Registrierung abgerufen. | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszdisplayname* angegeben werden, ohne dass Registrierungs Werte verwendet werden. |
| BESCHREIBUNG  | Beschreibender Text, der unter dem Listenfeld angezeigt wird, wenn der Name des Handlers ausgewählt ist. | Wenn *ppwszdescription* den Wert **null** hat, wird der Standardwert aus der Registrierung abgerufen. | In *ppwszdescription* muss eine ordnungsgemäß lokalisierte Zeichenfolge angegeben werden, da keine Registrierungs Werte verwendet werden. |
| Schaltflächentext  | Text für die optionale Schaltfläche, mit der Benutzer die Benutzeroberfläche des Handlers anzeigen können.        | Es ist kein Parameter verfügbar. Muss in der Registrierung angegeben werden.                           | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszbtntext* angegeben werden. es werden keine Registrierungs Werte verwendet.     |



 

Der *pdwflags* -Parameter, der in beiden Initialisierungs Methoden gefunden wird, erkennt denselben Satz von Flags. Zwei dieser Flags werden vom Datenträger Bereinigungs-Manager an die-Methode übermittelt.

-   **eVCF \_ settingsmode**

    Wenn der datenträgercleanupmanager nach einem Zeitplan ausgeführt wird, wird das Flag " **eVCF \_ settingsmode** " festgelegt. Wenn dieses Flag festgelegt ist, ruft der datenträgercleanupmanager nicht die Methoden [getspaceused](#getspaceused), [Purge](#purge)oder [showProperties](#showproperties) auf. Die [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) -Methode oder die [**initializeex**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) -Methode des Handlers muss alle Aufgaben verarbeiten, die normalerweise von [**getspaceused**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) und [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge)ausgeführt werden. Da es keine Gelegenheit für Benutzer Feedback gibt, sollten nur die Dateien berührt werden, die äußerst sicher zu bereinigen sind. Sie sollten den *pcwszvolume* -Parameter der Initialisierungs Methode ignorieren und nicht benötigte Dateien bereinigen, unabhängig davon, auf welchem Laufwerk Sie sich befinden.

-   **eVCF- \_ ouesfile Disk Space**

    Wenn das **eVCF-Flag " \_ ouchangspace** " festgelegt ist, ist der Speicherplatz auf dem Datenträger des Benutzers äußerst kurz. Der Handler sollte beim Löschen von Dateien aggressiv sein, auch wenn er zu einem Leistungsverlust führt. Der Handler sollte jedoch offensichtlich keine Dateien löschen, die dazu führen, dass eine Anwendung fehlschlägt oder wenn der Benutzerdaten verliert.

Die verbleibenden Flags werden vom Datenträger Bereinigungs Handler festgelegt und an den Datenträger Bereinigungs Manager zurückgegeben. Weitere Informationen finden Sie auf den Referenzseiten der-Methode für [**iemptyvolumecache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) und [**IEmptyVolumeCache2:: initializeex**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   eVCF \_ dontshowif Zero

    Zeigen Sie den Handler nur im Listenfeld Datenträger Bereinigungs-Manager an, wenn der von [**getspaceused**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) zurückgegebene Wert angibt, dass der Handler Speicherplatz freigeben kann.

-   eVCF \_ enablebydefault

    Gibt an, dass der Handler standardmäßig aktiviert ist. Es wird jedes Mal ausgeführt, wenn eine Datenträger Bereinigung durchgeführt wird, wenn der Benutzer das Kontrollkästchen in der Liste der Handler des Datenträgerbereinigungs-Managers deaktiviert.

-   eVCF \_ enablebydefault \_ Auto

    Gibt an, dass der Handler für die Ausführung bei geplanten Cleanups automatisch aktiviert wird.

-   eVCF- \_ hassettings

    Legen Sie dieses Flag fest, wenn Ihr Handler eine Benutzeroberfläche für die Anzeige hat. In der Antwort zeigt der Datenträger Bereinigungs-Manager eine Schaltfläche an, wenn dieser Handler im Listenfeld ausgewählt ist. Wenn auf diese Schaltfläche geklickt wird, ruft der Datenträger Bereinigungs-Manager [**showProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties)auf.

-   eVCF \_ RemoveFromList

    Löschen Sie den Namen des Handler aus der Liste der verfügbaren Handler, nachdem der Handler einmal ausgeführt wurde. Die Registrierungsinformationen des Handlers werden ebenfalls gelöscht.

### <a name="getspaceused"></a>Getspaceused

Der Datenträgerbereinigungs-Manager ruft diese Methode auf, um zu bestimmen, wie viel Speicherplatz ein Datenträger Bereinigungs Handler Der datenträgercleanupmanager zeigt diesen Wert dann rechts neben dem Namen des Handlers im Listenfeld an. Dieser Vorgang wird für alle Handler ausgeführt, die beim Datenträger Bereinigungs-Manager registriert sind, wenn der Manager gestartet wird und bevor die Hauptbenutzer Oberfläche des Managers angezeigt wird. Wenn [**getspaceused**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) aufgerufen wird, sollte der Handler die für ihn Verantwortlichen Dateien scannen, ermitteln, welche der Bereinigungs Kandidaten sind, und den freien Speicherplatz zurückgeben.

Da das Scannen ein langwieriger Prozess sein kann, verwendet der datenträgercleanupmanager den *PICB* -Parameter dieser Methode, um einen Zeiger auf eine [**iemptyvolumecachecallback**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) -Schnittstelle zu übergeben. Der Handler verwendet die-Schnittstelle in regelmäßigen Abständen während der Überprüfung, um [**iemptyvolumecachecallback:: scanprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)aufzurufen. Dies dient zwei Zwecken.

-   Ermöglicht dem datenträgercleanupmanager, eine Statusanzeige zu aktualisieren, um den Benutzer darüber zu informieren, wie der Scanvorgang voranschreitet.
-   Benachrichtigt den Handler, den Scanvorgang zu beenden, wenn auf die Schaltfläche **Abbrechen** des Fortschritts Fensters geklickt wird. Dieses Schaltflächen Ereignis wird nicht direkt an den Handler übermittelt. Stattdessen gibt der datenträgercleanupmanager E \_ Abort zurück, wenn [**getspaceused**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) das nächste Mal [**iemptyvolumecachecallback:: scanprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)aufruft.

### <a name="showproperties"></a>ShowProperties

Vor dem Bereinigung kann der Handler eine Benutzeroberfläche in der Regel in Form eines Windows-Explorer-Fensters anzeigen, mit dem Benutzer eine Liste der Dateien oder Klassen von Dateien anzeigen können, die vom Handler für die Bereinigung ausgewählt wurden. Wenn der Handler beim Aufrufen von [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) oder [**initializeex**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) das eVCF-Flag " **\_ hassettings** " festlegt, kann der Benutzer die Benutzeroberfläche anfordern, indem er im Datenträger Bereinigungs-Manager auf die für diesen Zweck angezeigte Schaltfläche klickt. Der Schaltflächen Text variiert von Handler zu Handler, aber "Dateien anzeigen", "Seiten anzeigen" und "Optionen" sind gängige Bezeichnungen.

Wenn auf die Schaltfläche geklickt wird, ruft der Datenträger Bereinigungs-Manager [**showProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) auf, um den Handler aufzufordern, die Benutzeroberfläche anzuzeigen. Die Benutzeroberfläche sollte als untergeordnetes Element des Fensters erstellt werden, dessen Handle in den *HWND* -Parameter der **showProperties** -Methode übergeben wird.

### <a name="purge"></a>Bereinigen

Der Datenträger Bereinigungs [**-Manager**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) Ruft die Löschmethode des Handlers auf, um die Bereinigung in Motion festzulegen. Der *PICB* -Parameter der Methode ist ein Zeiger auf die [**iemptyvolumecachecallback**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) -Schnittstelle des Datenträgerbereinigungs-Managers. Wie bei der [**getspaceused**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) -Methode sollte der Handler die Rückruf Schnittstelle regelmäßig verwenden, um den Fortschritt zu melden und den Datenträger Bereinigungs-Manager abzufragen, ob der Benutzer auf **Abbrechen** geklickt hat. Beachten Sie jedoch, dass **die Lösch** Methode [**iemptyvolumecachecallback aufrufen muss::P urgeprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress), nicht [**scanprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="deactivate"></a>Deaktivieren

Die Deaktivierungs Methode wird aufgerufen, wenn der Datenträger Bereinigungs- [**Manager das herunter**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) fahren vorbereitet. Der Handler sollte alle benötigten Bereinigungs Aufgaben ausführen und zurückgeben. Wenn Sie nicht möchten, dass der Handler erneut ausgeführt wird, legen Sie das **eVCF \_ RemoveFromList** -Flag im *pdwflags* -Parameter der Initialisierungs Methode fest. Wenn dieses Flag festgelegt ist, entfernt der datenträgercleanupmanager den Handler aus der Liste und löscht die Registrierungseinträge des Handlers. Sie müssen die Registrierungseinträge erneut hinzufügen, um den Handler erneut auszuführen. Dieses Flag wird in der Regel für Handler verwendet, die nur einmal ausgeführt werden.

## <a name="registering-a-disk-cleanup-handler"></a>Registrieren eines Laufwerks Bereinigungs Handlers

Zum Hinzufügen eines Handlers zur Liste der Datenträger Bereinigungs-Manager müssen bestimmte Schlüssel und Werte der Windows-Registrierung hinzugefügt werden.

-   [Registrieren der CLSID eines Handlers](#registering-a-handlers-clsid)
-   [Registrieren eines Handlers beim datenträgercleanupmanager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registrieren eines Handlers beim datenträgercleanupmanager: Windows 2000 oder höher](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Verwenden des datadrivencleaner-Objekts](#using-the-datadrivencleaner-object)
-   [Beispiel Registrierung eines Laufwerks Bereinigungs Handlers](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrieren der CLSID eines Handlers

Wie bei allen COM-Objekten müssen die GUID und die DLL des Handlerobjekts unter dem **CLSID** -Schlüssel in **HKEY \_ Classes \_ root** registriert werden. Sie können auch ein Symbol registrieren, das neben dem Namen des Handlers im Listenfeld Datenträgerbereinigungs-Manager angezeigt wird. Dies ist jedoch optional. Im folgenden Beispiel werden die Schlüssel, Werte und Daten gezeigt, die beteiligt sind.

```
HKEY_CLASSES_ROOT
   CLSID
      Handler's GUID
         DefaultIcon
            (Default) = Handler's Icon Path, Icon Index
         InprocServer32
            (Default) = Handler's DLL path
            ThreadingModel = Apartment
```

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registrieren eines Handlers beim datenträgercleanupmanager: Allgemein

Um die Registrierung abzuschließen, muss ein Handler einen Schlüssel mit seinen Besonderheiten hinzufügen, wie hier gezeigt. Im restlichen Teil dieses Abschnitts wird der Inhalt dieses Schlüssels behandelt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Handler's Key
```

Im Allgemeinen wird der Name des Schlüssels, der die Details eines Handlers enthält, für den Dateityp benannt, den er verarbeitet, z. b. **heruntergeladene Programmdateien**, dies ist jedoch nicht zwingend erforderlich. In der folgenden Tabelle sind die möglichen Werte aufgeführt, die unter diesem Schlüssel gefunden werden.

> [!Note]  
> Nur der Standardwert, der den Klassen Bezeichner (CLSID) des Handlers angibt, ist erforderlich, alle anderen Werte sind optional.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>type</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Standard</td>
<td>REG_SZ</td>
<td>Die CLSID des Handlers, die unter <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>registriert ist.</td>
</tr>
<tr class="even">
<td>Advancedbuttontext</td>
<td>REG_SZ</td>
<td>Text für die optionale Schaltfläche, auf die Benutzer klicken können, um die Benutzeroberfläche des Handlers anzuzeigen. Das & Zeichen kann vor einem Zeichen platziert werden, um eine Tastenkombination für die Schaltfläche zuzuweisen. Der advancedbuttontext-Wert wird von Handlern ignoriert, die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: initializeex</strong></a>verfügbar machen.</td>
</tr>
<tr class="odd">
<td>Cleanupstring</td>
<td>REG_SZ</td>
<td>Befehlszeile, die eine ausführbare Datei und optionale Befehlszeilenparameter angibt. Diese Befehlszeile wird nach Abschluss der Datenträger Bereinigung ausgeführt.</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>Ein System unabhängiger Bezeichner für einen speziellen Ordner, der in die Dateisuche einbezogen werden soll. Dieser Wert muss als numerischer Wert eingegeben werden, z. b. 0x0000001c anstelle CSIDL_LOCAL_APPDATA. Eine Liste möglicher Werte finden Sie unter <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Es kann nur ein einziger Wert verwendet werden.<br/> Wenn der Ordner Wert angegeben wird, wird der durch den CSIDL-Wert angegebene Speicherort diesen Informationen vorangestellt, um einen Suchpfad zu erstellen. Sehen Sie sich beispielsweise das folgende Szenario an.<br/>
<ul>
<li>Der CSIDL-Wert wird als 0x0000000d (CSIDL_MYMUSIC) angegeben.</li>
<li>Ihr eigener Musik Ordner befindet sich unter "c:\Dokumente und Einstellungen \<em>Benutzername</em>\Eigene Musik".</li>
<li>Der Ordner Wert enthält " &quot; jazz\singers".&quot;</li>
</ul>
Das Ergebnis dieses Szenarios besteht darin, dass der datenträgercleanuphandler den Ordner "c:\Dokumente und Einstellungen \<em>Benutzername</em>\Eigene music\jazz\singers" durchsucht. Beachten Sie, dass der Schrägstrich vor dem Ordner Wert hinzugefügt wird, wenn er nicht vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td>BESCHREIBUNG</td>
<td>REG_SZ</td>
<td>Beschreibender Text, der unter dem Listenfeld Datenträger Bereinigungs-Manager angezeigt wird, wenn der Name des Handlers ausgewählt ist. Hier können Sie erläutern, was der Handler tut, für welche Dateien er sich bezieht, und alle anderen Informationen, die dem Benutzer erklärt werden. Wenn <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: initializeex</strong></a> nicht vom Handler verfügbar gemacht wird, kann dieser Text durch die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>iemptyvolumecache:: Initialize</strong></a> -Methode des Handlers überschrieben werden, indem beim Aufruf der-Methode eine Alternative Zeichenfolge im <em>ppwszdescription</em> -Parameter angegeben wird.</td>
</tr>
<tr class="even">
<td>Anzeige</td>
<td>REG_SZ</td>
<td>Der Name des Handlers, der im Listenfeld Datenträgerbereinigungs-Manager angezeigt werden soll. Wenn <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: initializeex</strong></a> nicht vom Handler verfügbar gemacht wird, kann dieser Text durch die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>iemptyvolumecache:: Initialize</strong></a> -Methode des Handlers überschrieben werden, indem eine Alternative Zeichenfolge im <em>ppwszdisplayname</em> -Parameter angegeben wird, wenn die-Methode aufgerufen wird.</td>
</tr>
<tr class="odd">
<td>FileList</td>
<td>REG_SZ oder REG_MULTI_SZ</td>
<td>Eine Liste der Dateien, die von diesem Handler gesucht und bereinigt wurden. Sie können Platzhalter mithilfe von angeben. oder * Zeichen. Wenn der Wert vom Typ REG_SZ ist, werden mehrere Erweiterungen mithilfe von | oder: Zeichen, ohne Leerzeichen auf beiden Seiten.<br/> Wenn das DDEVCF_REMOVEDIRS-Flag im Flags-Wert festgelegt ist, können diese Werte Verzeichnisnamen und Dateien angeben.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Flags, die Elemente der Such-und Reinigungs Prozedur steuern. Einer oder mehrere der folgenden Werte.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Rekursiv suchen und entfernen.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Nachdem der Handler einmal ausgeführt wurde, entfernen Sie ihn aus der Registrierung.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn Sie schreibgeschützt sind.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Entfernen Sie Dateien, die die Suchkriterien erfüllen, selbst wenn es sich um Systemdateien handelt.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn es sich um verborgene Dateien handelt.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Dieser Handler sollte im Datenträger Bereinigungs-Manager nicht angezeigt werden, wenn keine Dateien mit den Suchkriterien übereinstimmen.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Vergleichen Sie den FileList-Wert mit Verzeichnissen, und entfernen Sie die Übereinstimmungen und alle zugehörigen Unterverzeichnisse.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Führen Sie diesen Handler nur aus, wenn der verfügbare Speicherplatz unter den kritischen Wert gefallen ist, der vom datenträgercleanupmanager festgelegt wurde, indem Sie das EVCF_OUTOFDISKSPACE-Flag über <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>iemptyvolumecache:: Initialize</strong></a> oder <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: initializeex</strong></a>festlegen</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Entfernen Sie das übergeordnete Verzeichnis der angegebenen Dateien, nachdem der Reinigungsprozess ausgeführt wurde.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Verwenden Sie ggf. den LastAccess-Wert, um die zu bereinigenden Dateien zu ermitteln. Dieses Flag wird ignoriert, wenn Sie den <a href="#using-the-datadrivencleaner-object">datadrivencleaner</a> -Wert verwenden, sofern der angegebene LastAccess-Wert immer verwendet wird.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ordner</td>
<td>REG_SZ, REG_MULTI_SZ oder REG_EXPAND_SZ</td>
<td>Ein bestimmter Ordner oder Ordner, in dem nach Elementen gesucht wird, die mit Einträgen im filelist-Wert übereinstimmen. Sie können Platzhalter mithilfe von angeben. oder * Zeichen. Wenn der Wert vom Typ REG_SZ ist, werden mehrere Ordnernamen mithilfe von | ohne Leerzeichen auf beiden Seiten.<br/> Wenn ein CSIDL-Wert vorhanden ist, kann nur ein Ordner in diesem Wert angegeben werden. Der durch den CSIDL-Wert festgestellte Speicherort wird diesem Ordner Pfad vorangestellt, um einen Suchpfad zu erstellen. Ein Beispiel finden Sie in der Beschreibung des CSIDL-Werts.<br/> Wenn dieser Wert unter Windows Vista Service Pack 1 (SP1) und höher fehlt, wird der Bereinigungs Handler ignoriert und gibt S_FALSE bei der Initialisierung zurück.<br/> Wenn dieser Wert in der ursprünglichen Version von Windows Vista und früher fehlt, wird der Stamm Ordner des aktuellen Volumes verwendet. Das DDEVCF_DOSUBDIRS-Flag ist in diesem Fall erforderlich, um das gesamte Laufwerk zu durchsuchen. Ohne diese wird nur der Stamm Ordner durchsucht.<br/> Ein Laufwerk oder Laufwerke müssen angegeben werden. Dies kann über den CSIDL-Wert oder über eine REG_EXPAND_SZ Zeichenfolge bereitgestellt werden. Wenn Sie diese Optionen nicht angeben, muss das zu durchsuchende Laufwerk jedoch im Ordnernamen angegeben werden. Verwenden Sie?:, um den Ordner auf dem aktuellen Laufwerk zu durchsuchen.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ oder REG_EXPAND_SZ</td>
<td>Der Pfad zu der Ressource, von der ein Symbol abgerufen werden soll, das in Verbindung mit dem Handler verwendet werden soll.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Die Anzahl der Tage, die seit dem letzten Zugriff auf eine Datei verstrichen sein müssen, oder für diese Datei oder dieses Verzeichnis wurde ein Verzeichnis erstellt, das für die Bereinigung in Erwägung gezogen werden soll.</td>
</tr>
<tr class="even">
<td>Priorität</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Bestimmt die Reihenfolge, in der der Handler in Bezug auf andere Handler ausgeführt wird. Je höher die Zahl, desto weiter oben in dem Prozess, den der Handler ausführt. Es ist kein definierter Bereich vorhanden. eine beliebige Zahl ist zulässig.</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>Die CLSID einer Ressource, mit der lokalisierter Text für den anzeigen Amen, die Beschreibung und den Schaltflächen Text bereitgestellt wird. Diese Ressource ist in Situationen nützlich, in denen <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>iemptyvolumecache</strong></a> von einem Handler nicht implementiert wird und der Handler unter Microsoft Windows NT oder Windows XP ausgeführt wird.<br/> Der datenträgercleanupmanager überprüft zunächst, ob die Initialisierungs Routine des Handlers diese Zeichen folgen zurückgegeben hat, wie es bei der Implementierung von <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> der Fall wäre. Wenn ein Fehler auftritt, wechselt der Manager als nächstes zu einem Eigenschaften Behälter mit dem Namen in diesem Wert. Wenn keine Angabe erfolgt ist, wird der Text aus der Registrierung abgerufen.<br/></td>
</tr>
<tr class="even">
<td>Stateflags</td>
<td>REG_DWORD</td>
<td>Durch Ausführen der ausführbaren Datei des datenträgercleanupmanagers Cleanmgr.exe von einer Befehlszeile aus können Sie Bereinigungs <em>profile</em>deklarieren. Diese Profile bestehen aus einer Teilmenge der verfügbaren Handler und erhalten eine eindeutige numerische Bezeichnung. Dies ermöglicht es Ihnen, die Ausführung verschiedener Sätze von Handlern zu unterschiedlichen Zeiten zu automatisieren.<br/> Die Befehlszeile &quot;cleanmgr.exe/sageset:<strong>nnnn</strong> &quot; , wobei <strong>nnnn</strong> eine eindeutige numerische Bezeichnung ist, zeigt eine Benutzeroberfläche an, die es Ihnen ermöglicht, die in dieses Profil einzuschließenden Handler auszuwählen. Ebenso wie das Profil definiert, schreibt der sageset-Parameter auch einen Wert mit dem Namen stateflags<strong>nnnn</strong>, wobei <strong>nnnn</strong> die Bezeichnung ist, die Sie im-Parameter für alle Unterschlüssel unter <strong>VolumeCaches</strong>verwendet haben. Es gibt zwei mögliche Datenwerte für diese Einträge.
<ul>
<li>0: führen Sie diesen Handler nicht aus, wenn dieses Profil ausgeführt wird.</li>
<li>2: diesen Handler einschließen, wenn dieses Profil ausgeführt wird.</li>
</ul>
<br/> Nehmen wir beispielsweise an, dass die Befehlszeile &quot;cleanmgr.exe/sageset: 1234 &quot; ausgeführt wird. In der angezeigten Benutzeroberfläche wählt der Benutzer <strong>heruntergeladene Programmdateien</strong>aus, wählt jedoch keine <strong>temporären Internet Dateien</strong>aus. Anschließend werden die folgenden Werte in die Registrierung geschrieben.<br/>
<pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Downloaded Program Files
                        StateFlags1234 = 0x00000002
                     Internet Cache Files
                        StateFlags1234 = 0x00000000</code></pre>
<br/> Die Befehlszeile &quot;cleanmgr.exe/sagerun:<strong>nnnn</strong> &quot; , bei der der Wert von <strong>nnnn</strong> mit der mit dem sageset-Parameter deklarierten Bezeichnung übereinstimmt, führt alle in diesem Profil ausgewählten Handler aus.<br/> Ein generischer stateflags-Wert wird in die Registrierung geschrieben, wenn die Datenträger Bereinigung normal ausgeführt wird. Dieser Wert speichert einfach den Zustand (aktiviert oder deaktiviert) des Handlers, der das letzte Mal als Option für den Benutzer angezeigt wurde. Es gibt zwei mögliche Datenwerte für diese Einträge.
<ul>
<li>0: der Handler wurde nicht ausgewählt.</li>
<li>1: der Handler wurde ausgewählt.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrieren eines Handlers beim datenträgercleanupmanager: Windows 2000 oder höher

Das Angeben von Anzeige Text in der Registrierung kann die Lokalisierung von Software erschweren. Aus diesem Grund unterstützen Windows 2000 und Windows XP die [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) -Schnittstelle mit der bevorzugten Initialisierungs Methode [**initializeex**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). Unter Windows 2000 oder höher wird immer versucht, **IEmptyVolumeCache2:: initializeex** vor [**iemptyvolumecache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize)aufzurufen. Das System verwendet **initialisieren** nur zum Initialisieren eines Handlers, wenn **IEmptyVolumeCache2** nicht verfügbar gemacht wird.

Im Hinblick auf die Registrierung ist der einzige Unterschied unter Windows 2000 oder höher, dass Sie die Werte advancedbuttontext, Display und Description weglassen können, wenn [**IEmptyVolumeCache2:: initializeex**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) vom Handler verfügbar gemacht wird. Diese Werte, die ordnungsgemäß lokalisierten Text enthalten, werden für den Datenträger Bereinigungs Manager bereitgestellt, wenn **initializeex** aufgerufen wird.

### <a name="using-the-datadrivencleaner-object"></a>Verwenden des datadrivencleaner-Objekts

Ein grundlegender datenträgercleanuphandler, der als datadrivencleaner bezeichnet wird, wird vom Betriebssystem bereitgestellt. Wenn Sie dieses Objekt als Handler verwenden möchten, anstatt es zu implementieren, verwenden Sie die CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} als Standardwert für den Unterschlüssel des Handlers in **VolumeCaches** , wie unter [Registrieren eines Handlers beim datenträgercleanupmanager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)beschrieben.

Datadrivencleaner macht [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)nicht verfügbar, sodass die Anzeige-und Beschreibungs Werte über die Registrierung bereitgestellt werden. Beachten Sie beim Deklarieren dieser Zeichen folgen, dass dies Lokalisierungs Probleme verursachen kann. Lokalisierter Text kann über den PropertyBag-Wert bereitgestellt werden. Der advancedbuttontext-Wert wird ignoriert, da keine Benutzeroberfläche und somit keine Schaltfläche zur Anzeige verfügbar ist.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Beispiel Registrierung eines Laufwerks Bereinigungs Handlers

Im folgenden finden Sie ein Beispiel für die Registrierung eines Laufwerks Bereinigungs Handlers, der vom Telefonunternehmen implementiert wird. Dieser Handler implementiert sowohl [**iemptyvolumecache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) als auch [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)und bietet daher advancedbuttontext-, Description-und Display-Werte für den Fall, dass er auf einem Computer verwendet wird, auf dem Windows 98 ausgeführt wird. Der Handler kombiniert die CSIDL-und Ordner Werte, um Dateien in den C:- \\ Programmdateien im temporären Verzeichnis des Phone-Unternehmens zu suchen \\ \\ . das Flag ddevcf \_ dosubdirs ist so festgelegt, dass auch die zugehörigen Unterverzeichnisse durchsucht werden. Nur die Dateien mit tmp-und TPC-Erweiterungen werden für die Bereinigung berücksichtigt, und das private ddevcf- \_ \_ Flag "LastAccess" ist so festgelegt, dass aus diesen Dateien nur diejenigen berücksichtigt werden, auf die mindestens 14 Tage lang nicht zugegriffen wurde. Das Flag ddevcf \_ dontshowif Zero ist ebenfalls so festgelegt, dass der Handler nicht in der Liste angezeigt wird, wenn keine Bereinigungs Kandidaten gefunden wurden.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     The Phone Company Files
                        (Default) = {the CLSID GUID}
                        AdvancedButtonText = &View Files
                        CleanupString = c:\tpc.exe
                        CSIDL = 0x00000026
                        Description = Old temporary files.
                        Display = The Phone Company Files
                        FileList = *.tmp|*.tpc
                        Flags = 0x10000021
                        Folder = \The Phone Company\Temp
                        IconPath = c:\Program Files\The Phone Company\tpc.dll,2
                        LastAccess = 0x0000000e
                        Priority = 200
                        PropertyBag = {Property Bag CLSID GUID}
```

 

