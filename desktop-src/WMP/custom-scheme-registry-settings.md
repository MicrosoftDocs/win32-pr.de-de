---
title: Registrierungs Einstellungen für benutzerdefinierte Schemas
description: Registrierungs Einstellungen für benutzerdefinierte Schemas
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, Registrierungs Einstellungen für benutzerdefinierte Schemas
- Windows Media Player, Schemas
- Windows Media Player, Registrierung
- Registrierung, benutzerdefinierte Schema Einstellungen
- Registrierung, Schemas
- Registrierung, Einstellungen für Windows-Media Player
- Schemas
- Registrierungs Einstellungen für benutzerdefinierte Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036552"
---
# <a name="custom-scheme-registry-settings"></a>Registrierungs Einstellungen für benutzerdefinierte Schemas

Schemas sind benutzerdefinierte Protokolle. Windows Media Player verwaltet eine Liste der Schemas in der Registrierung auf dem Computer des Benutzers. Wenn der Benutzer versucht, eine digitale Mediendatei wiederzugeben, prüft der Spieler zunächst, ob das Windows Media Format SDK das Schema unterstützt. Wenn dies nicht der Fall ist, überprüft der Spieler das Schema anhand der Liste in der Registrierung. Wenn eine Entsprechung gefunden wird, überprüft der Spieler einen Wert, der angibt, welche zugrunde liegende Technologie oder *Laufzeit* (z. b. Microsoft DirectShow oder das Windows Media Format SDK) verwendet werden kann, um die Datei wiederzugeben. Wenn keine Entsprechung gefunden wird, wird dem Benutzer ein Warn Dialogfeld angezeigt, in dem der Benutzer zur Eingabe der Berechtigung aufgefordert wird, die Datei wiederzugeben. Wenn Sie digitale Mediendateien mit einem benutzerdefinierten Protokoll Schema streamen, können Sie verhindern, dass diese Warnung auf dem Computer des Benutzers angezeigt wird, indem Sie das Schema registrieren und einen Wert für die Laufzeit bereitstellen.

Die Liste der Schemas wird als Satz von Registrierungs Schlüsseln verwaltet, die den registrierten Schemas entsprechen, ohne den Doppelpunkt und die beiden Schrägstriche (://). Beispielsweise wird der Schlüssel für das wmhtml://-Schema, das zum Streamen von Rich-Media-Daten verwendet wird, als "wmhtml" bezeichnet. Für den lokalen Computer und für jeden Benutzer wird eine separate Liste beibehalten. Die Schema Schlüssel für den lokalen Computer sind Unterschlüssel des folgenden Registrierungsschlüssels:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Schemas\\**

Der Schlüssel für das wmhtml://-Schema für den lokalen Computer lautet beispielsweise wie folgt:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ Schemas \\ wmhtml**

Um Werte in diesem Schlüssel zu ändern oder um einen neuen Unterschlüssel zu erstellen, muss der aktuelle Benutzer ein Administrator für den Computer sein.

Für einzelne Benutzer sind die Schema Schlüssel Unterschlüssel des folgenden Registrierungsschlüssels:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Player \\ Schemas\\**

Der Schlüssel für das wmhtml://-Schema für den aktuellen Benutzer lautet z. b.:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Player \\ Schemas \\ wmhtml**

Bei der Überprüfung auf registrierte Schemas prüft der Spieler zunächst die Werte auf dem **lokalen HKEY- \_ \_ Computer**. Wenn keine für das aktuelle Schema gefunden wird, überprüft der Spieler die Werte im **aktuellen HKEY \_ - \_ Benutzer**. Wenn keine für das aktuelle Schema gefunden wird, zeigt der Player dem Benutzer die Warnung an.

Jeder Schema Unterschlüssel kann einen der folgenden möglichen Werte für die *Laufzeit* enthalten.



| Wert | BESCHREIBUNG                                |
|-------|--------------------------------------------|
| 6     | Rendering mit dem Windows Media-Format-SDK. |
| 7     | Rendering mithilfe von Microsoft DirectShow.         |



 

Das Ändern des *Lauf* Zeit Werts für ein Schema, das vom Windows Media Format SDK unterstützt wird, hat keine Auswirkungen. Der Player verwendet immer das SDK für den Windows Media-Format als Laufzeit für Schemas, die das Windows Media Format SDK unterstützt. Dieser Registrierungs Wert ermöglicht die Laufzeitkonfiguration für benutzerdefinierte Schemas.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> </dl>

 

 




