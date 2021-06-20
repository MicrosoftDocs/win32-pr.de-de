---
title: Erweitern des Index (Ältere Windows-Umgebungsfeatures)
description: Erfahren Sie, wie Sie den Index in der Windows-Desktopsuche 2.x erweitern. Verwenden Sie für Windows-Releases, die höher als Windows XP und Windows Server 2003 sind, Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407353"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Erweitern des Index (Ältere Windows-Umgebungsfeatures)

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Die Verwendung von und entwicklung für die 2.x-Versionen von Microsoft Windows Desktop Search (WDS) wird dringend zugunsten von [Windows Search.](../search/-search-3x-wds-overview.md)

WDS kann erweitert werden, um den Inhalt neuer Dateitypen und Datenspeicher zu indizieren. Derzeit enthält WDS 2.x Filter für mehr als 200 Elementtypen (einschließlich Klartextelementen wie HTML-, XML- und Quellcodedateien) und verwendet die gleiche [**IFilter-**](/windows/desktop/api/filter/nn-filter-ifilter)und Protokollhandlertechnologie wie SharePoint Services. Wenn Sie bereits Filterimplementierungen für Ihre neuen Dateitypen installiert haben, kann WDS die vorhandenen Filterschnittstellen verwenden, um diese Daten zu indizieren.

WDS 2.x-Add-Ins ermöglichen es dem Index, neue Daten und Datenstrukturen zu durchlaufen und zu analysieren, um Informationen zum durchsuchbaren Katalog hinzuzufügen. Diese Add-Ins können auch die Windows-Shell erweitern, um den neuen Dateitypen und Datenspeichern Symbole und Kontextmenühandler zu zuordnen. Um neue Dateitypen in den WDS-Katalog ein include zu setzen, muss ein Add-In die [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)implementieren. Um neue Datenspeicher ein include, muss ein Add-In ein Protokollhandler sein. Wenn der neue Datenspeicher eingebettete Dateien oder neue Dateitypen selbst enthält, müssen Sie auch einen entsprechenden Filter schreiben.

> [!Note]
>
> Filter und Protokollhandler müssen aufgrund potenzieller CLR-Versionsprobleme mit dem Prozess, in dem alle Add-Ins ausgeführt werden, in nativem Code geschrieben werden.

 

## <a name="adding-file-types-to-the-index"></a>Hinzufügen von Dateitypen zum Index

Add-Ins können WDS erweitern, um neue oder proprietäre Dateitypen zu indizieren und jeden neuen Dateityp einem dateispezifischen Symbol oder Kontextmenü zu zuordnen. Hierzu können Sie ein Add-In erstellen und registrieren, das:

1.  Implementiert eine [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)für jeden Dateityp, damit WDS auf den Text und die Metadaten des Dateityps zugreifen und diese indizieren kann.
2.  Implementiert die **Schnittstellen IExtractIcon** und **IContextMenu,** um Symbole und Kontextmenüs hinzuzufügen, um die Integration und Benutzerfreundlichkeit zu verbessern.

Eine Erörterung zum Implementieren von Filtern finden Sie unter [Entwickeln von IFilter-Add-Ins.](-search-2x-wds-ifilteraddins.md)

## <a name="adding-data-stores-to-the-index"></a>Hinzufügen von Datenspeichern zum Index

Add-Ins können WDS erweitern, um neue Datenspeicher zu indizieren und Dateien einem dateispezifischen Symbol oder Kontextmenü zu zuordnen. Hierzu können Sie einen Protokollhandler erstellen und registrieren, der:

1.  Implementiert die **Schnittstellen ISearchProtocol** und **IUrlAccessor,** um einzelne Elemente in der Inhaltsquelle zu verarbeiten und zu binden. WDS verwendet URLs, um Elemente eindeutig zu identifizieren, unabhängig davon, ob sich diese Elemente im Dateisystem, in einem datenbankbasierten Speicher oder im Web befinden.
2.  Implementiert die **IPersistFolder-Schnittstelle** und Teile der **IShellFolder-Schnittstelle,** um Symbole und Kontextmenüs hinzuzufügen, um die Integration und Benutzerfreundlichkeit zu verbessern.

Eine Erörterung zur Implementierung von Protokollhandlern finden Sie unter Developing Protocol Handlers ( [Entwickeln von Protokollhandlern](-search-2x-wds-phaddins.md)).

## <a name="add-in-installer-guidelines"></a>Richtlinien für Das Add-In-Installationsprogramm

Die Installation eines Add-Ins sollte den folgenden Richtlinien entsprechen:

-   Das Installationsprogramm muss entweder EXE- oder MSI-Installationsprogramm verwenden.
-   Versionshinweise müssen bereitgestellt werden.
-   Für **jedes installierte Add-In** muss ein Eintrag Zum Hinzufügen/Entfernen von Programmen erstellt werden.
-   Das Installationsprogramm muss alle Registrierungseinstellungen für den jeweiligen Dateityp oder Speicher übernehmen, den das aktuelle Add-In versteht.
-   Wenn ein vorheriges Add-In überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn ein neueres Add-In das vorherige Add-In überschrieben hat, sollte es die Möglichkeit geben, die Funktionalität des vorherigen Add-Ins wiederherzustellen und es wieder zum Standard-Add-In für diesen Dateityp oder -speicher zu machen.

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

 

 
