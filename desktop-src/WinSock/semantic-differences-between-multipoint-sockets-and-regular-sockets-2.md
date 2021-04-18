---
title: Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets
description: Unterschiede zwischen c \_ -Stamm-Multipoint-Sockets und regulären Punkt-zu-Punkt-Sockets.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343822"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets

Auf der Steuerungsebene gibt es einige bedeutende semantische Unterschiede zwischen einem c \_ -root-Socket und einem regulären Punkt-zu-Punkt-Socket:

-   Der c-Stamm \_ Socket kann in [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) verwendet werden, um ein neues Blatt zu verknüpfen.
-   Das Platzieren eines c-Stamm \_ Sockets in den Empfangsmodus (durch Aufrufen von " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)") verhindert nicht, dass der c-Stamm \_ Socket in einem Aufruf von [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) zum Hinzufügen eines neuen Blatts oder zum Senden und empfangen von Multipoint-Daten verwendet wird.
-   Das Schließen eines c-Stamm \_ Sockets bewirkt, dass alle zugeordneten c- \_ Blatt Sockets eine Benachrichtigung über eine schließende FD erhalten \_ .

Es gibt keine semantischen Unterschiede zwischen einem c \_ -Blatt Socket und einem regulären Socket in der Steuerungsebene, mit dem Unterschied, dass der c \_ -Blatt Socket in [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)verwendet werden kann und die Verwendung des c- \_ Blatt Sockets in " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " anzeigt, dass nur Multipoint-Verbindungsanforderungen akzeptiert werden sollen.

In der Datenebene sind die semantischen Unterschiede zwischen dem d- \_ stammsocket und einem regulären Punkt-zu-Punkt-Socket:

-   Die Daten, die auf dem d-Stamm Socket gesendet werden \_ , werden an alle Blätter in derselben Multipoint-Sitzung übermittelt.
-   Die im Stamm-Socket von d empfangenen Daten \_ können von einem der Blätter stammen.

Der d- \_ Blatt Socket in der Datenebene für das Stammverzeichnis weist keinen semantischen Unterschied vom regulären Socket auf, aber in der Datenebene, die keine Daten enthält, werden die Daten, die auf dem d-Blatt Socket gesendet werden, \_ an alle anderen Endknoten gesendet, und die empfangenen Daten können von beliebigen anderen Endknoten stammen. Wie bereits erwähnt, sind die Informationen darüber, ob der d- \_ Blatt Socket sich in einer Datenebene befindet, die sich in einem Stamm oder einem Datenblatt befindet, in der entsprechenden [**wsaprotocol \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Informationsstruktur für den Socket enthalten

 

 
