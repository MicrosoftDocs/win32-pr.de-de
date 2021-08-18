---
title: Einstellungen der Dateinamenerweiterungsregistrierung
description: Einstellungen der Dateinamenerweiterungsregistrierung
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player,Registrierung
- Windows Media Player,Dateinamenerweiterungen
- Registrierung, Dateinamenerweiterungen
- Registrierung, Einstellungen für Windows Media Player
- Registrierungseinstellungen für die Dateinamenerweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4acea080c59b4f78d4b4053f6ae67e5d1eb2c820d68b4e4702485130d8f33a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996630"
---
# <a name="file-name-extension-registry-settings"></a>Einstellungen der Dateinamenerweiterungsregistrierung

Wenn Ihre digitalen Mediendateien ein benutzerdefiniertes Format aufweisen, können Sie Windows Media Player mit Informationen zu Ihrem benutzerdefinierten Format bereitstellen, indem Sie Einträge in der Registrierung auf dem Computer des Benutzers platzieren. Windows Media Player überprüft Ihre Registrierungseinträge, um zu bestimmen, wie sie Ihre Dateien behandeln sollen. Die folgende Liste zeigt einige der Möglichkeiten zum Erstellen von Registrierungseinträgen, die sich auf Ihr benutzerdefiniertes Mediendateiformat beziehen.

-   Erteilen Sie dem Player die Berechtigung zum Wiedergeben, Kopieren oder Transcodieren Ihrer Dateien.
-   Geben Sie die zugrunde liegende Technologie an, die der Player zum Wiedergeben Ihrer Dateien verwenden soll.
-   Geben Sie an, wo der Player Ihre Dateien in der Bibliotheksansicht anzeigen soll.
-   Geben Sie ein Plug-In an, das der Player verwenden soll, um Ihre Dateien in ein Standardformat zu konvertieren.
-   Geben Sie einen MTP-Formatcode (Media Transport Protocol) an, mit dem der Player bestimmen kann, ob ein bestimmtes portables Gerät Ihr Dateiformat unterstützt.

Die meisten einträge, die Sie angeben, werden unter einem Unterschlüssel gespeichert, der Ihrer benutzerdefinierten Dateinamenerweiterung zugeordnet ist. Sie können diesen Unterschlüssel in der Unterstruktur HKEY \_ LOCAL MACHINE und in der \_ Unterstruktur HKEY \_ CURRENT USER \_ erstellen. Windows Media Player wird zuerst in der Unterstruktur HKEY \_ LOCAL \_ MACHINE gesucht. Wenn die Benötigten dort nicht gefunden werden, wird in der Unterstruktur HKEY \_ CURRENT \_ USER gesucht. Beachten Sie, dass jeder Code, der versucht, in die Registrierung auf dem Computer des Benutzers zu schreiben, nur dann in die \_ HKEY LOCAL \_ MACHINE-Unterstruktur schreiben kann, wenn der aktuelle Benutzer über Administratorrechte verfügt.

Um Informationen zu Ihrem benutzerdefinierten Dateiformat in die Unterstruktur HKEY LOCAL MACHINE zu \_ \_ schreiben, erstellen Sie den folgenden Unterschlüssel.

**HKEY \_ LOCAL \_ MACHINE Software Microsoft Multimedia \\ \\ \\ \\ WMPlayer \\ Extensions \\** *customExtension*

wobei *customExtension* die Dateinamenerweiterung einschließlich des Punkttrennzeichens (.) ist. Wenn die Erweiterung für Ihr benutzerdefiniertes Dateiformat beispielsweise ".xyz" lautet, erstellen Sie den folgenden Unterschlüssel.

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer Extensions \\ \\ .xyz**

Um Informationen zu Ihrem benutzerdefinierten Dateiformat in die \_ HKEY CURRENT \_ USER-Unterstruktur zu schreiben, erstellen Sie den folgenden Unterschlüssel.

**HKEY \_ CURRENT \_ USER Software Microsoft \\ \\ \\ MediaPlayer Player \\ \\ Extensions \\** *customExtension*

Sie können einen oder mehrere der folgenden Einträge in Ihren *CustomExtension-Unterschlüssel* schreiben.

-   **Berechtigungen**
-   **Laufzeit**
-   **FormatCode**

Um Konvertierungs-Plug-Ins für Ihr benutzerdefiniertes Mediendateiformat anzugeben, erstellen Sie einen **ConvertPluginCLSID-Unterschlüssel** in Ihrem *customExtension-Unterschlüssel.*

Um anzugeben, wo Windows Media Player Ihre Dateien in der Bibliotheksansicht anzeigen soll, schreiben Sie einen Eintrag, der Ihr benutzerdefiniertes Dateiformat im folgenden Unterschlüssel darstellt.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

In den folgenden Themen werden die Registrierungsunterschlüssel und -einträge beschrieben, die Windows Media Player mit Informationen zu benutzerdefinierten Mediendateiformaten bereitstellen.

-   [Registrierungseintrag "Berechtigungen"](permissions-registry-entry.md)
-   [Laufzeitregistrierungseintrag](runtime-registry-entry.md)
-   [Registrierungseintrag "FormatCode"](formatcode-registry-entry.md)
-   [Einträge in der Bibliotheksklassifizierungsregistrierung](library-classification-registry-entries.md)
-   [ConvertPluginCLSID-Unterschlüssel](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> <dt>

[**Windows Media Player Konvertierungs-Plug-Ins**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




