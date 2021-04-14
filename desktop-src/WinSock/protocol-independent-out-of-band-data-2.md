---
description: Die Stream-Socket-Abstraktion enthält das Konzept von OOB-Daten (Out-of-Band).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Out-of-Band-Daten Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a929f4273d9cc9f268a296b711649406622ca9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343469"
---
# <a name="protocol-independent-out-of-band-data"></a>Out-of-Band-Daten Protocol-Independent

Die Stream-Socket-Abstraktion enthält das Konzept von OOB-Daten (Out-of-Band). Viele Protokolle ermöglichen es, dass Teile eingehender Daten in gewisser Weise als Sonderzeichen gekennzeichnet werden, und diese speziellen Datenblöcke können an den Benutzer aus der normalen Reihenfolge übermittelt werden. Beispiele hierfür sind beschleunigte Daten in X. 25 und anderen OSI-Protokollen sowie dringende Daten in der Verwendung von TCP von BSD Unix. Im folgenden Abschnitt wird die OOB-Datenverarbeitung in einer Protokoll unabhängigen Weise beschrieben. Eine Erörterung von OOB-Daten, die mithilfe von TCP-Daten implementiert werden, folgt der Protokoll unabhängigen Erläuterung. In jeder Erörterung impliziert die Verwendung [**von empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) auch [**"recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)", " [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)" und " [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)", und Verweise auf " [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) " gelten ebenfalls für " [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)".

## <a name="protocol-independent-oob-data"></a>Protokoll unabhängige OOB-Daten

OOB-Daten sind ein logisch unabhängiger Übertragungskanal, der jedem Paar verbundener Streamsockets zugeordnet ist. OOB-Daten werden möglicherweise unabhängig von normalen Daten an den Benutzer übermittelt. Die Abstraktion definiert, dass die OOB-Datenfunktionen die zuverlässige Bereitstellung mindestens eines OOB-Datenblocks gleichzeitig unterstützen müssen. Dieser Datenblock kann mindestens ein Byte an Daten enthalten, und mindestens ein OOB-Datenblock kann gleichzeitig an den Benutzer übermittelt werden. Bei Kommunikationsprotokollen, die die in-Band-Signalisierung unterstützen (z. b. TCP, bei der die dringenden Daten nacheinander mit den normalen Daten geliefert werden), extrahiert das System normalerweise die OOB-Daten aus dem normalen Datenstrom und speichert Sie separat (wobei eine Lücke im normalen Datenstream besteht). Dies ermöglicht es Benutzern, die OOB-Daten in der richtigen Reihenfolge zu empfangen und Sie außerhalb der Reihenfolge zu empfangen, ohne dass alle dazwischen liegenden Daten gepuffert werden müssen. Es ist möglich, die Out-of-Band-Daten (OOB) zu sehen.

Ein Benutzer kann ermitteln, ob OOB-Daten mit der [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) -Funktion oder der [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mit der **siocatmark** ioctl auf den Lesevorgang warten. Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist, z. b. TCP, verwaltet ein Windows Sockets-Dienstanbieter einen konzeptionellen Marker, der die Position des letzten Bytes der OOB-Daten innerhalb des normalen Datenstroms angibt. Dies ist für die Implementierung der **ioctlsocket** -oder **WSAIoctl** -Funktionen, die **siocatmark** unterstützen, nicht erforderlich. Das vorhanden sein oder Fehlen von OOB-Daten ist vollständig erforderlich.

Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist, kann eine Anwendung out-of-Band-Daten Inline als Teil des normalen Datenstroms verarbeiten. Dies wird erreicht, indem die Socketoption " \_ oobinline" mit der Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " festgelegt wird. Bei anderen Protokollen, bei denen die OOB-Datenblöcke wirklich unabhängig vom normalen Datenstrom sind, führt der Versuch, so oobinline festzulegen, zu \_ einem Fehler. Eine Anwendung kann die [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) -oder die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mit der **siocatmark** ioctl verwenden, um zu bestimmen, ob vor der Markierung ungelesene OOB-Daten vorhanden sind. Sie kann diese Informationen z. b. verwenden, um eine erneute Synchronisierung mit dem Peer durchführen, indem Sie sicherstellen, dass alle Daten bis zu der Markierung im Datenstrom bei Bedarf verworfen werden.

Wenn " \_ oobinline" deaktiviert ist (Standardeinstellung):

-   Windows Sockets benachrichtigt eine Anwendung über ein FD- \_ OOB-Ereignis, wenn die Anwendung, die für eine Benachrichtigung mit [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)registriert ist, genau auf die gleiche Weise wie der FD- \_ Lesevorgang verwendet wird, um über das vorhanden sein normaler Daten zu benachrichtigen. Das heißt, FD \_ OOB wird bei Empfang von OOB-Daten ohne OOB-Daten, die zuvor in die Warteschlange eingereiht wurden Der FD \_ OOB wird auch bereitgestellt, wenn Daten mit dem OOB-Flag "msg" gelesen werden, \_ während einige OOB-Daten nach der Rückgabe des Lesevorgangs in die Warteschlange eingereiht werden. FD- \_ Lese Nachrichten werden für OOB-Daten nicht gepostet.
-   Windows Sockets kehrt von [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) mit dem entsprechenden *exceptfds* -socketsatz zurück, wenn OOB-Daten im Socket in die Warteschlange eingereiht werden.
-   Die Anwendung kann [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) mit der Meldung \_ OOB aufgerufen werden, um den dringenden Datenblock zu lesen. Der Block der OOB-Daten springt in der Warteschlange.
-   Die Anwendung kann [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) ohne msg \_ OOB aufgerufen werden, um den normalen Datenstrom zu lesen. Der OOB-Datenblock wird nicht im Datenstrom mit normalen Daten angezeigt. Wenn OOB-Daten nach einem beliebigen Rückruf von **empfangener** verbleiben, benachrichtigt Windows Sockets die Anwendung mit FD \_ OOB oder mit *exceptfds* bei Verwendung von [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Bei Protokollen, bei denen die OOB-Daten über eine Position innerhalb des normalen Datenstroms verfügen, wird diese Position von einem einzelnen [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Vorgang nicht überspannt. Ein **empfangener** gibt die normalen Daten vor der Markierung zurück, und ein zweites **empfangener** ist erforderlich, um mit dem Lesen von Daten nach der Markierung zu beginnen.

Mit \_ aktiviertem oobinline:

-   FD \_ OOB-Nachrichten werden nicht für OOB-Daten gepostet. OOB-Daten werden für den Zweck der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion und der [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Funktion als normal behandelt und durch Festlegen des *Sockets in der* Schreibweise oder durch das Senden einer FD- \_ Lese Nachricht angezeigt.
-   Die Anwendung kann [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) nicht mit dem OOB-Flag "msg" aufgerufen werden \_ , um den OOB-Datenblock zu lesen. Der Fehlercode wsaabval wird zurückgegeben.
-   Die Anwendung kann [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) aufgerufen werden, ohne dass das \_ OOB-Flag der Nachricht festgelegt wurde Alle OOB-Daten werden in der richtigen Reihenfolge innerhalb des normalen Datenstroms zugestellt. OOB-Daten werden nie mit normalen Daten gemischt. Es müssen drei Lese Anforderungen vorhanden sein, um die OOB-Daten zu übernehmen. Der erste gibt die normalen Daten vor dem OOB-Datenblock zurück, der zweite gibt die OOB-Daten zurück, das dritte gibt die normalen Daten nach den OOB-Daten zurück. Anders ausgedrückt: die OOB-Datenblock Grenzen bleiben erhalten.

Die " [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) "-Routine eignet sich besonders gut für die Behandlung von Benachrichtigungen über das vorhanden sein von Out-of-Band-Daten, wenn " \_ oobinline" deaktiviert ist.

## <a name="oob-data-in-tcp"></a>OOB-Daten in TCP

> [!IMPORTANT]
> Die folgende Erörterung von Out-of-Band-Daten (OOB), die mithilfe von TCP-dringenden Daten implementiert wurde, folgt dem in der Berkeley-Software Verteilung verwendeten Modell. Benutzer und Implementierer sollten Folgendes beachten:

 

-   Es gibt zurzeit zwei widersprüchliche Interpretationen von [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (wo das Konzept eingeführt wird).
-   Die Implementierung von OOB-Daten in der Berkeley Software Distribution (BSD) entspricht nicht den in [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt)angegebenen Host Anforderungen.

    Insbesondere der dringende TCP-Zeiger in BSD zeigt auf das Byte nach dem dringenden Daten Byte, und ein RFC-konformer, nicht-interner TCP-Zeiger zeigt auf das dringende Daten Byte. Wenn eine Anwendung dringende Daten von einer BSD-kompatiblen Implementierung an eine Implementierung sendet, die mit RFC 1122 kompatibel ist, liest der Empfänger daher das falsche dringende Daten Byte (das Byte, das sich nach dem richtigen Byte im Datenstrom befindet, als dringender Daten Byte).

    Um Interoperabilitätsprobleme zu minimieren, sollten Anwendungs Schreiber OOB-Daten nicht verwenden, es sei denn, dies ist für die Interaktion mit einem vorhandenen Dienst erforderlich. Windows Sockets-Lieferanten werden dazu aufgefordert, die OOB-Semantik (BSD oder RFC 1122) zu dokumentieren, die Ihr Produkt implementiert.

Die Ankunft eines TCP-Segments mit dem URG-Flag (für dringlich) gibt an, dass ein einzelnes Byte von OOB-Daten im TCP-Datenstrom vorhanden ist. Der OOB-Datenblock ist ein Byte groß. Der dringende Zeiger ist ein positiver Offset von der aktuellen Sequenznummer im TCP-Header, der den Speicherort des OOB-Datenblocks angibt (eindeutig, wie im vorherigen Abschnitt erwähnt). Daher können Sie auf Daten verweisen, die noch nicht empfangen wurden.

Wenn " \_ oobinline" deaktiviert ist (Standard), wenn das TCP-Segment mit dem Byte, auf das der dringende Zeiger zeigt, erreicht wird, wird der OOB-Datenblock (ein Byte) aus dem Datenstrom entfernt und gepuffert. Wenn ein nachfolgendes TCP-Segment mit dem Satz für dringende Flags (und einem neuen dringenden Zeiger) eingeht, kann das OOB-Byte, das momentan in die Warteschlange eingereiht wird, verloren gehen, da es durch den neuen OOB-Datenblock ersetzt wird (wie in der Berkeley-Software Verteilung Sie wird jedoch nie im Datenstrom ersetzt.

\_Wenn oobinline aktiviert ist, verbleiben die dringenden Daten im Datenstrom. Folglich geht der OOB-Datenblock nie verloren, wenn ein neues TCP-Segment mit dringenden Daten eintrifft. Die vorhandene OOB-Daten Markierung wird an die neue Position aktualisiert.

> [!Note]  
> Wenn die \_ Option oobinline Socket festgelegt ist, gibt die siocatmark ioctl immer **true** zurück, und OOB-Daten werden als normale Daten an den Benutzer zurückgegeben.

 

 

 



