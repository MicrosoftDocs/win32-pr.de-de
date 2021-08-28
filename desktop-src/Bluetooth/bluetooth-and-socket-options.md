---
title: Bluetooth und Socketoptionen
description: Bluetooth for Windows unterstützt die folgenden Socketoptionen.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth und Socketoptionen Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631eb2b041fcc320723155d4a5df1742e6c0dc79cb579815de141334906708e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588430"
---
# <a name="bluetooth-and-socket-options"></a>Bluetooth und Socketoptionen

Bluetooth for Windows unterstützt die folgenden Socketoptionen. Socketoptionen werden mithilfe der Funktionen [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) bzw. [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) festgelegt und abgefragt. Alle folgenden Optionen können mit der **setsockopt-Funktion** verwendet werden, aber nur die **SO \_ BTH \_ MTU-Option** ist für die Verwendung mit der **getsockopt-Funktion** verfügbar.

Die folgenden Einstellungen sind für die Arbeit mit Socketoptionen Bluetooth erforderlich:

-   Der *s-Parameter* muss ein Bluetooth sein.
-   Der *Levelparameter* muss **SOL \_ RFCOMM sein.**

## <a name="so_bth_authenticate"></a>\_BTH-AUTHENTIFIZIERUNG \_

Bei getrennten Sockets gibt **so \_ BTH \_ AUTHENTICATE** an, [](/windows/desktop/api/winsock2/nf-winsock2-connect) dass eine Authentifizierung erforderlich ist, damit ein Verbindungs- oder [**Annahmevorgang**](/windows/desktop/api/winsock2/nf-winsock2-accept) erfolgreich abgeschlossen werden kann. Wenn Sie diese Socketoption festlegen, wird die Authentifizierung während der Verbindungseinrichtung aktiv initiiert, wenn Bluetooth Geräte zuvor nicht authentifiziert wurden. Die Benutzeroberfläche für den Austausch von Hauptschlüsseln wird bei Bedarf vom Betriebssystem außerhalb des Anwendungskontexts bereitgestellt.

Bei ausgehenden Verbindungen, die eine Authentifizierung erfordern, schlägt [**der Verbindungsvorgang**](/windows/desktop/api/winsock2/nf-winsock2-connect) mit **WSAEACCES** fehl, wenn die Authentifizierung nicht erfolgreich ist. Als Reaktion darauf fordert die Anwendung den Benutzer möglicherweise auf, die beiden Geräte vor der Bluetooth zu authentifizieren.

Bei eingehenden Verbindungen wird die Verbindung abgelehnt, wenn die Authentifizierung nicht hergestellt werden kann, und gibt einen **WSAEHOSTDOWN-Fehler** zurück. Weitere Informationen zum Authentifizieren Bluetooth Geräten finden Sie unter [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Für die **Socketoption SO \_ BTH \_ AUTHENTICATE** ist *optval* ein Zeiger auf ULONG bAuthenticate und muss **TRUE sein.** *optlen* entspricht "sizeof(ULONG)".

**Windows XP mit SP2: SO \_ BTH \_ AUTHENTICATE startet** die Authentifizierung für verbundene Sockets und erzwingt die Authentifizierung bei der Verbindung für nicht verbundene Sockets. Bei eingehenden Verbindungen wird die Verbindung abgelehnt, wenn die Authentifizierung nicht durchgeführt werden kann.

## <a name="so_bth_encrypt"></a>SO \_ BTH \_ ENCRYPT

Bei nicht verbundenen Sockets erzwingt die **Socketoption SO \_ BTH \_ ENCRYPT** die Verschlüsselung, um eine Verbindung herzustellen. Verschlüsselung ist nur für authentifizierte Verbindungen verfügbar. Bei eingehenden Verbindungen wird eine Verbindung, für die keine Verschlüsselung hergestellt werden kann, automatisch abgelehnt und **gibt WSAEHOSTDOWN** als Fehler zurück. Bei ausgehenden Verbindungen schlägt die [**Connect-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-connect) **mit WSAEACCES** fehl, wenn keine Verschlüsselung eingerichtet werden kann. Als Reaktion darauf fordert die Anwendung den Benutzer möglicherweise auf, die beiden Geräte vor der Bluetooth zu authentifizieren. Weitere Informationen zum Authentifizieren Bluetooth Geräten finden Sie unter [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Für die Socketoption SO BTH ENCRYPT ist optval ein Zeiger auf \_ \_ ULONG **bEncrypt** und muss **TRUE sein.**  *optlen* entspricht sizeof(ULONG).

**Windows XP mit SP2:** Für einen Socket, der verbunden und authentifiziert ist, **startet \_ BTH \_ ENCRYPT** die Verschlüsselung.

## <a name="so_bth_mtu"></a>SO \_ BTH \_ MTU

Die **SO \_ BTH \_ MTU-Socketoption** ist eine erweiterte Option, die hauptsächlich für die Validierung verwendet wird. Die **\_ SO-BTH-MTU-Option \_** erhält oder legt den Standardwert der RFCOMM-MTU (maximale Übertragungseinheit) für die Verbindungsaushandlung auf einen anderen Wert als den Standardwert des RFCOMM-Protokolls fest.

Da RFCOMM MTU von der zugrunde liegenden L2CAP-MTU sowie den Mindest- und Höchstwerten für Protokolle und Anwendungen betroffen ist, ist der Standardwert für **SO \_ BTH \_ MTU** nur ein Ausgangspunkt für die Aushandlung mit dem Remote-Peer, und die endgültige ausgehandelte MTU wird wahrscheinlich vom Standard abweichen. Das Festlegen **des \_ SO-BTH-MTU-Werts \_** kann sich negativ auf den Durchsatz auswirken. Daher sollten alle Änderungen mit Kenntnis des zugrunde liegenden Bluetooth werden.

Die **\_ So-BTH-MTU-Socketoption \_** kann für verbundene Sockets ausgeführt werden, hat jedoch keine Auswirkungen, wenn die Aushandlung bereits abgeschlossen wurde. Das Festlegen auf den lauschenden Socket (Server) hat keine Auswirkungen.

Die Datenmenge, die eine Anwendung in einem einzelnen Socketaufruf senden oder empfangen kann, ist von der MTU nicht betroffen. MTU wirkt sich nur darauf aus, wie der zugrunde liegende Windows Sockets-Dienstanbieter Pakete für den Transport segmentiert. Sowohl die vorgeschlagene MTU als auch die letztlich ausgehandelte MTU müssen zwischen **RFCOMM \_ MIN \_ MTU** und **RFCOMM \_ MAX \_ MTU** liegen, wie in der Ws2bth.h-Headerdatei definiert.

Bei der **SO \_ BTH \_ MTU-Socketoption** *ist optval* ein Zeiger auf ULONG mtu; *optlen* entspricht "sizeof(ULONG)".

## <a name="so_bth_mtu_max"></a>SO \_ BTH \_ MTU \_ MAX

Die **Socketoption SO \_ BTH \_ MTU \_ MAX** ist eine erweiterte Option, die hauptsächlich für die Validierung verwendet wird. Die **Socketoption SO \_ BTH \_ MTU \_ MAX** legt die maximale RFCOMM-MTU (maximale Übertragungseinheit) für die Verbindungsaushandlung fest. Bei Verbindungen mit einer RFCOMM-MTU, die größer oder gleich diesem Wert ist, treten während des Verbindungsan [**annahmeprozesses**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**Fehler**](/windows/desktop/api/winsock2/nf-winsock2-accept) auf. Das Festlegen dieser Socketoption ist für einen verbundenen Socket zulässig, hat jedoch keine Auswirkungen, wenn die Aushandlung abgeschlossen wurde. Wenn Sie diese Socketoption für einen lauschenden Socket festlegen, wird der Wert für alle eingehenden Verbindungen propagiert. Der MAX MTU-Wert muss zwischen **RFCOMM \_ MIN \_ MTU** und **RFCOMM \_ MAX \_ MTU** liegen, wie in der Ws2bth.h-Headerdatei definiert.

Für die **Socketoption SO \_ BTH \_ MTU \_ MAX** ist *optval* ein Zeiger auf die ULONG max \_ mtu. *optlen* entspricht "sizeof(ULONG)".

## <a name="so_bth_mtu_min"></a>SO \_ BTH \_ MTU \_ MIN

Die **SOCKEToption SO \_ BTH \_ MTU \_ MIN** ist eine erweiterte Option, die hauptsächlich für die Validierung verwendet wird. Die **SOCKEToption SO \_ BTH \_ MTU \_ MIN** legt die minimale RFCOMM-MTU (maximale Übertragungseinheit) für die Verbindungsaushandlung fest. Bei Verbindungen mit einer RFCOMM-MTU, die kleiner als dieser Wert ist, treten während des [**Verbindungsan**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**annahmeprozesses Fehler**](/windows/desktop/api/winsock2/nf-winsock2-accept) auf. Das Festlegen dieser Socketoption ist für einen verbundenen Socket zulässig, hat jedoch keine Auswirkungen, wenn die Aushandlung abgeschlossen wurde. Wenn Sie diese Socketoption für einen lauschenden Socket festlegen, wird der Wert für alle eingehenden Verbindungen propagiert.

Nur ein lauschendes Socket kann die MTU nach unten überarbeiten. Wenn der vom verbindenden Socket vorgeschlagene Wert daher kleiner als der wert ist, der für **SO \_ BTH \_ MTU \_ MIN** auf dem lauschenden Socket festgelegt ist, wird die Verbindung abgelehnt. Die minimale MTU muss zwischen **RFCOMM \_ MIN \_ MTU** und **RFCOMM \_ MAX \_ MTU** liegen, wie in der Ws2bth.h-Headerdatei definiert.

Für die SOCKEToption SO BTH MTU MIN ist optval ein Zeiger \_ \_ auf \_ ULONG min  \_ mtu; *optlen* entspricht "sizeof(ULONG)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**Verbinden**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**Akzeptieren**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 