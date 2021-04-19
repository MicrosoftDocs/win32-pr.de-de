---
description: Unterschiede zwischen regulären Punkt-zu-Punkt-Sockets und c-Stamm- \_ Multipoint-Sockets im SPI von Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345247"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets in der SPI

Auf der Steuerungsebene gibt es einige bedeutende semantische Unterschiede zwischen einem c \_ -root-Socket und einem regulären Punkt-zu-Punkt-Socket:

-   Der c-Stamm \_ Socket kann in [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) verwendet werden, um einem neuen Blatt beizutreten.
-   Durch das Platzieren eines c-Stamm \_ Sockets in den Empfangsmodus (durch Aufrufen von [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) wird nicht verhindert, dass der c-Stamm \_ Socket in einem Aufruf von [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zum Hinzufügen eines neuen Blatts oder zum Senden und empfangen von Multipoint-Daten verwendet wird.
-   Das Schließen eines c-Stamm \_ Sockets bewirkt, dass alle zugeordneten c- \_ Blatt Sockets eine Benachrichtigung über eine schließende FD erhalten \_ .

Es gibt keine semantischen Unterschiede zwischen einem c \_ -Blatt Socket und einem regulären Socket in der Steuerungsebene, mit dem Unterschied, dass der c \_ -Blatt Socket in [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)verwendet werden kann und die Verwendung des c- \_ Blatt Sockets in [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) anzeigt, dass nur Multipoint-Verbindungsanforderungen akzeptiert werden sollen.

In der Datenebene sind die semantischen Unterschiede zwischen dem d- \_ stammsocket und einem regulären Punkt-zu-Punkt-Socket

-   Die Daten, die auf dem d-Stamm Socket gesendet werden \_ , werden an alle Blätter in derselben Multipoint-Sitzung übermittelt.
-   Die im Stamm-Socket von d empfangenen Daten \_ können von einem der Blätter stammen.

Der d- \_ Blatt Socket in der Datenebene "Rooting" hat keinen semantischen Unterschied vom regulären Socket, aber in der Datenebene ohne Stamm werden die Daten, die auf dem d- \_ Blatt Socket gesendet werden, an alle anderen Endknoten gesendet, und die empfangenen Daten können von einem beliebigen anderen Blattknoten stammen. Wie bereits erwähnt, sind die Informationen darüber, ob der d- \_ Blatt Socket sich in einer Datenebene befindet, die sich in einem Stamm oder einem Datenblatt befindet, in der entsprechenden [**wsaprotocol \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Informationsstruktur für den Socket enthalten

 

 
