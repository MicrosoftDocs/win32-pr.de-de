---
title: Aktivieren der DRM-Unterstützung
description: Aktivieren der DRM-Unterstützung
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Medienformat-SDK, aktivieren der DRM-Unterstützung
- Advanced Systems Format (ASF), aktivieren der DRM-Unterstützung
- ASF (Advanced Systems Format), aktivieren der DRM-Unterstützung
- Digital Rights Management (DRM), Aktivieren der Unterstützung
- DRM (Digital Rights Management), Aktivieren der Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dca900089e93b9f2c149f1e349bdf5b91f88a7c3d549b5f54147839a8ed9296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089750"
---
# <a name="enabling-drm-support"></a>Aktivieren der DRM-Unterstützung

Sie können das Microsoft Windows Media Format Software Development Kit (SDK) verwenden, um Anwendungen zu erstellen, die DRM-Schutz (Digital Rights Management) anwenden und Live-DRM-Streams oder DRM-geschützte Dateien wiedergeben können. Außerdem wird Unterstützung für das Sichern und Wiederherstellen der DRM-Lizenzen eines Players sowie für die [*Individualisierung*](wmformat-glossary.md) von Playern bereitgestellt.

In dieser Dokumentation wird davon ausgegangen, dass Sie mit der Digital Rights Management-Technologie von Microsoft vertraut sind. Eine grundlegende Übersicht über Windows Media DRM finden Sie im Abschnitt [Digital Rights Management Features](digital-rights-management-features.md) dieser Dokumentation. Weitere Informationen zu DRM finden Sie auf der Seite Digitale Rights Management auf der [Microsoft-Website](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

In den folgenden Abschnitten wird beschrieben, wie Sie die DRM-Unterstützung aktivieren.



| `Section`                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Abrufen der erforderlichen DRM-Bibliothek](obtaining-the-required-drm-library.md)                                                   | Beschreibt die Schritte, die zum Abrufen der statischen Bibliothek erforderlich sind, um DRM-fähige Anwendungen zu erstellen.                                                                               |
| [DRM-Schutz und Inhaltslizenzverteilung](drm-protection-and-content-license-distribution.md)                         | Vergleicht die DRM-Funktionen des Windows Media Format SDK mit dem Windows Media Rights Manager SDK.                                                                                        |
| [DRM-Netzwerkvorgänge](drm-network-operations.md)                                                                           | Beschreibt, wie Ihre Anwendung die DRM-Vorgänge behandeln soll, die über das Internet oder andere Netzwerke kommunizieren.                                                                          |
| [Erstellen geschützter Dateien](creating-protected-files.md)                                                                       | Beschreibt, wie DRM-geschützte Dateien erstellt werden.                                                                                                                                                    |
| [Lesen von geschützten Dateien](reading-protected-files.md)                                                                         | Beschreibt Möglichkeiten zum Erwerben von Lizenzen für Inhalte und die Vorteile der Implementierung des automatischen Lizenzerwerbs.                                                                                     |
| [Anzeigen von Attributen von geschützten Dateien](viewing-attributes-of-protected-files.md)                                             | Beschreibt, wie die [**IWMDRMEditor-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) für das Metadaten-Editor-Objekt verwendet wird, um Attribute geschützter Dateien anzuzeigen, ohne über die erforderliche statische Bibliothek für DRM zu verfügen. |
| [Arbeiten mit Sperrlisten](working-with-revocation-lists.md)                                                             | Beschreibt Sperrlisten und deren Implementierung.                                                                                                                                        |
| [Sichern und Wiederherstellen von Lizenzen](backing-up-and-restoring-licenses.md)                                                     | Beschreibt, wie Benutzer ihre Inhaltslizenzen verwalten können, indem sie sie auf ihrem aktuellen Computer oder auf anderen Computern sichern und wiederherstellen.                                                         |
| [Individualisieren von DRM-Anwendungen](individualizing-drm-applications.md)                                                       | Beschreibt, wie die [*Individualisierungsfunktion*](wmformat-glossary.md) die Sicherheit in einem DRM-System erhöht.                                                           |
| [Arbeiten mit Ausgabeschutzebenen](working-with-output-protection-levels.md)                                             | Beschreibt die Unterstützung von Ausgabeschutzebenen, die zum Aufzeichnen zulässiger Aktionen in DRM-Lizenzen der Version 10 verwendet werden.                                                                         |
| [Verwenden des Windows Media DRM 10 for Network Devices Protocol](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Beschreibt die Unterstützung von sicherem Gerätestreaming mithilfe des Windows Media DRM 10 for Network Devices-Protokolls.                                                                                |
| [Implementieren der Lizenzsperrung](implementing-license-revocation.md)                                                         | Beschreibt den Prozess der Lizenzsperrung und die Aktionen, die Ihre Anwendung ausführen muss, um sie zu implementieren.                                                                                        |
| [Brennen von Wiedergabelisten, die sichere Dateien enthalten](burning-playlists-that-contain-secure-files.md)                                 | Beschreibt, wie Wiedergabelistenwiedergaben in Ihrer Anwendung implementiert werden.                                                                                                                                |



 

Das SDK enthält mehrere Beispielanwendungen, die veranschaulichen, wie geschützte Dateien gelesen werden. Das umfassendste Beispiel ist DRMShow. Weitere Informationen finden Sie unter [Beispielanwendungen.](sample-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features**](features.md)
</dt> </dl>

 

 




