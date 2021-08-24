---
title: Entwickeln von Protokollhandler-Add-Ins
description: Sie können Microsoft Windows DesktopSuche (WDS) erweitern, um neue Datenspeicher einzubeziehen, indem Sie einen benutzerdefinierten Protokollhandler implementieren.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc107c8ca51d43e2602206eb993cea6cac6dd9ec866670235daf7fb81452f5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726500"
---
# <a name="developing-protocol-handler-add-ins"></a>Entwickeln von Protokollhandler-Add-Ins

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search.](../search/-search-3x-wds-overview.md)

Sie können Microsoft Windows DesktopSuche (WDS) erweitern, um neue Datenspeicher einzubeziehen, indem Sie einen benutzerdefinierten Protokollhandler implementieren.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indizieren von Datenspeichern mit Protokollhandlern

Ein Datenspeicher ist eine Inhaltsquelle (ein Datenbanksystem, ein Verzeichnis, ein Dateisystem), in der Daten gespeichert werden und vom WDS-Indexer durchforstet werden können. Der Speicher kann hierarchisch (z. B. eine Datenbank) oder linkbasiert (z. B. eine Website) sein. Ein Protokollhandler ermöglicht es Indizierungsanwendungen wie WDS, die Knoten eines Datenspeichers systematisch zu durchforsten, um relevante Informationen zu extrahieren, die in den Index eingeschlossen werden sollen. Jeder Protokollhandler wird zum Indizierung eines bestimmten Datenspeichertyps verwendet. WDS wird mit Protokollhandlern für Dateisystemspeicher und sowohl für Microsoft Outlook als auch für Microsoft Outlook Express-Datenspeicher (E-Mail-Speicher, ) ausgeliefert. PST-Dateien usw.). Beim Indizieren Outlook E-Mail durchforstet der Protokollhandler beispielsweise alle Nachrichten in allen Ordnern und extrahiert Informationen aus jeder Nachricht und Anlage. Diese Informationen werden an den Indexer übergeben, der in den WDS-Katalog aufgenommen werden soll.

Häufig müssen Benutzer andere Datenspeicher durchsuchen, z. B. Legacydatenbanken, E-Mail-Speicher oder Datenstrukturen, die von WDS nicht unterstützt werden. Sie können WDS erweitern, um einen neuen Datenspeicher zu durchforsten, indem Sie einen Protokollhandler speziell für diesen Datenspeicher verwenden oder implementieren. Zunächst sollten Sie ermitteln, ob bereits ein Protokollhandler für Ihren Datenspeicher vorhanden ist, möglicherweise für die Verwendung mit einer anderen Anwendung wie SharePoint Services. Wenn ja, können Sie diesen Protokollhandler auf dem System installieren. Wenn jedoch kein anderer Protokollhandler vorhanden ist, müssen Sie einen implementieren. WDS-Protokollhandler verwenden die gleichen Entwurfsspezifikationen wie SharePoint Services und können häufig austauschbar verwendet werden.

Wenn der Datenspeicher andere Daten- oder Dateitypen als einen der 200 Dateitypen enthält, die von WDS unterstützt werden, müssen Sie außerdem einen Filter implementieren, um auf den Inhalt von Elementen im Speicher zuzugreifen und diese zu indiziert. WDS 2.x verwendet den Protokollhandler und die [**IFilter-Technologie,**](/windows/desktop/api/filter/nn-filter-ifilter)die von SharePoint Services verwendet werden. Wenn Sie bereits Filter für einen bestimmten Speicher und Dateityp auf dem zu indizierten System installiert haben, verwendet WDS die vorhandenen Schnittstellen zum Indizierung dieser Daten.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Roadmap zum Hinzufügen neuer Datenspeicher

Um WDS zum Durchforsten neuer Datenspeicher zu erweitern, können Sie einen Protokollhandler und mindestens eines der folgenden Add-Ins erstellen: Kontextmenühandler, Symbolhandler und ein SearchProtocolOptions-Add-In.

1.  Erstellen und registrieren Sie einen Multithreadprotokollhandler für den Datenspeicher:
    -   **ISearchProtocol:** Diese Schnittstelle greift auf ein Protokoll zu und ordnet eine URL einem IUrlAccessor zu.
    -   **IUrlAccessor:** Dies ist die Hauptschnittstelle, die für den Zugriff auf Elemente aus der Inhaltsquelle und das Binden des Inhalts an den entsprechenden Filter verwendet wird.
    -   **IProtocolHandlerSite:** Diese Schnittstelle wird verwendet, um zusätzliche Filter anzufordern und zu laden.
    -   **IFilter:** Diese Schnittstelle gibt die URL jedes Elements in einem Ordner als Werteigenschaften für die Verarbeitung zurück.

    > [!Note]
    >
    > Die mindest erforderliche Add-In-Funktionalität zum Zurückgeben von Suchergebnissen aus einem nicht hierarchischen Datenspeicher ist eine Implementierung von ISearchProtocol- und IUrlAccessor-Schnittstellen.

     

2.  Implementieren Sie die ISearchProtocolOptions-Schnittstelle, um benutzerdefinierte Protokollhandleroptionen wie vordefinierte Startseiten einzubeziehen:
    -   **ISearchProtocolOptions:** Diese Schnittstelle definiert Standard-URLs für den zu verarbeitenden Protokollhandler, bestimmt die Anforderungen für einen Protokollhandler und bestimmt, ob die Anforderungen für ein bestimmtes System erfüllt wurden.
3.  Erweitern Sie die Shell, um Benutzeroberflächenelemente wie Kontextmenüs und dateispezifische Symbole einzuschließen, indem Sie die folgenden Schnittstellen implementieren:
    -   **IShellFolder:** Diese Schnittstelle, die zum Verwalten von Ordnern verwendet wird, ist erforderlich, um die Schnittstellen IContextMenu und IExtractIcon für eine URL in einem neuen Speicher bereitzustellen.
    -   **IPersistFolder:** Diese Schnittstelle ist erforderlich, um ein Shell-Ordnerobjekt anzuweisen, sich selbst zu initialisieren.
    -   **IPersist:** Diese Schnittstelle stellt den Klassenbezeichner (CLSID) eines Objekts zur Verfügung, das dauerhaft im System gespeichert werden kann.
    -   **IContextMenu:** Diese Schnittstelle definiert das Kontextmenü mit der rechten Maustaste für ein Element, auf das über die URL verwiesen wird.
    -   **IExtractIcon:** Diese Schnittstelle definiert das Symbol, das für ein Element angezeigt werden soll, auf das über die URL verwiesen wird.
4.  Implementieren Sie einen Mechanismus, um den Indexer über Änderungen an Ihrem Datenspeicher zu benachrichtigen:
    -   **ISearchItemsChangedSink:** Mit dieser Schnittstelle kann Ihr Protokollhandler den Index über Änderungen an Ihrem Datenspeicher benachrichtigen. Dadurch wird die Leistung verbessert, indem sichergestellt wird, dass der Indexer nicht den gesamten Speicher in inkrementellen Indizes durchforstet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Implementieren eines Protokollhandlers für WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Hinzufügen von Symbolen, Vorschauen und Kontextmenüs mit Shellerweiterungen](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Benachrichtigen des Änderungsindexes](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Installieren und Registrieren von Protokollhandlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 