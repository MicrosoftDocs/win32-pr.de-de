---
title: Ändern von Attributwerten
description: Ändern von Attributwerten
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player,Attribute für Medienelemente
- Windows Media Player Objektmodell,Attribute für Medienelemente
- Objektmodell,Attribute für Medienelemente
- Windows Media Player Mobil,Attribute für Medienelemente
- Windows Media Player ActiveX,Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement,Attribute für Medienelemente
- ActiveX,Attribute für Medienelemente
- Windows Media Player Bibliothek,Attribute für Medienelemente
- Bibliothek,Attribute für Medienelemente
- Attribute,Ändern von Werten
- Ändern von Attributwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870d8bfa13012bd79fdd672f1543db4a484ca5d9674ef1a9e48e832119ea1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581116"
---
# <a name="changing-attribute-values"></a>Ändern von Attributwerten

Sie können den Wert eines Attributs ändern, wenn Ihre Webseite oder Anwendung Lese-/Schreibzugriff auf die Bibliothek hat und das Attribut sowohl gelesen als auch geschrieben werden kann.

Sie können ein Attribut des aktuellen Medienelements ändern. Um Attribute mehrerer Medienelemente zu ändern, können Sie jede der Reihe nach dem *Player zuweisen.* **currentMedia-Eigenschaft.**

In diesem Thema wurde **das Player-Objekt** wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Um ein Attribut zu ändern, rufen Sie den *Player auf.* *currentMedia*. **setItemInfo-Methode,** wie im folgenden C#-Beispiel gezeigt.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Es wird empfohlen, den Medienaufruf *auf zu verwenden.* **isReadOnlyItem-Methode,** um zu bestimmen, ob Sie ein bestimmtes Attribut ändern können.

> [!Note]  
> Wenn Sie das Steuerelement in Ihre Anwendung einbetten, werden dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player. Wenn Sie das Steuerelement in einer in C++ geschriebenen Remoteanwendung verwenden, werden Dateiattribute, die Sie ändern, kurz nach dem Vornehmen der Änderungen in die digitale Mediendatei geschrieben. In beiden Fällen sind die Änderungen sofort über die Bibliothek verfügbar.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medienelementattribute**](media-item-attributes.md)
</dt> <dt>

[**Bibliothekszugriff**](library-access.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> </dl>

 

 




