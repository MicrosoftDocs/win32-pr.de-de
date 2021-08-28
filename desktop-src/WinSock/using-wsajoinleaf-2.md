---
description: Wie bereits erwähnt, wird die WSAJoinLeaf-Funktion verwendet, um einen Blattknoten in eine Multipointsitzung zu verbinden.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Verwenden von WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13b6d82960f74135fa519a1284a1274b878e18c32f59d9c2b8c46ebd592c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121020"
---
# <a name="using-wsajoinleaf"></a>Verwenden von WSAJoinLeaf

Wie bereits erwähnt, wird die [**WSAJoinLeaf-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) verwendet, um einen Blattknoten in eine Multipointsitzung zu verbinden. **WSAJoinLeaf** verfügt über die gleichen Parameter und Semantik wie [**WSAConnect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) gibt jedoch einen Socketdeskriptor zurück (wie in [**WSAAccept),**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)und es verfügt über einen zusätzlichen *dwFlags-Parameter.*

Der *dwFlags-Parameter* wird verwendet, um anzugeben, ob der Socket nur als Absender, nur als Empfänger oder beides dient. In dieser Funktion können nur Multipointsockets für *Eingabeparameter* verwendet werden. Wenn sich der Multipointsocket im Nichtblockierungsmodus befindet, kann der zurückgegebene Socketdeskriptor erst verwendet werden, nachdem eine entsprechende FD \_ CONNECT-Angabe empfangen wurde. Eine Stammanwendung in einer Multipointsitzung kann [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) ein oder mehrere Male aufrufen, um eine Reihe von Blattknoten hinzuzufügen. Es kann jedoch immer nur eine Mehrpunktverbindungsanforderung gleichzeitig ausstehen.

Der von [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) zurückgegebene Socketdeskriptor unterscheidet sich je nachdem, ob der Eingabesocketdeskriptor *s* ein C-Stamm oder ein \_ \_ C-Blatt ist. Bei Verwendung mit einem c-Stammsocket bestimmt der Name-Parameter einen bestimmten Blattknoten, der hinzugefügt werden soll, und der zurückgegebene Socketdeskriptor ist ein C-Blattsocket, der dem neu hinzugefügten Blattknoten \_  \_ entspricht. Sie ist nicht für den Austausch von Multipointdaten vorgesehen, sondern wird zum Empfangen von FD XXX-Hinweisen (z. B. FD CLOSE) für die Verbindung verwendet, die mit dem bestimmten Blatt c vorhanden \_ \_ \_ ist. Einige Multipointimplementierungen ermöglichen möglicherweise auch die Verwendung dieses Sockets für Seitenchats zwischen dem Stammknoten und einem einzelnen Blattknoten. Für diesen Socket wird eine FD CLOSE-Angabe empfangen, wenn der entsprechende Blattknoten \_ [**closesocket aufruft,**](/windows/desktop/api/winsock/nf-winsock-closesocket) um die Multipointsitzung zu beenden. Symmetrisch bewirkt der Aufruf von **closesocket** auf dem von WSAJoinLeaf zurückgegebenen Blattsocket, dass der Socket im entsprechenden Blattknoten eine \_ FD CLOSE-Benachrichtigung  \_ aufruft.

Wenn [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) mit einem C-Blattsocket aufgerufen wird, enthält der Name-Parameter die Adresse der Stammanwendung (für ein Root-Steuerelementschema) oder einer vorhandenen Multipointsitzung (Schema für nichtstammige Steuerung), und der zurückgegebene Socketdeskriptor ist mit dem Eingabesocketdeskriptor \_ identisch.  In einem Root-Steuerelementschema versetzt die Stammanwendung ihren c-Stammsocket in den \_ Lauschenmodus, indem sie [**listen aufruft.**](/windows/desktop/api/Winsock2/nf-winsock2-listen) Die standardmäßige FD ACCEPT-Benachrichtigung wird übermittelt, wenn der Blattknoten anfängt, \_ sich selbst mit der Multipointsitzung zu verbinden. Die Stammanwendung verwendet [](/windows/desktop/api/Winsock2/nf-winsock2-accept)die üblichen / [**Accept-WSAAccept-Funktionen,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) um den neuen Blattknoten zu übernehmen. Der von accept  oder **WSAAccept** zurückgegebene Wert ist ebenso wie der von WSAJoinLeaf zurückgegebene C-Blattsocketdeskriptor. \_  Um Multipointschemas zu unterstützen, die sowohl vom Stamm als auch vom Blatt initiierte Joins zulassen, ist es akzeptabel, dass ein C-Stammsocket, der sich bereits im Lauschmodus befindet, als Eingabe für \_ **WSAJoinLeaf verwendet wird.**

Eine Multipoint-Stammanwendung ist im Allgemeinen für die geordnete Auflösung einer Multipointsitzung verantwortlich. Eine solche Anwendung [](/windows/desktop/api/winsock/nf-winsock-shutdown) kann shutdown oder [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) auf einem c-Stammsocket verwenden, um alle zugeordneten C-Blattsockets, einschließlich der von \_ \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) zurückgegebenen Sockets und der entsprechenden c-Blattsockets in den Remoteblattknoten, zu verursachen, um eine FD CLOSE-Benachrichtigung zu \_ \_ erhalten.

 

 



