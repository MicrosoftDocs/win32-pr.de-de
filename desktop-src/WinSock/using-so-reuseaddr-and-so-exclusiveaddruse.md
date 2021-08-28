---
description: Die Entwicklung einer sicheren netzwerkbasierten Netzwerkinfrastruktur hat für die meisten Entwickler von Netzwerkanwendung prioritätsbasierte Priorität. Die Socketsicherheit wird jedoch häufig übersehen, obwohl sie bei der Berücksichtigung einer vollständig sicheren Lösung sehr wichtig ist.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Verwenden SO_REUSEADDR und SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d58b0249ab19b4c7a1655a1c65130d545d328ef4fba3fd56ae9b05a911cb3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121145"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Verwenden von SO \_ REUSEADDR und SO \_ EXCLUSIVEADDRUSE

Die Entwicklung einer sicheren netzwerkbasierten Netzwerkinfrastruktur hat für die meisten Entwickler von Netzwerkanwendung prioritätsbasierte Priorität. Die Socketsicherheit wird jedoch häufig übersehen, obwohl sie bei der Berücksichtigung einer vollständig sicheren Lösung sehr wichtig ist. Socketsicherheit befasst sich insbesondere mit Prozessen, die an denselben Port gebunden sind, der zuvor von einem anderen Anwendungsprozess gebunden wurde. In der Vergangenheit war es möglich, dass eine Netzwerkanwendung den Port einer anderen Anwendung "hijack" hat, was leicht zu einem Denial-of-Service-Angriff oder Datendiebstahl führen konnte.

Im Allgemeinen gilt Socketsicherheit für serverseitige Prozesse. Genauer gesagt gilt Socketsicherheit für jede Netzwerkanwendung, die Verbindungen akzeptiert und IP-Datagrammdatenverkehr empfängt. Diese Anwendungen binden in der Regel an einen bekannten Port und sind allgemeine Ziele für schädlichen Netzwerkcode.

Clientanwendungen sind weniger wahrscheinlich ziele solcher Angriffe – nicht, weil sie weniger anfällig sind, sondern weil die meisten Clients an "kurzlebige" lokale Ports anstatt an statische "Dienstports" gebunden sind. Clientnetzwerkanwendungen sollten immer an kurzlebigen Ports gebunden werden (durch Angabe von Port 0  in der [**SOCKADDR-Struktur,**](sockaddr-2.md) auf die der Name-Parameter beim Aufrufen der [**bind-Funktion**](/windows/win32/api/winsock/nf-winsock-bind) verweist), es sei denn, es gibt einen überzeugenden architektonischen Grund dafür. Die kurzlebigen lokalen Ports bestehen aus Ports, die größer als Port 49151 sind. Die meisten Serveranwendungen für dedizierte Dienste sind an einen bekannten reservierten Port gebunden, der kleiner oder gleich Port 49151 ist. Für die meisten Anwendungen besteht also in der Regel kein Konflikt bei Bindungsanforderungen zwischen Client- und Serveranwendungen.

In diesem Abschnitt wird die Standardsicherheitsstufe auf verschiedenen Microsoft Windows-Plattformen beschrieben, und es wird beschrieben, wie sich die spezifischen Socketoptionen **SO \_ REUSEADDR** und [SO \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) auf die Sicherheit der Netzwerkanwendung auswirken. Ein zusätzliches Feature namens erweiterte Socketsicherheit ist auf Windows Server 2003 und höher verfügbar. Die Verfügbarkeit dieser Socketoptionen und die verbesserte Socketsicherheit variieren je nach Version von Microsoft-Betriebssystemen, wie in der folgenden Tabelle dargestellt.

| Plattform            | ALSO \_ WIEDERVERWENDENADDR | SO \_ EXCLUSIVEADDRUSE                  | Verbesserte Socketsicherheit |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Verfügbar     | Nicht verfügbar                         | Nicht verfügbar.            |
| Windows 98          | Verfügbar     | Nicht verfügbar                         | Nicht verfügbar.            |
| Windows Ich          | Verfügbar     | Nicht verfügbar                         | Nicht verfügbar.            |
| Windows NT 4.0      | Verfügbar     | Verfügbar in Service Pack 4 und höher | Nicht verfügbar            |
| Windows 2000        | Verfügbar     | Verfügbar                             | Nicht verfügbar            |
| Windows XP          | Verfügbar     | Verfügbar                             | Nicht verfügbar            |
| Windows Server 2003 | Verfügbar     | Verfügbar                             | Verfügbar                |
| Windows Vista       | Verfügbar     | Verfügbar                             | Verfügbar                |
| Windows Server 2008 | Verfügbar     | Verfügbar                             | Verfügbar                |
| Windows 7 und neuer  | Verfügbar     | Verfügbar                             | Verfügbar                |

## <a name="using-so_reuseaddr"></a>Verwenden von SO \_ REUSEADDR

Mit **der Socketoption SO \_ REUSEADDR** kann ein Socket eine Bindung an einen Port ersingen, der von einem anderen Socket verwendet wird. Der zweite Socket ruft [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) auf, während der *parameter optname* auf **SO \_ REUSEADDR** und der *optval-Parameter* auf den booleschen Wert **TRUE** festgelegt sind, bevor [**bind**](/windows/win32/api/winsock/nf-winsock-bind) an demselben Port wie der ursprüngliche Socket aufruft. Sobald der zweite Socket erfolgreich gebunden wurde, ist das Verhalten für alle Sockets, die an diesen Port gebunden sind, unbestimmt. Wenn beispielsweise alle Sockets am gleichen Port TCP-Dienst bereitstellen, kann nicht garantiert werden, dass eingehende TCP-Verbindungsanforderungen über den Port vom richtigen Socket verarbeitet werden – das Verhalten ist nicht deterministisch. Ein schädliches Programm kann **SO \_ REUSEADDR** verwenden, um sockets zu binden, die bereits für Standard-Netzwerkprotokolldienste verwendet werden, um den Zugriff auf diesen Dienst zu verweigern. Für die Verwendung dieser Option sind keine besonderen Berechtigungen erforderlich.

Wenn eine Clientanwendung an einen Port gebunden wird, bevor eine Serveranwendung eine Bindung an denselben Port herstellen kann, können Probleme auftreten. Wenn die Serveranwendung mithilfe der Socketoption **SO \_ REUSEADDR** eine Bindung an denselben Port ersingt, ist das Verhalten für alle sockets, die an diesen Port gebunden sind, unbestimmt.

Eine Ausnahme von diesem nicht deterministischen Verhalten sind Multicastsockets. Wenn zwei Sockets an die gleiche Schnittstelle und denselben Port gebunden sind und Mitglieder derselben Multicastgruppe sind, werden Daten an beide Sockets übermittelt und nicht an eine willkürlich ausgewählte.

## <a name="using-so_exclusiveaddruse"></a>Verwenden von SO \_ EXCLUSIVEADDRUSE

Vor der Einführung der **Socketoption SO \_ EXCLUSIVEADDRUSE** konnte ein Entwickler einer Netzwerkanwendung nur sehr wenig tun, um zu verhindern, dass ein schädliches Programm an den Port gebunden ist, an dem die Netzwerkanwendung eigene Sockets gebunden hat. Um dieses Sicherheitsproblem zu beheben, hat Windows Sockets die **Socketoption SO \_ EXCLUSIVEADDRUSE** eingeführt, die unter Windows NT 4.0 mit Service Pack 4 (SP4) und höher verfügbar wurde.

Die **\_ Socketoption SO EXCLUSIVEADDRUSE** kann nur von Mitgliedern der Sicherheitsgruppe Administratoren auf Windows XP und früher verwendet werden. Die Gründe, warum diese Anforderung auf Windows Server 2003 und höher geändert wurde, werden weiter oben in diesem Artikel erläutert.

Die **OPTION SO \_ EXCLUSIVEADDRUSE** wird festgelegt, indem die [**setsockopt-Funktion**](/windows/win32/api/winsock/nf-winsock-setsockopt) mit dem *optname-Parameter* auf **SO \_ EXCLUSIVEADDRUSE** und dem *optval-Parameter* auf den booleschen Wert **TRUE** festgelegt wird, bevor der Socket gebunden wird. Nachdem die Option festgelegt wurde, [](/windows/win32/api/winsock/nf-winsock-bind) unterscheidet sich das Verhalten nachfolgender Bindungsaufrufe abhängig von der Netzwerkadresse, die in jedem Bindungsaufruf **angegeben** ist.

In der folgenden Tabelle wird das Verhalten beschrieben, das in Windows XP und früher auftritt, wenn ein zweiter Socket versucht, eine Bindung an eine Adresse zu erstellen, an die zuvor ein erster Socket mithilfe bestimmter Socketoptionen gebunden war.

> [!NOTE]  
> In der folgenden Tabelle gibt "Platzhalter" die Platzhalteradresse für das angegebene Protokoll an (z.B. "0.0.0.0" für IPv4 und "::" für IPv6). "Spezifisch" gibt eine bestimmte IP-Adresse an, der eine Schnittstelle zugewiesen ist. Die Tabellenzellen geben an, ob die Bindung erfolgreich ist ("Erfolg") oder ob ein Fehler ("INUSE" für den [WSAEADDRINUSE-Fehler zurückgegeben](windows-sockets-error-codes-2.md) wird; "ACCESS" für den [WSAEACCES-Fehler).](windows-sockets-error-codes-2.md)

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Erster <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungsaufruf</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Zweiter <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungsaufruf</strong></a></td>
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
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Wenn zwei Sockets an dieselbe Portnummer gebunden sind, aber auf verschiedenen expliziten Schnittstellen, gibt es keinen Konflikt. Wenn ein Computer beispielsweise über zwei IP-Schnittstellen verfügt, 10.0.0.1 und 10.99.99.99, Wenn der erste Aufruf von [**bind**](/windows/win32/api/winsock/nf-winsock-bind) auf 10.0.0.1 erfolgt und der Port auf  5150 und **SO \_ EXCLUSIVEADDRUSE** festgelegt ist, ist ein zweiter Aufruf der Bindung an 10.99.99.99 erfolgreich, bei dem der Port ebenfalls auf 5150 festgelegt ist. Es werden keine Optionen angegeben. Wenn der erste Socket jedoch an die Platzhalteradresse und den Port 5150 gebunden ist, wird bei jedem nachfolgenden Bindungsaufruf an Port 5150, für den **SO \_ EXCLUSIVEADDRUSE** festgelegt ist, ein Fehler zurückgegeben, wenn [entweder WSAEADDRINUSE](windows-sockets-error-codes-2.md) oder [WSAEACCES](windows-sockets-error-codes-2.md) vom Bindungsvorgang zurückgegeben **wird.**

Wenn beim ersten Aufruf von [**bind**](/windows/win32/api/winsock/nf-winsock-bind) entweder **SO \_ REUSEADDR** oder gar  keine Socketoptionen festgelegt werden, "hijack" der zweite Bindungsaufruf den Port, und die Anwendung kann nicht bestimmen, welcher der beiden Sockets bestimmte Pakete empfangen hat, die an den "freigegebenen" Port gesendet wurden.

Eine typische Anwendung, die die [**bind-Funktion**](/windows/win32/api/winsock/nf-winsock-bind) aufruft, ordnet den gebundenen Socket nicht zur exklusiven Verwendung zu, es sei denn, die **Socketoption SO \_ EXCLUSIVEADDRUSE** wird für den Socket vor dem Aufruf der bind-Funktion **aufgerufen.** Wenn eine Clientanwendung an einen kurzlebigen Port oder einen bestimmten Port gebunden wird, bevor eine Serveranwendung an denselben Port gebunden wird, können Probleme auftreten. Die Serveranwendung kann mithilfe der Socketoption **SO \_ REUSEADDR** auf dem Socket vor  dem Aufrufen der bind-Funktion eine Bindung an denselben Port ersingen, aber das Verhalten für alle sockets, die an diesen Port gebunden sind, ist dann unbestimmt. Wenn die Serveranwendung versucht, die **Socketoption SO \_ EXCLUSIVEADDRUSE** für die exklusive Verwendung des Ports zu verwenden, ist die Anforderung nicht möglich.

Umgekehrt kann ein Socket, für den **SO \_ EXCLUSIVEADDRUSE** festgelegt ist, nicht unbedingt sofort nach dem Schließen des Sockets wiederverwendet werden. Wenn z. B. ein lauschenden Socket mit **SO \_ EXCLUSIVEADDRUSE-Satz** eine Verbindung akzeptiert und anschließend geschlossen wird, kann ein anderer Socket (auch mit **SO \_ EXCLUSIVEADDRUSE**) nicht an denselben Port wie der erste Socket gebunden werden, bis die ursprüngliche Verbindung inaktiv wird.

Dieses Problem kann kompliziert werden, da das zugrunde liegende Transportprotokoll die Verbindung möglicherweise nicht beendet, obwohl der Socket geschlossen wurde. Auch nachdem der Socket von der Anwendung geschlossen wurde, muss das System alle gepufferten Daten übertragen, eine ordnungsgemäß getrennte Nachricht an den Peer senden und auf eine entsprechende ordnungsgemäß getrennte Nachricht vom Peer warten. Es ist möglich, dass das zugrunde liegende Transportprotokoll die Verbindung niemals frei gibt. Beispielsweise könnte der Peer, der an der ursprünglichen Verbindung beteiligt ist, ein Fenster der Größe 0 (null) oder eine andere Form der "Angriffskonfiguration" anknten. In einem solchen Fall verbleibt die Clientverbindung trotz der Anforderung zum Schließen in einem aktiven Zustand, da nicht bekannte Daten im Puffer bleiben.

Um diese Situation zu vermeiden, sollten Netzwerkanwendungen ein ordnungsgemäßes Herunterfahren sicherstellen, indem sie [**shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) mit dem festgelegten SD SEND-Flag aufrufen und dann in einer \_ [**recv-Schleife**](/windows/win32/api/winsock/nf-winsock-recv) warten, bis null Bytes über die Verbindung zurückgegeben werden. Dadurch wird sichergestellt, dass alle Daten vom Peer empfangen werden. Ebenso wird mit dem Peer bestätigt, dass alle übertragenen Daten empfangen wurden. Außerdem wird das oben genannte Problem bei der Portwiederverwendung vermieden.

Die So-LINGER-Socketoption kann auf einem Socket festgelegt werden, um zu verhindern, dass der Port in einen "aktiven" Wartezustand über geht. Dies wird jedoch davon abgeraten, da dies zu gewünschten Auswirkungen führen kann, z. B. zum Zurücksetzen von \_ Verbindungen. Wenn z. B. Daten vom Peer empfangen werden, aber davon nicht bekannt sind, und der lokale Computer den Socket schließt, auf dem SO LINGER festgelegt ist, wird die Verbindung zwischen den beiden Computern zurückgesetzt, und die nicht bekannten Daten werden vom Peer \_ verworfen. Die Auswahl eines geeigneten Zeitpunkts für den Abbruch ist schwierig, da ein kleinerer Timeoutwert häufig zu plötzlich abgebrochenen Verbindungen führt, während größere Timeoutwerte das System anfällig für Denial-of-Service-Angriffe machen (indem viele Verbindungen herstellen und Anwendungsthreads möglicherweise blockiert/blockiert werden). Das Schließen eines Sockets mit einem Timeoutwert ungleich 0 (null) kann auch dazu führen, dass [**der closesocket-Aufruf**](/windows/win32/api/winsock/nf-winsock-closesocket) blockiert wird.

## <a name="enhanced-socket-security"></a>Erweiterte Socketsicherheit

Die verbesserte Socketsicherheit wurde mit dem Release von Windows Server 2003 hinzugefügt. In früheren Versionen des Microsoft-Serverbetriebssystems ermöglichte die Standardmäßige Socketsicherheit es Prozessen leicht, Ports von unergesehenen Anwendungen zu entwenden. In Windows Server 2003 befinden sich Sockets standardmäßig nicht in einem sharable-Zustand. Wenn eine Anwendung anderen Prozessen die Wiederverwendung eines Ports ermöglichen möchte, an dem bereits ein Socket gebunden ist, muss sie ihn daher explizit aktivieren. Wenn dies der Fall ist, muss für den ersten Socket, der [**bind**](/windows/win32/api/winsock/nf-winsock-bind) auf dem Port aufruft, **SO \_ REUSEADDR** auf dem Socket festgelegt sein. Die einzige Ausnahme in diesem Fall tritt auf, wenn der **zweite** Bindungsaufruf von demselben Benutzerkonto ausgeführt wird, das den ursprünglichen Aufruf zum Binden von **vorgenommen hat.** Diese Ausnahme dient ausschließlich der Abwärtskompatibilität.

Die folgende Tabelle beschreibt das Verhalten, das in Windows Server 2003- und höher-Betriebssystemen auftritt, wenn ein zweiter Socket versucht, eine Bindung an eine Adresse herzustellen, an die zuvor ein erster Socket mithilfe bestimmter Socketoptionen gebunden war.

> [!NOTE]
> In der folgenden Tabelle gibt "Platzhalter" die Platzhalteradresse für das angegebene Protokoll an (z.B. "0.0.0.0" für IPv4 und "::" für IPv6). "Spezifisch" gibt eine bestimmte IP-Adresse an, der eine Schnittstelle zugewiesen ist. Die Tabellenzellen geben an, ob die Bindung erfolgreich ist ("Erfolg") oder der zurückgegebene Fehler ("INUSE" für den [WSAEADDRINUSE-Fehler;](windows-sockets-error-codes-2.md) "ACCESS" für den [WSAEACCES-Fehler).](windows-sockets-error-codes-2.md)
>
> Beachten Sie auch, dass [](/windows/win32/api/winsock/nf-winsock-bind) in dieser spezifischen Tabelle beide Bindungsaufrufe unter demselben Benutzerkonto vorgenommen werden.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Erster <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungsaufruf</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Zweiter <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungsaufruf</strong></a></td>
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
        <td>INUSE</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolg</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>Erfolg</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

In der obigen Tabelle sind einige Einträge aufgeführt.

Wenn der erste Aufrufer beispielsweise **SO \_ EXCLUSIVEADDRUSE** für eine bestimmte Adresse und der zweite Aufrufer versucht, [**bind**](/windows/win32/api/winsock/nf-winsock-bind)  mit einer Platzhalteradresse auf demselben Port auf aufruft, ist der zweite Bindungsaufruf erfolgreich. In diesem speziellen Fall ist der zweite Aufrufer an alle Schnittstellen gebunden, mit Ausnahme der spezifischen Adresse, an die der erste Aufrufer gebunden ist. Beachten Sie, dass die Umkehrung dieses Falls nicht zutrifft: Wenn der  erste Aufrufer **SO \_ EXCLUSIVEADDRUSE** fest  legt und die Bindung mit dem Platzhalterflag aufruft, kann der zweite Aufrufer bind nicht mit demselben Port aufrufen.

Das Verhalten der Socketbindung ändert sich, wenn die Socketbindungsaufrufe unter verschiedenen Benutzerkonten vorgenommen werden. Die folgende Tabelle gibt das Verhalten an, das in Windows Server 2003- und höher-Betriebssystemen auftritt, wenn ein zweiter Socket versucht, eine Bindung an eine Adresse herzustellen, an die zuvor ein erster Socket mithilfe bestimmter Socketoptionen und eines anderen Benutzerkontos gebunden war.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Erster <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungsaufruf</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Zweiter <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Bindungsaufruf</strong></a></td>
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
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolgreich</td>
        <td>Erfolgreich</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Platzhalter</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spezifisch</td>
        <td>Erfolg</td>
        <td>INUSE</td>
        <td>Erfolg</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Beachten Sie, dass das [](/windows/win32/api/winsock/nf-winsock-bind) Standardverhalten unterschiedlich ist, wenn die Bindungsaufrufe unter verschiedenen Benutzerkonten vorgenommen werden. Wenn der erste Aufrufer keine Optionen für den Socket festgelegt und an die Platzhalteradresse gebunden wird, kann der zweite Aufrufer die **Option SO \_ REUSEADDR** nicht festlegen und erfolgreich an denselben Port binden. Das Standardverhalten ohne festgelegten Optionen gibt auch einen Fehler zurück.

Unter Windows Vista und höher kann ein Doppelstapelsocket erstellt werden, der sowohl über IPv6 als auch über IPv4 funktioniert. Wenn ein Doppelstapelsocket an die Platzhalteradresse gebunden ist, wird der angegebene Port sowohl für die IPv4- als auch die IPv6-Netzwerkstapel reserviert, und die Überprüfungen, die **SO \_ REUSEADDR** und **SO \_ EXCLUSIVEADDRUSE** (sofern festgelegt) zugeordnet sind, werden durchgeführt. Diese Überprüfungen müssen auf beiden Netzwerkstapeln erfolgreich sein. Wenn beispielsweise ein TCP-Socket mit dualem Stapel **SO \_ EXCLUSIVEADDRUSE** einbindet und dann versucht, eine Bindung an Port 5000 zu erhalten, kann zuvor kein anderer TCP-Socket an Port 5000 gebunden werden (entweder Platzhalter oder spezifisch). Wenn in diesem Fall ein IPv4-TCP-Socket zuvor an die Loopbackadresse [](/windows/win32/api/winsock/nf-winsock-bind) an Port 5000 gebunden war, würde der Bindungsaufruf für den Doppelstapelsocket mit [WSAEACCES fehlschlagen.](windows-sockets-error-codes-2.md)

## <a name="application-strategies"></a>Anwendungsstrategien

Bei der Entwicklung einer Netzwerkanwendung, die auf Socketebene betrieben wird, ist es wichtig, die Art der erforderlichen Socketsicherheit zu berücksichtigen. Clientanwendungen – Anwendungen, die Eine Verbindung mit einem Dienst herstellen oder Daten an einen Dienst senden – erfordern selten zusätzliche Schritte, da sie an einen zufälligen lokalen (kurzlebigen) Port gebunden werden. Wenn der Client eine bestimmte lokale Portbindung erfordert, um ordnungsgemäß zu funktionieren, müssen Sie die Socketsicherheit in Betracht ziehen.

Die **OPTION SO \_ REUSEADDR** hat nur sehr wenige Verwendungsmöglichkeiten in normalen Anwendungen, abgesehen von Multicastsockets, bei denen Daten an alle Sockets übermittelt werden, die an denselben Port gebunden sind. Andernfalls sollte jede Anwendung, die diese Socketoption einschließt, neu gestaltet werden, um die Abhängigkeit zu entfernen, da sie äußerst anfällig für "Socket Hijacking" ist. Solange die **SO \_ REUSEADDR-Socketoption** verwendet werden kann, um einen Port in einer Serveranwendung zu übertragen, muss die Anwendung als nicht sicher angesehen werden.

Für eine hohe Socketsicherheit müssen alle Serveranwendungen **SO \_ EXCLUSIVEADDRUSE** festlegen. Sie verhindert nicht nur, dass Schadsoftware den Port übernimmt, sondern gibt auch an, ob eine andere Anwendung an den angeforderten Port gebunden ist. Beispielsweise kann ein [](/windows/win32/api/winsock/nf-winsock-bind) Aufruf der Bindung an die Platzhalteradresse durch einen Prozess, für den die **Socketoption SO \_ EXCLUSIVEADDRUSE** festgelegt ist, fehlschlagen, wenn ein anderer Prozess derzeit an denselben Port auf einer bestimmten Schnittstelle gebunden ist.

Auch wenn die Socketsicherheit in Windows Server 2003 verbessert wurde, sollte eine Anwendung immer die Socketoption **SO \_ EXCLUSIVEADDRUSE** festlegen, um sicherzustellen, dass sie an alle spezifischen Schnittstellen gebunden wird, die der Prozess angefordert hat. Die Socketsicherheit in Windows Server 2003 erhöht die Sicherheit für Legacyanwendungen, anwendungsentwickler müssen ihre Produkte jedoch weiterhin unter Aspekten aller Sicherheitsaspekte entwerfen.
