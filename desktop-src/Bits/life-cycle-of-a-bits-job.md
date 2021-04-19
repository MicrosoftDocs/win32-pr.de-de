---
title: Lebenszyklus eines Bits-Auftrags
description: Der Lebenszyklus eines Bits-Auftrags beginnt, wenn Sie einen Auftrag erstellen.
ms.assetid: b765a8ef-74bd-475e-9cd9-e9e2cf4f0305
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c6ac23c598d28681968e9c0cbed776ba24c57e98
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357164"
---
# <a name="bits-job-states"></a>Bits-Auftrags Zustände
Es gibt vier Klassen von Bits- [**Zuständen**](/windows/desktop/api/Bits/ne-bits-bg_job_state): starten, Aktion, übertragen und endgültig. Während der Ausführung eines Auftrags wechselt er zwischen den Zuständen in den verschiedenen Zustands Klassen. Sobald sich ein Auftrag in einem Endzustand befindet, wird er nicht mehr in den Endzustand versetzt und wird nicht in einer [Auftrags Enumeration](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs)angezeigt.

## <a name="state-changing-methods"></a>Status veränderliche Methoden
Es gibt vier Status veränderliche Methoden für einen Auftrag: [**Abbrechen**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel), [**vervollständigen**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete), [**fort**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)setzen und [**aussetzen**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend). Solange sich ein Auftrag nicht in einem Endzustand befindet, können Sie jede der Zustands veränderlichen Methoden aufzurufen. 

Die [**Suspend**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend) -Methode wird verwendet, um einen Auftrag in den Zustand "angehalten" zu wechseln. Wenn ein Auftrag angehalten wird, werden alle zugehörigen Übertragungen angehalten und werden erst wieder fortgesetzt, wenn Sie "Resume" aufgerufen haben.
Ein Auftrag, der bereits angehalten wurde, bleibt einfach angehalten.

Die [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) -Methode wird verwendet, um einen Auftrag zu starten, der angehalten wurde. Aufträge in einem Fehler-oder vorübergehenden Fehlerzustand werden so eingerichtet, dass Sie wiederholt werden. Aufträge, die sich zurzeit in einem Aktionszustand befinden, bleiben in diesem Zustand.

Die [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode wird verwendet, um einen Auftrag abzubrechen. Der Status wechselt zu "abgebrochen". Derzeit übertragene Dateien werden nicht abgeschlossen. Alle vollständig übertragenen und teilweise übertragenen Dateien werden gelöscht.

Mit der [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode wird eine Übertragung abgeschlossen. Alle vollständig heruntergeladenen Dateien werden beibehalten. Dateien, die nicht vollständig übertragen werden, werden gelöscht.

Sie müssen entweder abbrechen oder abgeschlossen anrufen, um den Auftrag in einen Endzustand zu verschieben und bereinigt zu werden. Bei Aufträgen, die nicht in den Endzustand übergehen, werden Systemressourcen verschwendet. Mit Bits werden letztendlich alte Aufträge automatisch abgebrochen. Der Standardwert für " [jobinactivitytimeout](/windows/desktop/Bits/group-policies) " besteht darin, Aufträge nach 90 Tagen abzubrechen.


## <a name="starting-state"></a>Anfangsstatus 
Der Start **Status ist "** angehalten". Von hier aus können Sie dem Auftrag Dateien hinzufügen und Auftrags-und Dateieigenschaften festlegen. Um die Übertragung eines Auftrags zu starten, wenden Sie den Vorgang für den Auftrag an. Wenn Sie einen Auftrag ohne Dateien wieder aufnehmen, wird ein BG_E_EMPTY Fehlercodes zurückgegeben, und der Auftrag bleibt angehalten.

## <a name="action-states"></a>Aktionszustände
In den Status in der **Warteschlange**, **verbinden** und über **tragen** wird die aktuelle interne Aktivität des Auftrags angezeigt. Ein Auftrag, der in die Warteschlange eingereiht wird, ist für die Planung bereit und wartet möglicherweise auf den Bits-Planer oder wartet darauf, dass sich der Benutzer angemeldet hat. Ein Auftrag, der eine Verbindung herstellt, versucht, eine Verbindung mit dem Server herzustellen, um mit der Dateiübertragung zu beginnen Ein Auftrag, der übertragen wird, lädt Ihre Dateien aktiv hoch oder lädt Sie herunter.

Der **vorübergehende Fehler** Zustand bedeutet, dass der Auftrag versucht hat, die Datei zu übertragen. Dies kann aus Netzwerk Richtlinien Gründen der Grund sein. der Auftrag kann blockiert werden, weil das aktuelle Netzwerk zu teuer ist. Dies kann auch für System Gründe blockiert werden, z. b. wenn sich das System im Akku-oder Spielmodus befindet oder weil keine Internetverbindung besteht. 

Aufträge, die den vorübergehenden Fehlerstatus aufweisen, werden bei Bedarf automatisch von Bits erneut versucht. Bits enthält einen [minimumretrydelay](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) -und einen [noprogresstimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) -Wert, um zu steuern, wann ein Auftrag wiederholt wird und wann Bits den Wiederholungsversuch beendet.


## <a name="transferred-states"></a>Übertragene Zustände
Die übertragenen Zustände erfolgen, wenn keine Übertragung mehr erfolgt. Sie müssen einen Auftrag in diesem Zustand entweder abbrechen oder beenden. Sie können auch weitere Dateien hinzufügen, die übertragen werden sollen, und "Resume ()" aufzurufen, aber dies ist nicht üblich.

Der **Fehler** Zustand tritt auf, wenn eine Übertragung erfolgt (es wird kein erneuter Versuch unternommen), aber nicht vollständig erfolgreich war. Alle Dateien müssen übertragen werden, damit Sie erfolgreich sind. bei einem permanenten Fehler tritt beim Auftrag ein Fehler auf. In der Regel rufen Sie entweder abbrechen oder Fertigstellen auf, um den Auftrag in einen Endzustand zu verschieben. Der Unterschied besteht darin, dass beim Anrufen von "Abbrechen" alle erfolgreich übertragenen Dateien gelöscht werden. Wenn Sie jedoch "Complete" (abgeschlossen) abrufen, werden alle erfolgreich übertragenen Dateien nicht gelöscht.

Mögliche Gründe für einen Fehlerzustand sind 
* Der Status "vorübergehender Fehler" (über die [noprogresstimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) -Einstellung hinaus) ist zu lang.
* Erhalten eines BG_E_TOKEN_REQUIRED Fehlers und benötigen Unterstützung [bei](/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs) Hilfsobjekten

Es ist eine gängige Vorgehensweise, einen Fehler im Auftrag neu zu konfigurieren und dann fortsetzen aufzurufen, um den Auftrag zu wiederholen. Beispielsweise kann es sein, dass Ihre APP den Remote Namen einer Datei über " [Server](/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename)Name" aktualisieren muss.

Der **übertragene** Zustand tritt auf, wenn eine Übertragung abgeschlossen und erfolgreich war. Zum Abschließen des Auftrags muss Complete aufgerufen werden. für Download Aufträge sind die heruntergeladenen Dateien erst verfügbar, wenn Sie "Complete" aufgerufen haben. Eine Ausnahme von dieser Regel sind Aufträge, bei denen es sich um Hochleistungs Aufträge handelt (und Sie sollten trotzdem "Complete" aufzurufen).

## <a name="final-states"></a>Endgültige Zustände
Sobald sich ein Auftrag in einem Endzustand befindet, können Sie keine der Zustands veränderlichen Methoden mehr abrufen. Der Auftrag wird **bestätigt** , nachdem Sie "Complete ()" aufgerufen haben und alle abgeschlossenen heruntergeladenen Dateien verfügbar sind. Der Auftrag wird **abgebrochen** , nachdem Sie Cancel () aufgerufen haben und alle heruntergeladenen Dateien gelöscht werden. 


## <a name="life-cycle-of-a-bits-job"></a>Lebenszyklus eines Bits-Auftrags

Der Lebenszyklus eines Bits-Auftrags beginnt, wenn Sie einen Auftrag erstellen. Ein Auftrag ist ein Container, der eine oder mehrere zu übertragenden Dateien enthält. Ein Auftrag verfügt auch über Eigenschaften, die angeben, wie Bits die Dateien überträgt und mit Ihrer Anwendung interagiert. Beispielsweise können Sie die Priorität des Auftrags angeben, unabhängig davon, ob es sich um einen Upload-oder Download Auftrag handelt und für welche Ereignisse eine Benachrichtigung empfangen werden soll.

Nachdem Sie den Auftrag erstellt haben, fügen Sie eine oder mehrere Dateien (hochgeladene Aufträge können nur eine Datei enthalten) für den Auftrag hinzu, und ändern Sie die Eigenschaftswerte entsprechend Ihrer Anwendung. Wenn Sie dem Auftrag eine Datei hinzufügen, geben Sie den lokalen (Client-) und den Remote Namen (Server) der Datei an. Für den Remote Dateinamen muss das http-, HTTPS-oder SMB-Protokoll verwendet werden. Dateien innerhalb eines Auftrags werden sequenziell verarbeitet (zuerst in, First Out).

Bits hält Aufträge automatisch an, wenn Sie erstellt werden. Sie müssen den Auftrag fortsetzen, um ihn in der Übertragungs Warteschlange zu aktivieren. Sie können einen Auftrag jederzeit aussetzen oder fortsetzen. Durch das Fortsetzen des Auftrags wird der Auftrag aus dem Zustand "angehalten" in den Warteschlangen Status verschoben. Der Auftrag verbleibt im Zustand "in Warteschlange", bis der Planer feststellt, dass er zum Übertragen von Dateien für den Auftrag steht. Alle Vordergrund Aufträge werden gleichzeitig mit einem Hintergrund Auftrag ausgeführt. Bits verarbeitet die Dateien in Vordergrund Aufträgen serialisiert.

Wenn es sich um einen Auftrag zum Übertragen von Dateien handelt, wechselt der Auftrag in den Verbindungsstatus, während Bits eine Verbindung mit dem Remote Server herstellt (angegeben im Remote Dateinamen). Wenn Bits eine Verbindung mit dem Remote Server herstellen kann, wird der Auftrag in den Übertragungs Status versetzt, wo er bleibt, bis der Zeit Slice endet, die Übertragung abgeschlossen ist, ein Fehler auftritt oder die Anwendung den Auftrag anhält.

Der Auftrag wechselt zwischen den Status "in Warteschlange", "Verbindung" und "übertragen", bis Bits alle Dateien im Auftrag überträgt. An diesem Punkt wechselt der Auftrag in den übertragenen Zustand. Bits verwendet die Roundrobin-Planung, um Aufträge zu planen, die dieselbe Prioritätsstufe haben. Jeder Auftrag erhält einen Zeitanteil, um seine Dateien zu verarbeiten. Wenn der Auftrag während des Zeitabschnitts nicht beendet wird, wird der Auftrag in den Warteschlangen Status zurückversetzt, und der nächste Auftrag in der Warteschlange wird aktiviert. Dadurch wird verhindert, dass große Aufträge kleinere Aufträge blockieren. Aufträge werden größtenteils auf der Grundlage einer FIFO-Basis (First in, First Out) verarbeitet. Allerdings kann Bits die FIFO-Verarbeitung aufgrund von Roundrobin-Zeitplänen, Auftrags Fehlern und Dienst Neustarts nicht garantieren.

Die übertragenen Dateien stehen dem Client erst zur Verfügung, wenn die Anwendung die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufruft, um den Besitz der Dateien von Bits an den Benutzer zu übertragen. Uploadaufträge werden auch auf den übertragenen Status festgelegt, wenn die Datei vom Server erfolgreich empfangen wird. Upload-Antwort-Aufträge werden auf den übertragenen Status festgelegt, nachdem die Datei erfolgreich an den Server gesendet wurde und die Antwort von der Serveranwendung erfolgreich an den Client übertragen wurde.

Wenn ein Fehler auftritt, wird der Auftrag entweder in den schwerwiegenden oder vorübergehenden Fehlerzustand verschoben. Schwerwiegende Fehler sind Fehler, die von Bits nicht wieder hergestellt werden können oder für die ein Eingriff erforderlich ist. Wenn die Anwendung den Fehler beheben kann, wird der Auftrag von der Anwendung fortgesetzt, und Bits verschiebt den Auftrag in den Warteschlangen Zustand. Vorübergehende Fehler sind Fehler, die sich möglicherweise selbst auflösen. Bits führt einen Wiederholungsversuch für Aufträge im vorübergehenden Fehlerstatus aus, bis die Übertragung erfolgreich ist oder für den Auftrag ein Timeout eintritt. Für den Auftrag wird ein Timeout ausgelöst, wenn innerhalb eines von der Anwendung angegebenen Zeitraums kein Fortschritt erfolgt. Wenn für den Auftrag ein Timeout auftritt, verschiebt Bits den Auftrag in einen schwerwiegenden Fehlerzustand.

Weitere Informationen zu Auftrags Zuständen finden Sie unter [**\_ \_ Status der BG-Aufträge**](/windows/desktop/api/Bits/ne-bits-bg_job_state).
