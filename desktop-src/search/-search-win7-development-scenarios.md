---
description: Enthält eine Übersicht über die Einführung von Bibliotheken für Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Windows Shell-Bibliotheken in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb94551d80d0230966626f1bd6499801aff889c4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106365211"
---
# <a name="windows-shell-libraries-in-windows"></a>Windows Shell-Bibliotheken in Windows

Dieses Thema enthält eine Übersicht über die Einführung von Bibliotheken für Windows 7 und höher. Bibliotheken sind eine Windows-Shell-Funktion. Für den Zugriff auf Windows Shell-Funktionen, wie z. b. Bibliotheken, müssen Entwickler von Windows Search-Anwendungen von Drittanbietern zuerst einen shelldatenspeicher implementieren. Weitere Informationen finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Dieses Thema ist wie folgt organisiert:

- [Libraries](#libraries)
  - [Einstiegspunkte für Benutzerdaten](#user-data-entry-points)
  - [Ordner Sammlungen](#collections-of-folders)
  - [Unterstützte Ordner in Bibliotheken](#supported-folders-in-libraries)
  - [Speicher gestützt](#storage-backed)
  - [Nicht-Datei systemshellcontainer](#non-file-system-shell-containers)
  - [Bibliotheks Beschreibungen](#library-descriptions)
- [Zugehörige Themen](#related-topics)

## <a name="libraries"></a>Bibliotheken

In Windows 7 und höher sind Bibliotheken das standardrepository von Benutzerdaten. Benutzer können Ihre Dateien auf die gleiche Weise durchsuchen wie in einem Ordner, oder Sie können Ihre Dateien nach Eigenschaften wie "Date", "Type" und "Author" anordnen. Im Gegensatz zu einem Ordner speichert eine Bibliothek nicht tatsächlich Elemente, sondern zeigt Dateien an, die gleichzeitig in mehreren Ordnern gespeichert sind. Bibliotheken bieten einen einzelnen Zugriffspunkt und umfangreiche Ansicht-Pivots für Benutzer Ihrer aggregierten Inhalte. Wenn ein Benutzer beispielsweise über Musikdateien in Ordnern auf einem externen Laufwerk zusätzlich zum Ordner **eigene Musik** verfügt, kann er sofort auf alle Musikdateien über die Musikbibliothek zugreifen.

### <a name="user-data-entry-points"></a>Einstiegspunkte für Benutzerdaten

Standardbibliotheken (z. b. **eigene** Dateien, **eigene Bilder** usw.) entsprechen dem [bekannten Ordner](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). Standardbibliotheken stellen Benutzern vertraute Einstiegspunkte zur Verfügung, aber da Bibliotheksinhalte nicht auf bekannte Ordner-Inhalts Bibliotheken beschränkt sind, haben Benutzer mehr Freiheit, zu bestimmen, wo Dokumente und Medien gespeichert werden sollen. Bibliotheken werden über den Shell-Namespace (shelldatenquelle) verfügbar gemacht. Die Anwendung kann den Benutzern die gleichen vertrauten Einstiegspunkte für Ihre Daten bereitstellen, indem Sie die Bibliothek Informationen aktivieren und durchsuchen.

### <a name="collections-of-folders"></a>Ordner Sammlungen

Bibliotheken sind benutzerdefinierte Inhalts Auflistungen. Windows Search indiziert unterstützte Ordner, wenn Sie in Bibliotheken enthalten sind. Dies ermöglicht die sofortige Suche und Eigenschaften basierte Stapel Ansichts Sichten in Bibliotheken.

### <a name="supported-folders-in-libraries"></a>Unterstützte Ordner in Bibliotheken

Für Ordner, die in Bibliotheken unterstützt werden sollen, müssen Sie auf dem lokalen Computer indizierbar sein und entweder auf einem Windows-Remote Computer oder auf einem Server mit von Windows Search indizierten Dateien indiziert werden.

Nicht unterstützte Ordner können von Benutzern im Dialogfeld "Windows-Bibliotheksverwaltung" nicht mehr hinzugefügt werden. Wenn nicht indizierte Remote Ordner einer Bibliothek mithilfe der [ishelllibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) -API hinzugefügt werden, wird die Benutzer Darstellung der Bibliothek auf den **Modus** für die Bibliotheks Sicherheit zurückgesetzt. Im abgesicherten **Modus** werden Features wie Eigenschaften basierte Stapel Ansichts Ansichten, Filter Vorschläge und die Suchunterstützung für das **Start Menü** aus der betroffenen Bibliothek entfernt.

In der folgenden Tabelle werden die in Bibliotheken enthaltenen Ordner mithilfe des Dialog Felds Bibliothek Verwaltung von Windows Explorer und Ordner aufgelistet, die im abgesicherten **Modus** nicht unterstützt werden:

| Unterstützte Ordner                                                                                                                            | Nicht unterstützte Ordner                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Feste und externe NTFS-und FAT32-Festplatten                                                                                                | Wechsel Datenträger (z. b. Finger und SD-Karten)                                                     |
| Von Windows Search indizierte Freigaben (z. b. Abteilungs Server und Computer, auf denen Windows 10 und Windows 7 Home Edition ausgeführt wird) | Wechselmedien (z. b. CDs und DVDs)                                                                  |
| Offline verfügbare Freigaben (z. b. **umgeleitete Eigene Dokumente**, **Client seitiger Cache**)                                               | Netzwerkfreigaben, die weder Offline noch Remote indiziert sind (z. b. NAS-Laufwerke)             |
| –                                                                                                                                          | Andere Datenquellen (z. b. Microsoft SharePoint, Microsoft Exchange, Microsoft onedrive usw.) |

### <a name="storage-backed"></a>Storage-Backed

Bibliotheken sind Sammlungen von Speicher Ordnern. Benutzer können Dateien direkt in eine Bibliothek speichern und kopieren, da jede Bibliothek über einen Standard Speicherort verfügt, an den diese Dateien gesendet werden. Bei Standardbibliotheken ist dies ein Benutzer bekannter Ordner, der in einer Bibliothek (z. b. " **Eigene Dokumente**") enthalten ist, oder der erste Ordner, der einer benutzerdefinierten Bibliothek hinzugefügt wird. Dabei handelt es sich um den Ordner, in dem Dateien gespeichert werden, wenn ein Benutzer die Dateien in eine Bibliothek zieht, oder Sie speichert Sie in einer Bibliothek mit dem allgemeinen Datei Dialogfeld. Der Benutzer kann den Standard Speicherort einer Bibliothek jederzeit ändern. wenn er jedoch den Standard Speicherort entfernt, wird der nächste Ordner in der Bibliothek als neuer Speicherort ausgewählt. Benutzer können zusätzlich in einem Ordner speichern, für den Sie über Berechtigungen verfügen, die in einer Bibliothek enthalten sind.

### <a name="non-file-system-shell-containers"></a>Nicht-Datei systemshellcontainer

Bibliotheken können Dateisystem-shellcontainer enthalten, wie z. b. **Computer** und System **Steuerung**, aber auch Dateisystem Elemente enthalten. Bibliotheks Ordner und-Inhalte können mithilfe von APIs für Dateisystem Dateien und-Ordner in früheren Betriebssystemen aufgelistet und darauf zugegriffen werden. Wenn Ihre Anwendung stark von Dateisystem spezifischen APIs abhängig ist, kann die [ishelllibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) -API verwendet werden, um die Dateisystem Pfade von Ordnern und Dateien innerhalb von Bibliotheken abzurufen. In den meisten Fällen wird empfohlen, das shellprogrammierungs Modell zu verwenden, um mehrere Windows-Versionen und Element Flexibilität zu unterstützen. Weitere Informationen finden Sie unter [Navigieren im Shell-Namespace](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Bibliotheks Beschreibungen

Bibliotheks Beschreibungen werden auf dem Datenträger als XML-Datei im Ordner% APPDATA% Microsoft \\ Windows- \\ Bibliotheken (und potenziell als **folderid- \_ Bibliotheken**) gespeichert. Weitere Informationen zu **folderid- \_ Bibliotheken** finden Sie unter [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Bibliotheks Beschreibungsdateien sind XML-Dateien mit der Dateinamenerweiterung. Library-ms. Diese Dateien sollten nie von Anwendungen abgerufen oder bearbeitet werden. Der in den Bibliotheks Beschreibungsdateien beibehaltene Ordner Pfad Text ist nicht immer aktuell. Bibliotheks Ordner werden in der Bibliotheks Beschreibungsdatei im serialisierten Binary [Shell Links](/windows/desktop/shell/links) -Format beibehalten. Weitere Informationen zu Bibliotheken und zum Beschreibungs Schema der Bibliothek finden Sie unter [Bibliotheks Beschreibungs Schema](../shell/library-schema-entry.md). Weitere Informationen zu Verbund Suchconnectors und zum Beschreibungs Schema des Suchconnectors finden Sie unter [Connector Description Schema](search-sconn-desc-schema-entry.md).

> [HINWEIS]  
> Anwendungen sollten immer das shellprogrammierungs Modell oder die [ishelllibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) -API verwenden, um Bibliotheksinhalte zu nutzen und zu bearbeiten, und nie versuchen, manuell auf die Bibliotheks Beschreibungsdatei zuzugreifen oder diese zu bearbeiten.

## <a name="related-topics"></a>Zugehörige Themen

[Windows 7-Suche](./-search-3x-wds-overview.md)

[Neu bei der Windows 7-Suche](new-for-windows-7-search.md)

[Indizieren von Priorisierungs-und rowsetereignissen in Windows 7](indexing-prioritization-and-rowset-events.md)