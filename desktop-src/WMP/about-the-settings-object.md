---
title: Informationen zum Einstellungs Objekt
description: Informationen zum Einstellungs Objekt
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, Einstellungs Objekt
- Windows Media Player-Objektmodell, Einstellungs Objekt
- Objektmodell, Einstellungs Objekt
- Windows Media Player ActiveX-Steuerelement, Einstellungs Objekt
- ActiveX-Steuerelement, Einstellungs Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Einstellungs Objekt
- Windows Media Player Mobile, Einstellungs Objekt
- Einstellungs Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855568"
---
# <a name="about-the-settings-object"></a>Informationen zum Einstellungs Objekt

Das **Einstellungs** Objekt steuert die Einstellungen des Steuer Elements, z. b. Volume, Wiedergabe Anzahl, stumm Schaltung usw. Der Zugriff erfolgt nur über die **Settings** -Eigenschaft des **Player** -Objekts. Die **Settings** -Eigenschaft gibt das **Settings** -Objekt zurück. Sie können nur auf die Eigenschaften des **Einstellungs** Objekts zugreifen, nachdem Sie es erstellt haben. Um z. b. den Wert der **Volume** -Eigenschaft zu erhalten, müssen Sie den folgenden Code verwenden:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 




