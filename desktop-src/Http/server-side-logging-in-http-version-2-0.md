---
title: Server-Side Protokollierung
description: Die serverseitige Protokollierung ist für eine URL-Gruppe oder Serversitzung verfügbar.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8caf7475fe6d2b408f6e2a1f924bad73df64c315ef5e0acd1c7c317ce5eac6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829840"
---
# <a name="server-side-logging"></a>Server-Side Protokollierung

Die serverseitige Protokollierung ist für eine URL-Gruppe oder Serversitzung verfügbar. Wenn die Protokollierung in einer Serversitzung aktiviert ist, fungiert sie als zentralisierte Form der Protokollierung für alle URL-Gruppen unter der Serversitzung. Wenn die Protokollierung für eine URL-Gruppe aktiviert ist, erfolgt die Protokollierung nur für Anforderungen, die an die URL-Gruppe geroutet werden. Die folgenden Protokollierungstypen werden von der HTTP-Server-API unterstützt:

-   [W3C-Protokollierung:](w3c-logging.md)Verfügbar in der Serversitzung und URL-Gruppe.
-   [NCSA-Protokollierung:](ncsa-logging.md)Verfügbar in der URL-Gruppe.
-   [IIS-Protokollierung:](iis-logging.md)Verfügbar in der URL-Gruppe.
-   [Zentralisierte binäre Protokollierung:](centralized-binary-logging.md)Verfügbar in der Serversitzung.

Um das HTTP-Protokollierungsfeature zu nutzen, aktiviert und konfiguriert die Anwendung einen Protokollierungstyp für die Serversitzung oder URL-Gruppe. Weitere Informationen finden Sie unter [Konfigurieren und Aktivieren der serverseitigen Protokollierung.](configuring-and-enabling-server-side-logging.md)

 

 




