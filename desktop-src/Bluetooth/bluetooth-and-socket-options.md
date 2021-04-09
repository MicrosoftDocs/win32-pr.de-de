---
title: Bluetooth-und Socket-Optionen
description: 'Bluetooth für Windows unterstützt die folgenden Socketoptionen:'
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth-und Socket-Optionen Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948830"
---
# <a name="bluetooth-and-socket-options"></a>Bluetooth-und Socket-Optionen

Bluetooth für Windows unterstützt die folgenden Socketoptionen: Socketoptionen werden mithilfe der Funktionen [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) bzw. [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) festgelegt und abgefragt. Alle der folgenden Optionen können mit der Funktion " **setsockopt** " verwendet werden, aber nur die Option " **so \_ BTH \_ MTU** " ist für die Verwendung mit der Funktion " **getsockopt** " verfügbar.

Zum Arbeiten mit Bluetooth-Socketoptionen sind die folgenden Einstellungen erforderlich:

-   Der *s* -Parameter muss ein Bluetooth-Socket sein.
-   Der *Level* -Parameter muss " **Sol \_ RFCOMM**" lauten.

## <a name="so_bth_authenticate"></a>\_BTH \_ Authenticate

Bei getrennten Sockets gibt das **\_ BTH- \_ Authentifizieren** an, dass eine Authentifizierung erforderlich ist, damit ein [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -oder [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Vorgang erfolgreich abgeschlossen werden kann. Wenn diese Socketoption aktiviert ist, wird die Authentifizierung während der Verbindungs Herstellung aktiv initiiert, wenn die beiden Bluetooth-Geräte zuvor nicht authentifiziert wurden. Die Benutzeroberfläche für den Hauptschlüssel-Austausch wird ggf. vom Betriebssystem außerhalb des Anwendungs Kontexts bereitgestellt.

Bei ausgehenden Verbindungen, für die eine Authentifizierung erforderlich ist, schlägt der [**Verbindungs**](/windows/desktop/api/winsock2/nf-winsock2-connect) Vorgang mit **WSAEACCES** fehl, wenn die Authentifizierung nicht erfolgreich ist. Als Antwort wird der Benutzer von der Anwendung möglicherweise aufgefordert, die zwei Bluetooth-Geräte vor der Verbindung zu authentifizieren.

Für eingehende Verbindungen wird die Verbindung zurückgewiesen, wenn keine Authentifizierung hergestellt werden kann, und es wird ein **wsaehostdown** -Fehler zurückgegeben. Weitere Informationen zum Authentifizieren von Bluetooth-Geräten finden Sie unter [**bluetoothauthenticatedevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Bei der **so \_ BTH \_ Authenticate** Socket-Option ist *optval* ein Zeiger auf ULONG bauthenticate und muss den Wert **true** haben. *optlen* entspricht "sizeof (ULONG)".

**Windows XP mit SP2: so \_ BTH \_ Authenticate** startet die Authentifizierung für verbundene Sockets und erzwingt die Authentifizierung bei Verbindung für nicht verbundene Sockets. Für eingehende Verbindungen wird die Verbindung zurückgewiesen, wenn die Authentifizierung nicht ausgeführt werden kann.

## <a name="so_bth_encrypt"></a>\_BTH \_ verschlüsseln

Bei nicht verbundenen Sockets erzwingt die Option " **\_ BTH \_** Encryption Socket" die Verschlüsselung, um eine Verbindung herzustellen. Die Verschlüsselung ist nur für authentifizierte Verbindungen verfügbar. Für eingehende Verbindungen wird eine Verbindung, für die keine Verschlüsselung eingerichtet werden kann, automatisch abgelehnt, und **wsaehostdown** wird als Fehler zurückgegeben. Bei ausgehenden Verbindungen schlägt die [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktion mit **WSAEACCES** fehl, wenn die Verschlüsselung nicht hergestellt werden kann. Als Antwort wird der Benutzer von der Anwendung möglicherweise aufgefordert, die zwei Bluetooth-Geräte vor der Verbindung zu authentifizieren. Weitere Informationen zum Authentifizieren von Bluetooth-Geräten finden Sie unter [**bluetoothauthenticatedevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Bei der so \_ BTH- \_ Verschlüsselung (Socket-Option) ist *optval* ein Zeiger auf ULONG **bencrypt** und muss **true** sein. *optlen* entspricht sizeof (ULONG).

**Windows XP mit SP2:** Bei einem verknüpften und authentifizierten Socket startet **\_ BTH \_** Encryption die Verschlüsselung.

## <a name="so_bth_mtu"></a>\_BTH \_ MTU

Die Option " **\_ BTH \_ MTU** Socket" ist eine erweiterte Option, die in erster Linie für die Validierung verwendet wird. Die Option "Dr **\_ . BTH \_ MTU** " Ruft die Standard-RFCOMM-MTU (maximale Übertragungseinheit) für die Verbindungs Aushandlung mit einem anderen Wert ab als das RFCOMM-Protokoll (Standardwert).

Da die MTU von der zugrunde liegenden L2CAP-MTU und von Protokoll-und Anwendungs Mindestgebühren und Maximums betroffen ist, ist der Standardwert für die **\_ BTH- \_ MTU** nur ein Ausgangspunkt für die Aushandlung mit dem Remotepeer, und die endgültige ausgehandelte MTU ist wahrscheinlich von der Standardeinstellung abhängig. Wenn Sie den Wert der **\_ BTH- \_ MTU** festlegen, wirkt sich dies möglicherweise negativ auf den Durchsatz aus. Daher sollten alle Änderungen mit Kenntnis des zugrunde liegenden Bluetooth-Protokolls durchgeführt werden.

Die Option " **\_ BTH \_ MTU** Socket" kann für verbundene Sockets ausgeführt werden, hat jedoch keine Auswirkung, wenn die Aushandlung bereits abgeschlossen ist. Die Festlegung auf den Überwachungssocket (Server) hat keine Auswirkungen.

Die Datenmenge, die eine Anwendung in einem einzelnen socketbefehl senden oder empfangen kann, ist von der MTU nicht betroffen. Die MTU wirkt sich nur darauf aus, wie der zugrunde liegende Windows Sockets-Dienstanbieter die Pakete für den Transport Sowohl die vorgeschlagene MTU als auch die MTU, die letztendlich verhandelt hat, müssen zwischen **RFCOMM \_ Min \_ MTU** und **RFCOMM \_ Max \_ MTU** liegen, wie in der Header Datei Ws2bth. h definiert.

Bei der Option " **so \_ BTH \_ MTU** Socket" ist *optval* ein Zeiger auf ULONG MTU. *optlen* entspricht "sizeof (ULONG)".

## <a name="so_bth_mtu_max"></a>\_BTH \_ MTU \_ Max

Die Option für die maximale Anzahl von **\_ BTH \_ MTU \_** ist eine erweiterte Option, die hauptsächlich für die Validierung verwendet wird. Die Option für die Option **\_ BTH \_ MTU \_ Max** Socket legt die maximale RFCOMM-MTU (maximale Übertragungseinheit) für die Verbindungs Aushandlung fest. Verbindungen mit einer RFCOMM-MTU, die gleich oder größer als dieser Wert ist, schlagen während des [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)- / [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Prozesses fehl. Wenn diese Socketoption für einen verbundenen Socket festgelegt wird, hat Sie keine Auswirkung, wenn die Aushandlung abgeschlossen wurde. Wenn Sie diese Socketoption für einen Abhör Socket festlegen, wird der Wert für alle eingehenden Verbindungen weitergegeben. Der Wert der maximalen MTU muss zwischen **RFCOMM \_ Min \_ MTU** und **RFCOMM \_ Max \_ MTU** liegen, wie in der Header Datei Ws2bth. h definiert.

Bei der Option " **so ist \_ BTH \_ MTU \_ Max** Socket" ist *optval* ein Zeiger auf ULONG Max \_ MTU; *optlen* entspricht "sizeof (ULONG)".

## <a name="so_bth_mtu_min"></a>\_BTH \_ MTU \_ Min

Die Option " **\_ BTH \_ MTU \_ Min** Socket" ist eine erweiterte Option, die in erster Linie für die Validierung verwendet wird. Die Option " **\_ BTH \_ MTU \_ Min** Socket" legt die minimale RFCOMM-MTU (maximale Übertragungseinheit) für die Verbindungs Aushandlung fest. Verbindungen mit einer RFCOMM-MTU, die kleiner als dieser Wert ist, schlagen während des [**Verbindungs**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Prozesses fehl. Wenn diese Socketoption für einen verbundenen Socket festgelegt wird, hat Sie keine Auswirkung, wenn die Aushandlung abgeschlossen wurde. Wenn Sie diese Socketoption für einen Abhör Socket festlegen, wird der Wert für alle eingehenden Verbindungen weitergegeben.

Nur ein lausch ender Socket kann die MTU abwärts überarbeiten. wenn der vom Verbindungs-Socket vorgeschlagene Wert also kleiner ist als der Wert, der für **\_ BTH \_ MTU \_ Min** für den Abhör Socket festgelegt ist, wird die Verbindung verweigert. Die Mindestanzahl von MTU muss zwischen **RFCOMM \_ Min \_ MTU** und **RFCOMM \_ Max \_ MTU** liegen, wie in der Header Datei Ws2bth. h definiert.

Für die Option "so \_ BTH \_ MTU \_ Min Socket" ist *optval* ein Zeiger auf ULONG Min \_ MTU; *optlen* entspricht "sizeof (ULONG)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Bluetoothauthenticatedevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**herzustellen**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**erst**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 