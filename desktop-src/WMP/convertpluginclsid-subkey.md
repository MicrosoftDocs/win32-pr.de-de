---
title: Convertpluginclsid-Unterschlüssel
description: Convertpluginclsid-Unterschlüssel
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player, convertpluginclsid-Unterschlüssel
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, convertpluginclsid-Unterschlüssel
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Convertpluginclsid-Unterschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037055"
---
# <a name="convertpluginclsid-subkey"></a>Convertpluginclsid-Unterschlüssel

Wenn Windows Media Player 11 auf eine benutzerdefinierte Dateierweiterung stößt, sucht Sie nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben. In einigen Fällen verfügt der Unterschlüssel der Erweiterung über einen Unterschlüssel namens **convertpluginclsid**.

Nehmen Sie beispielsweise an, Sie haben ein benutzerdefiniertes Dateiformat (mit der Dateinamenerweiterung. XYZ) und ein Konvertierungs-Plug-in erstellt, das die Dateien in ein von Windows unterstütztes Format konvertiert Media Player dann würden Sie die Klassen-ID des Plug-ins in einem oder beiden der folgenden untergeordneten Schlüssel speichern.

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . XYZ \\ convertpluginclsid**

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Player \\ Extensions \\ . XYZ \\ convertpluginclsid**

Der **convertpluginclsid** -Unterschlüssel gibt die Klassen-IDs von Plug-ins an, die von Windows Media Player verwendet werden können, um eine Mediendatei aus dem benutzerdefinierten Format in ein Format zu konvertieren, das vom Player unterstützt wird.

Der **convertpluginclsid** -Unterschlüssel weist die folgenden Einträge auf.

-   Ein Standardeintrag, der das Standard Konvertierungs-Plug-in darstellt.
-   Ein benannter Eintrag, der das Standard Konvertierungs-Plug-in darstellt.
-   Zusätzliche benannte Einträge, die Alternative konvertierungsplug-ins darstellen.

Nehmen Sie beispielsweise an, ein benutzerdefiniertes Dateiformat verfügt über ein Standard Konvertierungs-Plug-in und zwei alternative Konvertierungs-Plug-ins. Die Registrierungseinträge unter dem **convertpluginclsid** -Unterschlüssel weisen die folgende Form auf:



| Name                                                                          | type        | Wert                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Standard                                                                       | **REG- \_ SZ** | Die Klassen-ID des Standard Konvertierungs-Plug-ins im Registrierungs Format. |
| Die Klassen-ID des Standard Konvertierungs-Plug-ins im Registrierungs Format.          | **REG- \_ SZ** | Der Anzeige Name des Standard Konvertierungs-Plug-ins.                 |
| Die Klassen-ID im Registrierungs Format des ersten alternativen Konvertierungs-Plug-ins.  | **REG- \_ SZ** | Der Anzeige Name des ersten alternativen Konvertierungs-Plug-ins.         |
| Die Klassen-ID im Registrierungs Format des zweiten Alternativen Konvertierungs-Plug-ins. | **REG- \_ SZ** | Der Anzeige Name des zweiten Alternativen Konvertierungs-Plug-ins.        |



 

Beachten Sie, dass das Standard Konvertierungs-Plug-in durch zwei Registrierungseinträge dargestellt wird: der Standardeintrag und ein benannter Eintrag. Windows Media Player verwendet den Standardeintrag, um zu bestimmen, welches Plug-in das standardmäßige (primäre) Konvertierungs-Plug-in ist. Windows Media Player verwendet die benannten Einträge zum Abrufen von anzeigen Amen für alle Konvertierungs-Plug-ins, einschließlich des Standard-Plug-ins.

Der Anzeige Name eines Konvertierungs-Plug-ins wird von dem Unternehmen bestimmt, das das Plug-in erstellt. In Windows Media Player kann der Anzeige Name in der Benutzeroberfläche angezeigt werden.

Wenn Windows Media Player versucht, eine Datei aus einem benutzerdefinierten Format in ein Standardformat zu konvertieren, wird zuerst das Standard-Plug-in geladen. Wenn das Standard-Plug-in die Datei nicht konvertieren kann und die \_ Datei \_ Besitzer NS E WMP \_ Convert Plugin UNKNOWN zurückgibt \_ \_ \_ \_ , lädt der Player jedes Alternative Plug-in, bis eine erfolgreiche Konvertierung erfolgt, oder es sind keine weiteren Plug-ins zum ausprobieren vorhanden. Der Player zeigt keine Warnmeldung an, wenn kein Konvertierungs-Plug-in für die Dateinamenerweiterung gefunden wird.

Der Registrierungs Eintrag **convertpluginclsid** wird von Windows Media Player 11 unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen für die Dateinamenerweiterung**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Windows Media Player-Konvertierungs-Plug-ins**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




