---
title: Verwenden von WER
description: Ab Windows Vista bietet Windows standardmäßig Absturz-, Nichtantwort- und Kernelfehlerberichte, ohne dass Änderungen an Ihrer Anwendung erforderlich sind.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Windows fehlerberichterstattung Windows-Fehlerberichterstattung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dfa8bc2235f43770cd177ad3e5d9a7d1aacde36034152b88cb06af3879e8c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442240"
---
# <a name="using-wer"></a>Verwenden von WER

Ab Windows Vista bietet Windows standardmäßig Absturz-, Nichtantwort- und Kernelfehlerberichte, ohne dass Änderungen an Ihrer Anwendung erforderlich sind. Der Bericht enthält bei Bedarf Minidump- und Heapabbildinformationen. Anwendungen verwenden stattdessen die WER-API, um anwendungsspezifische Problemberichte an Microsoft zu senden.

Da Windows automatisch nicht behandelte Ausnahmen meldet, sollte die Anwendung keine schwerwiegenden Ausnahmen behandeln. Wenn der fehlerhafte oder nicht reagierende Prozess interaktiv ist, zeigt WER eine Benutzeroberfläche an, die den Benutzer über das Problem informiert. Eine Anwendung gilt als nicht reagierend, wenn sie fünf Sekunden lang nicht Windows antwortet, während der Benutzer versucht, mit der Anwendung zu interagieren.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Windows-Fehlerberichterstattung bei Abstürzen, Nichtantwortfehlern und Kernelfehlern

Im Folgenden werden die Schritte gezeigt, die bei einem Anwendungsabsturz, einer Nichtantwort oder einem Kernelfehler auftreten.

1.  Das Problemereignis tritt auf.
2.  Das Betriebssystem ruft WER auf.
3.  WER sammelt die Daten, erstellt einen Bericht und fordert den Benutzer zur Zustimmung auf (falls erforderlich).
4.  WER sendet den Bericht an Microsoft (Watson Server), wenn der Benutzer zugestimmt hat.
5.  Wenn der Watson-Server zusätzliche Daten an fordert, sammelt WER die Daten und fordert den Benutzer zur Zustimmung auf (falls erforderlich).
6.  Wenn sich die Anwendung für die Wiederherstellung und den Neustart registriert hat, führt WER die registrierten Rückruffunktionen aus, während die Daten komprimiert und an Microsoft gesendet werden (wenn der Benutzer zugestimmt hat).
7.  Wenn eine Antwort auf das Problem von Microsoft verfügbar ist, wird der Benutzer benachrichtigt.

Anwendungen können die folgenden Funktionen verwenden, um den Inhalt des Berichts anzupassen, der an Microsoft gesendet wird. Die Registrierungsfunktionen teilen WER mit, dass die spezifischen Dateien und Speicherblöcke in den von ihm erstellten Fehlerbericht enthalten sind.

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Windows-Fehlerberichterstattung für die generische Ereignisberichterstattung

Die folgenden Schritte zeigen, wie Anwendungen einen Fehlerbericht für einen nicht schwerwiegenden Fehlerzustand erhalten können.

1.  Das nicht schwerwiegende Problemereignis tritt auf.
2.  Die Anwendung erkennt das Ereignis und verwendet die folgende Sequenz von Funktionsaufrufen, um den Bericht zu generieren.
    1.  Rufen Sie die [**WerReportCreate-Funktion**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) auf, um den Bericht zu erstellen.
    2.  Rufen Sie die [**WerReportSetParameter-Funktion**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) auf, um die Berichtsparameter festlegen.
    3.  Rufen Sie die [**WerReportAddFile-Funktion**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) auf, um dem Bericht Dateien hinzuzufügen.
    4.  Rufen Sie die [**WerReportAddDump-Funktion**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) auf, um dem Bericht (falls erforderlich) einen Minidump hinzuzufügen.
    5.  Rufen Sie die [**WerReportSubmit-Funktion auf,**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) um den Bericht zu senden.
    6.  Rufen Sie [**WerReportCloseHandle auf, um**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) Ressourcen frei zu geben.
3.  Abhängig von den spezifischen Optionen, die beim Aufrufen der Funktionen in Schritt 2 verwendet werden, beendet WER die Fehlerberichterstattung. WER stellt sicher, dass die Berichterstellung in Übereinstimmung mit den vom Benutzer festgelegten Richtlinien erfolgt. BEISPIELSWEISE sendet WER den Bericht an Microsoft, stellt den Bericht in die Warteschlange und zeigt dem Benutzer die entsprechenden Benutzeroberflächen an.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Ausschließen einer Anwendung aus Windows-Fehlerberichterstattung

Verwenden Sie die [**WerAddExcludedApplication-Windows,**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) um Ihre Anwendung von der Fehlerberichterstattung auszuschließen. Verwenden Sie die [**WerRemoveExcludedApplication-Funktion,**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication) um die Fehlerberichterstattung für Ihre Anwendung wiederherzustellen.

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Automatisches Wiederherstellen von Daten und Neustarten einer fehlerhaften Anwendung

Eine Anwendung kann Application Recovery und Restart verwenden, um Daten und Zustandsinformationen zu speichern, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird oder wenn die Anwendung nicht mehr reagiert. Die Anwendung wird auch neu gestartet, wenn dies angefordert wird. Weitere Informationen finden Sie unter [Anwendungswiederherstellung und Neustarten](/windows/desktop/Recovery/application-recovery-and-restart-portal)von .

## <a name="legacy-api"></a>Legacy-API

Eine Anwendung kann einen Fehler melden, indem sie die [**ReportFault-Funktion**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) aufruft. Sie sollten die **ReportFault-Funktion** jedoch nur verwenden, wenn sie eine sehr spezifische Anforderung haben, dass das Standardverhalten der Fehlerberichterstattung des Betriebssystems nicht erfüllt werden kann.

Wenn die Fehlerberichterstattung aktiviert ist, zeigt das System dem Benutzer ein Dialogfeld an, das angibt, dass die Anwendung ein Problem festgestellt hat und geschlossen wird. Wenn in der **HKEY LOCAL \_ \_ MACHINE \\ SOFTWARE Microsoft Windows \\ \\ NT \\ CurrentVersion \\ AeDebug-Taste** ein Debugger konfiguriert ist, erhält der Benutzer die Möglichkeit, den Debugger zu starten. Der Benutzer erhält auch die Möglichkeit, einen Bericht an Microsoft zu senden. Wenn der Benutzer den Bericht sendet, zeigt das System ein weiteres Dialogfeld an, das dem Benutzer für den Bericht dankt und einen Link zu weiteren Informationen enthält.

Das Fehlerberichterstattungssystem unterstützt die folgenden Betriebsmodi.



| Betriebsmodus          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Berichterstellung für freigegebenen Speicher | Wenn der Sicherheitskontext der Anwendung mit dem Sicherheitskontext des angemeldeten Benutzers identisch ist, verwendet das Fehlerberichterstattungssystem einen Block freigegebenen Speichers für die Kommunikation. Dieser Modus kann nicht mit dem Manifestberichtsmodus verwendet werden.<br/>                                                                                               |
| Manifestberichterstellung      | Wenn der Sicherheitskontext der Anwendung nicht mit dem Sicherheitskontext des angemeldeten Benutzers identisch ist, verwendet das Fehlerberichterstattungssystem eine Datei für die Kommunikation. Dieser Modus wird auch verwendet, um nicht reagierende Anwendungen und Kernelfehler zu melden. Dieser Modus kann nicht mit dem Berichterstellungsmodus für freigegebenen Speicher verwendet werden.<br/>                      |
| Internetberichterstellung      | Das Fehlerberichterstattungssystem sendet alle Daten über das Internet an Microsoft. Dies ist der Standardbetriebsmodus. Sie kann nicht im Berichterstellungsmodus des Unternehmens verwendet werden. Dieser Modus wird verwendet, wenn vom Administrator kein Unternehmensuploadpfad angegeben wurde.<br/>                                                                     |
| Unternehmensberichte     | Das Fehlerberichterstattungssystem sendet alle Daten an eine Dateifreigabe, anstatt sie direkt an Microsoft hochzuladen. Auf diese Weise können IT-Manager von Unternehmen Daten überprüfen, bevor sie an Microsoft gesendet werden. Dieser Modus wird verwendet, wenn vom Administrator ein Unternehmensuploadpfad angegeben wird. Sie kann nicht mit dem Internetberichtsmodus verwendet werden.<br/> |
| Headless Reporting      | Das Fehlerberichterstattungssystem zeigt dem Benutzer keine Dialogfelder an. Auf diese Weise können IT-Manager in Unternehmen jederzeit Fehlerberichte von ihren Mitarbeitern erfassen. Dieser Modus wird verwendet, wenn die Berichterstellung vom Administrator aktiviert wird, die Benachrichtigung jedoch deaktiviert ist. Sie kann nur im Berichterstellungsmodus des Unternehmens verwendet werden.<br/>        |



 

Um Ihre Anwendung von der Fehlerberichterstattung auszuschließen, verwenden Sie die [**AddERExcludedApplication-Funktion.**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa)

 

