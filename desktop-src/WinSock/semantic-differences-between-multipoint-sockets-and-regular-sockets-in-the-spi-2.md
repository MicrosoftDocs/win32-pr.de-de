---
description: Unterschiede zwischen regulären Point-to-Point-Sockets und c-Stamm-Multipointsockes in Windows \_ Sockets (Winsock) SPI.
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Semantische Unterschiede zwischen Multipointsockets und regulären Sockets in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e585c335d7503d884d58e25b6fc0ad6dd0c0c3356064ebb1504898770d4b7b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740608"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Semantische Unterschiede zwischen Multipointsockets und regulären Sockets in der SPI

Auf der Steuerungsebene gibt es einige signifikante semantische Unterschiede zwischen einem c-Stammsocket und einem regulären \_ Point-to-Point-Socket:

-   Der \_ C-Stammsocket kann in [**WSPJoinLeaf verwendet**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) werden, um ein neues Blatt zu verbinden.
-   Das Platzieren eines c-Stammsocket in den Lauschmodus (durch Aufrufen von WSPListen) schließt nicht aus, dass der C-Stammsocket in einem Aufruf von \_ [](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zum Hinzufügen eines neuen Blatts oder zum Senden und Empfangen von Multipointdaten verwendet wird.
-   Das Schließen eines \_ C-Stammsockets verursacht, dass alle zugeordneten \_ C-Blattsockes eine FD \_ CLOSE-Benachrichtigung erhalten.

Es gibt keine semantischen Unterschiede zwischen einem C-Blattsocket und einem regulären Socket in der Steuerungsebene, außer dass der Blattsocket \_ c \_ in [**WSPJoinLeaf verwendet werden**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)kann, und die Verwendung von c leaf socket in \_ [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) gibt an, dass nur Multipoint-Verbindungsanforderungen akzeptiert werden sollten.

In der Datenebene sind die semantischen Unterschiede zwischen dem D-Stammsocket und einem regulären \_ Point-to-Point-Socket:

-   Die auf dem Stammsocket d gesendeten Daten werden an alle Blätter \_ in derselben Multipointsitzung übermittelt.
-   Die auf dem \_ D-Stammsocket empfangenen Daten können aus einem der Blätter kommen.

Der Blattsocket auf der Datenebene mit Stamm hat keinen semantischen Unterschied zum regulären Socket. Auf der nicht entfernten Datenebene werden die auf dem Blattsocket gesendeten Daten jedoch an alle anderen Blattknoten gesendet, und die empfangenen Daten können von einem der anderen Blattknoten \_ \_ sein. Wie bereits erwähnt, sind die Informationen darüber, ob sich der Blattsocket auf einer Stamm- oder Nicht-Stammdatenebene befindet, in der entsprechenden \_ [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den Socket enthalten.

 

 
