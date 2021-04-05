---
title: Attributwerte für TV-Inhalt
description: Attributwerte für TV-Inhalt
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
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
- Attribute, TV-Inhalt
- Werte für TV-Inhalts Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037599"
---
# <a name="attribute-values-for-tv-content"></a>Attributwerte für TV-Inhalt

In diesem Thema wurde das **Player** -Objekt wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 oder höher kann TV-Inhalte in der Bibliothek organisieren. Windows Media Player behandelt TV-Inhalte als Unterkategorie von Videoinhalten. Um Videoinhalte in den TV-Knoten in der Bibliothek anzuzeigen, legen Sie die Attribute **WM/mediaclassprimaryid** und **WM/MediaClassSecondaryID** mithilfe der *Medien* auf die Werte in der folgenden Tabelle fest. die Methode " **stiteminfo** ":



| Attribut                    | Wert                                |
|------------------------------|--------------------------------------|
| **WM/mediaclassprimaryid**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

Sie können diese Werte auch verwenden, um zu bestimmen, ob ein bestimmtes digitales Medien Element TV-Inhalte mithilfe der *Medien* enthält. **getiteminfo** oder *Medium*. **getItemInfoByType** -Methoden.

Denken Sie daran, die **GUID** -Werte als **Zeichen** folgen Werte zu verwenden, wenn Sie diese Werte angeben oder abrufen.

Im folgenden c#-Beispielcode werden die Medien Klassenattribute so festgelegt, dass ein Medien Element als Fernseh Inhalt identifiziert wird.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Weitere Informationen zu den möglichen Werten für die Medien Klassenattribute finden Sie in den [Richtlinien zur Verwendung von Windows Media-Metadaten](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medien Element Attribute**](media-item-attributes.md)
</dt> <dt>

[**Bibliotheks Zugriff**](library-access.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> </dl>

 

 




