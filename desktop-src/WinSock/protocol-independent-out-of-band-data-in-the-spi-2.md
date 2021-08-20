---
description: Out-of-Band-Daten (OOB) sind ein logisch unabhängiger Übertragungskanal, der einem Paar verbundener Streamsockets zugeordnet ist.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Protokollunabhängige Out-of-Band-Daten in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55e186e34e401e56017097271d5f036f2666bdc51f8bc27c6692be7e12874e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993610"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Protokollunabhängige Out-of-Band-Daten in der SPI

Out-of-Band-Daten (OOB) sind ein logisch unabhängiger Übertragungskanal, der einem Paar verbundener Streamsockets zugeordnet ist. OOB-Daten können unabhängig von normalen Daten an den Benutzer übermittelt werden. Die Abstraktion definiert, dass die OOB-Datenfunktionen die zuverlässige Übermittlung von mindestens einem OOB-Datenblock gleichzeitig unterstützen müssen. Dieser Datenblock kann mindestens ein Byte an Daten enthalten, und mindestens ein OOB-Datenblock steht möglicherweise gleichzeitig an den Benutzer. Für Kommunikationsprotokolle, die In-Band-Signalisierung unterstützen (also TCP, bei dem die dringenden Daten nacheinander mit den normalen Daten übermittelt werden), extrahiert das System normalerweise die OOB-Daten aus dem normalen Datenstrom und speichert sie separat (wodurch eine Lücke im normalen Datenstrom entsteht). Dadurch können Benutzer zwischen dem Empfang der OOB-Daten in der angegebenen Reihenfolge und dem Empfang außerhalb der Sequenz wählen, ohne dass alle dazwischen liegenden Daten gepuffert werden müssen. Sie können OOB-Daten einsehen.

Ein Benutzer kann mithilfe der [**WSPIoctl-Funktion**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK) ermitteln, ob OOB-Daten auf das Lesen warten. Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks im normalen Datenstrom sinnvoll ist (d. h. TCP), verwaltet ein Windows Sockets-Dienstanbieter einen konzeptionellen Marker, der die Position des letzten Byte der OOB-Daten im normalen Datenstrom angibt. Dies ist für die Implementierung der **WSPIoctl-Funktionalität** (SIOCATMARK) nicht erforderlich. Das Vorhandensein oder Fehlen von OOB-Daten ist alles, was erforderlich ist.

Bei Protokollen, bei denen das Konzept der Position des OOB-Datenblocks innerhalb des normalen Datenstroms sinnvoll ist, kann eine Anwendung es vorziehen, Out-of-Band-Daten inline als Teil des normalen Datenstroms zu verarbeiten. Dies wird erreicht, indem die Socketoption SO \_ OOBINLINE festgelegt wird (siehe Abschnitt [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). Bei anderen Protokollen, bei denen die OOB-Datenblöcke wirklich unabhängig vom normalen Datenstrom sind, führt der Versuch, SO OOBINLINE festzulegen, zu \_ einem Fehler. Eine Anwendung kann den SIOCATMARK WSPIoctl-Befehl verwenden, um zu bestimmen, ob ungelesene OOB-Daten vor der Markierung vorhanden sind. Dies kann beispielsweise zum erneuten Synchronisieren mit dem Peer verwendet werden, indem sichergestellt wird, dass alle Daten bis zur Markierung im Datenstrom nach Bedarf verworfen werden.

Wenn SO \_ OOBINLINE deaktiviert ist (standardmäßig):

-   Der Winsock-Dienstanbieter benachrichtigt einen Client über ein \_ FD-OOB-Ereignis, wenn der Client für die Benachrichtigung mit [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))registriert ist, auf die gleiche Weise wie FD \_ READ verwendet wird, um das Vorhandensein normaler Daten zu benachrichtigen. Das heißt, FD \_ OOB wird bereitgestellt, wenn OOB-Daten eintreffen und zuvor keine OOB-Daten in die Warteschlange eingereiht wurden, und auch wenn Daten mithilfe des \_ MSG-OOB-Flags gelesen werden, und einige OOB-Daten nach der Rückgabe des Lesevorgangs gelesen werden müssen. FD \_ READ-Nachrichten werden für OOB-Daten nicht bereitgestellt.
-   Der Winsock-Dienstanbieter gibt aus [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) mit dem entsprechenden *exceptfds-Socketsatz* zurück, wenn OOB-Daten im Socket in die Warteschlange eingereiht werden.
-   Der Client kann [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) mit MSG \_ OOB aufrufen, um den dringenden Datenblock jederzeit zu lesen. Der OOB-Datenblock springt in die Warteschlange.
-   Der Client kann [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ohne \_ MSG-OOB aufrufen, um den normalen Datenstrom zu lesen. Der OOB-Datenblock wird nicht mit normalen Daten im Datenstrom angezeigt. Wenn OOB-Daten nach einem Aufruf von **WSPRecv** verbleiben, benachrichtigt der Dienstanbieter den Client mit FD \_ OOB oder über *exceptfds,* wenn [**WSPSelect verwendet**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))wird.
-   Bei Protokollen, bei denen die OOB-Daten eine Position innerhalb des normalen Datenstroms haben, erstreckt sich ein einzelner [**WSPRecv-Vorgang**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) nicht über diese Position. Ein **WSPRecv** gibt die normalen Daten vor der Markierung zurück, und ein **zweites WSPRecv** ist erforderlich, um mit dem Lesen von Daten nach der Markierung zu beginnen.

Bei \_ aktivierter SO OOBINLINE:

-   \_FD-OOB-Nachrichten werden nicht für OOB-Daten bereitgestellt. Für die Funktionen [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) und [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) werden OOB-Daten als normale Daten behandelt und durch Festlegen des Sockets in *Readfds* bzw. durch Senden einer FD \_ READ-Nachricht angegeben.
-   Der Client darf [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) nicht aufrufen, wenn das \_ MSG-OOB-Flag zum Lesen des OOB-Datenblocks festgelegt ist. Der Fehlercode WSAEINVAL wird zurückgegeben.
-   Der Client kann [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) aufrufen, ohne dass das \_ MSG-OOB-Flag festgelegt ist. Alle OOB-Daten werden in der richtigen Reihenfolge innerhalb des normalen Datenstroms übermittelt. OOB-Daten werden nie mit normalen Daten kombiniert. Es müssen drei Leseanforderungen vorhanden sein, um die OOB-Daten zu umgehen. Die erste gibt die normalen Daten vor dem OOB-Datenblock zurück, die zweite gibt die OOB-Daten zurück, die dritte gibt die normalen Daten nach den OOB-Daten zurück. Anders ausgedrückt: Die Grenzen des OOB-Datenblocks bleiben erhalten.

Die [**WSPAsyncSelect-Routine**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) eignet sich besonders gut für die Behandlung von Benachrichtigungen über das Vorhandensein von OOB-Daten, wenn SO \_ OOBINLINE deaktiviert ist.

 

 
