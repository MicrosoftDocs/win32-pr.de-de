---
description: Die wsadupliingesocket-Funktion wird eingeführt, um die prozessübergreifende socketfreigabe zu aktivieren.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Freigegebene Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6753b01f6389254756254d2ebe196af8e2a8a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959333"
---
# <a name="shared-sockets"></a>Freigegebene Sockets

Die [**wsadupliingesocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) -Funktion wird eingeführt, um die prozessübergreifende socketfreigabe zu aktivieren. Von einem Quell Prozess wird **wsadupliplatesocket** aufgerufen, um eine spezielle [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für einen Ziel Prozess Bezeichner zu erhalten. Er verwendet einen gewissen Prozess für die prozessübergreifende Kommunikation (IPC), um den Inhalt dieser Struktur an einen Ziel Prozess zu übergeben. Der Ziel Prozess verwendet dann die **wsaprotocol- \_ Informations** Struktur in einem [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)-aufrufsvorgang. Der von dieser Funktion zurückgegebene socketdeskriptor ist ein zusätzlicher socketdeskriptor für einen zugrunde liegenden Socket, der freigegeben wird. Sockets können von Threads in einem bestimmten Prozess gemeinsam genutzt werden, ohne dass die **wsadupliallesocket** -Funktion verwendet wird, da ein socketdeskriptor in allen Threads eines Prozesses gültig ist.

Die zwei (oder mehr) Deskriptoren, die auf einen freigegebenen Socket verweisen, können unabhängig von den e/a-Vorgängen verwendet werden. Die Winsock-Schnittstelle implementiert jedoch keinen Zugriffs Steuerungstyp, sodass die Prozesse alle Vorgänge für einen freigegebenen Socket koordinieren müssen. Ein typisches Beispiel für die Freigabe von Sockets besteht darin, einen Prozess zum Erstellen von Sockets und zum Herstellen von Verbindungen zu verwenden. Dieser Prozess übergibt Sockets an andere Prozesse, die für den Informationsaustausch zuständig sind.

Die [**wsaduplitoresocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) -Funktion erstellt socketdeskriptoren und nicht den zugrunde liegenden Socket. Folglich werden alle einem Socket zugeordneten Zustände in allen Deskriptoren gemeinsam gespeichert. Beispielsweise wird ein [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Vorgang, der mit einem Deskriptor ausgeführt wird, anschließend mithilfe von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) von einem beliebigen oder allen Deskriptoren sichtbar. Ein Prozess kann [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) für einen duplizierten Socket aufzurufen, und die Zuordnung des Deskriptors wird aufgehoben. Der zugrunde liegende Socket bleibt jedoch geöffnet, bis **closesocket** mit dem letzten verbleibenden Deskriptor aufgerufen wird.

Benachrichtigungen zu freigegebenen Sockets unterliegen den üblichen Einschränkungen der [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -und [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktionen. Wenn Sie einen dieser Aufrufe mit einem der freigegebenen Deskriptoren ausgeben, werden alle vorherigen Ereignis Registrierungen für den Socket abgebrochen, unabhängig davon, welcher Deskriptor für die Registrierung verwendet wurde. Folglich wäre es z. B. nicht möglich, den Prozess A Receive FD \_ -Lese Ereignisse und Process B-Receive-Write-Ereignisse zu verarbeiten \_ . In Situationen, in denen eine solche strenge Koordination erforderlich ist, wird empfohlen, dass Entwickler anstelle von separaten Prozessen Threads verwenden.

 

 
