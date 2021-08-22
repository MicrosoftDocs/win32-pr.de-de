---
description: Die WSADuplicateSocket-Funktion wird eingeführt, um die prozessübergreifende Socketfreigabe zu ermöglichen.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Freigegebene Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3f2663aa618b1bacab40b1cb29735c972e1d8b9e9db3528ee5079a336747c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612910"
---
# <a name="shared-sockets"></a>Freigegebene Sockets

Die [**WSADuplicateSocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) wird eingeführt, um die prozessübergreifende Socketfreigabe zu ermöglichen. Ein Quellprozess ruft **WSADuplicateSocket auf,** um eine spezielle [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für einen Zielprozessbezeichner zu erhalten. Sie verwendet einen Mechanismus der prozessübergreifenden Kommunikation (Interprocess Communications, IPC), um den Inhalt dieser Struktur an einen Zielprozess zu übergeben. Der Zielprozess verwendet dann die **WSAPROTOCOL \_ INFO-Struktur** in einem Aufruf von [**WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Der von dieser Funktion zurückgegebene Socketdeskriptor ist ein zusätzlicher Socketdeskriptor für einen zugrunde liegenden Socket, der somit freigegeben wird. Sockets können von Threads in einem bestimmten Prozess gemeinsam genutzt werden, ohne die **WSADuplicateSocket-Funktion** zu verwenden, da ein Socketdeskriptor in allen Threads eines Prozesses gültig ist.

Die beiden (oder mehr) Deskriptoren, die auf einen freigegebenen Socket verweisen, können unabhängig verwendet werden, wenn es um E/A geht. Die Winsock-Schnittstelle implementiert jedoch keine Zugriffssteuerungstypen, sodass die Prozesse alle Vorgänge auf einem freigegebenen Socket koordinieren müssen. Ein typisches Beispiel für die Gemeinsame Nutzung von Sockets ist die Verwendung eines Prozesses zum Erstellen von Sockets und Herstellen von Verbindungen. Dieser Prozess übergibt Sockets dann an andere Prozesse, die für den Informationsaustausch verantwortlich sind.

Die [**WSADuplicateSocket-Funktion erstellt**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) Socketdeskriptoren und nicht den zugrunde liegenden Socket. Daher werden alle einem Socket zugeordneten Zustände für alle Deskriptoren gemeinsam gehalten. Beispielsweise wird ein [**setsockopt-Vorgang,**](/windows/desktop/api/winsock/nf-winsock-setsockopt) der mit einem Deskriptor ausgeführt wird, anschließend mithilfe eines [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) aus einem oder allen Deskriptoren angezeigt. Ein Prozess kann [**closesocket für einen**](/windows/desktop/api/winsock/nf-winsock-closesocket) duplizierten Socket aufrufen, und der Deskriptor wird zugewiesen. Der zugrunde liegende Socket bleibt jedoch geöffnet, bis **closesocket** mit dem letzten verbleibenden Deskriptor aufgerufen wird.

Die Benachrichtigung über freigegebene Sockets unterliegt den üblichen Einschränkungen der [**Funktionen WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) und [**WSAEventSelect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) Durch das Ausstellen eines dieser Aufrufe mit einem der freigegebenen Deskriptoren wird jede vorherige Ereignisregistrierung für den Socket abgebrochen, unabhängig davon, welcher Deskriptor für diese Registrierung verwendet wurde. Daher wäre es beispielsweise nicht möglich, dass Prozess A FD READ-Ereignisse und Prozess \_ B FD \_ WRITE-Ereignisse erhält. In Situationen, in denen eine solche enge Koordination erforderlich ist, wird empfohlen, dass Entwickler Threads anstelle separater Prozesse verwenden.

 

 
