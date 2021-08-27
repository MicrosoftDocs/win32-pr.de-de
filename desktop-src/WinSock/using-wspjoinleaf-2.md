---
description: Wie bereits erwähnt, wird WSPJoinLeaf verwendet, um einen Blattknoten in eine Multipointsitzung zu verbinden.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Verwenden von WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 057be0e2c1f2c3ffec21d64f3e95f6ad0ee584698e66f57cf4489ff6be887dc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121010"
---
# <a name="using-wspjoinleaf"></a>Verwenden von WSPJoinLeaf

Wie bereits erwähnt, [**wird WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) verwendet, um einen Blattknoten in eine Multipointsitzung zu verbinden. **WSPJoinLeaf** verfügt über dieselben Parameter und Semantik wie [**WSPConnect,**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) gibt jedoch einen Socketdeskriptor zurück (wie in [**WSPAccept),**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)und es verfügt über einen zusätzlichen *dwFlags-Parameter.* Der *dwFlags-Parameter* wird verwendet, um anzugeben, ob der Socket nur als Absender, nur als Empfänger oder beides dient. In dieser Funktion können nur Multipointsockets für *Eingabeparameter* verwendet werden. Wenn sich der Multipointsocket im Nichtblockierungsmodus befindet, kann der zurückgegebene Socketdeskriptor erst verwendet werden, nachdem eine entsprechende FD \_ CONNECT-Angabe empfangen wurde. Eine Stammanwendung in einer Multipointsitzung kann **WSPJoinLeaf** ein oder mehrere Male aufrufen, um eine Reihe von Blattknoten hinzuzufügen. Es kann jedoch immer nur eine Mehrpunktverbindungsanforderung gleichzeitig ausstehen.

Der von [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zurückgegebene Socketdeskriptor ist unterschiedlich, je nachdem, ob der Eingabesocketdeskriptor *s* ein C-Stamm oder ein \_ C-Blatt \_ ist. Bei Verwendung mit einem c-Stammsocket bestimmt der Name-Parameter einen bestimmten Blattknoten, der hinzugefügt werden soll, und der zurückgegebene Socketdeskriptor ist ein C-Blattsocket, der dem neu hinzugefügten Blattknoten \_  \_ entspricht. Er ist nicht für den Austausch von Multipointdaten vorgesehen, sondern wird zum Empfangen von Netzwerkereignisanzeigen (z. B. FD CLOSE) für die Verbindung verwendet, die mit dem bestimmten \_ Blatt "c" \_ vorhanden ist. Einige Multipointimplementierungen ermöglichen möglicherweise auch die Verwendung dieses Sockets für Seitenchats zwischen dem Stammknoten und einem einzelnen Blattknoten. Für diesen Socket sollte eine FD CLOSE-Angabe angegeben werden, wenn der entsprechende Blattknoten \_ [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) aufruft, um die Multipointsitzung zu beenden. Symmetrisch verursacht das Aufrufen von **WSPCloseSocket** auf dem von \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zurückgegebenen Blattsocket c, dass der Socket im entsprechenden Blattknoten eine FD CLOSE-Benachrichtigung \_ erhalten kann.

Wenn [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) mit einem Blattsocket "c" aufgerufen wird, enthält der Name-Parameter die Adresse der Stammanwendung (für ein Root-Steuerelementschema) oder einer vorhandenen Multipointsitzung (Nichtstammsteuerelementschema), und der zurückgegebene Socketdeskriptor ist mit dem Eingabesocketdeskriptor \_ identisch.  In einem Root-Steuerelementschema würde der Stammclient seinen c-Stammsocket durch Aufrufen von WSPListen in den \_ [**Lauschenmodus bringen.**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) Die standardmäßige FD ACCEPT-Benachrichtigung wird übermittelt, wenn der Blattknoten anfängt, sich \_ selbst mit der Multipointsitzung zu verbinden. Der Stammclient verwendet die übliche [**WSPAccept-Funktion,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) um den neuen Blattknoten zu begrünen. Der von **WSPAccept zurückgegebene** Wert ist ebenso wie der von \_ WSPJoinLeaf zurückgegebene C-Blattsocketdeskriptor.  Um Multipointschemas zu unterstützen, die sowohl vom Stamm als auch vom Blatt initiierte Joins zulassen, ist es akzeptabel, dass ein C-Stammsocket, der sich bereits im Lauschmodus befindet, wie in der Eingabe \_ in **WSPJoinLeaf verwendet** wird.

Ein Multipoint-Stammclient ist im Allgemeinen für die geordnete Auflösung einer Multipointsitzung verantwortlich. Eine solche Anwendung kann [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) oder [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) auf einem C-Stammsocket verwenden, um alle zugeordneten C-Blattsockets, einschließlich der von \_ \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zurückgegebenen Sockets und der entsprechenden C-Blattsockets auf den Remoteblattknoten, zu verursachen, um eine FD CLOSE-Benachrichtigung zu \_ \_ erhalten.

 

 
