---
description: Die Entwicklung einer sicheren hochstufigen Netzwerkinfrastruktur ist für die meisten Netzwerk Anwendungsentwickler eine Priorität. Die Socketsicherheit wird jedoch oft übersehen, obwohl Sie sehr wichtig ist, wenn Sie eine vollständig sichere Lösung in Erwägung ziehen
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Verwenden von SO_REUSEADDR und SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756997"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Verwenden von " \_ reuseaddr" und " \_ exclusiveaddruse"

Die Entwicklung einer sicheren hochstufigen Netzwerkinfrastruktur ist für die meisten Netzwerk Anwendungsentwickler eine Priorität. Die Socketsicherheit wird jedoch oft übersehen, obwohl Sie sehr wichtig ist, wenn Sie eine vollständig sichere Lösung in Erwägung ziehen Socketsicherheit behandelt insbesondere Prozesse, die an denselben Port gebunden sind, der zuvor von einem anderen Anwendungsprozess gebunden wurde. In der Vergangenheit war es möglich, dass eine Netzwerk Anwendung den Port einer anderen Anwendung "Hijack", was zu einem Denial-of-Service-Angriff oder Datendiebstahl führen konnte.

Im Allgemeinen gilt die Socketsicherheit für serverseitige Prozesse. Genauer gesagt gilt die Socketsicherheit für alle Netzwerkanwendungen, die Verbindungen akzeptieren und IP-Datagramm-Datenverkehr empfangen. Diese Anwendungen werden in der Regel an einen bekannten Port gebunden und sind gängige Ziele für bösartigen Netzwerkcode.

Bei Client Anwendungen handelt es sich weniger wahrscheinlich um die Ziele solcher Angriffe – nicht, weil Sie weniger anfällig sind, aber weil die meisten Clients an die "kurzlebigen" lokalen Ports und nicht an statische "Service"-Ports gebunden sind. Client Netzwerkanwendungen sollten immer an kurzlebige Ports gebunden werden (durch Angabe von Port 0 in der [**sockaddr**](sockaddr-2.md) -Struktur, auf die durch den *Name* -Parameter beim Aufrufen der [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) -Funktion verwiesen wird), es sei denn, es gibt einen überzeugenden architektonischen Grund, nicht zu Die kurzlebigen lokalen Ports bestehen aus Ports, die größer sind als Port 49151. Die meisten Server Anwendungen für dedizierte Dienste binden an einen bekannten reservierten Port, der kleiner oder gleich Port 49151 ist. Bei den meisten Anwendungen kommt es in der Regel nicht zu einem Konflikt zwischen Client-und Server Anwendungen.

In diesem Abschnitt wird die Standardstufe der Sicherheit auf verschiedenen Microsoft Windows-Plattformen beschrieben, und es wird erläutert, wie sich die spezifischen Socketoptionen **so \_ reuseaddr** und [ \_ exclusiveaddruse](so-exclusiveaddruse.md) auf die Sicherheit der Netzwerk Anwendung auswirken. Ein zusätzliches Feature namens erweiterte Socketsicherheit ist unter Windows Server 2003 und höher verfügbar. Die Verfügbarkeit dieser Socketoptionen und der erweiterten Socketsicherheit variieren in den verschiedenen Versionen von Microsoft-Betriebssystemen, wie in der folgenden Tabelle dargestellt.

| Plattform            | \_reuseaddr | " \_ exclusiveaddruse"                  | Erweiterte Socketsicherheit |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Verfügbar     | Nicht verfügbar.                         | Nicht verfügbar.            |
| Windows 98          | Verfügbar     | Nicht verfügbar.                         | Nicht verfügbar.            |
| Windows Me          | Verfügbar     | Nicht verfügbar.                         | Nicht verfügbar.            |
| Windows NT 4.0      | Verfügbar     | Verfügbar in Service Pack 4 und höher | Nicht verfügbar.            |
| Windows 2000        | Verfügbar     | Verfügbar                             | Nicht verfügbar.            |
| Windows XP          | Verfügbar     | Verfügbar                             | Nicht verfügbar.            |
| Windows Server 2003 | Verfügbar     | Verfügbar                             | Verfügbar                |
| Windows Vista       | Verfügbar     | Verfügbar                             | Verfügbar                |
| Windows Server 2008 | Verfügbar     | Verfügbar                             | Verfügbar                |
| Windows 7 und höher  | Verfügbar     | Verfügbar                             | Verfügbar                |

## <a name="using-so_reuseaddr"></a>Verwenden von " \_ reuseaddr"

Die **\_ reuseaddr** -Socketoption ermöglicht einem Socket das erzwungene binden an einen Port, der von einem anderen Socket verwendet wird. Der zweite Socket ruft [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) auf, wobei der *optname* -Parameter auf festgelegt ist, **sodass \_ reuseaddr** und der *optval* -Parameter auf den booleschen Wert **true** festgelegt sind, bevor [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) am gleichen Port wie der ursprüngliche Socket aufgerufen wird. Nachdem der zweite Socket erfolgreich gebunden wurde, ist das Verhalten für alle Sockets, die an diesen Port gebunden sind, unbestimmt. Wenn z. b. alle Sockets am gleichen Port den TCP-Dienst bereitstellen, können alle eingehenden TCP-Verbindungsanforderungen über den Port nicht sichergestellt werden, dass Sie vom richtigen Socket verarbeitet werden – das Verhalten ist nicht deterministisch. Ein böswilliges Programm kann **so \_ reuseaddr** verwenden, um die bereits in Verwendung der standardmäßigen Netzwerkprotokoll Dienste verwendeten Sockets zu erzwingen, um den Zugriff auf diesen Dienst zu verweigern. Zur Verwendung dieser Option sind keine speziellen Berechtigungen erforderlich.

Wenn eine Client Anwendung an einen Port gebunden wird, bevor eine Serveranwendung an denselben Port gebunden werden kann, kann dies zu Problemen führen. Wenn die Serveranwendung die Bindung mit der " **so \_ reuseaddr** "-Socketoption an denselben Port erzwungen hat, ist das Verhalten für alle Sockets, die an diesen Port gebunden sind, unbestimmt.

Eine Ausnahme von diesem nicht deterministischen Verhalten sind Multicast-Sockets. Wenn zwei Sockets an dieselbe Schnittstelle und denselben Port gebunden sind und Mitglieder derselben Multicast Gruppe sind, werden die Daten an beide Sockets und nicht an einen willkürlich ausgewählten gebunden.

## <a name="using-so_exclusiveaddruse"></a>Verwenden von " \_ exclusiveaddruse"

Bevor die Socketoption " **so \_ exclusiveaddruse** " eingeführt wurde, gab es nur sehr wenig Netzwerk Anwendungsentwickler, um zu verhindern, dass ein schädliches Programm an den Port gebunden ist, an dem die Netzwerk Anwendung über eigene Sockets verfügt. Um dieses Sicherheitsproblem zu beheben, wurde in Windows Sockets die Socketoption " **so \_ exclusiveaddruse** " eingeführt, die unter Windows NT 4,0 mit Service Pack 4 (SP4) und höher verfügbar wurde.

Die " **so \_ exclusiveaddruse** "-Socketoption kann nur von Mitgliedern der Sicherheitsgruppe "Administratoren" auf Windows XP und früher verwendet werden. Die Gründe, warum diese Anforderung auf Windows Server 2003 und höher geändert wurde, werden später in diesem Artikel erläutert.

Die Option " **so \_ exclusiveaddruse** " wird festgelegt, indem die Funktion " [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) " aufgerufen wird, wobei der *optname* -Parameter auf " **\_ exclusiveaddruse** " und der *optval* -Parameter auf den booleschen Wert " **true** " festgelegt ist, bevor der Socket gebunden wird. Nachdem die Option festgelegt wurde, unterscheidet sich das Verhalten der nachfolgenden [**Bindungs**](/windows/win32/api/winsock/nf-winsock-bind) Aufrufe abhängig von der in den einzelnen **Bindungs** aufrufen angegebenen Netzwerkadresse.

In der folgenden Tabelle wird das Verhalten beschrieben, das in Windows XP und früher auftritt, wenn ein zweiter Socket versucht, eine Bindung an eine Adresse herzustellen, die zuvor durch einen ersten Socket mithilfe spezifischer Socketoptionen an gebunden wurde.

> [!NOTE]  
> In der folgenden Tabelle bezeichnet "Platzhalter" die Platzhalter Adresse für das angegebene Protokoll (z. b. "0.0.0.0" für IPv4 und "::" für IPv6). "Specific" bezeichnet eine bestimmte IP-Adresse, die einer Schnittstelle zugewiesen ist. In den Tabellenzellen wird angegeben, ob die Bindung erfolgreich war ("Erfolg"), oder es wird ein Fehler zurückgegeben ("InUse" für den Fehler " [WSAEADDRINUSE](windows-sockets-error-codes-2.md) "). "Access" für den [WSAEACCES](windows-sockets-error-codes-2.md) -Fehler).

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Erster <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungs</strong></a> Befehl</td>
        <td bgcolor="#C0C0C0" colspan="6">Zweiter <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungs</strong></a> Befehl</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Standard</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Standard</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
</table>

Wenn zwei Sockets an dieselbe Portnummer gebunden sind, aber an unterschiedlichen expliziten Schnittstellen, gibt es keinen Konflikt. Wenn ein Computer z. b. über zwei IP-Schnittstellen verfügt, 10.0.0.1 und 10.99.99.99, wenn der erste [**Bindungs**](/windows/win32/api/winsock/nf-winsock-bind) Vorgang auf 10.0.0.1 festgelegt ist und der Port auf 5150 und **somit \_ exclusiveaddruse** angegeben ist, wird ein zweiter **Bindungs** Vorgang an 10.99.99.99 mit dem Port auf 5150 festgelegt, und es werden keine Optionen angegeben. Wenn der erste Socket jedoch an die Platzhalter Adresse und den Port 5150 gebunden ist, schlagen alle nachfolgenden Bindungs Aufrufe an Port 5150 mit dem Wert " **\_ exclusiveaddruse** " fehl, wenn entweder [WSAEADDRINUSE](windows-sockets-error-codes-2.md) oder [WSAEACCES](windows-sockets-error-codes-2.md) vom **Bindungs** Vorgang zurückgegeben wird.

Wenn der [**erste Bindungs Vorgang**](/windows/win32/api/winsock/nf-winsock-bind) entweder " **\_ reuseaddr** " oder gar keine Socketoptionen festlegt, wird der zweite **Bindungs** Befehl den Port "Hijack" und die Anwendung nicht ermitteln können, welche der beiden Sockets bestimmte Pakete empfangen hat, die an den freigegebenen Port gesendet wurden.

Eine typische Anwendung, die die [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) -Funktion aufruft, weist den gebundenen Socket nicht zur exklusiven Verwendung zu, es sei denn, die Socketoption " **so \_ exclusiveaddruse** " wird für den Socket vor dem Aufruf der **Bind** -Funktion aufgerufen. Wenn eine Client Anwendung an einen kurzlebigen Port oder einen bestimmten Port gebunden wird, bevor eine Serveranwendung an denselben Port gebunden wird, können Probleme auftreten. Die Serveranwendung kann die Bindung an denselben Port erzwingen, indem die **so \_ reuseaddr** -Socketoption auf dem Socket verwendet wird, bevor die **Bind** -Funktion aufgerufen wird, aber das Verhalten für alle an diesen Port gebundenen Sockets ist dann unbestimmt. Wenn die Serveranwendung versucht, die " **so \_ exclusiveaddruse** "-Socketoption für die exklusive Verwendung des Ports zu verwenden, schlägt die Anforderung fehl.

Umgekehrt kann ein Socket mit der " **so \_ exclusiveaddruse** "-Menge nicht unbedingt sofort nach dem Socket-Abschluss wieder verwendet werden. Wenn z. b. ein lausch ender Socket mit der " **\_ exclusiveaddruse** "-Gruppe eine Verbindung akzeptiert und anschließend geschlossen wird, kann ein anderer Socket (auch mit " **\_ exclusiveaddruse**") nicht an denselben Port wie der erste Socket gebunden werden, bis die ursprüngliche Verbindung inaktiv wird.

Dieses Problem kann kompliziert werden, da das zugrunde liegende Transportprotokoll die Verbindung möglicherweise nicht beendet, obwohl der Socket geschlossen wurde. Auch nachdem der Socket von der Anwendung geschlossen wurde, muss das System alle gepufferten Daten übertragen, eine ordnungsgemäße Disconnect-Nachricht an den Peer senden und auf eine entsprechende ordnungsgemäße Disconnect-Nachricht vom Peer warten. Es ist möglich, dass das zugrunde liegende Transportprotokoll die Verbindung möglicherweise niemals freigibt. Beispielsweise kann der Peer, der an der ursprünglichen Verbindung teilnimmt, ein Fenster der Größe 0 (null) oder eine andere Form der "Angriffs Konfiguration" ankündigen. In einem solchen Fall verbleibt die Client Verbindung trotz der Anforderung zum Schließen in einem aktiven Zustand, da unbestätigte Daten im Puffer verbleiben.

Um dieses Problem zu vermeiden, sollten Netzwerkanwendungen ein ordnungsgemäßes Herunterfahren sicherstellen, indem Sie [**Shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) mit dem \_ festgelegten SD-sendeflag aufrufen und dann in einer [**empfangener**](/windows/win32/api/winsock/nf-winsock-recv) -Schleife warten, bis null Bytes über die Verbindung zurückgegeben werden. Dadurch wird sichergestellt, dass alle Daten vom Peer empfangen werden und mit dem Peer bestätigt werden, dass alle übertragenen Daten empfangen wurden, und dass die oben genannte Probleme bei der Port Wiederverwendung vermieden werden.

Die \_ Option "so LINGER Socket" kann für einen Socket festgelegt werden, um zu verhindern, dass der Port in den Wartezustand "aktiv" übergeht. Dies wird jedoch nicht empfohlen, da dies zu den gewünschten Effekten führen kann, wie z. b. beim Zurücksetzen von Verbindungen. Wenn z. b. Daten vom Peer empfangen, aber nicht bestätigt werden, und der lokale Computer den Socket mit so \_ festgelegtem LINGER schließt, wird die Verbindung zwischen den beiden Computern zurückgesetzt, und die unbestätigten Daten werden vom Peer verworfen. Die Auswahl eines geeigneten Zeitlimits ist schwierig, da ein kleinerer Timeout Wert oft zu plötzlich abgebrochenen Verbindungen führt, während größere Timeout Werte das System anfällig für Denial-of-Service-Angriffe sind (indem Sie viele Verbindungen einrichten und Anwendungsthreads potenziell Stalling/blockieren). Wenn Sie einen Socket schließen, der einen Linger-Timeout Wert ungleich NULL aufweist, kann auch der [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) -Befehl blockiert werden.

## <a name="enhanced-socket-security"></a>Erweiterte Socketsicherheit

Erweiterte Socketsicherheit wurde mit der Veröffentlichung von Windows Server 2003 hinzugefügt. In früheren Versionen des Microsoft-Server Betriebssystems ermöglichte die Standard-Socketsicherheit leicht die Verarbeitung von Ports aus nicht ahnungslosen Anwendungen. In Windows Server 2003 sind Sockets standardmäßig nicht in einem freileg baren Zustand. Wenn eine Anwendung es anderen Prozessen gestatten soll, einen Port wiederzuverwenden, an dem bereits ein Socket gebunden ist, muss Sie daher speziell aktiviert werden. Wenn dies der Fall ist, muss für den ersten Socket, der [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) für den Port aufruft, " **\_ reuseaddr** " auf dem Socket festgelegt sein. Die einzige Ausnahme zu diesem Fall tritt auf, wenn der zweite **Bindungs** Aufrufvorgang von demselben Benutzerkonto ausgeführt wird, das den ursprünglichen **Bindungs** Vorgang durchgeführt hat. Diese Ausnahme ist ausschließlich zur Bereitstellung der Abwärtskompatibilität vorhanden.

In der folgenden Tabelle wird das Verhalten beschrieben, das in Windows Server 2003 und höheren Betriebssystemen auftritt, wenn ein zweiter Socket versucht, eine Bindung an eine Adresse herzustellen, die zuvor durch einen ersten Socket mithilfe spezifischer Socketoptionen an gebunden wurde.

> [!NOTE]
> In der folgenden Tabelle bezeichnet "Platzhalter" die Platzhalter Adresse für das angegebene Protokoll (z. b. "0.0.0.0" für IPv4 und "::" für IPv6). "Specific" bezeichnet eine bestimmte IP-Adresse, die einer Schnittstelle zugewiesen ist. In den Tabellenzellen wird angegeben, ob die Bindung erfolgreich war ("Erfolg") oder ob der Fehler zurückgegeben wurde ("InUse" für den Fehler " [WSAEADDRINUSE](windows-sockets-error-codes-2.md) "). "Access" für den [WSAEACCES](windows-sockets-error-codes-2.md) -Fehler).
>
> Beachten Sie auch, dass in dieser speziellen Tabelle beide [**Bindungs**](/windows/win32/api/winsock/nf-winsock-bind) Aufrufe unter demselben Benutzerkonto durchgeführt werden.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Erster <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungs</strong></a> Befehl</td>
        <td bgcolor="#C0C0C0" colspan="6">Zweiter <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungs</strong></a> Befehl</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Standard</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Standard</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
</table>

Einige Einträge in der obigen Tabelle verdienen eine Erläuterung.

Wenn der erste Aufrufer z. b. " **\_ exclusiveaddruse** " für eine bestimmte Adresse festlegt und der zweite Aufrufer versucht, eine [**Bindung**](/windows/win32/api/winsock/nf-winsock-bind) mit einer Platzhalter Adresse am gleichen Port aufzurufen, wird der zweite **Bindungs** Aufruf erfolgreich ausgeführt. In diesem speziellen Fall wird der zweite Aufrufer an alle Schnittstellen mit Ausnahme der spezifischen Adresse gebunden, an die der erste Aufrufer gebunden ist. Beachten Sie, dass das Gegenteil von diesem Fall nicht zutrifft: Wenn der erste Aufrufer " **\_ exclusiveaddruse** " festlegt und **Bind** mit dem Platzhalter Flag aufruft, kann der zweite Aufrufer keine **Bindung** mit dem gleichen Port aufrufen.

Das socketbindungsverhalten ändert sich, wenn die Socket-Bindungs Aufrufe unter verschiedenen Benutzerkonten durchgeführt werden. In der folgenden Tabelle wird das Verhalten für Windows Server 2003 und spätere Betriebssysteme angegeben, wenn ein zweiter Socket versucht, eine Bindung an eine Adresse herzustellen, die zuvor von einem ersten Socket an gebunden wurde. dabei werden bestimmte Socketoptionen und ein anderes Benutzerkonto verwendet.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Erster <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungs</strong></a> Befehl</td>
        <td bgcolor="#C0C0C0" colspan="6">Zweiter <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungs</strong></a> Befehl</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Standard</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td bgcolor="#C0C0C0">Spezifisch</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Standard</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>Derzeit verwendeten</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>Derzeit verwendeten</td>
        <td>Derzeit verwendeten</td>
    </tr>
</table>

Beachten Sie, dass das Standardverhalten anders ist, wenn die [**Bindungs**](/windows/win32/api/winsock/nf-winsock-bind) Aufrufe unter verschiedenen Benutzerkonten durchgeführt werden. Wenn der erste Aufrufer keine Optionen für den Socket festgelegt und an die Platzhalter Adresse bindet, kann der zweite Aufrufer die Option " **so \_ reuseaddr** " nicht festlegen und erfolgreich an denselben Port binden. Das Standardverhalten, bei dem keine Optionen festgelegt sind, gibt ebenfalls einen Fehler zurück.

Unter Windows Vista und höher kann ein Dual Stack-Socket erstellt werden, der sowohl IPv6 als auch IPv4 betreibt. Wenn ein Dual Stack-Socket an die Platzhalter Adresse gebunden ist, ist der angegebene Port sowohl für IPv4-als auch für IPv6-Netzwerk Stapel reserviert, und die mit " **\_ reuseaddr** " verbundenen Überprüfungen und **somit " \_ exclusiveaddruse** " (falls festgelegt) werden durchgeführt. Diese Überprüfungen müssen auf beiden Netzwerk Stapeln erfolgreich ausgeführt werden. Wenn z. b. ein Dual-Stack-TCP-Socket **so \_ exclusiveaddruse** festlegt und dann versucht, eine Bindung an Port 5000 herzustellen, kann kein anderer TCP-Socket zuvor an Port 5000 (Platzhalter oder spezifisch) gebunden werden. Wenn in diesem Fall ein IPv4-TCP-Socket zuvor an die Loopback Adresse an Port 5000 gebunden war, würde der [**Bindungs**](/windows/win32/api/winsock/nf-winsock-bind) Befehl für den Dual Stack-Socket mit [WSAEACCES](windows-sockets-error-codes-2.md)fehlschlagen.

## <a name="application-strategies"></a>Anwendungsstrategien

Beim Entwickeln von Netzwerkanwendungen, die auf der Socketebene betrieben werden, ist es wichtig, den Typ der erforderlichen Socketsicherheit zu beachten. Client Anwendungen – Anwendungen, die Daten an einen Dienst anschließen oder an einen Dienst senden – sind nur selten erforderlich, da Sie an einen zufälligen lokalen (kurzlebigen) Port gebunden werden. Wenn der Client eine bestimmte lokale Port Bindung erfordert, damit er ordnungsgemäß funktioniert, müssen Sie die Socketsicherheit in Erwägung gezogen.

Die Option " **\_ reuseaddr** " hat nur sehr wenige Verwendungsmöglichkeiten in normalen Anwendungen, abgesehen von Multicast-Sockets, bei denen Daten an alle an denselben Port gebundenen Sockets übermittelt werden. Andernfalls sollte jede Anwendung, die diese Socketoption festlegt, umgestaltet werden, um die Abhängigkeit zu entfernen, da Sie für "sockethijacking" ausgesprochen anfällig ist. Solange die **\_ reuseaddr** -Socketoption verwendet werden kann, um einen Port in einer Serveranwendung potenziell zu überdenken, muss die Anwendung als nicht sicher eingestuft werden.

Alle Server Anwendungen müssen " **\_ exclusiveaddruse** " für ein hohes Maß an Socketsicherheit festlegen. Dadurch wird nicht nur verhindert, dass Schadsoftware den Port Hijacking, sondern auch angibt, ob eine andere Anwendung an den angeforderten Port gebunden ist. Beispielsweise schlägt ein [**Bindungs**](/windows/win32/api/winsock/nf-winsock-bind) Rückruf für die Platzhalter Adresse durch einen Prozess mit der " **so \_ exclusiveaddruse** "-Socketoption fehl, wenn zurzeit ein anderer Prozess an denselben Port an einer bestimmten Schnittstelle gebunden ist.

Schließlich sollte eine Anwendung, auch wenn die Socketsicherheit in Windows Server 2003 verbessert wurde, immer die Socketoption " **so \_ exclusiveaddruse** " festlegen, um sicherzustellen, dass Sie an alle vom Prozess angeforderten Schnittstellen gebunden wird. Die Socketsicherheit in Windows Server 2003 bietet ein höheres Maß an Sicherheit für ältere Anwendungen, aber Anwendungsentwickler müssen ihre Produkte immer noch mit allen Aspekten der Sicherheit entwerfen.
