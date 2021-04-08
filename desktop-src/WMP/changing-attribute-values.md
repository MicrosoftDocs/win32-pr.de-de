---
title: Ändern von Attributwerten
description: Ändern von Attributwerten
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, Ändern von Werten
- Ändern von Attributwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037113"
---
# <a name="changing-attribute-values"></a>Ändern von Attributwerten

Sie können den Wert eines Attributs ändern, wenn Ihre Webseite oder Anwendung Lese-/Schreibzugriff auf die Bibliothek hat und das Attribut gelesen und geschrieben werden kann.

Sie können ein Attribut des aktuellen Medien Elements ändern. Wenn Sie Attribute mehrerer Medienelemente ändern möchten, können Sie diese wiederum dem *Player* zuweisen. **currentMedia** -Eigenschaft.

In diesem Thema wurde das **Player** -Objekt wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Um ein Attribut zu ändern, nennen Sie den *Player*. *currentMedia*. die Methode " **stiteminfo** ", wie im folgenden c#-Beispiel gezeigt.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Es wird empfohlen, das *Medium* aufzurufen. **isleseronlyitem** -Methode, um zu bestimmen, ob Sie ein bestimmtes Attribut ändern können.

> [!Note]  
> Wenn Sie das-Steuerelement in Ihre Anwendung einbetten, werden Dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player ausführt. Wenn Sie das-Steuerelement in einer Remote Anwendung verwenden, die in C++ geschrieben ist, werden die Dateiattribute, die Sie ändern, kurz nach dem vornehmen der Änderungen in die digitale Mediendatei geschrieben. In beiden Fällen sind die Änderungen sofort über die Bibliothek verfügbar.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medien Element Attribute**](media-item-attributes.md)
</dt> <dt>

[**Bibliotheks Zugriff**](library-access.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> </dl>

 

 




