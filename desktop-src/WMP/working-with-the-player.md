---
title: Arbeiten mit dem Player
description: Arbeiten mit dem Player
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player Skins,Player-Attribut in JScript
- skins,player-Attribut in JScript
- Attribute, Player
- Player-Attribut
- JScript für Skins,Player-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77098f161244488d5097d2d022f105628a43ba50a40218da01295d99f2de0cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566982"
---
# <a name="working-with-the-player"></a>Arbeiten mit dem Player

Wenn Sie Microsoft JScript für den Zugriff auf Methoden und Eigenschaften von Windows Media Player verwenden, müssen Sie den Namen "player" für den Namen des Steuerelements verwenden. Um beispielsweise auf die Stop-Methode zu verweisen, müssen Sie Folgendes eingeben:


```C++
player.Controls.Stop()

```



Das **globale Player-Attribut** ist der Schlüssel für den Zugriff auf das Windows Media Player-Steuerelement durch Skin scripting. Durch dieses Attribut können alle Objekte des Windows Media Player-Steuerelements über ihre Eigenschaften und Methoden zur Laufzeit geändert werden. Darüber hinaus ist **das PLAYER-Element** verfügbar, sodass Sie zur Entwurfszeit Ereignishandler und das **URL-Attribut** angeben können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden JScript**](using-jscript.md)
</dt> </dl>

 

 




