---
title: Registrierungs Eintrag für Berechtigungen
description: Registrierungs Eintrag für Berechtigungen
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Berechtigungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Berechtigungen
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038532"
---
# <a name="permissions-registry-entry"></a>Registrierungs Eintrag für Berechtigungen

Wenn Windows Media Player auf eine benutzerdefinierte Dateierweiterung trifft, sucht es nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben. Einer der Registrierungseinträge, der unter dem Unterschlüssel der Erweiterung angezeigt werden kann, ist der **Berechtigungs** Eintrag.

Der **Berechtigungs** Eintrag gibt die Aktionen an, die Windows Media Player für Dateien mit der benutzerdefinierten Erweiterung ausführen darf. Der **Berechtigungs** Eintrag weist das folgende Format auf.



| Name        | type           | Wert                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Berechtigungen | **REG \_ DWORD** | Ein Satz von Flags, von denen jeder die Berechtigung für eine bestimmte Aktion erteilt. |



 

Der Wert des **Berechtigungs** Eintrags ist ein bitweises **or** von einem oder mehreren der folgenden Flags.



| Flag (Dezimalwert) | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Berechtigung für die Wiedergabe. Dateien mit der registrierten Dateinamenerweiterung können wiedergegeben werden.                                                                                                                                                                                       |
| 2                    | Berechtigung zum Löschen des Ordners. Dateien mit der registrierten Dateinamenerweiterung werden in die Wiedergabeliste eingeschlossen, die erstellt wird, wenn der Benutzer einen Ordner zieht, der die Dateien enthält, und ihn auf der Benutzeroberfläche des Players ablegen.                                                      |
| 4                    | Berechtigung für Medien-CD. Dateien mit der registrierten Dateinamenerweiterung werden in die Wiedergabeliste eingeschlossen, die erstellt wird, wenn eine CD, die die Dateien enthält, in das CD-ROM-Laufwerk eingefügt wird.                                                                                           |
| 8                    | Berechtigung für die Bibliothek. Dateien mit der Dateinamenerweiterung "registriert" können der Bibliothek hinzugefügt werden. Erforderlich für Konvertierungs-Plug-ins.                                                                                                                                    |
| 16                   | Berechtigung für HTML-Streaming. Dateien mit der registrierten Dateinamenerweiterung werden in den Internet Explorer-Cache eingefügt, wenn Sie von einem Webstream übermittelt werden.                                                                                                            |
| 128                  | Berechtigung für die Transcodierung. Dateien mit der registrierten Dateinamenerweiterung können unter bestimmten Bedingungen in das Windows Media-Format transcodiert werden. Weitere Informationen finden Sie unter [iwmptranscodepolicy:: allowtranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Erfordert Windows Media Player 10 oder höher. |



 

Wenn der Benutzer versucht, eine Mediendatei mit einer benutzerdefinierten Dateinamenerweiterung wiederzugeben, sucht Windows Media Player nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht. Wenn keine Entsprechung gefunden wird, wird dem Benutzer ein Warn Dialogfeld angezeigt, in dem der Benutzer zur Eingabe der Berechtigung aufgefordert wird, die Datei wiederzugeben. Wenn Sie digitale Mediendateien mit benutzerdefinierten Dateinamen Erweiterungen erstellen, können Sie verhindern, dass diese Warnung auf dem Computer des Benutzers angezeigt wird, indem Sie die Dateinamenerweiterung registrieren und einen **Berechtigungs** Eintrag angeben.

Der **Berechtigungs** Eintrag (mit Ausnahme des Flagwerts 128) wird von der Windows Media Player 9-Serie und höher unterstützt. Der Flagwert 128 wird von Windows Media Player 10 und höher unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen für die Dateinamenerweiterung**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




