---
title: Registrierungseinträge zum Nachverfolgen des Installationsfortschritts
description: Registrierungseinträge zum Nachverfolgen des Installationsfortschritts
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player,Nachverfolgen des Installationsfortschritts
- Windows Media Player,Nachverfolgung des Installationsfortschritts
- Windows Media Player,Fortschrittsnachverfolgung von Installationen
- Windows Media Player,Registrierung
- Registrierung,Nachverfolgen des Installationsfortschritts
- Registrierung, Nachverfolgung des Installationsfortschritts
- Registrierung, Fortschrittsnachverfolgung von Installationen
- Registrierung, Einstellungen für Windows Media Player
- Nachverfolgen des Installationsfortschritts
- Installieren der Fortschrittsnachverfolgung
- Fortschrittsnachverfolgung von Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7febb9f25a04c5e4358e891f963ab6a8569cfd6facef7e4f2072807bd09e2605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570301"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Registrierungseinträge zum Nachverfolgen des Installationsfortschritts

Der Windows Media Player 11-Setupprogramm, setup \_wm.exe, schreibt die folgenden Einträge in die Registrierung, damit Installationsprogramme den Fortschritt des Windows Media Player Setupprogramms während der Ausführung nachverfolgen können.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



In der obigen Registrierungssyntax ist *value* ein Platzhalter für einen ganzzahligen Wert.

Progress \_ CurrentDialog gibt an, welches Dialogfeld Windows Media Player Setup derzeit angezeigt wird. Progress \_ MaxDialog gibt die Gesamtzahl der Dialogfelder an, die Windows Medien angezeigt werden. Wenn z. B. Progress \_ CurrentDialog = 2 und Progress \_ MaxDialog = 5, zeigt Windows Media Player derzeit das zweite Dialogfeld in einer Sequenz von fünf an.

Progress \_ CurrentInstall und Progress \_ MaxInstall geben zusammen den Prozentsatz des Abschlusses des aktuellen Dialogfelds an. Wenn z. B. Progress \_ CurrentInstall = 6 und Progress \_ MaxInstall = 25, ist das aktuelle Dialogfeld 6/25 (d.h. 24 %) abgeschlossen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




