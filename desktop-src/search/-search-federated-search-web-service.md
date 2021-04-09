---
description: In diesem Thema werden die Schritte zum Verbinden eines Webdiensts zwischen dem Datenspeicher und der Windows-Verbund Suche beschrieben, und es wird beschrieben, wie Sie Abfragen senden und Suchergebnisse in RSS oder Atom zurückgeben.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Verbinden des Webdiensts in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128577"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Verbinden des Webdiensts in der Windows-Verbund Suche

In diesem Thema werden die Schritte zum Verbinden eines Webdiensts zwischen dem Datenspeicher und der Windows-Verbund Suche beschrieben, und es wird beschrieben, wie Sie Abfragen senden und Suchergebnisse in RSS oder Atom zurückgeben.

Dieses Thema ist wie folgt organisiert:

-   [Webdienst verbinden](#connect-your-web-service)
-   [Registrieren eines vorhandenen Remote Datenspeicher](#register-an-existing-remote-data-store)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="connect-your-web-service"></a>Webdienst verbinden

**Führen Sie die folgenden Schritte aus, um den Webdienst des Datenspeicher mit der Verbund Suche zu verbinden:**

1.  Erstellen Sie eine OSDX-Datei.
2.  Stellen Sie die OSDX-Datei für Benutzer bereit, damit Sie den Dienst bei Bedarf hinzufügen können, indem Sie die OSDX-Datei öffnen.
3.  Generieren Sie einen Suchconnector, und stellen Sie ihn aktiv in Ihrem Unternehmen bereit.

## <a name="register-an-existing-remote-data-store"></a>Registrieren eines vorhandenen Remote Datenspeicher

Ein Benutzer registriert einen neuen Remote Datenspeicher bei der Windows-Verbund Suche, indem er eine OpenSearch-Beschreibungsdatei (OSDX-Datei) öffnet. Wenn der Benutzer dies tut, treten die folgenden Ereignisse auf:

1.  Eine searchconnector-MS-Datei (Search-Connector) wird im Ordner Windows-Suchvorgänge (% User Profile%/searches) erstellt.
2.  Eine Verknüpfung mit der Datei. searchconnector-MS wird im Ordner Verknüpfungen erstellt (% User Profile%/links).
3.  Im Windows Explorer-Navigations **Favoriten** Bereich wird eine Verknüpfung angezeigt, die es dem Benutzer ermöglicht, in den neuen Datenspeicher zu navigieren und den Webdienst abzufragen.

> [!Note]  
> Ein Datenspeicher, der bereits über einen [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst verfügt, der mit der Windows-Verbund Suche kompatibel ist, kann Windows-Explorer hinzugefügt werden, wenn ein Benutzer eine OSDX-Datei öffnet.

 

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Ersten Einstieg in die Verbund Suche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden bei der Windows-Verbund Suche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in der Windows-Verbund Suche](-search-federated-search-deploying.md)
</dt> </dl>

 

 
