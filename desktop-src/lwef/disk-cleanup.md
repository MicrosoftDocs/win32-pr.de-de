---
title: Erstellen eines Datenträgerbereinigungshandlers
description: Ein Axiom, das sich in der Welt der Computer immer wieder bewährt hat, ist, dass Sie es unabhängig von der Größe der Speicherkapazität Ihres Computers schließlich auffüllen.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- Datenträgerbereinigungshandler
- Datenträgerbereinigung
- DataDrivenCleaner
- Register,Datenträgerbereinigungshandler
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

Ein Axiom, das sich in der Welt der Computer immer wieder bewährt hat, ist, dass Sie es unabhängig von der Größe der Speicherkapazität Ihres Computers schließlich auffüllen. Während die durchschnittliche Größe der Festplatte eines Computers im Laufe der Zeit erheblich gestiegen ist, sind die Anwendungen auch entsprechend gestiegen, und Benutzer suchen nach Möglichkeiten, mehr freien Festplattenspeicher zu erstellen. Der verfügbare Speicherplatz wird auch durch die vielen temporären Dateien reduziert, die Anwendungen aus Sicherungs- oder Leistungsgründen erstellen. Wenn der Speicherplatz auf dem Datenträger zu niedrig wird, ist es notwendig, den von Anwendungen verwendeten Speicherplatz zu reduzieren. Speicherplatz auf dem Datenträger kann mit einer Vielzahl von Möglichkeiten, einschließlich der folgenden, frei werden:

-   Löschen von Dateien.
-   Komprimieren von Dateien.
-   Verschieben von Dateien auf ein Sicherungsmedium.
-   Übertragen von Dateien auf einen Remoteserver.

Dateien, die gute Kandidaten für die Bereinigung sind, sind:

-   Dateien, die der Benutzer nie mehr benötigt.
-   Temporäre Dateien, die nur aus Leistungsgründen vorhanden sind.
-   Dateien, die bei Bedarf von einer Installations-CD wiederhergestellt werden können.
-   Datendateien, die möglicherweise durch neuere Versionen ersetzt wurden, z. B. alte Sicherungsdateien.
-   Ältere Dateien, die seit langer Zeit nicht mehr verwendet wurden.

Das Löschen ist besonders für Dateien geeignet, die der Benutzer nie mehr benötigt, z. B. Dateien, die aus Leistungsgründen vorübergehend zwischengespeichert werden. Das Löschen ist auch für Dateien geeignet, die leicht wiederhergestellt werden können, z. B. Grafikdateien, die von einer Installations-CD erneut geladen werden können. Dateien, die der Benutzer später benötigen oder die schwer zu rekonstruieren sind, sind bessere Kandidaten für die Komprimierung oder Sicherung.

Die Erwartung, dass ein Benutzer das Dateisystem manuell bereinigt, ist keine gute Lösung. Der Benutzer weiß möglicherweise nicht, wo sich viele der Dateien befinden oder wie er erkennt, welche dateien sicher entfernt werden können. Darüber hinaus besteht das Risiko, dass der Benutzer wichtige Dateien löscht.

Die folgenden Facets des Datenträgerbereinigungs-Hilfsprogramms werden in diesem Thema erläutert.

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

Ab Windows 98 enthält das Windows-Betriebssystem Datenträgerbereinigung, ein Hilfsprogramm, das dem Benutzer die Verwaltung des verfügbaren Festplattenspeicherplatzes erheblich erleichtert. Das Hilfsprogramm Datenträgerbereinigung ist so konzipiert, dass so viel Speicherplatz wie möglich frei wird und das Risiko verringert wird, dass der Benutzer versehentlich wichtige Dateien löscht.

Die Datenträgerbereinigung kann auf drei Arten initiiert werden.

-   Der Benutzer kann die Datenträgerbereinigung initiieren, indem er auf **Starten klickt.** , die auf **Alle Programme,** **Zubehör** und **Systemtools zeigen;** und klicken Sie dann auf **Datenträgerbereinigung**.
-   Das System benachrichtigt den Benutzer mit einem Meldungsfeld, dass nicht verwendeter Speicherplatz den kritischen Modus erreicht hat. Der Schwellenwert für den kritischen Modus für ein Laufwerk, das größer als 2,25 GIGABYTE (GB) ist, beträgt 200 MEGABYTE (MB). Nachfolgende Warnungen werden bei 80, 50 und 1 MB angegeben. Der Benutzer erhält die Möglichkeit, Speicherplatz manuell freizugeben oder das Hilfsprogramm Datenträgerbereinigung zu starten.
-   Der Benutzer kann den assistenten für Windows Geplanter Task (auf älteren Systemen als Wartungs-Assistent bezeichnet) das Hilfsprogramm Datenträgerbereinigung automatisch zu geplanten Zeiten ausführen lassen.

Die grundlegende Herausforderung bei der Datenträgerbereinigung besteht darin, so viel Speicherplatz wie möglich frei zu geben, ohne wichtige Dateien zu löschen. Da es keine Standard-Möglichkeit gibt, Dateien für die Bereinigung zu markieren, kann keine einzelne Anwendung zuverlässig alle unerlädlichen Dateien erkennen und bereinigen. Das Hilfsprogramm Datenträgerbereinigung löst dieses Problem, indem  es den Bereinigungsvorgang zwischen einem einzelnen Datenträgerbereinigungs-Manager und einer Sammlung von Datenträgerbereinigungshandlern *aufteilt.*

Wenn das Hilfsprogramm Datenträgerbereinigung ausgeführt wird, wird dem Benutzer das folgende Dialogfeld angezeigt. (Wenn auf dem Computer mehrere Datenträger oder Datenträgerpartitionen vorhanden sind, wird der Benutzer zunächst aufgefordert, ein Laufwerk zu wählen, bevor dieses Dialogfeld angezeigt wird.)

![Screenshot des Dialogfelds "Bereinigung"](images/cleanup1.png)

Der Datenträgerbereinigungs-Manager ist Teil des Betriebssystems. Es zeigt das in der vorherigen Abbildung gezeigte Dialogfeld an, verarbeitet Benutzereingaben und verwaltet den Bereinigungsvorgang. Die tatsächliche Auswahl und Bereinigung nicht verwendeter Dateien erfolgt durch die einzelnen Datenträgerbereinigungshandler, die im Listenfeld des Datenträgerbereinigungs-Managers angezeigt werden. Der Benutzer hat die Möglichkeit, einzelne Handler zu aktivieren oder zu deaktivieren, indem er sein Kontrollkästchen auf der Benutzeroberfläche des Datenträgerbereinigungs-Managers aktivieren oder deaktivieren kann.

Jeder Handler ist für einen klar definierten Satz von Dateien verantwortlich. Beispielsweise ist der ausgewählte Handler in der Abbildung für das Bereinigen heruntergeladener Programmdateien verantwortlich. Der in der Abbildung ausgewählte Handler stellt auch die Schaltfläche **Dateien anzeigen** zur Auswahl. Durch Klicken auf die Schaltfläche kann der Benutzer anfordern, dass der Handler eine Benutzeroberfläche anzeigt, in der Regel ein Windows Explorer-Fenster, in dem der Benutzer angeben kann, welche Dateien oder Klassen von Dateien bereinigt werden.

Obwohl Windows eine Reihe von Datenträgerbereinigungshandlern enthält, sind sie nicht für die Behandlung von Dateien konzipiert, die von anderen Anwendungen erzeugt werden. Stattdessen ist der Datenträgerbereinigungs-Manager so konzipiert, dass er flexibel und erweiterbar ist, indem er es entwicklern ermöglicht, ihren eigenen Datenträgerbereinigungshandler zu implementieren und zu registrieren. Jeder Entwickler kann die verfügbaren Datenträgerbereinigungsdienste erweitern, indem er einen Datenträgerbereinigungshandler implementieren und registrieren kann.

Alle Anwendungen, die temporäre Dateien erstellen, können und sollten einen Datenträgerbereinigungshandler implementieren und registrieren. Auf diese Weise können Benutzer die temporären Dateien der Anwendung bequem und zuverlässig verwalten. Wenn Sie den Handler implementieren, können Sie entscheiden, welche Dateien betroffen sind, und bestimmen, wie die eigentliche Bereinigung erfolgt.

## <a name="implementation-basics"></a>Grundlagen der Implementierung

Bereinigungshandler sind In-Process-Server Component Object Model (COM)-Objekte. Windows stellt ein vorhandenes Handlerobjekt mit dem Namen DataDrivenCleaner für Ihre Verwendung zur Anwendung. Sie können auch einen Handler selbst implementieren, um mehr Flexibilität zu erhalten. Mit diesen Objekten können Sie dann angeben, wie Dateien ausgewählt und Speicherplatz auf dem Datenträger frei wird. Im Fall eines implementierten Handlers können Sie die optionale Benutzeroberfläche für eine präzisere Steuerung anzeigen. In diesem Abschnitt wird die Implementierung Ihres eigenen Handlers behandelt. Weitere Informationen zur Verwendung des DataDrivenCleaner-Objekts finden Sie unter [Verwenden des DataDrivenCleaner-Objekts.](#using-the-datadrivencleaner-object)

Ein Datenträgerbereinigungshandler sollte diese fünf grundlegenden Aufgaben ausführen.

-   Initialisiert das Handlerobjekt.
-   Überprüfen Sie den Datenträger, um zu bestimmen, wie viel Speicherplatz auf dem Datenträger frei werden kann.
-   Zeigen Sie die Benutzeroberfläche an, um Benutzerfeedback darüber zu erhalten, welche Dateien bereinigt werden müssen. (Optional)
-   Bereinigt sie.
-   Herunterfahren.

Damit der Datenträgerbereinigungs-Manager diese Aufgaben verwalten kann, muss ein Handler entweder [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) für Windows 98 oder [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) für Windows Edition (Windows Me), Windows 2000 und Windows XP exportieren. Da **IEmptyVolumeCache2** von **IEmptyVolumeCache** erbt und nur die zusätzliche **InitializeEx-Methode** hinzugefügt wird, ist relativ wenig zusätzlicher Arbeitsaufwand erforderlich, um beides zu implementieren. Sofern ihr Handler nicht nur für eines dieser Betriebssysteme vorgesehen ist, sollte er beide Schnittstellen exportieren.

Um diese Schnittstellen zu exportieren, müssen Sie diese Methoden implementieren, die den fünf grundlegenden Aufgaben entspricht.

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Bereinigen](#purge)
-   [Deaktivieren](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

Die beiden Initialisierungsmethoden, die sehr ähnlich sind, werden aufgerufen, wenn das Hilfsprogramm Für die Datenträgerbereinigung ausgeführt wird. Der Windows 98-Datenträgerbereinigungs-Manager ruft die [**IEmptyVolumeCache::Initialize-Methode**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) eines Handlers auf. Der Windows Editions-Manager (Windows Me), Windows 2000 oder Windows XP-Datenträgerbereinigungs-Manager versucht jedoch zuerst, [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) aufrufen und verwendet nur **IEmptyVolumeCache::Initialize,** wenn [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) nicht vom Handler verfügbar gemacht wird. Der Datenträgerbereinigungs-Manager übergibt Informationen an die -Methode, z. B. den Registrierungsschlüssel des Handlers und das Datenträgervolumen, das bereinigt werden soll.

Beide Methoden können verschiedene Anzeigezeichenfolgen zurückgeben und ein oder mehrere Flags festlegen. Der Hauptunterschied zwischen den beiden Methoden besteht darin, wie der im Datenträgerbereinigungs-Manager angezeigte Text behandelt wird. Die folgenden drei Zeichenfolgen sind betroffen.



| String       | Zweck                                                                            | Initialisieren                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Anzeigename | Der Name des Handlers, der im Listenfeld des Datenträgerbereinigungs-Managers angezeigt wird.               | Wenn *ppwszDisplayName* **NULL** ist, wird der Standardwert aus der Registrierung abgerufen. | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszDisplayName* angegeben werden, es werden keine Registrierungswerte verwendet. |
| Beschreibung  | Beschreibender Text, der unterhalb des Listenfelds angezeigt wird, wenn der Name des Handlers ausgewählt ist. | Wenn *ppwszDescription* **NULL** ist, wird der Standardwert aus der Registrierung abgerufen. | Eine ordnungsgemäß lokalisierte Zeichenfolge muss in *ppwszDescription* angegeben werden, es dürfen keine Registrierungswerte verwendet werden. |
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
<td>Text für die optionale Schaltfläche, auf die Benutzer klicken können, um die Benutzeroberfläche des Handlers anzuzeigen. Das & Zeichen kann vor einem Zeichen platziert werden, um eine Tastenkombination für die Schaltfläche zuzuweisen. Der AdvancedButtonText-Wert wird von Handlern ignoriert, die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a>verfügbar machen.</td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Befehlszeile, die eine ausführbare Datei und optionale Befehlszeilenparameter angibt. Diese Befehlszeile wird nach Abschluss der Datenträgerbereinigung ausgeführt.</td>
</tr>
<tr class="even">
<td>Csidl</td>
<td>REG_DWORD</td>
<td>Ein systemunabhängiger Bezeichner für einen speziellen Ordner, der in die Dateisuche eingeschlossen werden soll. Dieser Wert muss beispielsweise als numerischer Wert eingegeben werden, 0x0000001c anstatt als CSIDL_LOCAL_APPDATA. Eine Liste der möglichen Werte finden Sie unter <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Es kann nur ein einzelner Wert verwendet werden.<br/> Wenn der Ordnerwert angegeben wird, wird dieser Information der durch den CSIDL-Wert angegebene Speicherort voran gestellt, um einen Suchpfad zu erstellen. Betrachten Sie beispielsweise das folgende Szenario.<br/>
<ul>
<li>Der CSIDL-Wert wird als 0x0000000d (CSIDL_MYMUSIC) angegeben.</li>
<li>Ihr Ordner My Musik befindet sich unter C:\Documents and Einstellungen\<em>username</em>\My Musik</li>
<li>Der Ordnerwert enthält &quot; Jazz\Programme.&quot;</li>
</ul>
Das Ergebnis dieses Szenarios ist, dass der Datenträgerbereinigungshandler den Ordner C:\Documents und Einstellungen\<em>Username</em>\My Musik\Jazz\Programme durchsucht. Beachten Sie, dass der Schrägstrich vor dem Wert Ordner hinzugefügt wird, wenn er nicht vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td>Beschreibung</td>
<td>REG_SZ</td>
<td>Beschreibender Text, der unter dem Listenfeld des Datenträgerbereinigungs-Managers angezeigt wird, wenn der Name des Handlers ausgewählt ist. Hier können Sie die Aufgaben des Handlers, die Dateien, mit der er sich selbst befasst, und alle anderen Informationen erläutern, die dem Benutzer aufschlussant sind. Wenn <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> nicht vom Handler verfügbar gemacht wird, kann dieser Text durch die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize-Methode</strong></a> des Handlers überschrieben werden, indem eine alternative Zeichenfolge im <em>ppwszDescription-Parameter</em> angegeben wird, wenn die -Methode aufgerufen wird.</td>
</tr>
<tr class="even">
<td>Anzeige</td>
<td>REG_SZ</td>
<td>Der Name des Handlers, der im Listenfeld des Datenträgerbereinigungs-Managers angezeigt werden soll. Wenn <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> nicht vom Handler verfügbar gemacht wird, kann dieser Text durch die <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize-Methode</strong></a> des Handlers überschrieben werden, indem eine alternative Zeichenfolge im <em>ppwszDisplayName-Parameter</em> angegeben wird, wenn die -Methode aufgerufen wird.</td>
</tr>
<tr class="odd">
<td>Liste</td>
<td>REG_SZ oder REG_MULTI_SZ</td>
<td>Eine Liste der Dateien, die von diesem Handler gesucht und bereinigt werden. Sie können Platzhalter mithilfe von angeben. oder * Zeichen. Wenn der Wert vom Typ REG_SZ ist, werden mehrere Erweiterungen mithilfe des | oder : Zeichen ohne Leerzeichen auf beiden Seiten.<br/> Wenn das DDEVCF_REMOVEDIRS-Flag im Flags-Wert festgelegt ist, können diese Werte Verzeichnisnamen sowie Dateien angeben.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Flags, die Elemente der Such- und Bereinigungsprozedur steuern. Mindestens einer der folgenden Werte.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Rekursiv suchen und entfernen.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Nachdem der Handler einmal ausgeführt wurde, entfernen Sie ihn aus der Registrierung.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn sie schreibgeschützt sind.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn es sich um Systemdateien handelt.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Entfernen Sie Dateien, die die Suchkriterien erfüllen, auch wenn es sich um ausgeblendete Dateien handelt.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Zeigen Sie diesen Handler nicht im Datenträgerbereinigungs-Manager an, wenn keine Dateien den Suchkriterien entsprechen.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Übereinstimmung mit dem FileList-Wert mit Verzeichnissen und Entfernen von Übereinstimmungen und allen zugehörigen Unterverzeichnissen.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Führen Sie diesen Handler nur aus, wenn der verfügbare Speicherplatz unter den kritischen Wert gefallen ist, der durch den Datenträgerbereinigungs-Manager bestimmt wird, der das flag EVCF_OUTOFDISKSPACE über <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> oder <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a>festlegt.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Entfernen Sie das übergeordnete Verzeichnis der angegebenen Dateien, sobald die Bereinigung ausgeführt wurde.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Verwenden Sie ggf. den LastAccess-Wert, um festzustellen, welche Dateien bereinigt werden sollen. Dieses Flag wird ignoriert, wenn bei Verwendung von <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> jeder angegebene LastAccess-Wert immer verwendet wird.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ordner</td>
<td>REG_SZ, REG_MULTI_SZ oder REG_EXPAND_SZ</td>
<td>Ein bestimmter Ordner oder Ordner, in dem nach Elementen gesucht werden soll, die einträgen im FileList-Wert entsprechen. Sie können Platzhalter mithilfe von angeben. oder * Zeichen. Wenn der Wert vom Typ REG_SZ ist, werden mehrere Ordnernamen mithilfe der | zeichen, ohne Leerzeichen auf beiden Seiten.<br/> Wenn ein CSIDL-Wert vorhanden ist, kann in diesem Wert nur ein Ordner angegeben werden. Der durch den CSIDL-Wert angegebene Speicherort wird diesem Ordnerpfad voran gestellt, um einen Suchpfad zu erstellen. Ein Beispiel finden Sie in der Beschreibung des CSIDL-Werts.<br/> Wenn dieser Wert auf Windows Vista Service Pack 1 (SP1) und höher nicht vorhanden ist, wird der Bereinigungshandler ignoriert und gibt bei der Initialisierung S_FALSE zurück.<br/> Wenn dieser Wert in der ursprünglichen Version von Windows Vista und früher nicht vorhanden ist, wird der Stammordner des aktuellen Volumes verwendet. Das DDEVCF_DOSUBDIRS Flag ist in diesem Fall erforderlich, um das gesamte Laufwerk zu durchsuchen. Ohne diese wird nur der Stammordner selbst durchsucht.<br/> Ein Laufwerk oder Laufwerk muss angegeben werden. Dies kann über den CSIDL-Wert oder eine REG_EXPAND_SZ Zeichenfolge bereitgestellt werden. Wenn Sie diese Optionen nicht verwenden, muss das zu durchsuchende Laufwerk jedoch im Ordnernamen angegeben werden. Verwenden Sie ?: , um den Ordner auf dem aktuellen Laufwerk zu durchsuchen.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ oder REG_EXPAND_SZ</td>
<td>Der Pfad zu der Ressource, aus der ein Symbol zur Verwendung in Verbindung mit dem Handler abzurufen ist.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Die Anzahl von Tagen, die seit dem letzten Zugriff auf eine Datei oder der Erstellung eines Verzeichnisses für diese Datei oder dieses Verzeichnis verstrichen sein müssen, um für die Bereinigung berücksichtigt zu werden.</td>
</tr>
<tr class="even">
<td>Priorität</td>
<td>REG_DWORD oder REG_BINARY</td>
<td>Bestimmt die Reihenfolge, in der der Handler in Bezug auf andere Handler ausgeführt wird. Je höher die Zahl, desto früher im Prozess, in dem der Handler ausgeführt wird. Es gibt keinen definierten Bereich, für den eine beliebige Zahl zulässig ist.</td>
</tr>
<tr class="odd">
<td>Propertybag</td>
<td>REG_SZ</td>
<td>Die CLSID einer Ressource, die verwendet wird, um lokalisierten Text für den Anzeigenamen, die Beschreibung und den Schaltflächentext bereitzustellen. Diese Ressource ist in Situationen nützlich, in denen ein Handler <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> nicht implementiert und der Handler unter Microsoft Windows NT oder Windows XP ausgeführt wird.<br/> Der Datenträgerbereinigungs-Manager überprüft zunächst, ob die Initialisierungsroutine des Handlers diese Zeichenfolgen zurückgegeben hat, wie dies bei der Implementierung von <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> der Fall wäre. Andernfalls wechselt der Manager als Nächstes zu einem Eigenschaftenbehälter namens in diesem Wert. Wenn kein Text bereitgestellt wurde, wird der Text aus der Registrierung abgerufen.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Indem Sie die ausführbare Datei des Datenträgerbereinigungs-Managers Cleanmgr.exe über eine Befehlszeile ausführen, können Sie <em>Bereinigungsprofile</em>deklarieren. Diese Profile bestehen aus einer Teilmenge der verfügbaren Handler und erhalten eine eindeutige numerische Bezeichnung. Auf diese Weise können Sie die Ausführung verschiedener Handlersätze zu unterschiedlichen Zeiten automatisieren.<br/> Die Befehlszeile &quot;cleanmgr.exe /sageset:<strong>nnnn</strong>, wobei &quot; <strong>nnnn eine</strong> eindeutige numerische Bezeichnung ist, zeigt eine Benutzeroberfläche an, auf der Sie die Handler auswählen können, die in dieses Profil aufgenommen werden sollen. Zusätzlich zum Definieren des Profils schreibt der sageset-Parameter auch einen Wert namens StateFlags<strong>nnnn</strong>, wobei <strong>nnnn die</strong> Bezeichnung ist, die Sie im -Parameter verwendet haben, in alle Unterschlüssel unter <strong>VolumeCaches</strong>. Es gibt zwei mögliche Datenwerte für diese Einträge.
<ul>
<li>0: Führen Sie diesen Handler nicht aus, wenn dieses Profil ausgeführt wird.</li>
<li>2: Schließen Sie diesen Handler ein, wenn dieses Profil ausgeführt wird.</li>
</ul>
<br/> Angenommen, die Befehlszeilecleanmgr.exe &quot; /sageset:1234 wird &quot; ausgeführt. Auf der angezeigten Benutzeroberfläche wählt der Benutzer <strong>Heruntergeladene</strong>Programmdateien aus, aber keine <strong>temporären Internetdateien.</strong> Die folgenden Werte werden dann in die Registrierung geschrieben.<br/>
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
<br/> Die Befehlszeile &quot;cleanmgr.exe /sagerun:<strong>nnnn</strong>, wobei der Wert &quot; von <strong>nnnn</strong> der mit dem sageset-Parameter deklarierten Bezeichnung entspricht, führt alle in diesem Profil ausgewählten Handler aus.<br/> Ein generischer StateFlags-Wert wird in die Registrierung geschrieben, wenn die Datenträgerbereinigung normal ausgeführt wird. Dieser Wert speichert einfach den Zustand (aktiviert oder deaktiviert) des Handlers, als er zuletzt als Option für den Benutzer angezeigt wurde. Es gibt zwei mögliche Datenwerte für diese Einträge.
<ul>
<li>0: Der Handler wurde nicht ausgewählt.</li>
<li>1: Der Handler wurde ausgewählt.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrieren eines Handlers beim Datenträgerbereinigungs-Manager: Windows 2000 oder höher

Das Angeben von Anzeigetext in der Registrierung kann das Lokalisieren von Software erschweren. Aus diesem Grund unterstützen Windows 2000 und Windows XP die [**IEmptyVolumeCache2-Schnittstelle**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) mit ihrer bevorzugten [**Initialisierungsmethode InitializeEx.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) Unter Windows 2000 oder höher wird immer versucht, **IEmptyVolumeCache2::InitializeEx** vor [**IEmptyVolumeCache::Initialize aufrufen.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) Das System verwendet **Initialize** nur zum Initialisieren eines Handlers, wenn **IEmptyVolumeCache2** nicht verfügbar gemacht wird.

Im Hinblick auf die Registrierung besteht der einzige Unterschied unter Windows 2000 oder höher im Weglassen der Werte AdvancedButtonText, Display und Description, wenn [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) vom Handler verfügbar gemacht wird. Diese Werte, die ordnungsgemäß lokalisierten Text enthalten, werden dem Datenträgerbereinigungs-Manager beim Aufrufen von **InitializeEx bereitgestellt.**

### <a name="using-the-datadrivencleaner-object"></a>Verwenden des DataDrivenCleaner-Objekts

Das Betriebssystem stellt einen einfachen Datenträgerbereinigungshandler namens DataDrivenCleaner zur Verfügung. Verwenden Sie die CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} als Standardwert für den Unterschlüssel des Handlers unter **VolumeCaches,** wie unter Registrieren eines Handlers mit dem [Datenträgerbereinigungs-Manager: Allgemein](#registering-a-handler-with-the-disk-cleanup-manager-general)beschrieben, um dieses Objekt als Handler zu verwenden, anstatt Ihr eigenes zu implementieren.

DataDrivenCleaner macht [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)nicht verfügbar, sodass die Werte Anzeige und Beschreibung über die Registrierung bereitgestellt werden. Beachten Sie beim Deklarieren dieser Zeichenfolgen, dass dies zu Lokalisierungsproblemen führen kann. Lokalisierter Text kann über den PropertyBag-Wert bereitgestellt werden. Der AdvancedButtonText-Wert wird ignoriert, da für diesen Handler keine Benutzeroberfläche und somit keine Schaltfläche zum Anzeigen verfügbar ist.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Beispielregistrierung eines Datenträgerbereinigungshandlers

Im Folgenden finden Sie ein Beispiel für die Registrierung eines Datenträgerbereinigungshandlers, der von The Telefon Company implementiert wird. Dieser Handler implementiert sowohl [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) als auch [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)und stellt daher AdvancedButtonText-, Description- und Display-Werte für den Fall zur Verwendung auf einem Computer mit Windows 98 zur Anwendung. Der Handler kombiniert die CsIDL- und Folder-Werte, um nach Dateien im Verzeichnis C: Programme zu suchen. Das verzeichnis Telefon Company Temp und das \\ \\ \\ DDEVCF DOSUBDIRS-Flag wird so festgelegt, dass auch die Unterverzeichnisse durchsucht \_ werden. Nur dateien mit TMP- und TPC-Erweiterungen werden für die Bereinigung berücksichtigt, und das Flag DDEVCF PRIVATE LASTACCESS wird so festgelegt, dass von diesen Dateien nur dateien berücksichtigt werden, auf die 14 Tage oder mehr nicht zugegriffen \_ \_ wurde. Das DDEVCF DONTSHOWIFZERO-Flag wird ebenfalls so festgelegt, dass der Handler nicht in der Liste angezeigt wird, es sei denn, er hat \_ Cleanupkandidaten gefunden.

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

 

