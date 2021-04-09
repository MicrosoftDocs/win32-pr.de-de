---
description: Wie bereits erwähnt, wird die wsajoinleaf-Funktion verwendet, um einen Blattknoten in einer Multipoint-Sitzung zu verknüpfen.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Verwenden von wsajoinleaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027262a117edc5541a4809481aa4607837343b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865680"
---
# <a name="using-wsajoinleaf"></a>Verwenden von wsajoinleaf

Wie bereits erwähnt, wird die [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Funktion verwendet, um einen Blattknoten in einer Multipoint-Sitzung zu verknüpfen. **Wsajoinleaf** hat die gleichen Parameter und Semantik wie [**wsaconnetct**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) , mit dem Unterschied, dass ein socketdeskriptor (wie in [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) und ein zusätzlicher *dwFlags* -Parameter zurückgegeben wird.

Der *dwFlags* -Parameter wird verwendet, um anzugeben, ob der Socket nur als Absender, nur als Empfänger oder beides fungiert. *In dieser* Funktion können nur Multipoint-Sockets für Eingabeparameter verwendet werden. Wenn sich der Multipoint-Socket im nicht blockierenden Modus befindet, kann der zurückgegebene socketdeskriptor erst verwendet werden, nachdem eine entsprechende FD- \_ Verbindungsanzeige empfangen wurde. Eine Stamm Anwendung in einer Multipoint-Sitzung kann [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) einmal oder mehrmals aufzurufen, um eine Reihe von Blattknoten hinzuzufügen, es kann jedoch höchstens eine Multipoint-Verbindungsanforderung gleichzeitig ausstehen.

Der von [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) zurückgegebene socketdeskriptor unterscheidet sich abhängig davon, ob der Eingabe-Socket-Deskriptor, *s*, ein c-Stamm \_ oder ein c- \_ Blatt ist. Bei Verwendung mit einem c- \_ stammsocket legt der *namens* Parameter fest, dass ein bestimmter Blattknoten hinzugefügt werden soll, und der zurückgegebene socketdeskriptor ist ein c-Blatt-Socket, der \_ dem neu hinzugefügten Blattknoten entspricht. Sie ist nicht für den Austausch von Multipoint-Daten vorgesehen, sondern wird stattdessen zum Empfangen von FD xxx-hinweisen (z. b. " \_ FD \_ Close") für die Verbindung verwendet, die mit dem jeweiligen c-Blatt vorhanden ist \_ . Einige Multipoint-Implementierungen können auch zulassen, dass dieser Socket für Seiten Chats zwischen dem Stamm Knoten und einem einzelnen Blattknoten verwendet wird. \_Wenn der entsprechende Blattknoten [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) zum Ablegen aus der Multipoint-Sitzung aufruft, wird ein FD-Anschluss Hinweis für diesen Socket empfangen. Symmetrisch bewirkt das Aufrufen von **closesocket** im c- \_ Blatt Socket, das von **wsajoinleaf** zurückgegeben wurde, bewirkt, dass der Socket im entsprechenden Blattknoten eine "FD Close"- \_ Benachrichtigung erhält.

Wenn [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) mit einem c- \_ Blatt Socket aufgerufen wird, enthält der *Name* -Parameter die Adresse der Stamm Anwendung (für ein Stamm Steuerungs Schema) oder eine vorhandene Multipoint-Sitzung (nicht-Stamm Steuerungs Schema), und der zurückgegebene socketdeskriptor ist identisch mit dem Eingabe socketdeskriptor. In einem Stamm Steuerungs Schema platziert die Stamm Anwendung den c-Stamm \_ Socket durch Aufrufen von " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)" im Empfangsmodus. Die standardmäßige FD- \_ Accept-Benachrichtigung wird übermittelt, wenn der Blattknoten die Verknüpfung mit der Multipoint-Sitzung anfordert. Die Stamm Anwendung verwendet die üblichen [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) / [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktionen, um den neuen Blattknoten zuzulassen. Der von **Accept** oder **wsaaccept** zurückgegebene Wert ist ebenfalls ein c- \_ Blatt-socketdeskriptor, genau wie die von **wsajoinleaf** zurückgegebenen Werte. Um multipointschemas zu unterstützen, die sowohl vom Stamm initiierte als auch vom Blatt initiierte Joins zulassen, ist es zulässig, dass ein c-Stamm- \_ Socket, der sich bereits im Empfangsmodus befindet, als Eingabe für **wsajoinleaf** verwendet werden kann.

Eine Multipoint-Stamm Anwendung ist in der Regel für die ordnungsgemäße Demontage einer Multipoint-Sitzung verantwortlich. Eine solche Anwendung kann [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) oder [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) für einen c-Stamm Socket verwenden, \_ um alle zugeordneten c- \_ Blatt Sockets (einschließlich der von [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) und den entsprechenden c- \_ Blatt Sockets in den Remote Blattknoten) zu verwenden, um die Benachrichtigung zum Schließen von FD zu erhalten \_ .

 

 



