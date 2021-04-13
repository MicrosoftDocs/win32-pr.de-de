---
description: In diesem Thema wird erläutert, wie ein Benutzer einen neuen Remote Datenspeicher bei der Verbund-Suche registriert, indem er eine OpenSearch-Beschreibungsdatei (OSDX-Datei) öffnet, eine OSDX-Datei bereitstellt und die Verwendung des OpenSearch-Dienstanbieter nachverfolgt.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Bereitstellen von Suchconnectors in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484438"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Bereitstellen von Suchconnectors in der Windows-Verbund Suche

In diesem Thema wird erläutert, wie ein Benutzer einen neuen Remote Datenspeicher bei der Verbund-Suche registriert, indem er eine OpenSearch-Beschreibungsdatei (OSDX-Datei) öffnet, eine OSDX-Datei bereitstellt und die Verwendung des [OpenSearch](https://github.com/dewitt/opensearch) -Dienstanbieter nachverfolgt.

Dieses Thema ist wie folgt organisiert:

-   [Die Suchconnector-MS-Datei (Suchconnector)](#the-searchconnector-ms-search-connector-file)
-   [Bereitstellungs Methoden](#deployment-methods)
    -   [Pull-Bereitstellung](#pull-deployment)
    -   [Pushbereitstellung](#push-deployment)
-   [Nachverfolgung der Verwendung](#tracking-usage)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>Die Suchconnector-MS-Datei (Suchconnector)

Wenn Sie lediglich die OSDX-Datei öffnen, die beschreibt, wie Sie eine Verbindung mit dem Webdienst herstellen und benutzerdefinierte Elemente in ihrer RSS-oder Atom-XML-Datei zuordnen, wird der neue Remote Datenspeicher bei der Verbund Suche registriert. Ein Datenspeicher, der bereits über einen [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst verfügt, der mit der Verbund Suche kompatibel ist, kann Windows-Explorer hinzugefügt werden, wenn ein Benutzer eine OSDX-Datei öffnet.

Nachdem Sie die OSDX-Datei an den Benutzer übergeben haben und der Benutzer die OSDX-Datei öffnet, treten die folgenden Ereignisse auf.

1.  Eine searchconnector-MS-Datei wird im Ordner **Windows-Such** Vorgänge (% User Profile%/searches) erstellt.
2.  Eine Verknüpfung mit der Datei. searchconnector-MS wird im Ordner **Verknüpfungen** erstellt (% User Profile%/links).
3.  Im Windows Explorer-Navigations **Favoriten** Bereich wird eine Verknüpfung angezeigt, sodass der Benutzer in den neuen Datenspeicher navigieren und den Webdienst Abfragen kann.

## <a name="deployment-methods"></a>Bereitstellungsmethoden

Es gibt zwei Möglichkeiten zum Bereitstellen von Suchconnectors, der Pull-Bereitstellung und der pushbereitstellung.

### <a name="pull-deployment"></a>Pull-Bereitstellung

Bei der Pull-Bereitstellung werden alle Bereitstellungs Arten beschrieben, bei denen der Endbenutzer die Initiative zum Installieren der Suchconnectors übernimmt. Gängige Methoden der Pull-Bereitstellung sind:

-   Anfügen der OSDX-Datei in eine e-Mail.
-   Veröffentlichen der Datei auf einer Webseite.
-   Bereitstellen eines dynamischen Links auf der Intranetsite Beispielsweise wird eine benutzerdefinierte OSDX-Datei erstellt, die auf der Benutzer Auswahl oder dem aktuellen Bereich innerhalb des Standorts basiert.

Damit die Datei heruntergeladen wird, wenn der Benutzer in Ihrem Browser auf den Link klickt, muss der Webserver, auf dem der Webdienst gehostet wird, so konfiguriert werden, dass die OSDX-Datei als Datei bereitstellt wird. Daher müssen Sie die MIME-Typen auf dem Webserver so konfigurieren, dass OSDX-Dateien als behandelt werden `"application/opensearchdescription+xml"` . Optional können Sie das von Microsoft bereitgestellte Symbol zum Identifizieren des Suchconnector-Links verwenden.

### <a name="push-deployment"></a>Pushbereitstellung

Pushbereitstellung beschreibt jede Art von Bereitstellung, die nicht von der Benutzer Initiative abhängt, um die Suchconnectors zu installieren. Häufige Methoden der pushbereitstellung sind:

-   Gruppenrichtlinie Einstellungen (GPP)
-   Anmeldeskript
-   Roamingprofile
-   Bildverarbeitung

## <a name="tracking-usage"></a>Nachverfolgung der Verwendung

Um die Verwendung des [OpenSearch](https://github.com/dewitt/opensearch) -Diensts durch Benutzer zu verfolgen, die im Windows-Explorer suchen, Filtern Sie die Webserver-Protokolldateien für diese Benutzer-Agent-Zeichenfolge: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Ersten Einstieg in die Verbund Suche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Verbinden des Webdiensts in der Windows-Verbund Suche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden bei der Windows-Verbund Suche](-search-fedsearch-best.md)
</dt> </dl>

 

 
