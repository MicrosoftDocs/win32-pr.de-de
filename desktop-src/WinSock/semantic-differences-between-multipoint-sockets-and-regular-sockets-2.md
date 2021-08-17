---
title: Semantische Unterschiede zwischen Multipointsockets und regulären Sockets
description: Unterschiede zwischen \_ C-Stamm-Multipointsockets und regulären Point-to-Point-Sockets.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b30ff05c72fc43bf3f4e731242d9f22a2236e9f6fd275c382b57fb05d094cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740810"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Semantische Unterschiede zwischen Multipointsockets und regulären Sockets

Auf der Steuerungsebene gibt es einige signifikante semantische Unterschiede zwischen einem c-Stammsocket und einem regulären \_ Point-to-Point-Socket:

-   Der \_ C-Stammsocket kann in [**WSAJoinLeaf verwendet**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) werden, um ein neues Blatt zu verbinden.
-   Das Platzieren eines C-Stammsocket in den Lauschmodus (durch Aufrufen von listen) schließt nicht aus, dass der C-Stammsocket in einem Aufruf von \_ [](/windows/desktop/api/Winsock2/nf-winsock2-listen) \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) verwendet wird, um ein neues Blatt hinzuzufügen, oder zum Senden und Empfangen von Multipointdaten.
-   Das Schließen eines \_ C-Stammsocket bewirkt, dass alle zugeordneten \_ C-Blattsockes eine FD \_ CLOSE-Benachrichtigung erhalten.

Es gibt keine semantischen Unterschiede zwischen einem C-Blattsocket und einem regulären Socket in der Steuerungsebene, außer dass der Blattsocket \_ c \_ in [**WSAJoinLeaf verwendet**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)werden kann, und die Verwendung von c leaf socket in listen gibt an, dass nur Multipoint-Verbindungsanforderungen akzeptiert werden \_ sollen. [](/windows/desktop/api/Winsock2/nf-winsock2-listen)

In der Datenebene sind die semantischen Unterschiede zwischen dem D-Stammsocket und einem regulären \_ Point-to-Point-Socket:

-   Die auf dem D-Stammsocket gesendeten \_ Daten werden an alle Blätter in derselben Multipointsitzung übermittelt.
-   Die auf dem \_ D-Stammsocket empfangenen Daten können aus einem der Blätter kommen.

Der Blattsocket auf der Datenebene mit Stamm hat keinen semantischen Unterschied zum regulären Socket. Auf der nicht entfernten Datenebene werden die auf dem Blattsocket gesendeten Daten jedoch an alle anderen Blattknoten gesendet, und die empfangenen Daten können von anderen Blattknoten \_ \_ sein. Wie bereits erwähnt, sind die Informationen darüber, ob sich der Blattsocket auf einer Stamm- oder Nicht-Stammdatenebene befindet, in der entsprechenden \_ [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den Socket enthalten.

 

 
