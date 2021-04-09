---
title: Server-Side Protokollierung
description: Die serverseitige Protokollierung ist in einer URL-Gruppe oder Server Sitzung verfügbar.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856492"
---
# <a name="server-side-logging"></a>Server-Side Protokollierung

Die serverseitige Protokollierung ist in einer URL-Gruppe oder Server Sitzung verfügbar. Wenn die Protokollierung für eine Server Sitzung aktiviert ist, fungiert sie als zentralisierte Form der Protokollierung für alle URL-Gruppen in der Server Sitzung. Wenn die Protokollierung für eine URL-Gruppe aktiviert ist, wird die Protokollierung nur bei Anforderungen ausgeführt, die an die URL-Gruppe weitergeleitet werden. Die folgenden Protokollierungs Typen werden von der HTTP-Server-API unterstützt:

-   [W3C-Protokollierung](w3c-logging.md): verfügbar in der Server Sitzung und der URL-Gruppe.
-   [NCSA-Protokollierung](ncsa-logging.md): verfügbar in der URL-Gruppe.
-   [IIS-Protokollierung](iis-logging.md): verfügbar in der URL-Gruppe.
-   [Zentralisierte binäre Protokollierung](centralized-binary-logging.md): verfügbar in der Server Sitzung.

Um das http-Protokollierungs Feature nutzen zu können, aktiviert und konfiguriert die Anwendung einen Protokollierungstyp für die Server Sitzung oder URL-Gruppe. Weitere Informationen finden Sie unter [Konfigurieren und Aktivieren der Server seitigen Protokollierung](configuring-and-enabling-server-side-logging.md) .

 

 




