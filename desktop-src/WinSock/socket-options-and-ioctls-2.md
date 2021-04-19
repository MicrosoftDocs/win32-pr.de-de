---
description: Einige der Socketoptionen für Windows Sockets 2 werden in der folgenden Tabelle zusammengefasst.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Socketoptionen und IOCTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362382"
---
# <a name="socket-options-and-ioctls"></a>Socketoptionen und IOCTLs

Einige der Socketoptionen für Windows Sockets 2 werden in der folgenden Tabelle zusammengefasst. Ausführlichere Informationen finden Sie in Abschnitt 4 unter [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) und/oder [**wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)). Weitere neue Protokoll spezifische Socketoptionen finden Sie in der Protocol-Specific-Anlage. Eine komplette Liste der [**Socketoptionen**](socket-options.md) für Windows Sockets finden Sie in der Winsock-Referenz.

Eine Zusammenfassung der Winsock IOCTLs finden Sie unter [Zusammenfassung der socketioctl-Opcodes](summary-of-socket-ioctl-opcodes-2.md). Eine komplette Liste der [**Winsock IOCTLs**](winsock-ioctls.md) finden Sie in der Winsock-Referenz.

## <a name="summary-of-common-socket-options"></a>Zusammenfassung allgemeiner Socketoptionen

Ein Winsock-Dienstanbieter muss alle diese Optionen erkennen, und (für [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) gibt für jeden eine plausible Werte zurück. Der Standardwert für jede Option ist in der folgenden Tabelle aufgeführt.

Wert

type

Bedeutung

Standard

Hinweis

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>also \_ akzeptconn

BOOL

Der Socket lauscht.

FALSE, es sei denn, ein [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) wurde ausgeführt.

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>also \_ Broadcast

BOOL

Socket ist für die Übertragung und den Empfang von Broadcast Nachrichten konfiguriert.

false

<span id="SO_DEBUG"></span><span id="so_debug"></span>also \_ Debuggen

BOOL

Debuggen ist aktiviert.

false

Ich

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DontLinger

BOOL

True gibt an, dass die \_ Option so LINGER deaktiviert ist.

TRUE

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO \_ DontRoute

BOOL

Das Routing ist deaktiviert. Ist erfolgreich, wird aber bei AF \_ inet Sockets ignoriert; schlägt bei AF \_ inet6 Sockets mit [wsakooprodeopt](windows-sockets-error-codes-2.md)fehl. Wird nicht für ATM-Sockets unterstützt (führt zu einem Fehler).

false

Ich

<span id="SO_ERROR"></span><span id="so_error"></span>\_Fehler

INT

Ruft den Fehlerstatus ab und löscht ihn.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_Gruppen- \_ ID

GROUP

Reserviert.

NULL

Nur Get

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_Gruppen \_ Priorität

INT

Reserviert.

0

[**\_KeepAlive**](so-keepalive.md)

BOOL

Keepalives werden gesendet. Wird nicht für ATM-Sockets unterstützt (führt zu einem Fehler).

false

Ich

<span id="SO_LINGER"></span><span id="so_linger"></span>SO \_ LINGER

Struktur-Linger

Gibt die aktuellen Linger-Optionen zurück.

l \_ ToggleMicrophoneOnOff ist 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_Maximale Nachrichten \_ \_ Größe

INT

Maximale ausgehende Größe einer Nachricht für Nachrichten sockettypen. Es gibt keine Bereitstellung, um die maximale Größe eingehender Nachrichten zu ermitteln. Hat keine Bedeutung für Datenstrom orientierte Sockets.

Implementierungsabhängig

Nur Get

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_oobinline

BOOL

OOB-Daten werden im normalen Datenstrom empfangen.

false

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_Protokoll \_ infow

[ **wsaprotocol-Struktur \_ Informationen**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Beschreibung der Protokollinformationen für das Protokoll, das an diesen Socket gebunden ist.

Protokoll abhängig

Nur Get

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_rcvbuf

INT

Der gesamte pro-Socket-Pufferspeicher, der für Empfangs Vorgänge reserviert ist. Dies steht in keinem Zusammenhang mit \_ der maximalen Nachrichten \_ \_ Größe und entspricht nicht notwendigerweise der Größe des TCP-Empfangs Fensters.

Implementierungsabhängig

Ich

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_reuseaddr

BOOL

Die Adresse, an die dieser Socket gebunden ist, kann von anderen Benutzern verwendet werden. Gilt nicht für ATM-Sockets.

false

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_sndbuf

INT

Der Gesamt Puffer Speicherplatz pro Socket, der für Sende Vorgänge reserviert ist. Dies steht in keinem Zusammenhang mit \_ der maximalen Nachrichten \_ \_ Größe und entspricht nicht notwendigerweise der Größe eines TCP-Sende Fensters.

Implementierungsabhängig

Ich

<span id="SO_TYPE"></span><span id="so_type"></span>\_Typ

INT

Der Typ des Sockets (z. b. sock- \_ Stream).

Wie durch Socket erstellt.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD- \_ Konfiguration

char-weit \*

Ein undurchsichtiges Datenstruktur Objekt, das Konfigurationsinformationen des Dienstanbieters enthält.

Implementierungsabhängig

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP- \_ nodelay

BOOL

Deaktiviert den Nagle-Algorithmus für Sammelsendungen.

Implementierungsabhängig

(i) ein Dienstanbieter kann diese Option auf [**wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) im Hintergrund ignorieren und einen konstanten Wert für [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))zurückgeben. er kann auch einen Wert für **wspsetsockopt** annehmen und den entsprechenden Wert in **wspgetsockopt** zurückgeben, ohne den Wert zu verwenden.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Socketoptionen**](socket-options.md)
</dt> <dt>

[**Optionen des Sol- \_ socketsockets**](sol-socket-socket-options.md)
</dt> <dt>

[**Ipproto \_ TCP-Socketoptionen**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**Ipproto \_ UDP-Socketoptionen**](ipproto-udp-socket-options.md)
</dt> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> </dl>

 

 
