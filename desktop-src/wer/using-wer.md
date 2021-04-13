---
title: Verwenden von wer
description: Ab Windows Vista stellt Windows die Fehlerberichterstattung für Abstürze, nicht-Antworten und Kernel Fehler standardmäßig bereit, ohne dass Änderungen an der Anwendung erforderlich sind.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Windows-Fehlerberichterstattung für die Windows-Fehlerberichterstattung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bed6d11757d7d4e08cd00ac47479e1246f96b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104390134"
---
# <a name="using-wer"></a>Verwenden von wer

Ab Windows Vista stellt Windows die Fehlerberichterstattung für Abstürze, nicht-Antworten und Kernel Fehler standardmäßig bereit, ohne dass Änderungen an der Anwendung erforderlich sind. Der Bericht enthält bei Bedarf Minidump-und Heap-Dumpinformationen. Anwendungen verwenden stattdessen die wer-API, um anwendungsspezifische Problemberichte an Microsoft zu senden.

Da Windows automatisch nicht behandelte Ausnahmen meldet, sollte die Anwendung keine schwerwiegenden Ausnahmen verarbeiten. Wenn der fehlerhafte oder nicht reagierende Prozess interaktiv ist, zeigt wer eine Benutzeroberfläche an, die den Benutzer über das Problem informiert. Eine Anwendung gilt als nicht reagierend, wenn Sie fünf Sekunden lang nicht auf Windows-Meldungen antwortet, während der Benutzer versucht, mit der Anwendung zu interagieren.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Windows-Fehlerberichterstattung Fluss für Abstürze, nicht-Antwort-und Kernel Fehler

Im folgenden werden die Schritte gezeigt, die für einen Anwendungs Absturz, einen nicht-Antwort-oder einen Kernel Fehler auftreten.

1.  Das Problem Ereignis tritt auf.
2.  Das Betriebssystem ruft wer auf.
3.  Wer sammelt die Daten, erstellt einen Bericht und fordert den Benutzer zur Zustimmung auf (falls erforderlich).
4.  Wer sendet den Bericht an Microsoft (Watson Server), wenn der Benutzer zugestimmt hat.
5.  Wenn der Watson-Server zusätzliche Daten anfordert, sammelt wer die Daten und fordert den Benutzer zur Zustimmung auf (falls erforderlich).
6.  Wenn die Anwendung für die Wiederherstellung registriert und neu gestartet wird, führt wer die registrierten Rückruf Funktionen aus, während die Daten komprimiert und an Microsoft gesendet werden (wenn der Benutzer zugestimmt hat).
7.  Wenn bei Microsoft eine Antwort auf das Problem verfügbar ist, wird der Benutzer benachrichtigt.

Anwendungen können die folgenden Funktionen verwenden, um den Inhalt des Berichts anzupassen, der an Microsoft gesendet wird. Die Registrierungsfunktionen geben an, dass die bestimmten Dateien und Speicherblöcke in den von ihm erstellten Fehlerbericht eingeschlossen werden sollen.

-   [**Werregisterfile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**Werregistermemoryblock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**Wersetflags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**Werunregisterfile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**Werunregistermemoryblock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**Wergetflags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Windows-Fehlerberichterstattung Fluss für die generische Ereignis Berichterstattung

Die folgenden Schritte zeigen, wie Anwendungen einen Fehlerbericht für eine nicht schwerwiegende Fehlerbedingung erhalten können.

1.  Das nicht schwerwiegende Problem Ereignis tritt auf.
2.  Die Anwendung erkennt das Ereignis und verwendet die folgende Sequenz von Funktionsaufrufen, um den Bericht zu generieren.
    1.  Rufen Sie die Funktion " [**werreportcreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) " auf, um den Bericht zu erstellen.
    2.  Aufrufen der Funktion " [**werreportsetparameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) " zum Festlegen der Berichts Parameter.
    3.  Ruft die Funktion " [**werreportaddfile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) " auf, um dem Bericht Dateien hinzuzufügen.
    4.  Nennen Sie die Funktion " [**werreportadddump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) ", um dem Bericht ein Minidump hinzuzufügen (falls erforderlich).
    5.  Ruft die Funktion " [**werreportsubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) " auf, um den Bericht zu senden.
    6.  Wenden Sie das [**werreportclosehandle**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) an, um Ressourcen freizugeben.
3.  Abhängig von den spezifischen Optionen, die beim Aufrufen der Funktionen in Schritt 2 verwendet werden, beendet wer die Fehlerberichterstattung. Wer stellt sicher, dass die Berichterstellung gemäß den vom Benutzer festgelegten Richtlinien durchgeführt wird. Angenommen, der Bericht wird an Microsoft gesendet, der Bericht in die Warteschlange eingereiht und dem Benutzer die entsprechenden Benutzeroberflächen angezeigt.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Ausschließen einer Anwendung von Windows-Fehlerberichterstattung

Verwenden Sie die Funktion " [**weraddexcludedappliction"**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) , um Ihre Anwendung aus der Windows-Fehlerberichterstattung auszuschließen. Verwenden Sie die Funktion " [**werremoveexcludedappliction"**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication) , um die Fehlerberichterstattung für die Anwendung wiederherzustellen.

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Automatisches Wiederherstellen von Daten und Neustarten einer fehlerhaften Anwendung

Eine Anwendung kann zum Speichern von Daten-und Zustandsinformationen verwendet werden, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird, oder wenn die Anwendung nicht mehr reagiert. Die Anwendung wird bei Bedarf ebenfalls neu gestartet. Weitere Informationen finden Sie unter [Anwendungs Wiederherstellung und Neustart](/windows/desktop/Recovery/application-recovery-and-restart-portal).

## <a name="legacy-api"></a>Legacy-API

Eine Anwendung kann einen Fehler melden, indem Sie die [**reportfault**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) -Funktion aufrufen. Sie sollten jedoch nicht die Funktion **Report Fault** verwenden, es sei denn, Sie haben eine sehr spezielle Anforderung, dass das Standardverhalten der Fehlerberichterstattung des Betriebssystems nicht erfüllt werden kann.

Wenn die Fehlerberichterstattung aktiviert ist, zeigt das System dem Benutzer ein Dialogfeld an, das anzeigt, dass die Anwendung ein Problem feststellt und geschlossen wird. Wenn ein Debugger im Schlüssel **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AEDebug** konfiguriert ist, erhält der Benutzer die Möglichkeit, den Debugger zu starten. Der Benutzer erhält auch die Option, einen Bericht an Microsoft zu senden. Wenn der Benutzer den Bericht sendet, zeigt das System ein weiteres Dialogfeld an, in dem der Benutzer für den Bericht informiert ist, und stellt einen Link zu weiteren Informationen bereit.

Das Fehler Berichterstattungs System unterstützt die folgenden Vorgangs Modi:



| Betriebsmodus          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Shared Memory-Berichterstellung | Wenn der Sicherheitskontext der Anwendung mit dem Sicherheitskontext des angemeldeten Benutzers identisch ist, verwendet das Fehler Berichterstattungs System einen Block freigegebenen Speichers für die Kommunikation. Dieser Modus kann nicht mit dem Manifest-Berichtsmodus verwendet werden.<br/>                                                                                               |
| Manifeste Berichterstellung      | Wenn der Sicherheitskontext der Anwendung nicht mit dem Sicherheitskontext des angemeldeten Benutzers identisch ist, verwendet das Fehler Berichterstattungs System eine Datei für die Kommunikation. Dieser Modus wird auch zum Melden von nicht reagierenden Anwendungen und Kernel Fehlern verwendet. Dieser Modus kann nicht mit dem Berichtsmodus für freigegebenen Speicher verwendet werden.<br/>                      |
| Internet Berichterstellung      | Das Fehler Berichterstattungs System sendet alle Daten über das Internet an Microsoft. Dies ist der Standardbetriebsmodus. Sie kann nicht mit dem Unternehmensbericht Erstellungs Modus verwendet werden. Dieser Modus wird verwendet, wenn vom Administrator kein Unternehmens hoch Lade Pfad angegeben wird.<br/>                                                                     |
| Unternehmensbericht Erstellung     | Das Fehler Berichterstattungs System sendet alle Daten an eine Dateifreigabe, anstatt Sie direkt an Microsoft zu hochladen. Dadurch können IT-Manager von Unternehmen Daten überprüfen, bevor Sie an Microsoft gesendet werden. Dieser Modus wird verwendet, wenn ein vom Administrator angegebener unternehmensuploadpfad vorliegt. Sie kann nicht mit dem Internet Bericht Erstellungs Modus verwendet werden.<br/> |
| Kostenlose Berichterstellung      | Das Fehler Berichterstattungs System zeigt keine Dialogfelder für den Benutzer an. Dadurch können IT-Manager von Unternehmen jederzeit Fehlerberichte von ihren Mitarbeitern sammeln. Dieser Modus wird verwendet, wenn die Berichterstellung vom Administrator aktiviert wird, die Benachrichtigung aber deaktiviert ist. Sie kann nur mit dem Unternehmensbericht Erstellungs Modus verwendet werden.<br/>        |



 

Verwenden Sie die [**adderexcludedappliction-**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa) Funktion, um die Anwendung von der Fehlerberichterstattung auszuschließen.

 

