---
title: Erweitern des Indexes (Features der Legacy-Windows-Umgebung)
description: Die Verwendung der-und-Entwicklung für die 2. x-Versionen von Microsoft Windows Desktop Search (WDS) wird zugunsten von Windows Search dringend empfohlen.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102767"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Erweitern des Indexes (Features der Legacy-Windows-Umgebung)

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Die Verwendung der-und-Entwicklung für die 2. x-Versionen von Microsoft Windows Desktop Search (WDS) wird zugunsten von [Windows Search](../search/-search-3x-wds-overview.md)dringend empfohlen.

WDS kann erweitert werden, um den Inhalt neuer Dateitypen und Datenspeicher zu indizieren. Derzeit enthält WDS 2. x Filter für mehr als 200 Typen von Elementen (einschließlich Klartext-Elemente wie HTML-, XML-und Quell Code Dateien) und verwendet dieselbe [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-und protokollhandlertechnologie wie SharePoint Services. Wenn Sie bereits Filter Implementierungen für Ihre neuen Dateitypen installiert haben, kann WDS die vorhandenen Filter Schnittstellen verwenden, um diese Daten zu indizieren.

WDS 2. x-Add-Ins ermöglichen es dem Index, neue Daten und Datenstrukturen zu durchlaufen und zu analysieren, um Informationen zu dem durchsuchbaren Katalog hinzuzufügen. Diese Add-Ins können auch die Windows-Shell erweitern, um den neuen Dateitypen und Daten speichern Symbole und Kontextmenü Handler zuzuordnen. Wenn Sie neue Dateitypen in den WDS-Katalog einschließen möchten, muss ein Add-in die [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle implementieren. Wenn Sie neue Datenspeicher einschließen möchten, muss es sich bei einem Add-in um einen Protokollhandler handeln. Wenn der neue Datenspeicher eingebettete Dateien oder neue Dateitypen selbst enthält, müssen Sie auch einen entsprechenden Filter schreiben.

> [!Note]
>
> Filter und Protokollhandler müssen in nativem Code geschrieben werden, da mögliche Probleme mit der CLR-Versionsverwaltung bei der Verarbeitung aller Add-Ins auftreten.

 

## <a name="adding-file-types-to-the-index"></a>Hinzufügen von Dateitypen zum Index

Mit Add-Ins können WDS erweitert werden, um neue oder proprietäre Dateitypen zu indizieren und jeden neuen Dateityp einem Datei spezifischen Symbol oder einem Kontextmenü zuzuordnen. Zu diesem Zweck können Sie ein Add-in erstellen und registrieren, das Folgendes:

1.  Implementiert eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle für jeden Dateityp, sodass WDS auf den Text und die Metadaten des Dateityps zugreifen und diese indizieren kann.
2.  Implementiert die Schnittstellen **iextracticon** und **IContextMenu** zum Hinzufügen von Symbolen und Kontextmenüs für eine bessere Integration und Benutzerfreundlichkeit.

Eine Erläuterung zum Implementieren von Filtern finden [Sie unter Entwickeln von IFilter-Add-ins](-search-2x-wds-ifilteraddins.md).

## <a name="adding-data-stores-to-the-index"></a>Hinzufügen von Daten speichern zum Index

Mit Add-Ins können WDS erweitert werden, um neue Datenspeicher zu indizieren und um Dateien einem Datei spezifischen Symbol oder einem Kontextmenü zuzuordnen. Zu diesem Zweck können Sie einen Protokollhandler erstellen und registrieren, der Folgendes:

1.  Implementiert die **isearchprotocol** -und **iurlaccessor** -Schnittstellen, um einzelne Elemente in der Inhaltsquelle zu verarbeiten und zu binden. WDS verwendet URLs, um Elemente eindeutig zu identifizieren, unabhängig davon, ob sich diese Elemente im Dateisystem, in einem Daten bankähnlichen Speicher oder im Web befinden.
2.  Implementiert die **ipersistfolder** -Schnittstelle und Teile der **IShellFolder** -Schnittstelle zum Hinzufügen von Symbolen und Kontextmenüs für eine bessere Integration und Benutzerfreundlichkeit.

Eine Erörterung der Implementierung von Protokoll Handlern finden Sie unter [entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md).

## <a name="add-in-installer-guidelines"></a>Richtlinien für Add-in-Installer

Die Installation eines Add-ins sollte die folgenden Richtlinien befolgen:

-   Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.
-   Anmerkungen zu dieser Version müssen bereitgestellt werden.
-   Ein Eintrag zum **Hinzufügen/Entfernen von Programmen** muss für jedes installierte Add-in erstellt werden.
-   Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.
-   Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktion wiederherzustellen und Sie als Standard-Add-in für diesen Dateityp oder-Speicher zu speichern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Entwickeln von IFilter-Add-ins](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
