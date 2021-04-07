---
title: Registrierungs Einstellungen für die Dateinamenerweiterung
description: Registrierungs Einstellungen für die Dateinamenerweiterung
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player, Registrierung
- Windows Media Player, Dateinamen Erweiterungen
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712953"
---
# <a name="file-name-extension-registry-settings"></a>Registrierungs Einstellungen für die Dateinamenerweiterung

Wenn Ihre digitalen Mediendateien ein benutzerdefiniertes Format aufweisen, können Sie Windows Media Player Informationen über Ihr benutzerdefiniertes Format bereitstellen, indem Sie Einträge in der Registrierung auf dem Computer des Benutzers platzieren. Windows Media Player überprüft Ihre Registrierungseinträge, um zu bestimmen, wie die Dateien verarbeitet werden sollen. In der folgenden Liste sind einige Möglichkeiten aufgeführt, mit denen Sie Registrierungseinträge erstellen können, die das benutzerdefinierte Mediendatei Format betreffen.

-   Erteilen Sie dem Player die Berechtigung, Ihre Dateien wiederzugeben, zu kopieren oder zu transcodieren.
-   Geben Sie die zugrunde liegende Technologie an, die der Player für die Wiedergabe Ihrer Dateien verwenden soll.
-   Geben Sie an, wo die Dateien in der Bibliotheks Ansicht des Players angezeigt werden sollen.
-   Geben Sie ein Plug-in an, das der Player verwenden soll, um die Dateien in ein Standardformat zu konvertieren.
-   Geben Sie einen MTP-Format Code (Media Transport Protocol) an, mit dem der Player feststellen kann, ob ein bestimmtes tragbares Gerät das Dateiformat unterstützt.

Die meisten Einträge, die Sie bereitstellen, befinden sich unter einem Unterschlüssel, der der benutzerdefinierten Dateinamenerweiterung zugeordnet ist. Sie können diesen Unterschlüssel in der Unterstruktur HKEY \_ local \_ Machine und in der HKEY \_ Current \_ User-Unterstruktur erstellen. Windows Media Player sucht zuerst in der Unterstruktur des lokalen HKEY-Computers \_ \_ . Wenn er nicht finden kann, was er benötigt, sucht er in der aktuellen HKEY- \_ \_ Benutzer Unterstruktur. Beachten Sie, dass jeder Code, der versucht, in die Registrierung auf dem Computer des Benutzers zu schreiben, in die HKEY-Unterstruktur des lokalen Computers schreiben kann, \_ \_ Wenn der aktuelle Benutzer über Administratorrechte verfügt.

Um Informationen über das benutzerdefinierte Dateiformat in die Unterstruktur des lokalen HKEY-Computers zu schreiben \_ \_ , erstellen Sie den folgenden Unterschlüssel.

**HKEY \_ Lokale \_ Computer \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\** *CustomExtension*

Dabei ist *CustomExtension* die Dateinamenerweiterung, einschließlich des Punkt Trennzeichens (.). Wenn beispielsweise die Erweiterung für Ihr benutzerdefiniertes Dateiformat. XYZ lautet, erstellen Sie den folgenden Unterschlüssel.

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . XYZ**

Um Informationen über das benutzerdefinierte Dateiformat in die HKEY \_ Current \_ User-Teilstruktur zu schreiben, erstellen Sie den folgenden Unterschlüssel.

**HKEY \_ Aktuelle \_ Benutzer \\ Software \\ Microsoft \\ Media Player \\ Player \\ Extensions \\** *CustomExtension*

Sie können einen oder mehrere der folgenden Einträge in den Unterschlüssel *CustomExtension* schreiben.

-   **Berechtigungen**
-   **Laufzeit**
-   **Formatcode**

Um Konvertierungs-Plug-Ins für Ihr benutzerdefiniertes Mediendatei Format anzugeben, erstellen Sie einen **convertpluginclsid** -Unterschlüssel in Ihrem *CustomExtension* -Unterschlüssel.

Um anzugeben, wo Windows Media Player die Dateien in der Bibliotheks Ansicht anzeigen soll, schreiben Sie einen Eintrag, der das benutzerdefinierte Dateiformat im folgenden Unterschlüssel darstellt.

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Media Player \\ MLS \\ Extensions**

In den folgenden Themen werden die Registrierungs Unterschlüssel und-Einträge beschrieben, die Windows-Media Player Informationen zu benutzerdefinierten Mediendatei Formaten bereitstellen.

-   [Registrierungs Eintrag für Berechtigungen](permissions-registry-entry.md)
-   [Registrierungs Eintrag für die Laufzeit](runtime-registry-entry.md)
-   [Registrierungs Eintrag "Formatcode"](formatcode-registry-entry.md)
-   [Registrierungseinträge für die Bibliotheks Klassifizierung](library-classification-registry-entries.md)
-   [Convertpluginclsid-Unterschlüssel](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> <dt>

[**Windows Media Player-Konvertierungs-Plug-ins**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




