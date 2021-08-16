---
description: Die Streamsocketabstraktion umfasst das Konzept von Out-of-Band-Daten (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent Out-of-Band-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1918ba1525462f4352d76c989d7fb5d92beeb59766f92cdccbdda66a5b82744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860830"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent Out-of-Band-Daten

Die Streamsocketabstraktion umfasst das Konzept von Out-of-Band-Daten (OOB). Viele Protokolle ermöglichen es, Teile eingehender Daten in irgendeiner Weise als besonders zu markiert werden, und diese speziellen Datenblöcke können dem Benutzer aus der normalen Reihenfolge übermittelt werden. Beispiele hierfür sind beschleunigte Daten in X.25 und anderen OSI-Protokollen sowie dringende Daten in BSD UNIX verwendung von TCP. Im folgenden Abschnitt wird die protokollunabhängige OOB-Datenverarbeitung beschrieben. Eine Erläuterung der OOB-Daten, die mithilfe dringender TCP-Daten implementiert werden, folgt auf die protokollunabhängige Erklärung. In jeder Diskussion impliziert die Verwendung von recv auch [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)und [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), und Verweise auf [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) gelten auch für [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect). [](/windows/desktop/api/winsock/nf-winsock-recv)

## <a name="protocol-independent-oob-data"></a>Protokollunabhängige OOB-Daten

OOB-Daten sind ein logisch unabhängiger Übertragungskanal, der jedem Paar verbundener Streamsockes zugeordnet ist. OOB-Daten können unabhängig von normalen Daten an den Benutzer übermittelt werden. Die Abstraktion definiert, dass die OOB-Dateneinrichtung die zuverlässige Übermittlung von mindestens einem OOB-Datenblock gleichzeitig unterstützen muss. Dieser Datenblock kann mindestens ein Byte an Daten enthalten, und mindestens ein OOB-Datenblock kann die Übermittlung an den Benutzer zu einem beliebigen Zeitpunkt ausstehen. Für Kommunikationsprotokolle, die In-Band-Signalisierung unterstützen (z. B. TCP, bei dem die dringenden Daten nacheinander mit den normalen Daten übermittelt werden), extrahiert das System normalerweise die OOB-Daten aus dem normalen Datenstrom und speichert sie separat (was eine Lücke im normalen Datenstrom hinterlässt). Dadurch können Benutzer auswählen, ob die OOB-Daten in der richtigen Reihenfolge empfangen und nicht in der richtigen Reihenfolge empfangen werden, ohne alle dazwischen folgenden Daten puffern zu müssen. Es ist möglich, Out-of-Band-Daten (OOB) einsehen.

Ein Benutzer kann mithilfe der [**Funktion ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) oder [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mit **SIOCATMARK** IOCTL ermitteln, ob OOB-Daten gelesen werden sollen. Für Protokolle, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist, z. B. TCP, verwaltet ein Windows Sockets-Dienstanbieter einen konzeptionellen Marker, der die Position des letzten Byte von OOB-Daten innerhalb des normalen Datenstroms angibt. Dies ist für die Implementierung der **ioctlsocket-** oder **WSAIoctl-Funktionen,** die **SIOCATMARK unterstützen, nicht erforderlich.** Das Vorhandensein oder Fehlen von OOB-Daten ist erforderlich.

Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist, kann eine Anwendung Out-of-Band-Daten als Teil des normalen Datenstroms inline verarbeiten. Dies wird durch Festlegen der Socketoption SO \_ OOBINLINE mit der [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) erreicht. Bei anderen Protokollen, bei denen die OOB-Datenblöcke wirklich unabhängig vom normalen Datenstrom sind, führt der Versuch, SO \_ OOBINLINE zu setzen, zu einem Fehler. Eine Anwendung kann die [**Funktion ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) oder [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mit **SIOCATMARK** IOCTL verwenden, um zu bestimmen, ob vor der Markierung ungelesene OOB-Daten verfügbar sind. Beispielsweise kann er diese Informationen verwenden, um sich mit seinem Peer neu zusynchronisieren, indem sichergestellt wird, dass alle Daten bis zur Markierung im Datenstrom gegebenenfalls verworfen werden.

Wenn SO \_ OOBINLINE deaktiviert ist (Standardeinstellung):

-   Windows Sockets benachrichtigt eine Anwendung über ein FD-OOB-Ereignis, wenn die Anwendung für die Benachrichtigung mit \_ [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)registriert ist, auf die gleiche Weise wie FD READ verwendet wird, um über das Vorhandensein normaler Daten zu \_ benachrichtigen. Das bedeutet, dass FD OOB veröffentlicht wird, wenn OOB-Daten ohne OOB-Daten in der \_ Warteschlange eintreffen. Der FD-OOB wird auch veröffentlicht, wenn Daten mithilfe des MSG-OOB-Flags gelesen werden, während einige OOB-Daten nach der Rückkehr des Lesevorgang in die \_ \_ Warteschlange gestellt werden. FD \_ READ-Nachrichten werden für OOB-Daten nicht veröffentlicht.
-   Windows Sockets gibt von [**select mit dem**](/windows/desktop/api/Winsock2/nf-winsock2-select) entsprechenden *exceptfds-Socketsatz* zurück, wenn OOB-Daten auf dem Socket in die Warteschlange gestellt werden.
-   Die Anwendung kann [**recv mit**](/windows/desktop/api/winsock/nf-winsock-recv) MSG \_ OOB aufrufen, um den dringenden Datenblock jederzeit zu lesen. Der OOB-Datenblock springt in die Warteschlange.
-   Die Anwendung kann [**recv ohne**](/windows/desktop/api/winsock/nf-winsock-recv) MSG-OOB \_ aufrufen, um den normalen Datenstrom zu lesen. Der OOB-Datenblock wird nicht im Datenstrom mit normalen Daten angezeigt. Wenn OOB-Daten nach einem Aufruf von **recv** erhalten bleiben, benachrichtigt Windows Sockets die Anwendung mit FD OOB oder \_ *exceptfds,* wenn Sie [**auswählen.**](/windows/desktop/api/Winsock2/nf-winsock2-select)
-   Bei Protokollen, bei denen die OOB-Daten eine Position innerhalb des normalen Datenstroms haben, umfasst ein einzelner [**Recv-Vorgang**](/windows/desktop/api/winsock/nf-winsock-recv) diese Position nicht. Ein **Recv gibt** die normalen Daten vor der Markierung zurück, und ein zweites **Recv** ist erforderlich, um mit dem Lesen von Daten nach der Markierung zu beginnen.

Wenn SO \_ OOBINLINE aktiviert ist:

-   Für \_ OOB-Daten werden keine FD-OOB-Nachrichten gesendet. OOB-Daten werden für die Select- und [**WSAAsyncSelect-Funktionen**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) wie gewohnt behandelt und durch Festlegen des Sockets in *Readfds* oder durch Senden einer FD [](/windows/desktop/api/Winsock2/nf-winsock2-select) \_ READ-Nachricht angegeben.
-   Die Anwendung kann [**recv nicht aufrufen,**](/windows/desktop/api/winsock/nf-winsock-recv) wenn das MSG-OOB-Flag zum \_ Lesen des OOB-Datenblocks festgelegt ist. Der Fehlercode WSAEINVAL wird zurückgegeben.
-   Die Anwendung kann [**recv aufrufen,**](/windows/desktop/api/winsock/nf-winsock-recv) ohne dass das MSG-OOB-Flag \_ festgelegt ist. Alle OOB-Daten werden in der richtigen Reihenfolge innerhalb des normalen Datenstroms übermittelt. OOB-Daten werden nie mit normalen Daten gemischt. Es müssen drei Leseanforderungen angezeigt werden, um über die OOB-Daten zu erhalten. Die erste gibt die normalen Daten vor dem OOB-Datenblock zurück, die zweite die OOB-Daten, die dritte gibt die normalen Daten nach den OOB-Daten zurück. Anders ausgedrückt: Die OOB-Datenblockgrenzen werden beibehalten.

Die [**WSAAsyncSelect-Routine**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) eignet sich besonders gut für die Behandlung von Benachrichtigungen über das Vorhandensein von Out-of-Band-Daten, wenn SO \_ OOBINLINE deaktiviert ist.

## <a name="oob-data-in-tcp"></a>OOB-Daten in TCP

> [!IMPORTANT]
> Die folgende Diskussion über Out-of-Band-Daten (OOB), die mithilfe dringender TCP-Daten implementiert wurden, folgt dem Modell, das in der Softwareverteilung in Berkeley verwendet wird. Benutzer und Implementierer sollten dies beachten:

 

-   Derzeit gibt es zwei in Konflikt stehende Interpretationen von [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (wo das Konzept eingeführt wird).
-   Die Implementierung von OOB-Daten in der Softwareverteilung von Berkeley (BSD) entspricht nicht den in [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt)angegebenen Hostanforderungen.

    Insbesondere zeigt der dringende TCP-Zeiger in BSD auf das Byte nach dem dringenden Daten byte, und ein RFC-konformer dringender TCP-Zeiger verweist auf das dringende Daten-Byte. Wenn eine Anwendung daher dringende Daten von einer BSD-kompatiblen Implementierung an eine Implementierung sendet, die mit RFC 1122 kompatibel ist, liest der Empfänger das falsche dringende Daten byte (es liest das Byte, das sich nach dem richtigen Byte im Datenstrom befindet, als dringendes Daten byte).

    Um Interoperabilitätsprobleme zu minimieren, wird Anwendungsautoren empfohlen, keine OOB-Daten zu verwenden, es sei denn, dies ist für die Zusammenarbeit mit einem vorhandenen Dienst erforderlich. Windows Socketanbieter dokumentieren die OOB-Semantik (BSD oder RFC 1122), die ihr Produkt implementiert.

Der Eintreffen eines TCP-Segments mit dem Flag UFF (für dringende Probleme) gibt an, dass ein einzelnes Byte von OOB-Daten im TCP-Datenstrom vorlag. Der OOB-Datenblock ist ein Byte groß. Der dringende Zeiger ist ein positiver Offset von der aktuellen Sequenznummer im TCP-Header, der die Position des OOB-Datenblocks angibt (mehrdeutig, wie oben erwähnt). Es kann daher auf Daten verweisen, die noch nicht empfangen wurden.

Wenn SO OOBINLINE deaktiviert ist (Standard), wenn das TCP-Segment mit dem Byte eintrifft, auf das der dringende Zeiger verweist, wird der OOB-Datenblock (ein Byte) aus dem Datenstrom entfernt und \_ gepuffert. Wenn ein nachfolgendes TCP-Segment mit dem festgelegten dringenden Flag (und einem neuen dringenden Zeiger) eintrifft, kann das derzeit in die Warteschlange eingereihte OOB-Byte verloren gehen, da es durch den neuen OOB-Datenblock ersetzt wird (wie bei der Softwareverteilung in Berkeley). Sie wird jedoch nie im Datenstrom ersetzt.

Wenn SO \_ OOBINLINE aktiviert ist, bleiben die dringenden Daten im Datenstrom erhalten. Daher geht der OOB-Datenblock nie verloren, wenn ein neues TCP-Segment mit dringenden Daten eintrifft. Die vorhandene OOB-Datenmarkung wird auf die neue Position aktualisiert.

> [!Note]  
> Wenn die Socketoption SO OOBINLINE festgelegt ist, gibt \_ SIOCATMARK IOCTL immer **TRUE** zurück, und OOB-Daten werden als normale Daten an den Benutzer zurückgegeben.

 

 

 



