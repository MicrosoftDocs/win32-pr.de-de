---
description: In diesem Thema werden die Schritte zum Verbinden eines Webdiensts zwischen Ihrem Datenspeicher und Windows Federated Search beschrieben, und es wird beschrieben, wie Abfragen gesendet und Suchergebnisse in RSS oder Atom zurückgeben werden.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Verbinden Ihres Webdiensts in Windows Verbundsuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4980b2d62f766806cf89856b8ef9e5231284be0dfea3258d2e5d5155e7a46598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456720"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Verbinden Ihres Webdiensts in Windows Verbundsuche

In diesem Thema werden die Schritte zum Verbinden eines Webdiensts zwischen Ihrem Datenspeicher und Windows Federated Search beschrieben, und es wird beschrieben, wie Abfragen gesendet und Suchergebnisse in RSS oder Atom zurückgeben werden.

Dieses Thema ist wie folgt organisiert:

-   [Verbinden Ihr Webdienst](#connect-your-web-service)
-   [Registrieren eines vorhandenen Remotedaten-Store](#register-an-existing-remote-data-store)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="connect-your-web-service"></a>Verbinden Ihr Webdienst

**Führen Sie die folgenden Schritte aus, um den Webdienst Ihres Datenspeichers mit der Verbundsuche zu verbinden:**

1.  Erstellen Sie eine OSDX-Datei.
2.  Stellen Sie die OSDX-Datei für Benutzer zur Verfügung, damit sie den Dienst bei Bedarf hinzufügen können, indem Sie die OSDX-Datei öffnen.
3.  Generieren Sie einen Suchconnector, und stellen Sie ihn aktiv in Ihrem Unternehmen zur Anwendung.

## <a name="register-an-existing-remote-data-store"></a>Registrieren eines vorhandenen Remotedaten-Store

Ein Benutzer registriert einen neuen Remotedatenspeicher bei Windows Verbundsuche, indem er eine Datei OpenSearch Description (.osdx) öffnet. Wenn der Benutzer dies tut, treten die folgenden Ereignisse auf:

1.  Eine SEARCHCONNECTOR-MS-Datei (Suchconnector) wird im Ordner Windows Search (%userprofile%/Searches) erstellt.
2.  Eine Verknüpfung zur Datei .searchconnector-ms wird im Ordner Links (%userprofile%/Links) erstellt.
3.  Im Navigationsfavoritenbereich Windows  Explorer wird eine Verknüpfung angezeigt, mit der der Benutzer zum neuen Datenspeicher navigieren und den Webdienst abfragen kann.

> [!Note]  
> Ein Datenspeicher, der bereits über einen [OpenSearch-Webdienst](https://github.com/dewitt/opensearch) verfügt, der mit Windows Federated Search kompatibel ist, kann dem Windows-Explorer hinzugefügt werden, wenn ein Benutzer eine OSDX-Datei öffnet.

 

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren des Suchverbunds in Remotedatenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "Zusätzliche Ressourcen" unter Verbundsuche [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Erste Schritte mit Der Verbundsuche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Aktivieren Ihrer Store in Windows Verbundsuche](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden für die Windows Verbundsuche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in Windows Verbundsuche](-search-federated-search-deploying.md)
</dt> </dl>

 

 
