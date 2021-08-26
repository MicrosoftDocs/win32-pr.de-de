---
title: Angehaltene Zustände
description: Während eines Verbindungsvorgangs kann es zu Zeiten kommen, in denen der Remoteserver ohne zusätzliche Informationen des lokalen Benutzers nicht fortgesetzt werden kann.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec66a63adbee524ec231b5c9dd9b0b410c8f4fbc73746ae9b924294c680b4a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029140"
---
# <a name="paused-states"></a>Angehaltene Zustände

Während eines Verbindungsvorgangs kann es zu Zeiten kommen, in denen der Remoteserver ohne zusätzliche Informationen des lokalen Benutzers nicht fortgesetzt werden kann. Ab Windows NT 3.5 unterstützt die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) angehaltene Zustände. Ein angehaltener Zustand ermöglicht dem Remotezugriffs-Verbindungs-Manager, einen Verbindungsvorgang anzuhalten, damit die RAS-Clientanwendung Informationen vom Benutzer sammeln kann.

Angehaltene Zustände sind in den folgenden Situationen nützlich:

-   Wenn der Benutzer eine [Rückrufnummer](callback-connections.md) angeben muss.
-   Wenn die Benutzerauthentifizierung fehlschlägt, kann der Benutzer einen anderen Benutzernamen und ein anderes Kennwort eingeben.
-   Wenn das Kennwort des Benutzers abgelaufen ist, kann der Benutzer ein neues Kennwort angeben.

Standardmäßig ist die Unterstützung für angehaltene Zustände deaktiviert. RAS-Clients, die angehaltene Zustände unterstützen möchten, müssen das RDEOPTS \_ PausedStates-Flag in der [**RASDIALEXTENSIONS-Struktur**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) festlegen, das als Parameter an [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)übergeben wird.

Wenn ein angehaltener Zustand auftritt, ruft die Remotezugriffs-Verbindungs-Manager den Benachrichtigungshandler des Clients auf. Wenn die Unterstützung für den angehaltenen Zustand deaktiviert ist, wird in der Benachrichtigung ein Fehler angezeigt, und der Verbindungsvorgang schlägt fehl. Wenn sie aktiviert ist, hält der Verbindungs-Manager den Verbindungsvorgang an, um auf die Antwort des RAS-Clients zu warten. Der RAS-Client kann den Verbindungsvorgang durch einen zweiten [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) fortsetzen oder durch Aufrufen der [**RasHangUp-Funktion**](/windows/desktop/api/Ras/nf-ras-rashangupa) beenden.

Nach dem Abrufen der Benutzereingabe startet der RAS-Client den Verbindungsvorgang neu, indem [**er RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) erneut aufruft. Dieser zweite **RasDial-Aufruf** muss die folgenden Informationen angeben:

-   Das Verbindungshandle, das vom ursprünglichen [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) zurückgegeben wurde.
-   Der gleiche Benachrichtigungshandler wie der ursprüngliche [**RasDial-Aufruf.**](/windows/desktop/api/Ras/nf-ras-rasdiala)
-   Die Eingabe des Benutzers in den entsprechenden Membern der [**RASDIALPARAMS-Struktur.**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) Andere Member der **RASDIALPARAMS-Struktur** sollten die gleichen Informationen wie im ursprünglichen [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) angegeben haben.

Der zweite [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) kann nicht innerhalb des Benachrichtigungshandlers erfolgen.

 

 