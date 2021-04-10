---
description: Wie bereits erwähnt, wird wspjoinleaf verwendet, um einen Blattknoten in einer Multipoint-Sitzung zu verknüpfen.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Verwenden von wspjoinleaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4426c0d22657b26dcc2217d856865d9ebe98db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214583"
---
# <a name="using-wspjoinleaf"></a>Verwenden von wspjoinleaf

Wie bereits erwähnt, wird [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) verwendet, um einen Blattknoten in einer Multipoint-Sitzung zu verknüpfen. **Wspjoinleaf** hat dieselben Parameter und Semantik wie [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , mit der Ausnahme, dass ein socketdeskriptor (wie in [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) und ein zusätzlicher *dwFlags* -Parameter zurückgegeben wird. Der *dwFlags* -Parameter wird verwendet, um anzugeben, ob der Socket nur als Absender, nur als Empfänger oder beides fungiert. *In dieser* Funktion können nur Multipoint-Sockets für Eingabeparameter verwendet werden. Wenn sich der Multipoint-Socket im nicht blockierenden Modus befindet, kann der zurückgegebene socketdeskriptor erst verwendet werden, nachdem eine entsprechende FD- \_ Verbindungsanzeige empfangen wurde. Eine Stamm Anwendung in einer Multipoint-Sitzung kann **wspjoinleaf** einmal oder mehrmals aufzurufen, um eine Anzahl von Blattknoten hinzuzufügen, es kann jedoch höchstens eine Multipoint-Verbindungsanforderung gleichzeitig ausstehen.

Der von [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zurückgegebene socketdeskriptor ist unterschiedlich, je nachdem, ob der Eingabe-Socket-Deskriptor, *s*, ein c-Stamm \_ oder ein c- \_ Blatt ist. Bei Verwendung mit einem c- \_ stammsocket legt der *namens* Parameter fest, dass ein bestimmter Blattknoten hinzugefügt werden soll, und der zurückgegebene socketdeskriptor ist ein c-Blatt-Socket, der \_ dem neu hinzugefügten Blattknoten entspricht. Sie ist nicht für den Austausch von Multipoint-Daten vorgesehen, sondern wird stattdessen zum Empfangen von Netzwerk Ereignis hinweisen (z. b. "FD \_ Close") für die Verbindung verwendet, die mit dem jeweiligen c-Blatt vorhanden ist \_ . Einige Multipoint-Implementierungen können auch zulassen, dass dieser Socket für Seiten Chats zwischen dem Stamm Knoten und einem einzelnen Blattknoten verwendet wird. \_Für diesen Socket sollte ein FD-Schluss Hinweis angegeben werden, wenn der entsprechende Blattknoten [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) zum Ablegen aus der Multipoint-Sitzung aufruft. Symmetrisch bewirkt das Aufrufen von **wspclosesocket** im c- \_ Blatt Socket, das von [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zurückgegeben wird, dass der Socket im entsprechenden Blattknoten eine Benachrichtigung über den Schließvorgang von FD erhält \_ .

Wenn [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) mit einem c- \_ Blatt Socket aufgerufen wird, enthält der *Name* -Parameter die Adresse der Stamm Anwendung (für ein Stamm Steuerungs Schema) oder eine vorhandene Multipoint-Sitzung (nicht-Stamm Steuerungs Schema), und der zurückgegebene socketdeskriptor ist derselbe wie der Eingabe-socketdeskriptor. In einem Stamm Steuerungs Schema platziert der Stamm Client den c- \_ stammsocket im Empfangsmodus, indem er [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))aufruft. Die standardmäßige FD- \_ Accept-Benachrichtigung wird übermittelt, wenn der Blattknoten den Beitritt zur Multipoint-Sitzung anfordert. Der Stamm Client verwendet die übliche [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) -Funktion, um den neuen Blattknoten zuzulassen. Der von **wspaccept** zurückgegebene Wert ist ebenfalls ein c- \_ Blatt-socketdeskriptor, genau wie die von **wspjoinleaf** zurückgegebenen Werte. Um multipointschemas zu unterstützen, die sowohl vom Stamm initiierte als auch vom Blatt initiierte Joins zulassen, ist es zulässig, dass ein c-Stamm- \_ Socket, der sich bereits im Empfangsmodus befindet, als Eingabe für **wspjoinleaf** verwendet werden kann.

Ein Multipoint-Stamm Client ist im Allgemeinen für die ordnungsgemäße Demontage einer Multipoint-Sitzung verantwortlich. Eine solche Anwendung kann [**wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) oder [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) für einen c-Stamm Socket verwenden, \_ um alle zugeordneten c \_ -Blatt Sockets, einschließlich der von [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) und der entsprechenden c- \_ Blatt Sockets in den Remote Blattknoten, zu verwenden, um die Benachrichtigung zum Schließen von FD zu erhalten \_ .

 

 
