---
title: ConvertPluginCLSID-Unterschlüssel
description: ConvertPluginCLSID-Unterschlüssel
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player,ConvertPluginCLSID-Unterschlüssel
- Windows Media Player,Dateierweiterungen
- Windows Media Player,Registrierung
- Registrierung, Dateinamenerweiterungen
- registry,ConvertPluginCLSID-Unterschlüssel
- registry,settings for Windows Media Player
- Registrierungseinstellungen der Dateinamenerweiterung
- ConvertPluginCLSID-Unterschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5deeda3e7eb0b5fe465152aa7711717d086c94a06ebed4f9549dc9f6a9b62dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341664"
---
# <a name="convertpluginclsid-subkey"></a>ConvertPluginCLSID-Unterschlüssel

Wenn Windows Media Player 11 auf eine benutzerdefinierte Dateierweiterung trifft, sucht er nach einem Registrierungsunterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird unter [Dateinamenerweiterungsregistrierung Einstellungen.](file-name-extension-registry-settings.md) In einigen Fällen verfügt der Unterschlüssel der Erweiterung über einen Unterschlüssel namens **ConvertPluginCLSID**.

Angenommen, Sie haben ein benutzerdefiniertes Dateiformat (mit der Dateinamenerweiterung .xyz) und ein Konvertierungs-Plug-In erstellt, das die Dateien in ein von Windows Media Player unterstütztes Format konvertiert. Anschließend speichern Sie die Klassen-ID des Plug-Ins in einem oder beiden der folgenden Unterschlüssel.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Multimedia \\ WMPlayer \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

Der **Unterschlüssel ConvertPluginCLSID** gibt die Klassen-IDs von Plug-Ins an, mit denen Windows Media Player eine Mediendatei aus dem benutzerdefinierten Format in ein vom Player unterstütztes Format konvertieren kann.

Der **Unterschlüssel ConvertPluginCLSID** verfügt über die folgenden Einträge.

-   Ein Standardeintrag, der das Standardkonvertierungs-Plug-In darstellt.
-   Ein benannter Eintrag, der das Standardkonvertierungs-Plug-In darstellt.
-   Zusätzliche benannte Einträge, die alternative Konvertierungs-Plug-Ins darstellen.

Angenommen, ein benutzerdefiniertes Dateiformat verfügt über ein Standardkonvertierungs-Plug-In und zwei alternative Konvertierungs-Plug-Ins. Die Registrierungseinträge unter dem **Unterschlüssel ConvertPluginCLSID** haben das folgende Formular.



| Name                                                                          | type        | Wert                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Standard                                                                       | **REG \_ SZ** | Die Klassen-ID des Standardkonvertierungs-Plug-Ins im Registrierungsformat. |
| Die Klassen-ID des Standardkonvertierungs-Plug-Ins im Registrierungsformat.          | **REG \_ SZ** | Der Angezeigte Name des Standardkonvertierungs-Plug-Ins.                 |
| Die Klassen-ID des ersten alternativen Konvertierungs-Plug-Ins im Registrierungsformat.  | **REG \_ SZ** | Der Benutzername des ersten alternativen Konvertierungs-Plug-Ins.         |
| Die Klassen-ID des zweiten alternativen Konvertierungs-Plug-Ins im Registrierungsformat. | **REG \_ SZ** | Der Benutzername des zweiten alternativen Konvertierungs-Plug-Ins.        |



 

Beachten Sie, dass das Standardkonvertierungs-Plug-In durch zwei Registrierungseinträge dargestellt wird: den Standardeintrag und einen benannten Eintrag. Windows Media Player verwendet den Standardeintrag, um zu bestimmen, welches Plug-In das (primäre) Standardkonvertierungs-Plug-In ist. Windows Media Player verwendet die benannten Einträge, um Diesnamen für alle Konvertierungs-Plug-Ins einschließlich des Standard-Plug-Ins zu erhalten.

Der Benutzername eines Konvertierungs-Plug-Ins wird von dem Unternehmen bestimmt, das das Plug-In erstellt. Windows Media Player Anzeigename wird möglicherweise auf der Benutzeroberfläche angezeigt.

Wenn Windows Media Player versucht, eine Datei aus einem benutzerdefinierten Format in ein Standardformat zu konvertieren, wird zuerst das Standard-Plug-In geladen. Wenn das Standard-Plug-In die Datei nicht konvertieren kann und NS E WMP CONVERT PLUGIN UNKNOWN FILE OWNER zurückgibt, lädt der Player jedes alternative Plug-In, bis eine erfolgreiche Konvertierung erfolgt oder keine \_ \_ \_ \_ \_ \_ \_ Plug-Ins mehr versucht werden. Der Player zeigt keine Warnmeldung an, wenn kein Konvertierungs-Plug-In für die Dateierweiterung gefunden wurde.

Der **Registrierungseintrag ConvertPluginCLSID** wird von Windows Media Player 11 unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierung der Dateinamenerweiterung Einstellungen**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Windows Media Player Konvertierungs-Plug-Ins**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




