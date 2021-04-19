---
description: In den folgenden Fällen wird ein Multipoint-Socket häufig durch beschreiben seiner Rolle in einer der beiden Ebenen (Steuerelement oder Daten) bezeichnet.
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: SPI-Semantik zum beitreten von Multipoint-Blättern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0e77203e5405f6cb820baba5d545de03e3a8ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353548"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>SPI-Semantik zum beitreten von Multipoint-Blättern

In den folgenden Fällen wird ein Multipoint-Socket häufig durch beschreiben seiner Rolle in einer der beiden Ebenen (Steuerelement oder Daten) bezeichnet. Es sollte erkannt werden, dass derselbe Socket eine Rolle in der anderen Ebene aufweist, aber dies wird nicht erwähnt, um die Verweise kurz zu halten. Beispielsweise kann ein Verweis auf einen c- \_ stammsocket entweder auf einen c-Stamm \_ /d-Stamm \_ oder einen c-Stamm- \_ /d- \_ Blatt-Socket verweisen.

In den Schemas der Ebene der Steuerungsebene werden einer Multipoint-Sitzung auf zwei verschiedene Arten neue Blattknoten hinzugefügt. In der ersten Methode verwendet der Stamm [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) , um eine Verbindung mit einem Blattknoten zu initiieren und ihn zu einem Teilnehmer einzuladen. Auf dem Blattknoten muss die Peer Anwendung einen c \_ -Blatt Socket erstellt haben und [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) verwenden, um Sie in den Abhör Modus einzustellen. Der Blattknoten empfängt \_ bei Einladung zum Beitreten zur Sitzung eine FD-Annahme-Anzeige und signalisiert seine Bereitschaft, durch Aufrufen von [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)verknüpft zu werden. Die Stamm Anwendung empfängt eine FD- \_ Verbindungsanzeige, wenn der Joinvorgang abgeschlossen wurde.

In der zweiten Methode werden die Rollen im Grunde umgekehrt. Der Stamm Client erstellt einen c \_ -root-Socket und legt ihn in den Abhör Modus fest. Ein Blattknoten, der an der Sitzung teilnehmen möchte, erstellt einen c \_ -Blatt Socket und verwendet [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) , um die Verbindung zu initiieren und die Anforderung anzufordern. Der Stamm Client empfängt den FD \_ -Accept-Befehl, wenn eine eingehende Zutritt-Anforderung eingeht, und gibt den Blattknoten durch Aufrufen von [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)an. Der Blattknoten empfängt FD \_ Connect, wenn er zugelassen wurde.

In einer nicht-Stamm Steuerungsebene, bei der alle Knoten c- \_ Blätter sind, wird die [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) -Funktion verwendet, um die Einbindung eines Knotens in eine vorhandene Multipoint-Sitzung zu initiieren. Eine FD \_ -Verbindungsanzeige wird bereitgestellt, wenn der Join abgeschlossen wurde und der zurückgegebene socketdeskriptor in der Multipoint-Sitzung verwendet werden kann. Im Fall von IP-Multicast entspricht dies der IP-Option zum \_ Hinzufügen von \_ Mitgliedschafts Sockets.

Daher gibt es drei Instanzen, in denen ein Client [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)verwendet:

-   Das fungieren als Multipoint-Stamm und das Einladen eines neuen Blatts, um der Sitzung beizutreten.
-   Das fungieren als Blatt, das eine Zutritt-Anforderung an eine Stamm-Multipoint-Sitzung sendet.
-   Das fungieren als Blatt, das die Zutritt für eine nicht-Stamm Sitzung (z. b. IP-Multicast) anfordert.

 

 
