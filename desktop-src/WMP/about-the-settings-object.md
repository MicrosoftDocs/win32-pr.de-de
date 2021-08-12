---
title: Informationen zum Einstellungen-Objekt
description: Informationen zum Einstellungen-Objekt
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player,Einstellungen-Objekt
- Windows Media Player-Objektmodell,Einstellungen-Objekt
- Objektmodell,Einstellungen Objekt
- Windows Media Player ActiveX-Steuerelement,Einstellungen-Objekt
- ActiveX-Steuerelement,Einstellungen-Objekt
- Windows Media Player Mobiles ActiveX-Steuerelement, Einstellungen-Objekt
- Windows Media Player Mobiles,Einstellungen-Objekt
- Einstellungen-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74b8bd9db946a2915486647fa5831158198bef6115a34b6bb9fb81177f433de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583672"
---
# <a name="about-the-settings-object"></a>Informationen zum Einstellungen-Objekt

Das **Einstellungen** -Objekt steuert die Einstellungen des Steuerelements, z. B. Lautstärke, Wiedergabeanzahl, Stummschaltung usw. Der Zugriff erfolgt nur über die **Einstellungen-Eigenschaft** des **Player-Objekts.** Die **Einstellungen** -Eigenschaft gibt das **Einstellungen-Objekt** zurück. Sie können erst auf die Eigenschaften des **Einstellungen-Objekts** zugreifen, nachdem Sie es erstellt haben. Um beispielsweise den Wert der **Volume-Eigenschaft** abzurufen, müssen Sie den folgenden Code verwenden:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> </dl>

 

 




