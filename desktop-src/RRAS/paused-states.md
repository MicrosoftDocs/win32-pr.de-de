---
title: Angehaltene Zustände
description: Bei einem Verbindungsvorgang kann es vorkommen, dass der Remote Server ohne zusätzliche Informationen vom lokalen Benutzer nicht fortfahren kann.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914acb85ccf74c92b4bd4119966a421faddeb011
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316322"
---
# <a name="paused-states"></a>Angehaltene Zustände

Bei einem Verbindungsvorgang kann es vorkommen, dass der Remote Server ohne zusätzliche Informationen vom lokalen Benutzer nicht fortfahren kann. Ab Windows NT 3,5 unterstützt die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " angehaltene Zustände. Mit einem angehaltenen Status kann der RAS-Verbindungs-Manager einen Verbindungsvorgang anhalten, sodass die RAS-Client Anwendung Informationen vom Benutzer sammeln kann.

Angehaltene Zustände sind in den folgenden Situationen nützlich:

-   Wenn der Benutzer eine [Rückruf](callback-connections.md) Nummer angeben muss.
-   Wenn die Benutzerauthentifizierung fehlschlägt, kann der Benutzer einen anderen Benutzernamen und ein anderes Kennwort eingeben.
-   Wenn das Kennwort des Benutzers abgelaufen ist, kann der Benutzer ein neues Kennwort angeben.

Standardmäßig ist die Unterstützung des angehaltenen Zustands deaktiviert. RAS-Clients, von denen angehaltene Zustände unterstützt werden sollen, müssen das Flag "rdeopts \_ pausedstates" in der " [**rasdialextensions**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) "-Struktur festlegen, die als Parameter an " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Wenn ein angehaltene Status auftritt, ruft der RAS-Verbindungs-Manager den Benachrichtigungs Handler des Clients auf. Wenn die Unterstützung für angehaltene Zustände deaktiviert ist, weist die Benachrichtigungs Meldung auf einen Fehler hin, und der Verbindungsvorgang schlägt fehl. Wenn Sie aktiviert ist, hält der Verbindungs-Manager den Verbindungsvorgang an, um auf die Antwort des RAS-Clients zu warten. Der RAS-Client kann den Verbindungsvorgang mit einem zweiten Abruf Vorgang fortsetzen oder ihn beenden, indem er die [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) - [**Funktion aufruft.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Nachdem Sie die Eingabe des Benutzers erhalten haben, startet der RAS-Client den Verbindungsvorgang durch erneutes Aufrufen von " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " neu. Bei diesem zweiten **rasdial** -Befehl müssen die folgenden Informationen angegeben werden:

-   Das Verbindungs Handle, das vom ursprünglichen [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl zurückgegeben wurde.
-   Derselbe Benachrichtigungs Handler wie der ursprüngliche [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl.
-   Die Eingabe des Benutzers in die entsprechenden Member der [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) -Struktur. Andere Member der **rasdialparameams** -Struktur sollten über die gleichen Informationen verfügen wie im ursprünglichen [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl angegeben.

Der zweite [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl kann nicht innerhalb des Benachrichtigungs Handlers durchgeführt werden.

 

 