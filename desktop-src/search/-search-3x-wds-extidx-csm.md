---
description: Der Crawl Scope Manager (CSM) ist ein Satz von Schnittstellen, der Methoden bereitstellt, mit denen die Windows-Such-Engine über Container zum durchforsten und Elemente unter diesen Containern informiert werden kann, die im Katalog enthalten oder ausgeschlossen werden sollen.
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: Verwenden des Crawl Scope-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef79c9e5a2a4b1dda97bf8a8be7bbaa35d5ecd2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128612"
---
# <a name="using-the-crawl-scope-manager"></a>Verwenden des Crawl Scope-Managers

Der Crawl Scope Manager (CSM) ist ein Satz von Schnittstellen, der Methoden bereitstellt, mit denen die Windows-Such-Engine über Container zum durchforsten und Elemente unter diesen Containern informiert werden kann, die im Katalog enthalten oder ausgeschlossen werden sollen. Entwickler können das CSM verwenden, um einen Crawl Bereich für einen neuen Datenspeicher oder Protokollhandler Programm gesteuert zu definieren. Administratoren können das CSM verwenden, um alle Benutzer Indizes, Such Stämme und Bereichs Regeln anzuzeigen.

Dieser Abschnitt ist wie folgt organisiert:

-   [Was ist der Crawl Scope-Manager?](#what-is-the-crawl-scope-manager)
-   [Stämme und Bereichs Regeln suchen](#search-roots-and-scope-rules)
    -   [Stämme durchsuchen](#search-roots-and-scope-rules)
    -   [Bereichs Regeln](#scope-rules)
-   [Vom Crawl Bereichs-Manager unterstützte Gruppenrichtlinien](#group-policies-supported-by-the-crawl-scope-manager)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>Was ist der Crawl Scope-Manager?

Um den Crawl Scope-Manager zu verstehen, müssen Sie die folgenden Begriffe verstehen:

-   Ein *Crawl Bereich* ist ein Satz von URLs, die auf Datenspeicher oder Container (e-Mail-Datenspeicher, Datenbanken, Netzwerkdatei Freigaben usw.) verweisen, die der Indexer zum Indizieren von Elementen durchläuft. Bei einem hierarchischen Datenspeicher kann der Crawl Bereich eine übergeordnete URL einschließen, aber eine untergeordnete URL ausschließen und umgekehrt. Elemente innerhalb des Durchforstungs Bereichs werden indiziert. Elemente außerhalb des Crawl Bereichs werden ignoriert.
-   Ein *Suchstamm* ist die URL der obersten Ebene, die einen Container oder Datenspeicher identifiziert, der einem bestimmten Protokollhandler zugeordnet ist. Durch Such Stämme können Standorte identifiziert werden, die für einen Benutzer spezifisch sind, sich auf einem Remote Computer befinden oder der einem Platzhalter Muster entsprechen. Wenn Sie einen neuen Datenspeicher oder Protokollhandler hinzufügen, sollten Sie dem Crawl Bereich auch einen Suchstamm hinzufügen.
-   Eine *Bereichs Regel* ist eine Regel, die URLs innerhalb eines Suchstamms von der durch forchten und Indizierung enthält oder ausschließt. Nehmen Sie beispielsweise an, Sie möchten alles, was im Ordner "ProjectFiles" indiziert ist, mit Ausnahme der Unterordner Prototypen. Sie benötigen eine Inklusions Regel für file:///C: \\ workteama \\ ProjectFiles \\ und eine Ausschlussregel für file:///C: \\ workteama \\ ProjectFiles- \\ Prototypen \\ .

Der **Crawl Scope Manager (CSM)** ist ein Satz von APIs, mit denen Sie Such Stämme und Bereichs Regeln für den Windows Search-Indexer hinzufügen, entfernen und aufzählen können. Wenn Sie möchten, dass der Indexer mit dem Crawlen eines neuen Containers beginnt, können Sie das CSM verwenden, um die Such Stamm-und Bereichs Regeln für Pfade innerhalb der Such Stamm Ordner festzulegen. Wenn Sie z. b. einen neuen Protokollhandler installieren, können Sie einen Suchstamm erstellen und mindestens eine Inklusions Regel hinzufügen. Anschließend kann der Indexer eine durch Forstung für die anfängliche Indizierung starten. Das CSM bietet die folgenden Schnittstellen, damit Sie dies Programm gesteuert durchführen können.

-   [**Ienumsearchroots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [Ienumsearchscoperules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**Isearchroot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**Isearchscoperule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [Isearchitem](./-search-isearchitem.md)

Obwohl Sie die CSM-APIs verwenden können, um einen Crawl Bereich Programm gesteuert zu definieren, wurde das CSM auch für die Unterstützung von Endbenutzern entworfen. Nehmen Sie beispielsweise an, Sie haben einen Protokollhandler für einen neuen Datenspeicher entwickelt, und Sie möchten Benutzern oder Administratoren die Verwaltung der Pfade gestatten, die indiziert werden sollen. Sie können den Crawl Scope-Manager verwenden, um einen oder mehrere Such Stämme festzulegen (z. b. file:///C: \\ MyContainer \\ ), und die Windows Search-Benutzeroberfläche zum Festlegen von Indizierungs Optionen zeigt jeden Suchstamm mit einem Kontrollkästchen an. Benutzer können dann den Pfad oder die untergeordneten Elemente dieses Pfades einschließen bzw. ausschließen.

## <a name="search-roots-and-scope-rules"></a>Stämme und Bereichs Regeln suchen

Such Stämme und Bereichs Regeln definieren zusammen ein Workingset von URLs, die den Crawl Bereich des Indexers bilden.

### <a name="search-roots"></a>Stämme durchsuchen

Durch das Festlegen eines Suchstamms wird nicht angegeben, welche Teile dieses Informationsspeicher indiziert werden sollen. Es signalisiert lediglich, dass ein Inhalts Speicher vorhanden ist und einem registrierten Protokollhandler zugeordnet ist. Die Syntax eines Suchstamms enthält ein Protokoll, eine Website oder eine Benutzer Sicherheits-ID sowie einen Pfad zu den zu durchsuchenden Standorten.

Sie sollten neue Such Stämme erstellen, wenn Sie Folgendes durchführen:

-   Installieren eines Protokoll Handlers oder
-   Sie möchten einen neuen Datenspeicher indizieren.

AND

-   der Datenspeicher befindet sich nicht bereits im Crawl Bereich des Indexers.

Anweisungen zum Hinzufügen, entfernen und Auflisten von Such Stämmen finden Sie unter [Verwalten von Such](-search-3x-wds-extidx-csm-searchroots.md) Stamm Elementen.

### <a name="scope-rules"></a>Bereichs Regeln

Bereichs Regeln schließen URLs in einem Such Stamm aus, die durchforstet und indiziert werden. Bereichs Regeln können von Endbenutzern, von der Gruppenrichtlinie oder von Entwicklern von Drittanbietern festgelegt werden. Sie sollten Bereichs Regeln Programm gesteuert definieren, wenn Sie einen neuen Suchstamm definieren. Die Such Stämme und Bereichs Regeln bilden den standardmäßigen Crawl Bereich für Ihren Datenspeicher und den Protokollhandler.

> [!Note]  
> Benutzer mit Zugriff auf die Systemsteuerung können den Standard Crawl Bereich ändern. Daher sollte jede Anwendung, die die Bereichs Verwaltung bietet, die Regeln immer direkt aus dem CSM erhalten, indem Sie die Enumerationsmethoden verwendet, anstatt sich auf Ihre eigene gespeicherte Kopie der Benutzerregeln zu verlassen.

 

Anweisungen zum Hinzufügen, entfernen, wiederherstellen und Aufzählen von Bereichs Regeln finden Sie unter [Verwalten von Bereichs Regeln](-search-3x-wds-extidx-csm-scoperules.md) .

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>Vom Crawl Bereichs-Manager unterstützte Gruppenrichtlinien

System Administratoren können mithilfe von Gruppenrichtlinien Crawl Bereiche in ihren Organisationen definieren. Diese Gruppenrichtlinien Regeln können auch als Standardregeln fungieren, die Benutzer überschreiben können. Beispielsweise können Sie einen Satz von Verzeichnissen für eine Gruppe von Benutzern und einen anderen Satz für eine andere Gruppe von Benutzern indizieren, sodass die Benutzer diese Standardeinstellungen deaktivieren können. Gruppenrichtlinien Regeln können auch als erzwungene Ausschluss Regeln fungieren, die von Benutzern nicht außer Kraft gesetzt werden können. Dadurch wird verhindert, dass bestimmte Benutzer bestimmte Netzwerkfreigaben indizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Such Stämmen](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[Verwalten von Bereichs Regeln](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[Der Indizierungsprozess](-search-indexing-process-overview.md)
</dt> </dl>

 

 
