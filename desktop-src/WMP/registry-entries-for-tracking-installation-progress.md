---
title: Registrierungseinträge zum Nachverfolgen des Installations Fortschritts
description: Registrierungseinträge zum Nachverfolgen des Installations Fortschritts
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, Nachverfolgen des Installations Fortschritts
- Windows Media Player, Nachverfolgung von Installationsfortschritt
- Windows Media Player, Fortschritt Nachverfolgung von Installationen
- Windows Media Player, Registrierung
- Registrierung, Nachverfolgen des Installations Fortschritts
- Registrierung, Nachverfolgung von Installationsfortschritt
- Registrierung, Fortschritt Nachverfolgung von Installationen
- Registrierung, Einstellungen für Windows-Media Player
- Nachverfolgen des Installations Fortschritts
- Installieren der Statusüberwachung
- fortlaufende Nachverfolgung von Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037594"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Registrierungseinträge zum Nachverfolgen des Installations Fortschritts

Mit dem Setup Programm von Windows Media Player 11, Setup \_wm.exe, werden die folgenden Einträge in die Registrierung geschrieben, damit Installationsprogramme den Fortschritt des Windows Media Player Setup-Programms nachverfolgen können, während es ausgeführt wird.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



In der vorangehenden Registrierungs Syntax ist *value* ein Platzhalter für einen ganzzahligen Wert.

Der Fortschritt \_ currentdialog gibt an, welches Dialogfeld Windows Media Player-Setup aktuell angezeigt wird. Status \_ maxdialog gibt die Gesamtanzahl der Dialogfelder an, die von Windows Media angezeigt werden. Wenn z. b. Progress \_ currentdialog = 2 und Progress \_ maxdialog = 5 angezeigt wird, zeigt Windows Media Player momentan das zweite Dialogfeld in einer Sequenz von fünf an.

Der Fortschritt \_ currentinstall und Progress \_ maxinstall zeigen den Prozentsatz des Abschlusses des aktuellen Dialog Felds an. Wenn z. b. Progress \_ currentinstall = 6 und Progress \_ maxinstall = 25 ist, lautet der aktuelle Dialog 6/25 (24%). ganz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> </dl>

 

 




