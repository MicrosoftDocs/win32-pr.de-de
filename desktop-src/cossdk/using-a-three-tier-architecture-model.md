---
description: Das dreistufige Architekturmodell, bei dem es sich um das grundlegende Framework für das logische Entwurfs Modell handelt, segmentiert eine Anwendungs Komponente in drei Dienst Ebenen.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Verwenden eines Three-Tier-Architekturmodells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20b765a6d103f3c349ffd9a44853f495c64a070
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393189"
---
# <a name="using-a-three-tier-architecture-model"></a>Verwenden eines Three-Tier-Architekturmodells

Das dreistufige Architekturmodell, bei dem es sich um das grundlegende Framework für das [logische Entwurfs Modell](the-logical-model--application-definition-and-planning.md)handelt, segmentiert die Komponenten einer Anwendung in drei Dienst Ebenen. Diese Ebenen entsprechen nicht notwendigerweise physischen Standorten auf verschiedenen Computern in einem Netzwerk, sondern eher auf logischen Ebenen der Anwendung. Die Verteilung der Teile einer Anwendung in einer physischen Topologie kann je nach Systemanforderungen geändert werden.

Im folgenden finden Sie kurze Beschreibungen der Dienste, die den einzelnen Tarifen zugeordnet werden:

-   **Die Präsentationsebene oder die Benutzer Dienst Ebene ermöglicht einem Benutzer den Zugriff auf die Anwendung.** Diese Ebene stellt Daten für den Benutzer dar und ermöglicht optional die Datenbearbeitung und Dateneingabe. Die zwei Haupttypen von Benutzeroberflächen für diese Ebene sind die herkömmliche Anwendung und die webbasierte Anwendung. Webbasierte Anwendungen enthalten nun häufig die meisten Daten Bearbeitungs Features, die von herkömmlichen Anwendungen verwendet werden. Dies wird durch die Verwendung von dynamischem HTML-und Client seitiger Datenquellen und Daten Cursorn erreicht.

    > [!Note]  
    > In einer Anwendung mit drei Ebenen ist die Client seitige Anwendung skinnier als eine Client/Server-Anwendung, da Sie die Dienst Komponenten, die sich jetzt in der mittleren Ebene befinden, nicht enthält. Dies führt zu einem geringeren mehr Aufwand für den Benutzer, aber mehr Netzwerkverkehr für das System, da die Komponenten auf verschiedene Computer verteilt werden.

     

-   **Die Ebene der mittleren Ebene oder der Unternehmens Dienste besteht aus Geschäfts-und Daten Regeln.** Die mittlere Ebene wird auch als *Geschäftslogik* Schicht bezeichnet und bietet com+-Entwicklern die Möglichkeit, Unternehmens wichtige Geschäftsprobleme zu lösen und größere Produktivitätsvorteile zu erzielen. Die Komponenten, aus denen diese Ebene besteht, können auf einem Server Computer vorhanden sein, um die Ressourcen Freigabe zu unterstützen. Diese Komponenten können verwendet werden, um Geschäftsregeln zu erzwingen, z. b. Geschäfts Algorithmen, gesetzliche oder behördliche Vorschriften und Daten Regeln, die so entworfen wurden, dass die Datenstrukturen innerhalb bestimmter oder mehrerer Datenbanken konsistent bleiben. Da diese Komponenten der mittleren Ebene nicht an einen bestimmten Client gebunden sind, können Sie von allen Anwendungen verwendet werden und können an verschiedene Speicherorte verschoben werden, da die Antwortzeit und andere Regeln dies erfordern. Beispielsweise können einfache Änderungen auf der Clientseite platziert werden, um die Netzwerkroundtrips zu minimieren, oder Daten Regeln können in gespeicherten Prozeduren platziert werden.

-   **Die Datenebene bzw. die Datendienst Schicht interagiert mit permanenten Daten, die normalerweise in einer Datenbank oder in einem permanenten Speicher gespeichert werden.** Dies ist die tatsächliche DBMS-Zugriffs Schicht. Der Zugriff erfolgt über die Ebene der Geschäfts Dienste und gelegentlich über die Benutzer Dienst Ebene. Diese Ebene besteht aus Datenzugriffs Komponenten (anstelle von unformatierten DBMS-Verbindungen), um die Ressourcen Freigabe zu unterstützen und Clients zu ermöglichen, ohne die DBMS-Bibliotheken und ODBC-Treiber auf jedem Client zu installieren.

Während des Lebenszyklus einer Anwendung bietet der Ansatz mit drei Ebenen Vorteile wie z. b. Wiederverwendbarkeit, Flexibilität, Verwaltbarkeit, Verwaltbarkeit und Skalierbarkeit. Sie können die von Ihnen erstellten Komponenten und Dienste freigeben und wieder verwenden, und Sie können Sie nach Bedarf über ein Netzwerk von Computern verteilen. Sie können große und komplexe Projekte in einfachere Projekte aufteilen und Sie verschiedenen Programmierern oder Programmier Teams zuweisen. Sie können auch Komponenten und Dienste auf einem Server bereitstellen, um die Änderungen zu übernehmen, und Sie können Sie erneut bereitstellen, wenn die Benutzerbasis der Anwendung, die Daten und das Transaktions Volume vergrößert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das logische Modell: Anwendungs Definition und-Planung](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



