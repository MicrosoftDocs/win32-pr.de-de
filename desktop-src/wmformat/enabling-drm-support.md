---
title: Aktivieren DRM-Unterstützung
description: Aktivieren DRM-Unterstützung
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Media Format SDK, Aktivieren der DRM-Unterstützung
- Advanced Systems Format (ASF), Aktivieren der DRM-Unterstützung
- ASF (Advanced Systems Format), Aktivieren der DRM-Unterstützung
- Digital Rights Management (DRM), Aktivieren der Unterstützung
- DRM (Digital Rights Management), Aktivieren der Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106341971"
---
# <a name="enabling-drm-support"></a>Aktivieren DRM-Unterstützung

Sie können das Microsoft Windows Media-Format Software Development Kit (SDK) verwenden, um Anwendungen zu erstellen, die Digital Rights Management-Schutz (DRM) anwenden und Live-DRM-Streams oder DRM-geschützte Dateien abspielen können. Unterstützung wird auch zum Sichern und Wiederherstellen der DRM-Lizenzen eines Players und zum [*individualisieren*](wmformat-glossary.md) von Playern bereitgestellt.

In dieser Dokumentation wird davon ausgegangen, dass Sie eine grundlegende Vertrautheit mit der Digital Rights Management-Technologie von Microsoft haben. Eine grundlegende Übersicht über Windows Media DRM finden Sie in dieser Dokumentation im Abschnitt [Funktionen für digitale Rights Management](digital-rights-management-features.md) . Weitere Informationen zu DRM finden Sie auf der [Microsoft](https://windows.microsoft.com/windows/products/windows-media)-Website auf der Seite Digital Rights Management.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

In den folgenden Abschnitten wird beschrieben, wie Sie DRM-Unterstützung aktivieren.



| `Section`                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Abrufen der erforderlichen DRM-Bibliothek](obtaining-the-required-drm-library.md)                                                   | Beschreibt die Schritte, die zum Abrufen der statischen Bibliothek erforderlich sind, die zum Erstellen von DRM-fähigen Anwendungen erforderlich ist.                                                                               |
| [DRM-Schutz und Inhalts Lizenz Verteilung](drm-protection-and-content-license-distribution.md)                         | Vergleicht die DRM-Funktionen des Windows Media Format SDK mit dem Windows Media Rights Manager SDK.                                                                                        |
| [DRM-Netzwerk Vorgänge](drm-network-operations.md)                                                                           | Beschreibt, wie Ihre Anwendung die DRM-Vorgänge verarbeiten soll, die über das Internet oder andere Netzwerke kommunizieren.                                                                          |
| [Erstellen geschützter Dateien](creating-protected-files.md)                                                                       | Beschreibt das Erstellen von DRM-geschützten Dateien.                                                                                                                                                    |
| [Geschützte Dateien werden gelesen.](reading-protected-files.md)                                                                         | Beschreibt Möglichkeiten zum Erwerb von Lizenzen für Inhalte und die Vorteile der Implementierung der automatischen Lizenz Beschaffung.                                                                                     |
| [Anzeigen der Attribute geschützter Dateien](viewing-attributes-of-protected-files.md)                                             | Beschreibt, wie die [**iwmdrmeditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) -Schnittstelle für das Metadaten-Editor-Objekt verwendet wird, um Attribute geschützter Dateien anzuzeigen, ohne dass die erforderliche statische Bibliothek für DRM vorhanden ist. |
| [Arbeiten mit Sperr Listen](working-with-revocation-lists.md)                                                             | Beschreibt Sperr Listen und deren Implementierung.                                                                                                                                        |
| [Sichern und Wiederherstellen von Lizenzen](backing-up-and-restoring-licenses.md)                                                     | Beschreibt, wie Benutzer ihre Inhalts Lizenzen verwalten können, indem Sie Sie auf Ihrem aktuellen Computer oder auf anderen Computern sichern und wiederherstellen.                                                         |
| [Individualisieren von DRM-Anwendungen](individualizing-drm-applications.md)                                                       | Beschreibt, wie das Feature " [*Individualisierung*](wmformat-glossary.md) " die Sicherheit in einem DRM-System erhöht.                                                           |
| [Arbeiten mit Ausgabe Schutz Ebenen](working-with-output-protection-levels.md)                                             | Beschreibt die Unterstützung von Ausgabe Schutz Ebenen, die zum Aufzeichnen zulässiger Aktionen in DRM-Lizenzen der Version 10 verwendet werden.                                                                         |
| [Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"](using-the-windows-media-drm-10-for-network-devices-protocol.md) | In diesem Thema wird beschrieben, wie sicheres Geräte Streaming mithilfe des Windows Media DRM 10 for Network Devices-Protokolls unterstützt wird.                                                                                |
| [Implementieren der Lizenz Sperrung](implementing-license-revocation.md)                                                         | Beschreibt den Prozess der Lizenz Sperrung und die Aktionen, die Ihre Anwendung ausführen muss, um Sie zu implementieren.                                                                                        |
| [Brennen von Wiedergabelisten, die sichere Dateien enthalten](burning-playlists-that-contain-secure-files.md)                                 | Beschreibt, wie Wiedergabelisten brennen in der Anwendung implementiert wird.                                                                                                                                |



 

Das SDK enthält mehrere Beispielanwendungen, die veranschaulichen, wie geschützte Dateien gelesen werden. das vollständigste Beispiel ist drmshow. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features**](features.md)
</dt> </dl>

 

 




