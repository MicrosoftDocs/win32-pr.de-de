---
title: Erweitern des Index (Legacy-Windows-Umgebungsfeatures)
description: Erfahren Sie, wie Sie den Index in Windows Desktopsuche 2.x erweitern. Verwenden Sie für Windows Releases, die höher als Windows XP und Windows Server 2003 sind, stattdessen Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73bbf1ab143bcac581a59467e7a3813511e7b20204434ee5ae7dd7d8893b636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480922"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Erweitern des Index (Legacy-Windows-Umgebungsfeatures)

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search.](../search/-search-3x-wds-overview.md)

Die Verwendung von und der Entwicklung für die 2.x-Versionen von Microsoft Windows Desktop Search (WDS) wird dringend zugunsten von [Windows Search](../search/-search-3x-wds-overview.md)empfohlen.

WDS kann erweitert werden, um den Inhalt neuer Dateitypen und Datenspeicher zu indizierung. WDS 2.x enthält derzeit Filter für über 200 Elementtypen (einschließlich Klartextelemente wie HTML-, XML- und Quellcodedateien) und verwendet die gleiche [**IFilter-**](/windows/desktop/api/filter/nn-filter-ifilter)und Protokollhandlertechnologie wie SharePoint Services. Wenn Sie bereits Filterimplementierungen für Ihre neuen Dateitypen installiert haben, kann WDS die vorhandenen Filterschnittstellen verwenden, um diese Daten zu indizieren.

Mit WDS 2.x-Add-Ins kann der Index neue Daten- und Datenstrukturen durchlaufen und analysieren, um Informationen zum durchsuchbaren Katalog hinzuzufügen. Diese Add-Ins können auch die Windows Shell erweitern, um Symbole und Kontextmenühandler den neuen Dateitypen und Datenspeichern zuzuordnen. Um neue Dateitypen in den WDS-Katalog einzubinden, muss ein Add-In die [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)implementieren. Um neue Datenspeicher einzubeziehen, muss ein Add-In ein Protokollhandler sein. Wenn der neue Datenspeicher eingebettete Dateien oder neue Dateitypen selbst enthält, müssen Sie auch einen entsprechenden Filter schreiben.

> [!Note]
>
> Filter und Protokollhandler müssen in nativem Code geschrieben werden, da bei dem Prozess, in dem alle Add-Ins ausgeführt werden, probleme mit der CLR-Versionierung auftreten können.

 

## <a name="adding-file-types-to-the-index"></a>Hinzufügen von Dateitypen zum Index

Add-Ins können WDS erweitern, um neue oder proprietäre Dateitypen zu indizieren und jeden neuen Dateityp einem dateispezifischen Symbol oder Kontextmenü zuzuordnen. Hierzu können Sie ein Add-In erstellen und registrieren, das:

1.  Implementiert eine [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)für jeden Dateityp, damit WDS auf den Text und die Metadaten des Dateityps zugreifen und diese indiziert.
2.  Implementiert die **Schnittstellen IExtractIcon** und **IContextMenu,** um Symbole und Kontextmenüs für eine bessere Integration und Benutzerfreundlichkeit hinzuzufügen.

Eine Erläuterung zur Implementierung von Filtern finden Sie unter [Entwickeln von IFilter-Add-Ins.](-search-2x-wds-ifilteraddins.md)

## <a name="adding-data-stores-to-the-index"></a>Hinzufügen von Datenspeichern zum Index

Add-Ins können WDS erweitern, um neue Datenspeicher zu indizieren und Dateien einem dateispezifischen Symbol oder Kontextmenü zuzuordnen. Hierzu können Sie einen Protokollhandler erstellen und registrieren, der Folgendes ermöglicht:

1.  Implementiert die **Schnittstellen ISearchProtocol** und **IUrlAccessor,** um einzelne Elemente in der Inhaltsquelle zu verarbeiten und zu binden. WDS verwendet URLs, um Elemente eindeutig zu identifizieren, unabhängig davon, ob sich diese Elemente im Dateisystem, in einem datenbankähnlichen Speicher oder im Web befinden.
2.  Implementiert die **IPersistFolder-Schnittstelle** und Teile der **IShellFolder-Schnittstelle,** um Symbole und Kontextmenüs für eine bessere Integration und Benutzerfreundlichkeit hinzuzufügen.

Eine Erläuterung zur Implementierung von Protokollhandlern finden Sie unter [Entwickeln von Protokollhandlern.](-search-2x-wds-phaddins.md)

## <a name="add-in-installer-guidelines"></a>Richtlinien für den Add-In-Installer

Die Installation eines Add-Ins sollte den folgenden Richtlinien entsprechen:

-   Das Installationsprogramm muss entweder EXE- oder MSI-Installer verwenden.
-   Versionshinweise müssen bereitgestellt werden.
-   Für jedes installierte Add-In muss ein Eintrag **zum Hinzufügen/Entfernen** von Programmen erstellt werden.
-   Das Installationsprogramm muss alle Registrierungseinstellungen für den jeweiligen Dateityp oder -speicher übernehmen, den das aktuelle Add-In versteht.
-   Wenn ein vorheriges Add-In überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn ein neueres Add-In das vorherige Add-In überschrieben hat, sollte es die Möglichkeit geben, die Funktionalität des vorherigen Add-Ins wiederherzustellen und es zum Standard-Add-In für diesen Dateityp oder Speicher zu machen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Entwickeln von IFilter-Add-Ins](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Entwickeln von Protokollhandlern](-search-2x-wds-phaddins.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Ifilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
