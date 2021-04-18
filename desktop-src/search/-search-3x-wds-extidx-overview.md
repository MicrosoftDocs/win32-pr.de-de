---
description: Sie können die Windows-Suche so erweitern, dass der Inhalt und die Eigenschaften von neuen Dateiformaten und Daten speichern mithilfe von Daten-Add-in-Schnittstellen indiziert werden.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Erweitern des Indexes (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340166"
---
# <a name="extending-the-index-windows-search"></a>Erweitern des Indexes (Windows Search)

Sie können die Windows-Suche so erweitern, dass der Inhalt und die Eigenschaften von neuen Dateiformaten und Daten speichern mithilfe von [Daten-Add-in-Schnittstellen](./-search-data-addins-interfaces-entry-page.md)indiziert werden. Zum Erstellen von Add-Ins für Windows-Suche müssen Entwickler von Drittanbietern zuerst einen shelldatenspeicher implementieren und dann einen Protokollhandler entwickeln, damit Windows Search auf die Daten für die Indizierung zugreifen kann. Wenn Sie ein benutzerdefiniertes Dateiformat haben, müssen Sie einen Filter Handler zum Indizieren von Dateiinhalten und einen Eigenschafts Handler für jeden Dateityp zum Indizieren von Eigenschaften entwickeln.

Windows Search unterstützt derzeit die Indizierung von über 200 Typen von Elementen (z. b. txt-, HTML-und XML-Dateiformate) und kann mit mehreren Typen von Daten speichern (z. b. dem NTFS-Dateisystem und Microsoft Outlook) verwendet werden. Windows Search verwendet die Filter-und protokollhandlertechnologie, ähnlich wie SharePoint Server. Wenn Sie bereits über Implementierungen für das Dateiformat verfügen, können Sie daher die Implementierungen aktualisieren, die mit einem Stream initialisiert werden sollen, indem Sie [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) verwenden, damit der Filter mit Windows Search funktioniert.

> [!Note]  
> Filter Handler, Eigenschaften Handler und Protokollhandler müssen in nativem Code geschrieben werden. Ursache hierfür sind potenzielle Probleme bei der Common Language Runtime (CLR) mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden.

 

In diesem Abschnitt zur Erweiterung des Indexes mit Add-Ins finden Sie die folgenden Themen:

-   [Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)
-   [Entwickeln von Eigenschaften Handlern für Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
-   [Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Weitere Ressourcen

Verwandte Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-samples-ovw.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Leit Faden für Windows-Suche](-search-developers-guide-entry-page.md)
</dt> <dt>

[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
