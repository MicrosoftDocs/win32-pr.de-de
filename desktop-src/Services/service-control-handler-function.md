---
description: Jeder Dienst verfügt über einen Steuerelement Handler, die Handlerfunktion, die vom Steuerelement Verteiler aufgerufen wird, wenn der Dienst Prozess eine Steuerungs Anforderung von einem Dienst Steuerungsprogramm empfängt.
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: Dienststeuerungshandler-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1303bff45421ee7206d02be9ee30066324648823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343278"
---
# <a name="service-control-handler-function"></a>Dienststeuerungshandler-Funktion

Jeder Dienst verfügt über einen Steuerelement Handler, die [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) , die vom Steuerelement Verteiler aufgerufen wird, wenn der Dienst Prozess eine Steuerungs Anforderung von einem Dienst Steuerungsprogramm empfängt. Daher wird diese Funktion im Kontext des Steuerelement Verteilers ausgeführt. Ein Beispiel finden Sie unter [Schreiben einer Steuerelement Handler-Funktion](writing-a-control-handler-function.md).

Ein Dienst ruft die [**registerservicectrlhandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) -oder [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion auf, um seine Dienststeuerungs-Handlerfunktion zu registrieren.

Wenn der Dienst Steuerungs Handler aufgerufen wird, muss der Dienst die [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) -Funktion aufrufen, um seinen Status nur dann an den SCM zu melden, wenn die Verarbeitung des Steuerungs Codes bewirkt, dass der Dienststatus geändert wird. Wenn die Verarbeitung des Steuerungs Codes nicht bewirkt, dass der Dienststatus geändert wird, ist es nicht erforderlich, **SetServiceStatus** aufzurufen.

Ein Dienst Steuerungsprogramm kann Steuerungsanforderungen mithilfe der [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion senden. Alle Dienste müssen den Steuerungs Code der **\_ Dienststeuerungs- \_ Abfrage** akzeptieren und verarbeiten. Sie können die Annahme der anderen Kontrollcodes durch Aufrufen von [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)aktivieren oder deaktivieren. Sie müssen die [**registerdevicenotifi-**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) Funktion aufrufen, um den Steuerungs Code der **Dienst \_ Steuerung \_ deviceevent** zu erhalten. Dienste können auch zusätzliche benutzerdefinierte Steuerungs Codes verarbeiten.

Wenn ein Dienst den Steuerungs Code für die **\_ \_ Beendigung der Dienst Kontrolle** annimmt, muss er **nach der Bestätigung \_ \_** angeh **\_ alten** werden. Nachdem der SCM diesen Steuerungs Code gesendet hat, sendet er keine anderen Steuerungs Codes.

**Windows XP:** Wenn der Dienst **keinen \_ Fehler** zurückgibt und weiterhin ausgeführt wird, empfängt er weiterhin Steuerungs Codes. Dieses Verhalten hat sich seit Windows Server 2003 und Windows XP mit Service Pack 2 (SP2) geändert.

Der Steuerelement Handler muss innerhalb von 30 Sekunden zurückgeben, oder der SCM gibt einen Fehler zurück. Wenn ein Dienst eine lange Verarbeitung ausführen muss, während der Dienst den Steuerelement Handler ausführt, sollte er einen sekundären Thread erstellen, um die lange Verarbeitung auszuführen, und dann vom Steuerelement Handler zurückgeben. Dadurch wird verhindert, dass der Dienst den Steuerelement Verteiler bindet. Wenn Sie z. b. die Anforderung zum Beenden für einen Dienst verarbeiten, der lange dauert, erstellen Sie einen weiteren Thread, um den Vorgang zu beenden. Der Steuerelement Handler sollte einfach [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit dem **Dienst \_ " \_ ausstehende Nachricht Abbrechen** " aufrufen und zurückgeben.

Wenn der Benutzer das System herunterfährt, erhalten alle Steuerelemente, die [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit dem Dienst aufgerufen haben, den Steuerungs Code für das **\_ \_ vorab Herunterfahren der Dienst Kontrolle** . **\_ \_** Der Dienststeuerungs-Manager wartet, bis der Dienst beendet wird oder der angegebene Timeout Wert für das vorherunter fahren abläuft (dieser Wert kann mit der [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion festgelegt werden). Dieser Steuerungs Code sollte nur in besonderen Fällen verwendet werden, da ein Dienst, der diese Benachrichtigung verarbeitet, das Herunterfahren des Systems blockiert, bis der Dienst beendet wird oder das Timeout Intervall für das vorherunter fahren abläuft.

Nachdem die Benachrichtigungen vor dem Herunterfahren abgeschlossen wurden, erhalten alle Steuerelement Handler, die [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit dem Dienst mit dem **Dienst " \_ \_ herunter** fahren" aufgerufen haben, den Steuerungs Code für das Herunterfahren der **Dienst \_ \_ Kontrolle** . Sie werden in der Reihenfolge benachrichtigt, in der Sie in der Datenbank der installierten Dienste angezeigt werden. Standardmäßig hat ein Dienst ungefähr 20 Sekunden Zeit, um Bereinigungs Tasks auszuführen, bevor das System heruntergefahren wird. Nach Ablauf dieses Zeitraums wird das Herunterfahren des Systems unabhängig davon fortgesetzt, ob der Dienst beendet wurde. Beachten Sie, dass der Dienst weiterhin ausgeführt wird, wenn das System nicht neu gestartet oder ausgeschaltet wird.

Wenn für den Dienst mehr Zeit zum Bereinigen benötigt wird, **werden \_ ausstehende** Statusmeldungen angehalten und ein Wait-Hinweis gesendet, sodass der Dienst Controller weiß, wie lange gewartet werden muss, bevor eine Berichterstattung an das System erfolgt, in dem der Dienst heruntergefahren wird. Um zu verhindern, dass ein Dienst heruntergefahren wird, gibt es jedoch eine Beschränkung, wie lange der Dienst Controller wartet. Wenn der Dienst über das Dienste-Snap-in heruntergefahren wird, beträgt der Grenzwert 125 Sekunden oder 125.000 Millisekunden. Wenn das Betriebssystem neu gestartet wird, wird das Zeitlimit im Wert von **WaitToKillServiceTimeout** (in Millisekunden) des folgenden Registrierungsschlüssels angegeben:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet- \\ Steuerelement**

> [!IMPORTANT]
> Ein Dienst sollte nicht versuchen, das Zeitlimit durch Ändern dieses Werts zu erhöhen. Wenn Sie **waitykillservicetimeout** per Hand festlegen müssen, sollte der Wert in Millisekunden angegeben werden.

Kunden müssen das Betriebssystem schnell Herunterfahren. Wenn z. b. ein Computer, auf dem das PowerShell-Betriebsnetz ausgeführt wird, das Herunterfahren nicht beenden kann, bevor die Leistung von UPS nicht mehr besteht, Daher sollten die-Dienste ihre Bereinigungs Aufgaben so schnell wie möglich ausführen. Es wird empfohlen, nicht gespeicherte Daten zu minimieren, indem Sie Daten in regelmäßigen Abständen speichern, die auf dem Datenträger gespeicherten Daten nachverfolgen und nur die nicht gespeicherten Daten beim Herunterfahren speichern. Da der Computer heruntergefahren wird, verbringen Sie nicht Zeit, zugeordneten Arbeitsspeicher oder andere Systemressourcen freizugeben. Wenn Sie einen Server Benachrichtigen müssen, den Sie beenden möchten, minimieren Sie die Zeit, die auf eine Antwort gewartet hat, da Netzwerkprobleme das Herunterfahren des Dienes verzögern könnten.

Beachten Sie, dass der SCM beim Herunterfahren von Diensten standardmäßig keine Abhängigkeiten berücksichtigt. Der SCM listet die ausgelaufenden Dienste auf und sendet den Befehl zum **\_ \_ Herunterfahren der Dienst Kontrolle** . Daher kann ein Dienst fehlschlagen, weil ein anderer Dienst, von dem er abhängt, bereits beendet wurde.

Um die Konfiguration der Dienste manuell festzulegen, erstellen Sie einen Registrierungs Wert mit mehreren Zeichen folgen, der die Dienstnamen in der Reihenfolge enthält, in der Sie heruntergefahren werden sollen, und weisen Sie ihn wie folgt dem **preshutdownorder** -Wert des Steuer Elements zu.

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ preshutdownorder = "Shutdown Order"**

Verwenden Sie die Funktion [**setprocessshutdownparameters**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) , um die Shutdown-Reihenfolge abhängiger Dienste von der Anwendung festzulegen. Der SCM verwendet diese Funktion, um dem Handler die Priorität 0x1e0 zu übergeben. Der SCM sendet **Dienst \_ Steuerungs \_** Benachrichtigungen für das Herunterfahren, wenn der zugehörige Steuerelement Handler aufgerufen wird, und wartet, bis die Dienste beendet werden, bevor er vom Steuerelement Handler

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben einer Steuerelement Handler-Funktion](writing-a-control-handler-function.md)
</dt> </dl>

 

 
