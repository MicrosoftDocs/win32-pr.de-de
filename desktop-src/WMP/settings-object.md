---
title: Settings-Objekt (Windows Media Player SDK)
description: Das Settings-Objekt bietet eine Möglichkeit, verschiedene Einstellungen für Windows-Media Player mithilfe der folgenden Eigenschaften und Methoden zu ändern.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Einstellungs Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "103857740"
---
# <a name="settings-object"></a>Einstellungs Objekt

Das **Settings** -Objekt bietet eine Möglichkeit, verschiedene Einstellungen für Windows-Media Player mithilfe der folgenden Eigenschaften und Methoden zu ändern.

Das **Einstellungs** Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                                  | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Autostart](settings-autostart.md)                       | Gibt einen Wert an, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird, oder ruft diesen ab.                           |
| [Schwebe](settings-balance.md)                           | Gibt den aktuellen Stereo Saldo an oder ruft ihn ab.                                                                               |
| [Basis](settings-baseurl.md)                           | Gibt die Basis-URL an, die für die relative Pfad Auflösung mit in Mediendateien eingebetteten URL-Skript Befehlen verwendet wird, oder ruft Sie ab. |
| [defaultaudiolanguage](settings-defaultaudiolanguage.md) | Ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der in Windows Media Player angegebenen Standard Audiosprache ab.                          |
| [defaultframe](settings-defaultframe.md)                 | Gibt den Namen des Frames an oder ruft ihn ab, der zum Anzeigen einer URL verwendet wird, die in einem **ScriptCommand** -Ereignis empfangen wird.                |
| [enableerrordialogfelder](settings-enableerrordialogs.md)     | Gibt einen Wert an, der angibt, ob Fehler Dialogfelder automatisch angezeigt werden, oder ruft ihn ab.                                    |
| [invokeurls](settings-invokeurls.md)                     | Gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft diesen Wert ab.                                        |
| [isAvailable](settings-isavailable.md)                   | Ruft ab, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.                           |
| [mediaaccessrights](settings-mediaaccessrights.md)       | Ruft einen Wert ab, der die Rechte angibt, die derzeit für den Bibliotheks Zugriff gewährt werden.                                                    |
| [verstum](settings-mute.md)                                 | Gibt einen Wert an, der angibt, ob Audiodaten stumm geschaltet werden.                                                                |
| [playcount](settings-playcount.md)                       | Gibt an oder ruft die Häufigkeit ab, mit der ein Medien Element wiedergegeben wird.                                                               |
| [zinss](settings-rate.md)                                 | Gibt die aktuelle Wiedergabe Rate an oder ruft Sie ab.                                                                                |
| [volume](settings-volume.md)                             | Gibt das aktuelle Volume an oder ruft es ab.                                                                                       |



 

Das **Settings** -Objekt unterstützt die folgenden Methoden.



| Methode                                                            | BESCHREIBUNG                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | Bestimmt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist. |
| [requestmediaaccessrights](settings-requestmediaaccessrights.md) | Fordert eine angegebene Zugriffsebene für die Bibliothek an.        |
| [setMode](settings-setmode.md)                                   | Legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.   |



 

Der Zugriff auf das **Einstellungs** Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                        |
|-----------------------------|---------------------------------|
| [Player](player-object.md) | [settings](player-settings.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




