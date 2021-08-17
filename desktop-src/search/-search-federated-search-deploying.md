---
description: In diesem Thema wird erläutert, wie ein Benutzer einen neuen Remotedatenspeicher bei der Verbundsuche registriert, indem er eine osdx-Datei (OpenSearch Description) öffnet, wie eine OSDX-Datei bereitgestellt wird und wie sie die Nutzung Ihres OpenSearch-Diensts nachverfolgt.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Bereitstellen von Suchconnectors in Windows Verbundsuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7515fa905abf3767696457f30a52abdb0a36d78883e9649cb2bf42e77e8b8c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463135"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Bereitstellen von Suchconnectors in Windows Verbundsuche

In diesem Thema wird erläutert, wie ein Benutzer einen neuen Remotedatenspeicher bei der Verbundsuche registriert, indem er eine osdx-Datei (OpenSearch Description) öffnet, wie eine OSDX-Datei bereitgestellt wird und wie sie die Nutzung Ihres [OpenSearch-Diensts nachverfolgt.](https://github.com/dewitt/opensearch)

Dieses Thema ist wie folgt organisiert:

-   [Die Searchconnector-ms-Datei (Search Connector)](#the-searchconnector-ms-search-connector-file)
-   [Bereitstellungsmethoden](#deployment-methods)
    -   [Pullbereitstellung](#pull-deployment)
    -   [Pushbereitstellung](#push-deployment)
-   [Nachverfolgen der Nutzung](#tracking-usage)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>Die Searchconnector-ms-Datei (Search Connector)

Wenn Sie lediglich die OSDX-Datei öffnen, die beschreibt, wie sie eine Verbindung mit dem Webdienst herstellen und benutzerdefinierte Elemente in Rss- oder Atom-XML zuordnen, wird Ihr neuer Remotedatenspeicher bei der Verbundsuche registriert. Ein Datenspeicher, der bereits über einen [OpenSearch-Webdienst](https://github.com/dewitt/opensearch) verfügt, der mit der Verbundsuche kompatibel ist, kann dem Windows-Explorer hinzugefügt werden, wenn ein Benutzer eine OSDX-Datei öffnet.

Nachdem Sie ihrem Benutzer die OSDX-Datei angegeben haben und der Benutzer die OSDX-Datei geöffnet hat, treten die folgenden Ereignisse auf.

1.  Eine .searchconnector-ms-Datei wird im ordner Windows **Searches** (%userprofile%/Searches) erstellt.
2.  Eine Verknüpfung zur Datei .searchconnector-ms wird im Ordner **Links** (%userprofile%/Links) erstellt.
3.  Im Navigationsbereich favoriten des Windows Explorer **wird** eine Verknüpfung angezeigt, mit der der Benutzer zum neuen Datenspeicher navigieren und den Webdienst abfragen kann.

## <a name="deployment-methods"></a>Bereitstellungsmethoden

Es gibt zwei Möglichkeiten zum Bereitstellen von Suchconnectors: Pullbereitstellung und Pushbereitstellung.

### <a name="pull-deployment"></a>Pullbereitstellung

Die Pullbereitstellung beschreibt jede Art von Bereitstellung, bei der der Endbenutzer die Initiative zum Installieren der Suchconnectors übernimmt. Gängige Methoden der Pullbereitstellung sind:

-   Anfügen der OSDX-Datei in einer E-Mail.
-   Veröffentlichen der Datei auf einer Webseite.
-   Bereitstellen eines dynamischen Links auf Ihrer Intranetwebsite Beispielsweise eine , die benutzerdefinierte OSDX-Dateien basierend auf Benutzeroptionen oder dem aktuellen Bereich innerhalb der Website generiert.

Damit die Datei heruntergeladen werden kann, wenn der Benutzer in ihrem Browser auf den Link klickt, muss der Webserver, der den Webdienst hostet, so konfiguriert sein, dass die OSDX-Datei als Datei übermittelt wird. Daher müssen Sie die MIME-Typen auf dem Webserver so konfigurieren, dass OSDX-Dateien als behandelt `"application/opensearchdescription+xml"` werden. Optional können Sie das von Microsoft bereitgestellte Symbol verwenden, um den Suchconnectorlink zu identifizieren.

### <a name="push-deployment"></a>Pushbereitstellung

Bei der Pushbereitstellung wird jede Art von Bereitstellung beschrieben, die nicht von der Benutzerinitiative zum Installieren der Suchconnectors abhängig ist. Gängige Methoden für die Pushbereitstellung sind:

-   Gruppenrichtlinie Einstellungen (GPP)
-   Anmeldeskript
-   Roamingprofile
-   Bildverarbeitung

## <a name="tracking-usage"></a>Nachverfolgen der Nutzung

Um die Verwendung [](https://github.com/dewitt/opensearch) ihres OpenSearch-Diensts durch Benutzer nach Windows Explorer nachverfolgung zu können, filtern Sie die Webserverprotokolldateien nach dieser Benutzer-Agent-Zeichenfolge: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren des Suchverbunds in Remotedatenspeichern mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "Zusätzliche Ressourcen" unter [Verbundsuche in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Erste Schritte mit der Verbundsuche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Verbinden Ihres Webdiensts in Windows Verbundsuche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren ihrer Daten Store in Windows Verbundsuche](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Die folgenden bewährten Methoden in Windows Verbundsuche](-search-fedsearch-best.md)
</dt> </dl>

 

 
