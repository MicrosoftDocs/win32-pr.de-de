---
description: In diesem Thema werden die bewährten Methoden aufgeführt, mit denen Sie einen webbasierten Datenspeicher erstellen können, der mithilfe Windows Verbundsuche durchsucht werden kann. Außerdem werden Ihre Remotedatenquellen in Windows Explorer integriert, ohne Windows clientseitigen Code schreiben oder bereitstellen zu müssen.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Befolgen bewährter Methoden in Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e52d2b74f245e4ec76550cbf0a1c56b63db0a8ca6afcf9e8b736f3c7b39a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463091"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Befolgen bewährter Methoden in Windows Federated Search

In diesem Thema werden die bewährten Methoden aufgeführt, mit denen Sie einen webbasierten Datenspeicher erstellen können, der mithilfe Windows Verbundsuche durchsucht werden kann. Außerdem werden Ihre Remotedatenquellen in Windows Explorer integriert, ohne Windows clientseitigen Code schreiben oder bereitstellen zu müssen.

Dieses Thema ist wie folgt organisiert:

-   [Bewährte Methoden für Windows Federated Search](#best-practices-for-windows-federated-search)
-   [Bewährte Methoden zum Erstellen einer RSS-Ausgabe](#best-practices-for-creating-rss-output)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Bewährte Methoden für Windows Federated Search

Bewährte Methoden für die Arbeit mit [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7:

-   Unterstützen Sie die Parameter *{startIndex}* und *{count}* und achten Sie darauf, immer die Anzahl der angeforderten Elemente zurückzugeben, es sei denn, Sie geben die letzten Ergebnisse zurück.
-   Wenn Sie die Dateinamenerweiterung kennen, ordnen Sie sie der [Eigenschaft System.FileExtension](../properties/props-system-fileextension.md) Windows Shell zu. Die Verwendung von Dateinamenerweiterungen ist eine bessere Möglichkeit zum Identifizieren eines Dateityps als der MIME-Typ.
-   Stellen Sie sicher, dass der MIME-Typ oder die Dateinamenerweiterung, die Sie im RSS angeben, mit dem Dateinamen und dem MIME-Typ übereinstimmt, der im HTTP-Header vom Webserver zurückgegeben wird, der das Element hostet, wenn der Elementinhalt angefordert wird.
-   Wenn Sie Dateielemente zurückgeben, geben Sie nach Möglichkeit eine Dateigröße zurück. Dadurch wird sichergestellt, dass das Dialogfeld "Downloadfortschritt" korrekt ist.
-   Überprüfen Sie, ob Anforderungen für Elemente, die über das Ende des Resultset hinausgehen, keine Ergebnisse zurückgeben.
    > [!Note]  
    > Wiederholen Sie die Ergebnisse nicht.

     

-   Legen Sie keine HTML-Tags dort ab, wo sie nicht hin gehören. Gemäß DER RSS-Spezifikation sind sie im Beschreibungsfeld, aber nicht im Titelfeld gültig.
-   Erstellen Sie keine Gehäuse für Webseitenelemente. Wenn Sie beispielsweise ein Gehäuse erstellen und die Dateinamenerweiterung ASPX zuordnen, wird die Datei von Windows Explorer in den Internetcache heruntergeladen und von dort aus ausgeführt. Webbrowser verarbeiten den ASPX-Dateityp nicht. Der Benutzer erhält ein **Öffnen mit** Dialogfeld, oder die Datei wird von einer Anwendung wie Microsoft Visual Studio geöffnet. Vermeiden Sie dies, indem Sie ein Linkelement nur für Webseiten zurückgeben.
-   Geben Sie eine Webrollup-URL in der OSDX-Datei mithilfe einer URL-Vorlage mit `format="text\html"` an.
-   Geben Sie eine URL zum übergeordneten Ordner, Container oder zur Webseite an, indem Sie der [Eigenschaft System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell einen benutzerdefinierten Element-URL-Wert zuordnen.

## <a name="best-practices-for-creating-rss-output"></a>Bewährte Methoden zum Erstellen einer RSS-Ausgabe

Bewährte Methoden zum Erstellen einer RSS-Ausgabe:

-   Jedes Element MUSS eine URL oder einen `link` `enclosure` Wert (oder einen entsprechenden Wert, z. B. `media:content` ) zurückgeben.
-   Fügen Sie keine HTML-Formatierungstags in das **Title-Attribut** ein, da diese Tags im Titel angezeigt und im Windows-Explorer angezeigt werden.
-   Für  das description-Element:
    -   Zeigen Sie genügend Informationen an, damit der Benutzer weiß, warum dieses Ergebnis möglicherweise relevant ist.
    -   Fügen Sie keine HTML-Formatierung ein. Der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) entfernt die Formatierung, was zu weniger als wünschenswerten Ergebnissen für Ihre Beschreibung führen kann.
    -   Schließen Sie keine Metadaten ein, die bereits in anderen Elementen bereitgestellt wurden, z. B. Gehäusedateiname, Größe, Änderungsdatum usw., da Windows Explorer die Metadaten bereits anzeigt. Die Anzeige im **Description-Element** wäre redundant.
-   Für Gehäuse- oder Inhalts-URLs:
    -   Geben Sie das Typattribut als gültigen MIME-Typ an.
    -   Geben Sie die Dateigröße in Bytes an.
-   Wenn Sie die RSS-Ausgabe in .NET mit `DateTime` implementieren, testen Sie Ihren Feed in Microsoft Internet Explorer, um zu überprüfen, ob er gültig ist, bevor Sie ihn in Windows Explorer bereitstellen.

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren des Suchverbunds mit Remotedatenspeichern mithilfe von OpenSearch Technologien in Windows 7 und höher finden Sie unter "Zusätzliche Ressourcen" bei [der Verbundsuche in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Erste Schritte mit Verbundsuche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Verbinden Ihres Webdiensts in Windows Verbundsuche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren Ihrer Daten Store in Windows Federated Search](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in Windows Federated Search](-search-federated-search-deploying.md)
</dt> <dt>

[Erweitern des Index](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
