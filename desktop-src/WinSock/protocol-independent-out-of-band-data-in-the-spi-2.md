---
description: Out-of-Band (OOB)-Daten sind ein logisch unabhängiger Übertragungskanal, der mit einem Paar verbundener Streamsockets verknüpft ist.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Protokoll unabhängige out-of-Band-Daten in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e5c7c5c8c8ad7a5985ec101dd157370c5f32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526114"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Protokoll unabhängige out-of-Band-Daten in der SPI

Out-of-Band (OOB)-Daten sind ein logisch unabhängiger Übertragungskanal, der mit einem Paar verbundener Streamsockets verknüpft ist. OOB-Daten werden möglicherweise unabhängig von normalen Daten an den Benutzer übermittelt. Die Abstraktion definiert, dass die OOB-Datenfunktionen die zuverlässige Bereitstellung mindestens eines OOB-Datenblocks gleichzeitig unterstützen müssen. Dieser Datenblock enthält möglicherweise mindestens ein Byte an Daten, und mindestens ein OOB-Datenblock kann gleichzeitig an den Benutzer übermittelt werden. Bei Kommunikationsprotokollen, die die in-Band-Signalisierung unterstützen (d. h. TCP, bei der die dringenden Daten nacheinander mit den normalen Daten geliefert werden), extrahiert das System normalerweise die OOB-Daten aus dem normalen Datenstream und speichert Sie separat (wobei eine Lücke im normalen Datenstream besteht). Dies ermöglicht es Benutzern, die OOB-Daten in der richtigen Reihenfolge zu empfangen und Sie außerhalb der Reihenfolge zu empfangen, ohne dass alle dazwischen liegenden Daten gepuffert werden müssen. Sie können OOB-Daten einsehen.

Ein Benutzer kann ermitteln, ob OOB-Daten mit der [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (siocatmark)-Funktion gelesen werden sollen. Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist (d. h. TCP), behält ein Windows Sockets Service-Anbieter einen konzeptionellen Marker bei, der die Position des letzten Bytes der OOB-Daten innerhalb des normalen Datenstroms angibt. Dies ist für die Implementierung der **wspioctl** -Funktionalität (siocatmark) nicht erforderlich – das vorhanden sein oder Fehlen von OOB-Daten ist alles, was erforderlich ist.

Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist, kann es sinnvoll sein, out-of-Band-Daten Inline als Teil des normalen Datenstroms zu verarbeiten. Dies wird erreicht, indem die Socketoption so \_ oobinline festgelegt wird (siehe Abschnitt [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). Bei anderen Protokollen, bei denen die OOB-Datenblöcke wirklich unabhängig vom normalen Datenstream sind, führt der Versuch, so oobinline festzulegen, zu \_ einem Fehler. Eine Anwendung kann den Befehl "siocatmark wspioctl" verwenden, um zu bestimmen, ob vor der Markierung ungelesene OOB-Daten vorhanden sind. Dies kann z. b. verwendet werden, um eine erneute Synchronisierung mit dem Peer durchführen zu können, indem sichergestellt wird, dass alle Daten bis zur Markierung im Datenstrom bei Bedarf verworfen werden.

Mit \_ deaktiviertem oobinline (Standard):

-   Der Winsock-Dienstanbieter benachrichtigt den Client über ein FD- \_ OOB-Ereignis, wenn der Client für die Benachrichtigung mit [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))registriert ist, in genau derselben Weise, wie der FD-Lesevorgang für \_ die Benachrichtigung über das vorhanden sein normaler Daten verwendet wird. Das heißt, FD \_ OOB wird bereitgestellt, wenn OOB-Daten eintreffen und keine OOB-Daten in die Warteschlange eingereiht wurden, und auch wenn Daten mit dem OOB-Flag "msg" gelesen \_ werden und einige OOB-Daten nach der Rückgabe des Lesevorgangs noch gelesen werden müssen. FD- \_ Lese Nachrichten werden für OOB-Daten nicht gepostet.
-   Der Winsock-Dienstanbieter gibt aus [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) mit dem entsprechenden *exceptfds* -socketsatz zurück, wenn OOB-Daten im Socket in die Warteschlange eingereiht werden.
-   Der Client kann [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) mit der Meldung \_ OOB aufgerufen werden, um den dringenden Datenblock zu lesen. Der Block der OOB-Daten springt in der Warteschlange.
-   Der Client kann [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ohne msg \_ OOB aufgerufen werden, um den normalen Datenstrom zu lesen. Der OOB-Datenblock wird nicht im Datenstrom mit normalen Daten angezeigt. Wenn OOB-Daten nach einem **wsprecv**-Rückruf verbleiben, benachrichtigt der Dienstanbieter den Client mit FD \_ OOB oder durch *exceptfds* bei Verwendung von [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   Bei Protokollen, bei denen die OOB-Daten über eine Position innerhalb des normalen Datenstroms verfügen, wird die Position eines einzelnen [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) -Vorgangs nicht überspannen. Ein **wsprecv** gibt die normalen Daten vor der Markierung zurück, und ein zweites **wsprecv** ist erforderlich, um mit dem Lesen von Daten nach der Markierung zu beginnen.

Mit \_ aktiviertem oobinline:

-   FD \_ OOB-Nachrichten werden nicht für OOB-Daten gepostet – für den Zweck der [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) -und [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) -Funktionen werden OOB-Daten als normale Daten behandelt und durch Festlegen des  Sockets in der Schreibweise bzw. durch das Senden einer FD- \_ Lese Nachricht angegeben.
-   Der Client ruft möglicherweise [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) nicht \_ auf, wenn das Flag für die Meldung OOB zum Lesen des OOB-Datenblocks festgelegt ist – der Fehlercode wird zurückgegeben.
-   Vom Client kann [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) aufgerufen werden, ohne dass das Flag für die Nachrichten \_ OOB festgelegt ist. Alle OOB-Daten werden in der richtigen Reihenfolge innerhalb des normalen Datenstroms zugestellt. OOB-Daten werden nie mit normalen Daten gemischt – es müssen drei Lese Anforderungen vorliegen, um die OOB-Daten zu überschreiten. Der erste gibt die normalen Daten vor dem OOB-Datenblock zurück, der zweite gibt die OOB-Daten zurück, das dritte gibt die normalen Daten nach den OOB-Daten zurück. Anders ausgedrückt: die OOB-Datenblock Grenzen bleiben erhalten.

Die [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) -Routine eignet sich besonders gut für die Behandlung von Benachrichtigungen über das vorhanden sein von OOB-Daten, wenn " \_ oobinline" deaktiviert ist.

 

 
