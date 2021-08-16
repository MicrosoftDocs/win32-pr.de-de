---
title: Erstellen eines Datenträgerbereinigungshandlers
description: Ein Axiom, das sich in der Welt der Computer immer wieder bewährt hat, ist, dass sie unabhängig von der Größe der Speicherkapazität Ihres Computers letztendlich aufgefüllt werden.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- Datenträgerbereinigungshandler
- Datenträgerbereinigung
- DataDrivenCleaner
- Register, Datenträgerbereinigungshandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ce7fc96e16cb27168e00196b65d48d378758a47594122cca978dc1a1f4de94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479893"
---
# <a name="creating-a-disk-cleanup-handler"></a>Erstellen eines Datenträgerbereinigungshandlers

Ein Axiom, das sich in der Welt der Computer immer wieder bewährt hat, ist, dass sie unabhängig von der Größe der Speicherkapazität Ihres Computers letztendlich aufgefüllt werden. Während die durchschnittliche Größe der Festplatte eines Computers im Laufe der Zeit erheblich angestiegen ist, sind die Anwendungen ebenfalls entsprechend gestiegen, sodass Benutzer nach Möglichkeiten suchen, mehr freien Festplattenspeicher zu erstellen. Der verfügbare Speicherplatz wird auch durch die vielen temporären Dateien reduziert, die Anwendungen aus Sicherungs- oder Leistungsgründen erstellen. Wenn der Speicherplatz knapp wird, muss der von Anwendungen belegte Speicherplatz reduziert werden. Speicherplatz kann mit einer Vielzahl von Möglichkeiten freigegeben werden, einschließlich der folgenden:

-   Löschen von Dateien.
-   Komprimieren von Dateien.
-   Verschieben von Dateien auf ein Sicherungsmedium.
-   Übertragen von Dateien auf einen Remoteserver.

Dateien, die sich gut für die Bereinigung eignen, sind:

-   Dateien, die der Benutzer nie wieder benötigt.
-   Temporäre Dateien, die nur aus Leistungsgründen vorhanden sind.
-   Dateien, die bei Bedarf von einer Installations-CD wiederhergestellt werden können.
-   Datendateien, die möglicherweise durch neuere Versionen ersetzt wurden, z. B. alte Sicherungsdateien.
-   Ältere Dateien, die seit langem nicht mehr verwendet wurden.

Das Löschen eignet sich besonders für Dateien, die der Benutzer nie wieder benötigt, z. B. Dateien, die aus Leistungsgründen vorübergehend zwischengespeichert werden. Das Löschen eignet sich auch für Dateien, die leicht wiederhergestellt werden können, z. B. Grafikdateien, die von einer Installations-CD neu geladen werden können. Dateien, die der Benutzer möglicherweise später benötigt oder die schwer zu rekonstruieren sind, sind bessere Kandidaten für die Komprimierung oder Sicherung.

Die Erwartung, dass ein Benutzer das Dateisystem manuell bereinigt, ist keine gute Lösung. Der Benutzer weiß möglicherweise nicht, wo sich viele der Dateien befinden oder wie erkannt wird, welche Dateien sicher entfernt werden können. Darüber hinaus besteht das Risiko, dass der Benutzer wichtige Dateien löscht.

Die folgenden Facets des Hilfsprogramms "Datenträgerbereinigung" werden in diesem Thema erläutert.

-   [Das Windows-Hilfsprogramm für die Datenträgerbereinigung](#the-windows-disk-cleanup-utility)
-   [Grundlagen der Implementierung](#implementation-basics)
    -   [Initialize/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [ShowProperties](#showproperties)
    -   [Bereinigen](#purge)
    -   [Deaktivieren](#deactivate)
-   [Registrieren eines Datenträgerbereinigungshandlers](#registering-a-disk-cleanup-handler)
    -   [Registrieren der CLSID eines Handlers](#registering-a-handlers-clsid)
    -   [Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Windows 2000 oder höher](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Verwenden des DataDrivenCleaner-Objekts](#using-the-datadrivencleaner-object)
    -   [Beispielregistrierung eines Datenträgerbereinigungshandlers](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>Das Windows-Hilfsprogramm für die Datenträgerbereinigung

Ab Windows 98 enthält das Windows Betriebssystem die Datenträgerbereinigung, ein Hilfsprogramm, mit dem der Benutzer den verfügbaren Festplattenspeicher viel einfacher verwalten kann. Das Hilfsprogramm "Datenträgerbereinigung" ist so konzipiert, dass so viel Speicherplatz wie möglich freigegeben wird und das Risiko verringert wird, dass der Benutzer versehentlich wichtige Dateien löscht.

Die Datenträgerbereinigung kann auf drei Arten initiiert werden.

-   Der Benutzer kann die Datenträgerbereinigung initiieren, indem er auf **Starten** klickt. Verweisen auf **Alle Programme,** **Zubehör** und **Systemtools**; klicken Sie dann auf **Datenträgerbereinigung.**
-   Das System benachrichtigt den Benutzer mit einem Meldungsfeld, dass nicht verwendeter Speicherplatz den kritischen Modus erreicht hat. Der Schwellenwert für den kritischen Modus für ein Laufwerk, das größer als 2,25 Gigabyte (GB) ist, beträgt 200 MEGABYTE (MB). Nachfolgende Warnungen werden bei 80, 50 und 1 MB ausgegeben. Der Benutzer erhält die Möglichkeit, Speicherplatz manuell frei zu geben oder das Hilfsprogramm "Datenträgerbereinigung" zu starten.
-   Der Benutzer kann den Assistenten für Windows geplanten Task (auf älteren Systemen als Wartungs-Assistent bezeichnet) das Hilfsprogramm für die Datenträgerbereinigung automatisch zu geplanten Zeiten ausführen lassen.

Die grundlegende Herausforderung bei der Datenträgerbereinigung besteht darin, so viel Speicherplatz wie möglich frei zu machen, ohne wichtige Dateien zu löschen. Da es keine Standard-Möglichkeit gibt, Dateien für die Bereinigung zu markieren, kann keine einzelne Anwendung zuverlässig alle unwichtigen Dateien erkennen und bereinigen. Das Hilfsprogramm Datenträgerbereinigung löst dieses Problem, indem es den Bereinigungsvorgang zwischen einem einzelnen *Datenträgerbereinigungs-Manager* und einer Sammlung von *Datenträgerbereinigungshandlern aufteilt.*

Wenn das Hilfsprogramm Datenträgerbereinigung ausgeführt wird, wird dem Benutzer das folgende Dialogfeld angezeigt. (Wenn auf dem Computer mehrere Datenträger oder Datenträgerpartitionen vorhanden sind, wird der Benutzer zunächst aufgefordert, ein Laufwerk auszuwählen, bevor dieses Dialogfeld angezeigt wird.)

![Screenshot des Bereinigungsdialogfelds](images/cleanup1.png)

Der Datenträgerbereinigungs-Manager ist Teil des Betriebssystems. Es zeigt das in der vorherigen Abbildung gezeigte Dialogfeld an, verarbeitet Benutzereingaben und verwaltet den Bereinigungsvorgang. Die tatsächliche Auswahl und Bereinigung nicht benötigter Dateien erfolgt durch die einzelnen Datenträgerbereinigungshandler, die im Listenfeld des Datenträgerbereinigungs-Managers angezeigt werden. Der Benutzer hat die Möglichkeit, einzelne Handler zu aktivieren oder zu deaktivieren, indem er sein Kontrollkästchen in der Benutzeroberfläche des Datenträgerbereinigungs-Managers aktiviert oder deaktiviert.

Jeder Handler ist für einen klar definierten Satz von Dateien verantwortlich. Beispielsweise ist der ausgewählte Handler in der Abbildung für die Bereinigung heruntergeladener Programmdateien verantwortlich. Der in der Abbildung ausgewählte Handler stellt auch die Schaltfläche **Dateien anzeigen** bereit. Durch Klicken auf die Schaltfläche kann der Benutzer anfordern, dass der Handler in der Regel ein Windows Explorer-Fenster anzeigt, in dem der Benutzer angeben kann, welche Dateien oder Klassen von Dateien bereinigt werden sollen.

Obwohl Windows über eine Reihe von Datenträgerbereinigungshandlern verfügt, sind sie nicht für die Verarbeitung von Dateien konzipiert, die von anderen Anwendungen erzeugt werden. Stattdessen ist der Datenträgerbereinigungs-Manager flexibel und erweiterbar, indem jeder Entwickler seinen eigenen Datenträgerbereinigungshandler implementieren und registrieren kann. Jeder Entwickler kann die verfügbaren Datenträgerbereinigungsdienste erweitern, indem er einen Datenträgerbereinigungshandler implementiert und registriert.

Alle Anwendungen, die temporäre Dateien erzeugen, können und sollten einen Datenträgerbereinigungshandler implementieren und registrieren. Auf diese Weise können Benutzer die temporären Dateien der Anwendung bequem und zuverlässig verwalten. Wenn Sie den Handler implementieren, können Sie entscheiden, welche Dateien betroffen sind, und bestimmen, wie die eigentliche Bereinigung erfolgt.

## <a name="implementation-basics"></a>Grundlagen der Implementierung

Bereinigungshandler sind COM-Objekte (In-Process Server Component Object Model). Windows stellt ein vorhandenes Handlerobjekt namens DataDrivenCleaner für Ihre Verwendung bereit. Sie können einen Handler auch selbst implementieren, um mehr Flexibilität zu erhalten. Mit diesen Objekten können Sie dann angeben, wie Sie Dateien auswählen, Speicherplatz freigeben und im Fall eines implementierten Handlers die optionale Benutzeroberfläche für eine präzisere Steuerung anzeigen. In diesem Abschnitt wird die Implementierung eines eigenen Handlers behandelt. Ausführliche Informationen zur Verwendung des DataDrivenCleaner-Objekts finden Sie unter [Verwenden des DataDrivenCleaner-Objekts.](#using-the-datadrivencleaner-object)

Ein Datenträgerbereinigungshandler sollte diese fünf grundlegenden Aufgaben ausführen.

-   Initialisieren Sie das Handlerobjekt.
-   Überprüfen Sie den Datenträger, um zu ermitteln, wie viel Speicherplatz freigegeben werden kann.
-   Zeigen Sie die Benutzeroberfläche an, um Benutzerfeedback dazu zu erhalten, welche Dateien bereinigt werden sollen. (Optional)
-   Durchführen der Bereinigung.
-   Herunterfahren.

Damit der Datenträgerbereinigungs-Manager diese Aufgaben verwalten kann, muss ein Handler entweder [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) für Windows 98 oder [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) für Windows Edition (Windows Me), Windows 2000 und Windows XP exportieren. Da **IEmptyVolumeCache2** von **IEmptyVolumeCache** erbt und nur die zusätzliche **InitializeEx-Methode** hinzugefügt wird, ist relativ wenig zusätzlicher Aufwand erforderlich, um beides zu implementieren. Sofern ihr Handler nicht nur für eines dieser Betriebssysteme vorgesehen ist, sollten beide Schnittstellen exportiert werden.

Um diese Schnittstellen zu exportieren, müssen Sie diese Methoden implementieren, die den fünf grundlegenden Aufgaben entsprechen.

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Bereinigen](#purge)
-   [Deaktivieren](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

Die beiden Initialisierungsmethoden, die sehr ähnlich sind, werden aufgerufen, wenn das Hilfsprogramm für die Datenträgerbereinigung ausgeführt wird. Der Windows 98-Datenträgerbereinigungs-Manager ruft die [**IEmptyVolumeCache::Initialize-Methode**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) eines Handlers auf. Der Windows Windows Me), Windows 2000 oder Windows XP-Datenträgerbereinigungs-Manager versucht jedoch zunächst, [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) aufzurufen und verwendet nur **IEmptyVolumeCache::Initialize,** wenn [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) nicht vom Handler verfügbar gemacht wird. Der Datenträgerbereinigungs-Manager übergibt Informationen an die -Methode, z. B. den Registrierungsschlüssel des Handlers und das Datenträgervolume, das bereinigt werden soll.

Beide Methoden können verschiedene Anzeigezeichenfolgen zurückgeben und ein oder mehrere Flags festlegen. Der Hauptunterschied zwischen den beiden Methoden besteht darin, wie der im Datenträgerbereinigungs-Manager angezeigte Text behandelt wird. Die folgenden drei Zeichenfolgen sind betroffen.



| String       | Zweck                                                                            | Initialisieren                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Anzeigename | Der Name des Handlers, der im Listenfeld des Datenträgerbereinigungs-Managers angezeigt wird.               | Wenn *ppwszDisplayName* **NULL** ist, wird der Standardwert aus der Registrierung abgerufen. | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszDisplayName* angegeben werden, es werden keine Registrierungswerte verwendet. |
| BESCHREIBUNG  | Beschreibender Text, der unterhalb des Listenfelds angezeigt wird, wenn der Name des Handlers ausgewählt ist. | Wenn *ppwszDescription* **NULL** ist, wird der Standardwert aus der Registrierung abgerufen. | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszDescription* angegeben werden, es dürfen keine Registrierungswerte verwendet werden. |
| Schaltflächentext  | Text für die optionale Schaltfläche, mit der Benutzer die Benutzeroberfläche des Handlers anzeigen können.        | Kein Parameter verfügbar. Muss in der Registrierung angegeben werden.                           | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszBtnText* angegeben werden, es werden keine Registrierungswerte verwendet.     |



 

Der *pdwFlags-Parameter* in beiden Initialisierungsmethoden erkennt den gleichen Satz von Flags. Zwei dieser Flags werden vom Datenträgerbereinigungs-Manager an die -Methode übergeben.

-   **EVCF \_ SETTINGSMODE**

    Wenn der Datenträgerbereinigungs-Manager nach einem Zeitplan ausgeführt wird, wird das **EVCF \_ SETTINGSMODE-Flag** festgelegt. Wenn dieses Flag festgelegt ist, ruft der Datenträgerbereinigungs-Manager die Methoden [GetSpaceUsed,](#getspaceused) [Purge](#purge)oder [ShowProperties](#showproperties) nicht auf. Die [**Initialize-**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) oder [**InitializeEx-Methode**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) des Handlers muss alle Aufgaben verarbeiten, die normalerweise von [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) und [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge)ausgeführt werden. Da es keine Möglichkeit für Benutzerfeedback gibt, sollten nur die Dateien berührt werden, die äußerst sicher zu bereinigen sind. Sie sollten den *pcwszVolume-Parameter* der Initialisierungsmethode ignorieren und nicht benötigte Dateien bereinigen, unabhängig davon, auf welchem Laufwerk sie sich befinden.

-   **EVCF \_ OUTOFDISKSPACE**

    Wenn das **EVCF \_ OUTOFDISKSPACE-Flag** festgelegt ist, ist der Speicherplatz auf dem Laufwerk des Benutzers sehr knapp. Der Handler sollte beim Löschen von Dateien aggressiv vorgehen, auch wenn dies zu leistungseinbußen führt. Der Handler sollte jedoch offensichtlich keine Dateien löschen, die dazu führen würden, dass eine Anwendung fehlschlägt oder der Benutzer Daten verliert.

Die verbleibenden Flags werden vom Datenträgerbereinigungshandler festgelegt und an den Datenträgerbereinigungs-Manager zurückgegeben. Weitere Informationen finden Sie auf den Methodenverweisseiten für [**IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) und [**IEmptyVolumeCache2::InitializeEx.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex)

-   EVCF \_ DONTSHOWIFZERO

    Zeigen Sie den Handler nur dann im Listenfeld des Datenträgerbereinigungs-Managers an, wenn der von [**GetSpaceUsed zurückgegebene**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) Wert angibt, dass der Handler Speicherplatz freigeben kann.

-   EVCF \_ ENABLEBYDEFAULT

    Gibt an, dass der Handler standardmäßig aktiviert ist. Sie wird jedes Mal ausgeführt, wenn eine Datenträgerbereinigung durchgeführt wird, es sei denn, der Benutzer deaktiviert sie, indem er das Kontrollkästchen in der Liste der Handler des Datenträgerbereinigungs-Managers deaktiviert.

-   EVCF \_ ENABLEBYDEFAULT \_ AUTO

    Gibt an, dass der Handler automatisch für die Ausführung während geplanter Bereinigungen aktiviert wird.

-   EVCF \_ HASSETTINGS

    Legen Sie dieses Flag fest, wenn ihr Handler über eine Anzuzeigende Benutzeroberfläche verfügt. Als Antwort zeigt der Datenträgerbereinigungs-Manager eine Schaltfläche an, wenn dieser Handler im Listenfeld ausgewählt ist. Wenn auf diese Schaltfläche geklickt wird, ruft der Datenträgerbereinigungs-Manager [**ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties)auf.

-   EVCF \_ REMOVEFROMLIST

    Löschen Sie den Namen des Handlers aus der Liste der verfügbaren Handler, nachdem der Handler einmal ausgeführt wurde. Die Registrierungsinformationen des Handlers werden ebenfalls gelöscht.

### <a name="getspaceused"></a>GetSpaceUsed

Der Datenträgerbereinigungs-Manager ruft diese Methode auf, um zu bestimmen, wie viel Speicherplatz ein Datenträgerbereinigungshandler möglicherweise freigeben kann. Der Datenträgerbereinigungs-Manager zeigt diesen Wert dann rechts neben dem Namen des Handlers im Listenfeld an. Dieser Vorgang wird für alle Handler ausgeführt, die beim Datenträgerbereinigungs-Manager registriert sind, wenn der Manager gestartet wird und bevor die Hauptbenutzeroberfläche des Managers angezeigt wird. Wenn [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) aufgerufen wird, sollte der Handler die Dateien überprüfen, für die er verantwortlich ist, bestimmen, welche davon Bereinigungskandidaten sind, und den Speicherplatz zurückgeben, den er freigeben kann.

Da das Scannen ein langwieriger Prozess sein kann, verwendet der Datenträgerbereinigungs-Manager den *picb-Parameter* dieser Methode, um einen Zeiger auf eine [**IEmptyVolumeCacheCallBack-Schnittstelle**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) zu übergeben. Der Handler verwendet die -Schnittstelle regelmäßig während der Überprüfung, um [**IEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)aufzurufen, was zwei Zwecken dient.

-   Ermöglicht es dem Datenträgerbereinigungs-Manager, eine Statusanzeige zu aktualisieren und den Benutzer über den Fortschritt der Überprüfung zu informieren.
-   Benachrichtigt den Handler, die Überprüfung zu beenden, falls auf die Schaltfläche **Abbrechen** des Statusfensters geklickt wird. Dieses Schaltflächenereignis wird nicht direkt an den Handler kommuniziert. Stattdessen gibt der Datenträgerbereinigungs-Manager E \_ ABORT zurück, wenn [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) das nächste Mal [**IEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)aufruft.

### <a name="showproperties"></a>ShowProperties

Vor dem Starten der Bereinigung kann der Handler eine Benutzeroberfläche in der Regel in Form eines Windows Explorer-Fensters anzeigen, in dem dem Benutzer eine Liste von Dateien oder Klassen von Dateien angezeigt werden kann, die vom Handler für die Bereinigung ausgewählt wurden. Wenn der Handler beim Aufruf von [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) oder [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) das **EVCF \_ HASSETTINGS-Flag** festlegt, kann der Benutzer die Benutzeroberfläche anfordern, indem er im Datenträgerbereinigungs-Manager auf die zu diesem Zweck angezeigte Schaltfläche klickt. Der Schaltflächentext variiert von Handler zu Handler, aber "Dateien anzeigen", "Seiten anzeigen" und "Optionen" sind gängige Bezeichnungen.

Wenn auf die Schaltfläche geklickt wird, ruft der Datenträgerbereinigungs-Manager [**ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) auf, um den Handler zur Anzeige der Benutzeroberfläche aufzufordern. Die Benutzeroberfläche sollte als untergeordnetes Element des Fensters erstellt werden, dessen Handle im *hwnd-Parameter* der **ShowProperties-Methode** übergeben wird.

### <a name="purge"></a>Bereinigen

Der Datenträgerbereinigungs-Manager ruft die [**Bereinigungsmethode**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) des Handlers auf, um die Bereinigung in Bewegung festzulegen. Der *picb-Parameter* der Methode ist ein Zeiger auf die [**IEmptyVolumeCacheCallBack-Schnittstelle**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) des Datenträgerbereinigungs-Managers. Wie bei der [**GetSpaceUsed-Methode**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) sollte der Handler regelmäßig die Rückrufschnittstelle verwenden, um den Fortschritt zu melden und den Datenträgerbereinigungs-Manager abzufragen, ob der Benutzer auf **Abbrechen** geklickt hat. Beachten Sie jedoch, dass die **Purge-Methode** [**IEmptyVolumeCacheCallBack::P mosteProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress)und nicht [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)aufrufen muss.

### <a name="deactivate"></a>Deaktivieren

Die [**Deactivate-Methode**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) wird aufgerufen, wenn der Datenträgerbereinigungs-Manager das Herunterfahren vorbereitet. Der Handler sollte alle erforderlichen Bereinigungsaufgaben ausführen und zurückgeben. Wenn der Handler nicht erneut ausgeführt werden soll, legen Sie das **EVCF \_ REMOVEFROMLIST-Flag** im *pdwFlags-Parameter* der Initialisierungsmethode fest. Wenn dieses Flag festgelegt ist, entfernt der Datenträgerbereinigungs-Manager den Handler aus der Liste und löscht die Registrierungseinträge des Handlers. Sie müssen die Registrierungseinträge erneut hinzufügen, um den Handler erneut auszuführen. Dieses Flag wird in der Regel für Handler verwendet, die nur einmal ausgeführt werden.

## <a name="registering-a-disk-cleanup-handler"></a>Registrieren eines Datenträgerbereinigungshandlers

Um der Liste des Datenträgerbereinigungs-Managers einen Handler hinzuzufügen, müssen der Windows Registrierung bestimmte Schlüssel und Werte hinzugefügt werden.

-   [Registrieren der CLSID eines Handlers](#registering-a-handlers-clsid)
-   [Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Windows 2000 oder höher](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Verwenden des DataDrivenCleaner-Objekts](#using-the-datadrivencleaner-object)
-   [Beispielregistrierung eines Datenträgerbereinigungshandlers](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrieren der CLSID eines Handlers

Wie bei allen COM-Objekten müssen die GUID und DIE DLL des Handlerobjekts unter dem **CLSID-Schlüssel** in **HKEY \_ CLASSES \_ ROOT** registriert werden. Sie können auch ein Symbol registrieren, das neben dem Namen des Handlers im Listenfeld des Datenträgerbereinigungs-Managers angezeigt wird. Dies ist jedoch optional. Das folgende Beispiel zeigt die beteiligten Schlüssel, Werte und Daten.

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

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Allgemein

Um die Registrierung abzuschließen, muss ein Handler einen Schlüssel mit seinen Besonderheiten hinzufügen, wie hier gezeigt. Im weiteren Verlauf dieses Abschnitts wird der Inhalt dieses Schlüssels erläutert.

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

Im Allgemeinen wird der Name des Schlüssels, der die Besonderheiten eines Handlers enthält, für den Typ der verarbeiteten Datei benannt, z. B. **heruntergeladene Programmdateien,** aber dies ist keine Anforderung. In der folgenden Tabelle werden die möglichen Werte unter diesem Schlüssel aufgeführt.

> [!Note]  
> Nur der Standardwert, der den Klassenbezeichner des Handlers (CLSID) angibt, ist erforderlich. Alle anderen Werte sind optional.

 



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
<td>Die CLSID des Handlers, wie unter <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>registriert.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Text für die optionale Schaltfläche, auf die Benutzer klicken können, um die Benutzeroberfläche des Handlers anzuzeigen. Das & zeichen kann vor einem Zeichen platziert werden, um der Schaltfläche eine Tastenkombination zu zuweisen. Der AdvancedButtonText-Wert wird von Handlern ignoriert, die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx verfügbar machen.</strong></a></td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Befehlszeile, in der eine ausführbare Datei und optionale Befehlszeilenparameter angegeben werden. Diese Befehlszeile wird nach Abschluss der Datenträgerbereinigung ausgeführt.</td>
</tr>
<tr class="even">
<td>Csidl</td>
<td>REG_DWORD</td>
<td>Ein systemunabhängiger Bezeichner für einen speziellen Ordner, der in die Dateisuche integriert werden soll. Dieser Wert muss z. B. als numerischer Wert eingegeben werden, z. B. 0x0000001c als CSIDL_LOCAL_APPDATA. Eine Liste der möglichen Werte finden Sie unter <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Es kann nur ein einzelner Wert verwendet werden.<br/> Wenn der Wert Ordner angegeben wird, wird der durch den CSIDL-Wert angegebene Speicherort diesen Informationen vorausbewegt, um einen Suchpfad zu erstellen. Betrachten Sie beispielsweise das folgende Szenario.<br/>
<ul>
<li>Der CSIDL-Wert wird als 0x0000000d (CSIDL_MYMUSIC) angegeben.</li>
<li>Der Ordner "Mein Musik" befindet sich unter C:\Documents und Einstellungen\<em>username</em>\My Musik</li>
<li>Der Ordnerwert enthält &quot; "Jazz\Jazzs".&quot;</li>
</ul>
Das Ergebnis dieses Szenarios ist, dass der Datenträgerbereinigungshandler den<em></em>Ordner "C:\Documents" und "Einstellungen\username \My Musik\Jazz\Jazzs" durchsucht. Beachten Sie, dass der Schrägstrich vor dem Wert Ordner hinzugefügt wird, wenn er nicht vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td>BESCHREIBUNG</td>
<td>REG_SZ</td>
<td>Beschreibender Text, der unter dem Listenfeld des Datenträgerbereinigungs-Managers angezeigt wird, wenn der Handlername ausgewählt ist. Hier können Sie erläutern, was der Handler tut, mit welchen Dateien er sich selbst beschäftigt, und alle anderen Informationen, die für den Benutzer aufträumen. Wenn <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> vom Handler nicht verfügbar gemacht wird, kann dieser Text durch die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize-Methode</strong></a> des Handlers überschrieben werden, indem eine alternative Zeichenfolge im <em>ppwszDescription-Parameter</em> angegeben wird, wenn die -Methode aufgerufen wird.</td>
</tr>
<tr class="even">
<td>Anzeige</td>
<td>REG_SZ</td>
<td>Der Name des Handlers, der im Listenfeld des Datenträgerbereinigungs-Managers angezeigt werden soll. Wenn <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> vom Handler nicht verfügbar gemacht wird, kann dieser Text durch die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize-Methode</strong></a> des Handlers überschrieben werden, indem eine alternative Zeichenfolge im <em>ppwszDisplayName-Parameter</em> angegeben wird, wenn die Methode aufgerufen wird.</td>
</tr>
<tr class="odd">
<td>Liste</td>
<td>REG_SZ oder REG_MULTI_SZ</td>
<td>Eine Liste von Dateien, die von diesem Handler gesucht und bereinigt wurden. Sie können Platzhalter angeben, indem Sie ? oder * Zeichen. Wenn der Wert vom Typ REG_SZ, werden mehrere Erweiterungen mithilfe der | oder : Zeichen ohne Leerzeichen auf beiden Seiten.<br/> Wenn das DDEVCF_REMOVEDIRS flag im Flags-Wert festgelegt ist, können diese Werte Verzeichnisnamen sowie Dateien angeben.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Kennzeichnet steuernde Elemente der Such- und Bereinigungsprozedur. Mindestens einer der folgenden Werte.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Rekursiv suchen und entfernen.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Nachdem der Handler einmal ausgeführt wurde, entfernen Sie ihn aus der Registrierung.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn sie schreibgeschützt sind.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn es sich um Systemdateien handelt.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn es sich um ausgeblendete Dateien handelt.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Zeigen Sie diesen Handler nicht im Datenträgerbereinigungs-Manager an, wenn keine Dateien den Suchkriterien entsprechen.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Übereinstimmung des FileList-Werts mit Verzeichnissen und Entfernen von Übereinstimmungen und allen zugehörigen Unterverzeichnissen.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Führen Sie diesen Handler nur aus, wenn der verfügbare Speicherplatz unter den kritischen Wert gefallen ist, der vom Datenträgerbereinigungs-Manager festgelegt wird, der das EVCF_OUTOFDISKSPACE-Flag über <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> oder <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a>festgelegt hat.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Entfernen Sie das übergeordnete Verzeichnis der angegebenen Dateien, nachdem die Bereinigung ausgeführt wurde.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Verwenden Sie den LastAccess-Wert, falls angegeben, um zu ermitteln, welche Dateien bereinigt werden sollen. Dieses Flag wird ignoriert, wenn <a href="#using-the-datadrivencleaner-object">dataDrivenCleaner verwendet</a> wird. Jeder bereitgestellte LastAccess-Wert wird immer verwendet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ordner</td>
<td>REG_SZ, REG_MULTI_SZ oder REG_EXPAND_SZ</td>
<td>Ein bestimmter Ordner oder Ordner, um nach Elementen zu suchen, die einträgen im FileList-Wert übereinstimmen. Sie können Platzhalter angeben, indem Sie ? oder * Zeichen. Wenn der Wert vom Typ REG_SZ ist, werden mehrere Ordnernamen mithilfe der | zeichen, ohne Leerzeichen auf beiden Seiten.<br/> Wenn ein CSIDL-Wert vorhanden ist, kann in diesem Wert nur ein Ordner angegeben werden. Der durch den CSIDL-Wert angegebene Speicherort wird diesem Ordnerpfad vorgefertigt, um einen Suchpfad zu erstellen. Ein Beispiel finden Sie in der Beschreibung des CSIDL-Werts.<br/> Wenn dieser Wert in Windows Vista Service Pack 1 (SP1) und höher nicht vorhanden ist, wird der Bereinigungshandler ignoriert und S_FALSE initialisierung zurückgegeben.<br/> Wenn dieser Wert in der ursprünglichen Version von Windows Vista und früher nicht vorhanden ist, wird der Stammordner des aktuellen Volumes verwendet. Das DDEVCF_DOSUBDIRS-Flag ist in diesem Fall erforderlich, um das gesamte Laufwerk zu durchsuchen. Ohne sie wird nur der Stammordner selbst durchsucht.<br/> Ein Oder mehrere Laufwerke müssen angegeben werden. Dies kann über den CSIDL-Wert oder über eine Zeichenfolge REG_EXPAND_SZ werden. Wenn diese Optionen nicht verfügbar sind, muss das zu durchsuchende Laufwerk jedoch im Ordnernamen angegeben werden. Verwenden Sie ?: , um den Ordner auf dem aktuellen Laufwerk zu durchsuchen.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ oder REG_EXPAND_SZ</td>
<td>Der Pfad zu der Ressource, von der ein Symbol für die Zuordnung zum Handler erhalten werden soll.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Die Anzahl der Tage, die seit dem letzten Zugriff auf eine Datei oder dem Erstellen eines Verzeichnisses verstrichen sein müssen, damit diese Datei oder dieses Verzeichnis für die Bereinigung berücksichtigt wird.</td>
</tr>
<tr class="even">
<td>Priorität</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Bestimmt die Reihenfolge, in der der Handler in Bezug auf andere Handler ausgeführt wird. Je höher die Zahl ist, desto früher im Prozess wird der Handler ausgeführt. Es gibt keinen definierten Bereich, für den eine Beliebige Zahl akzeptabel ist.</td>
</tr>
<tr class="odd">
<td>Propertybag</td>
<td>REG_SZ</td>
<td>Die CLSID einer Ressource, mit der lokalisierter Text für den Anzeigenamen, die Beschreibung und den Schaltflächentext angegeben wird. Diese Ressource ist nützlich, wenn ein Handler <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> nicht implementiert und der Handler unter Microsoft Windows NT oder Windows XP ausgeführt wird.<br/> Der Datenträgerbereinigungs-Manager überprüft zunächst, ob die Initialisierungsroutine des Handlers diese Zeichenfolgen zurückgegeben hat, wie dies der Fall wäre, wenn <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> implementiert wird. Wenn dies nicht der Fall ist, wird der Manager als Nächstes zu einer Eigenschaftentüte mit dem Namen in diesem Wert. Wenn keine bereitgestellt wurde, wird der Text aus der Registrierung abgerufen.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Indem Sie die ausführbare Datei des Datenträgerbereinigungs-Managers über Cleanmgr.exe Befehlszeile ausführen, können Sie Bereinigungsprofile <em>deklarieren.</em> Diese Profile bestehen aus einer Teilmenge der verfügbaren Handler und erhalten eine eindeutige numerische Bezeichnung. Dadurch können Sie die Ausführung verschiedener Handlersätze zu unterschiedlichen Zeiten automatisieren.<br/> Die Befehlszeile &quot;cleanmgr.exe /sageset:<strong>nnnn</strong> &quot; , wobei <strong>nnnn</strong> eine eindeutige numerische Bezeichnung ist, zeigt eine Benutzeroberfläche an, über die Sie die Handler auswählen können, die in diesem Profil enthalten sein sollen. Neben der Definition des Profils schreibt der Sageset-Parameter auch einen Wert namens StateFlags<strong>nnnn</strong>, wobei <strong>nnnn</strong> die Bezeichnung ist, die Sie im -Parameter verwendet haben, in alle Unterschlüssel unter <strong>VolumeCaches</strong>. Es gibt zwei mögliche Datenwerte für diese Einträge.
<ul>
<li>0: Führen Sie diesen Handler nicht aus, wenn dieses Profil ausgeführt wird.</li>
<li>2: Schließen Sie diesen Handler ein, wenn dieses Profil ausgeführt wird.</li>
</ul>
<br/> Angenommen, die Befehlszeile &quot;cleanmgr.exe /sageset:1234 wird &quot; ausgeführt. Auf der angezeigten Benutzeroberfläche wählt der Benutzer <strong>heruntergeladene Programmdateien</strong>aus, aber nicht <strong>temporäre Internetdateien.</strong> Die folgenden Werte werden dann in die Registrierung geschrieben.<br/>
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
<br/> Die Befehlszeile &quot;cleanmgr.exe /sagerun:<strong>nnnn</strong> &quot; , wobei der Wert von <strong>nnnn mit</strong> der mit dem sageset-Parameter deklarierten Bezeichnung übereinstimmt, führt alle in diesem Profil ausgewählten Handler aus.<br/> Ein generischer StateFlags-Wert wird in die Registrierung geschrieben, wenn die Datenträgerbereinigung normal ausgeführt wird. Dieser Wert speichert einfach den Zustand (aktiviert oder deaktiviert) des Handlers, wenn er dem Benutzer zuletzt als Option angezeigt wurde. Es gibt zwei mögliche Datenwerte für diese Einträge.
<ul>
<li>0: Der Handler wurde nicht ausgewählt.</li>
<li>1: Der Handler wurde ausgewählt.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Windows 2000 oder höher

Das Angeben von Anzeigetext in der Registrierung kann die Lokalisierung von Software erschweren. Aus diesem Grund unterstützen Windows 2000 und Windows XP die [**IEmptyVolumeCache2-Schnittstelle**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) mit ihrer bevorzugten Initialisierungsmethode [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). Unter Windows 2000 oder höher wird immer versucht, **IEmptyVolumeCache2::InitializeEx** vor [**IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize)aufzurufen. Das System verwendet Initialize nur, um einen Handler zu **initialisieren,** wenn **IEmptyVolumeCache2** nicht verfügbar gemacht wird.

Im Hinblick auf die Registrierung besteht der einzige Unterschied unter Windows 2000 oder höher darin, dass Sie die Werte AdvancedButtonText, Display und Description weglassen können, wenn [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) vom Handler verfügbar gemacht wird. Diese Werte, die ordnungsgemäß lokalisierten Text enthalten, werden dem Datenträgerbereinigungs-Manager beim Aufrufen von **InitializeEx** bereitgestellt.

### <a name="using-the-datadrivencleaner-object"></a>Verwenden des DataDrivenCleaner-Objekts

Ein einfacher Datenträgerbereinigungshandler namens DataDrivenCleaner wird vom Betriebssystem bereitgestellt. Um dieses Objekt als Handler zu verwenden, anstatt ihren eigenen zu implementieren, verwenden Sie die CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} als Standardwert für den Unterschlüssel des Handlers unter **VolumeCaches,** wie unter [Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)beschrieben.

Der DataDrivenCleaner macht [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)nicht verfügbar, sodass die Werte Anzeige und Beschreibung über die Registrierung bereitgestellt werden. Beachten Sie beim Deklarieren dieser Zeichenfolgen, dass dies zu Lokalisierungsproblemen führen kann. Lokalisierter Text kann über den PropertyBag-Wert bereitgestellt werden. Der AdvancedButtonText-Wert wird ignoriert, da keine Benutzeroberfläche und somit keine Schaltfläche zum Anzeigen für diesen Handler verfügbar ist.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Beispielregistrierung eines Datenträgerbereinigungshandlers

Im Folgenden sehen Sie ein Beispiel für die Registrierung eines Datenträgerbereinigungshandlers, der von The Telefon Company implementiert wird. Dieser Handler implementiert sowohl [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) als [**auch IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)und stellt daher AdvancedButtonText-, Description- und Display-Werte für den Fall bereit, dass er auf einem Computer verwendet wird, auf dem Windows 98 ausgeführt wird. Der Handler kombiniert die CsIDL- und Folder-Werte, um nach Dateien im Verzeichnis C: Programme The Telefon Company Temp zu \\ \\ \\ suchen, und das DDEVCF \_ DOSUBDIRS-Flag ist so festgelegt, dass auch seine Unterverzeichnisse durchsucht werden. Nur dateien mit TMP- und TPC-Erweiterungen werden für die Bereinigung berücksichtigt, und das DDEVCF \_ PRIVATE \_ LASTACCESS-Flag wird so festgelegt, dass von diesen Dateien nur diejenigen berücksichtigt werden, auf die seit 14 Tagen oder mehr nicht zugegriffen wurde. Das DDEVCF-Flag \_ DONTSHOWIFZERO ist ebenfalls so festgelegt, dass der Handler nicht in der Liste angezeigt wird, es sei denn, er hat Bereinigungskandidaten gefunden.

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

 

