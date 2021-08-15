---
description: Das Registrieren eines Dateityps ist der erste Schritt beim Erstellen einer Dateizuordnung, die diesen Dateityp &\# 0034;bekannt&\# 0034; zur Shell macht. Ohne Dateityphandler kann die Shell jedoch keine Informationen aus und über die Datei für den Benutzer verfügbar machen.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Dateityphandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404cfd3be4c3e8a600b2f943bda1243ca243b70af411e104000245edd13d94c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459725"
---
# <a name="file-type-handlers"></a>Dateityphandler

[Das Registrieren eines Dateityps](fa-how-work.md) ist der erste Schritt beim Erstellen einer Dateizuordnung, wodurch dieser Dateityp der Shell "bekannt" wird. Ohne Dateityphandler kann die Shell jedoch keine Informationen aus und über die Datei für den Benutzer verfügbar machen.

Dieses Thema ist wie folgt organisiert:

-   [Machen Eines Dateityps der Shell bekannt](#make-a-file-type-known-to-shell)
-   [Beschreibungen des Dateityphandlers](#file-type-handler-descriptions)
-   [Zugehörige Themen](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Machen Eines Dateityps der Shell bekannt

Im folgenden Screenshot von Windows-Explorer wird die Bilddatei "Alias.known" in der Shell **Pictures-Bibliothek** angezeigt und nur der anwendung Paint zugeordnet.

![Screenshot des Explorers, der ein Bild ohne Dateityp öffnet](images/file-assoc/fileassoc-filetypehandler.png)

In der Datei "Dateierweiterung.known" im vorherigen Screenshot fehlt die folgende Funktionalität, die von einem Dateityphandler aktiviert wird:

-   Miniaturansicht oder Vorschau
-   Bildspezifische Verben im Kontextmenü, z. B.:
    -   Drehen der Vorschau
    -   Als Desktophintergrund festlegen
    -   Drucken
-   Bildspezifische Eigenschaften im **Detailbereich,** z. B.:
    -   Datum der Erstellung
    -   `Tags`
    -   Rating
-   Indizierung von Dateitext

Im folgenden Screenshot weist dieselbe Datei (Alias.known) die Erweiterung .jpg auf. Dabei handelt es sich um einen registrierten Dateityp mit zugeordneten Dateityphandlern, sodass ein Miniaturbild und weitere Eigenschaften angezeigt werden.

![Image mit einem registrierten Dateityp und zugeordneten Dateityphandlern](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Beschreibungen des Dateityphandlers

Die von den einzelnen Dateityphandlern bereitgestellten Funktionen sind in der folgenden Tabelle aufgeführt:



| Handler                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenü](context-menu-handlers.md)                   | Ein Kontextmenühandler, manchmal auch als Kontextmenühandler bezeichnet, ist ein Dateityphandler, der einem vorhandenen Kontextmenü Befehle hinzufügt. Diese Handler sind einem bestimmten Dateityp zugeordnet und werden jedes Mal aufgerufen, wenn ein Kontextmenü für einen Member des Dateityps angezeigt wird.                                                                                                                                                                                                                                                                           |
| [Miniaturansicht](thumbnail-providers.md)                         | Ein Handler, der ein Bild bereitstellt, das ein Shellelement darstellt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Eigenschaft](../properties/building-property-handlers-properties.md) | Ein Eigenschaftenhandler, der Zugriff auf Elementeigenschaften für Windows Search, den Windows-Explorer und andere Anwendungen bereitstellt, die auf Eigenschaften zugreifen müssen.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Vorschau](preview-handlers.md)                              | Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des Elements erzeugt, das im Vorschaubereich Windows Explorer angezeigt werden soll.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filter](../search/-search-3x-wds-extidx-filters.md)              | Ein Filter, eine Implementierung der [**IFilter-Schnittstelle,**](/windows/win32/api/filter/nn-filter-ifilter) der Dokumente auf Text und Eigenschaften (auch als Attribute bezeichnet) überprüft. Sie extrahiert Textblöcke aus diesen Dokumenten, filtert eingebettete Formatierungen heraus und behält Informationen über die Position des Texts bei. Außerdem werden Blöcke von Werten extrahiert, bei denen es sich um Eigenschaften eines gesamten Dokuments oder um klar definierte Teile eines Dokuments handelt. **IFilter** bietet die Grundlage für die Erstellung von Anwendungen auf höherer Ebene, z. B. Dokumentindexer und anwendungsunabhängige Viewer. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypüberprüfung](file-type-verifier.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 
