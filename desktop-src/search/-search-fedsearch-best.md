---
description: In diesem Thema werden die bewährten Methoden aufgeführt, mit denen Sie einen webbasierten Datenspeicher erstellen können, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und Ihre Remote Datenquellen mit Windows-Explorer integrieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Bewährte Methoden bei der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128576"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Bewährte Methoden bei der Windows-Verbund Suche

In diesem Thema werden die bewährten Methoden aufgeführt, mit denen Sie einen webbasierten Datenspeicher erstellen können, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und Ihre Remote Datenquellen mit Windows-Explorer integrieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.

Dieses Thema ist wie folgt organisiert:

-   [Bewährte Methoden für die Windows-Verbund Suche](#best-practices-for-windows-federated-search)
-   [Bewährte Methoden zum Erstellen von RSS-Ausgaben](#best-practices-for-creating-rss-output)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Bewährte Methoden für die Windows-Verbund Suche

Die bewährten Methoden für die Arbeit mit [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 lauten wie folgt:

-   Unterstützen Sie die Parameter " *{startIndex}* " und " *{count}* ", und geben Sie die Anzahl der angeforderten Elemente immer zurück, es sei denn, Sie geben die letzten Ergebnisse zurück.
-   Wenn Sie die Dateinamenerweiterung kennen, ordnen Sie Sie der Windows Shell-Eigenschaft [System. FileExtension](../properties/props-system-fileextension.md) zu. Die Verwendung von Dateinamen Erweiterungen ist eine bessere Möglichkeit, einen Dateityp als MIME-Typ zu identifizieren.
-   Stellen Sie sicher, dass der MIME-Typ oder die Dateinamenerweiterung, die Sie in der RSS angeben, mit dem Dateinamen und dem MIME-Typ übereinstimmt, der vom Webserver, der das Element hostet, wenn der Element Inhalt angefordert wird
-   Wenn Sie Dateielemente zurückgeben, sollten Sie nach Möglichkeit eine Dateigröße zurückgeben. Dadurch wird sichergestellt, dass das Dialogfeld Download Fortschritt korrekt ist.
-   Stellen Sie sicher, dass Anforderungen für Elemente hinter dem Ende des Resultsets keine Ergebnisse zurückgeben.
    > [!Note]  
    > Die Ergebnisse werden nicht wiederholt.

     

-   Fügen Sie keine HTML-Tags an, die nicht zu gehören. Gemäß der RSS-Spezifikation sind Sie im Beschreibungsfeld gültig, aber nicht im Feld "Title".
-   Erstellen Sie keine Gehäuse für Webseiten Elemente. Wenn Sie z. b. ein Gehäuse erstellen und die Dateinamenerweiterung ". aspx" zuordnen, wird die Datei vom Windows-Explorer in den Internet Cache heruntergeladen und von dort aus ausgeführt. Webbrowser verarbeiten den ASPX-Dateityp nicht. Der Benutzer erhält ein Dialogfeld " **Öffnen mit** ", oder die Datei wird möglicherweise von einer Anwendung wie Microsoft Visual Studio geöffnet. Vermeiden Sie dies, indem Sie ein Link Element nur für Webseiten zurückgeben.
-   Geben Sie mithilfe einer URL-Vorlage mit eine webrollenurl in der OSDX-Datei an `format="text\html"` .
-   Geben Sie eine URL für den übergeordneten Ordner, den Container oder die Webseite an, indem Sie der Eigenschaft [System. itemfolderpathdisplay](../properties/props-system-itempathdisplay.md) der Windows-Shell den Wert einer benutzerdefinierten Element-URL zuordnet.

## <a name="best-practices-for-creating-rss-output"></a>Bewährte Methoden zum Erstellen von RSS-Ausgaben

Es folgen die bewährten Methoden für das Erstellen von RSS-Ausgaben:

-   Jedes Element muss eine URL oder einen Wert zurückgeben `link` `enclosure` (oder äquivalent, z. b. `media:content` ).
-   Fügen Sie keine HTML-Formatierungs Tags in das **Title** -Attribut ein, oder diese Tags werden im Titel angezeigt und im Windows-Explorer angezeigt.
-   Für das **Description** -Element:
    -   Zeigen Sie genügend Informationen an, damit der Benutzer weiß, warum dieses Ergebnis relevant sein könnte.
    -   HTML-Formatierung nicht einschließen. Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter entfernt die Formatierung, was möglicherweise zu weniger als wünschenswerten für Ihre Beschreibung führt.
    -   Fügen Sie keine Metadaten ein, die bereits in anderen Elementen enthalten sind, wie z. b. den Dateinamen des Gehäuses, die Größe, das Änderungsdatum usw., da Windows Explorer die Metadaten bereits anzeigt. Die Anzeige im **Description** -Element wäre redundant.
-   Für Gehäuse-oder Inhalts-URLs:
    -   Geben Sie das Type-Attribut als gültigen MIME-Typ an.
    -   Geben Sie die Dateigröße in Bytes an.
-   Wenn Sie die RSS-Ausgabe in .NET mithilfe von implementieren `DateTime` , testen Sie Ihren Feed in Microsoft Internet Explorer, um zu überprüfen, ob er gültig ist, bevor Sie ihn in Windows Explorer bereitstellen.

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

[Bereitstellen von Suchconnectors in der Windows-Verbund Suche](-search-federated-search-deploying.md)
</dt> <dt>

[Erweitern des Indexes](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
