---
description: Das Architekturmodell mit drei Ebenen, das das grundlegende Framework für das logische Entwurfsmodell ist, segmentiert eine Anwendungskomponenten in drei Dienste.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Verwenden eines Three-Tier Architekturmodells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd08ee1363504c610ed650d59b3837d292fb3a1d447c882dbd39ddba6229503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546057"
---
# <a name="using-a-three-tier-architecture-model"></a>Verwenden eines Three-Tier Architekturmodells

Das Architekturmodell mit drei Ebenen, das das grundlegende Framework für das logische Entwurfsmodell [ist,](the-logical-model--application-definition-and-planning.md)segmentiert die Komponenten einer Anwendung in drei Dienste. Diese Ebenen entsprechen nicht unbedingt physischen Standorten auf verschiedenen Computern in einem Netzwerk, sondern eher logischen Ebenen der Anwendung. Wie die Teile einer Anwendung in einer physischen Topologie verteilt werden, kann sich je nach Systemanforderungen ändern.

Im Folgenden finden Sie kurze Beschreibungen der Dienste, die den einzelnen Ebenen zugeordnet sind:

-   **Die Präsentationsebene oder Benutzerdienstebene gewährt einem Benutzer Zugriff auf die Anwendung.** Diese Ebene stellt dem Benutzer Daten vor und ermöglicht optional die Datenbearbeitung und -eingabe. Die beiden Haupttypen der Benutzeroberfläche für diese Ebene sind die herkömmliche Anwendung und die webbasierte Anwendung. Webbasierte Anwendungen enthalten jetzt häufig die meisten Datenbearbeitungsfeatures, die herkömmliche Anwendungen verwenden. Dies wird durch die Verwendung von dynamischem HTML und clientseitigen Datenquellen und Datencursorn erreicht.

    > [!Note]  
    > In einer Anwendung mit drei Ebenen ist die clientseitige Anwendung skinrischer als eine Client-Server-Anwendung, da sie nicht die Dienstkomponenten enthält, die sich jetzt auf der mittleren Ebene befinden. Dies führt zu weniger Mehraufwand für den Benutzer, aber zu mehr Netzwerkdatenverkehr für das System, da Komponenten auf verschiedene Computer verteilt werden.

     

-   **Die mittlere Ebene (Business Services Layer) besteht aus Geschäfts- und Datenregeln.** Die mittlere Ebene, die auch als Geschäftslogikebene bezeichnet wird, ist der Ort, an dem COM+-Entwickler unternehmenskritische Geschäftsprobleme lösen und wichtige Produktivitätsvorteile erzielen können.  Die Komponenten, aus denen diese Schicht besteht, können auf einem Servercomputer vorhanden sein, um die Gemeinsame Nutzung von Ressourcen zu unterstützen. Diese Komponenten können verwendet werden, um Geschäftsregeln wie Geschäftsalgorithmen und gesetzliche oder behördliche Vorschriften sowie Datenregeln zu erzwingen, die darauf ausgelegt sind, die Datenstrukturen innerhalb bestimmter oder mehrerer Datenbanken konsistent zu halten. Da diese Komponenten der mittleren Ebene nicht an einen bestimmten Client gebunden sind, können sie von allen Anwendungen verwendet und an verschiedene Speicherorte verschoben werden, je nach Antwortzeit und anderen Regeln. Beispielsweise können einfache Bearbeitungen auf der Clientseite platziert werden, um Netzwerk-Roundtrips zu minimieren, oder Datenregeln können in gespeicherten Prozeduren platziert werden.

-   **Die Datenschicht oder Datendienstebene interagiert mit persistenten Daten, die normalerweise in einer Datenbank oder im permanenten Speicher gespeichert sind.** Dies ist die tatsächliche DBMS-Zugriffsebene. Der Zugriff darauf erfolgt über die Ebene der Geschäftsdienste und gelegentlich über die Ebene der Benutzerdienste. Diese Schicht besteht aus Datenzugriffskomponenten (anstelle von unformatierten DBMS-Verbindungen), um die Ressourcenfreigabe zu unterstützen und die Konfiguration von Clients zu ermöglichen, ohne die DBMS-Bibliotheken und ODBC-Treiber auf jedem Client zu installieren.

Während des Lebenszyklus einer Anwendung bietet der Drei-Ebenen-Ansatz Vorteile wie Wiederverwendbarkeit, Flexibilität, Verwaltbarkeit, Verwaltbarkeit und Skalierbarkeit. Sie können die von Ihnen erstellten Komponenten und Dienste freigeben und wiederverwenden und bei Bedarf auf ein Netzwerk von Computern verteilen. Sie können große und komplexe Projekte in einfachere Projekte unterteilen und sie verschiedenen Programmierern oder Programmierteams zuweisen. Sie können auch Komponenten und Dienste auf einem Server bereitstellen, um mit Änderungen mithalten zu können, und Sie können sie erneut bereitstellen, wenn die Benutzerbasis, die Daten und das Transaktionsvolumen der Anwendung wächst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Logisches Modell: Anwendungsdefinition und -planung](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



