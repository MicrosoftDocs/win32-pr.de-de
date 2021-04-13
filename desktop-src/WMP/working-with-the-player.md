---
title: Arbeiten mit dem Player
description: Arbeiten mit dem Player
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player Skins, Player-Attribut in JScript
- Skins, Player-Attribut in JScript
- Attribute, Player
- Player-Attribut
- JScript-Dateien für Skins, Player-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388757"
---
# <a name="working-with-the-player"></a>Arbeiten mit dem Player

Wenn Sie Microsoft JScript verwenden, um auf Methoden und Eigenschaften von Windows Media Player zuzugreifen, müssen Sie den Namen "Player" als Namen des Steuer Elements verwenden. Wenn Sie z. b. auf die Methode zum Abbrechen verweisen möchten, müssen Sie Folgendes eingeben:


```C++
player.Controls.Stop()

```



Das globale Attribut " **Player** " ist der Schlüssel für den Zugriff auf das Windows Media Player-Steuerelement über die Design Skripterstellung Über dieses Attribut werden alle Objekte des Windows Media Player-Steuer Elements für die Lauf Zeitänderung über ihre Eigenschaften und Methoden zugänglich. Außerdem ist das **Player** -Element verfügbar, sodass Sie Ereignishandler und das **URL** -Attribut zur Entwurfszeit angeben können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von JScript**](using-jscript.md)
</dt> </dl>

 

 




