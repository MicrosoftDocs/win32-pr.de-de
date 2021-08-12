---
title: Attributwerte für TV-Inhalte
description: Attributwerte für TV-Inhalte
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Windows Media Player,Attribute für Medienelemente
- Windows Media Player Objektmodell, Attribute für Medienelemente
- Objektmodell,Attribute für Medienelemente
- Windows Media Player Mobil, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobiles ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player bibliothek,Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, TV-Inhalt
- TV-Inhaltsattributwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96f855d90fe0b65c4e9483dcb2ba4ae3ff7be049f1346f1038097789b2126c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583031"
---
# <a name="attribute-values-for-tv-content"></a>Attributwerte für TV-Inhalte

In diesem Thema wurde das **Player-Objekt** wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 oder höher können TV-Inhalte in der Bibliothek organisieren. Windows Media Player behandelt TV-Inhalte als Unterkategorie von Videoinhalten. Damit Videoinhalte in den TV-Knoten in der Bibliothek angezeigt werden, legen Sie die ATTRIBUTE **WM/MediaClassPrimaryID** und **WM/MediaClassSecondaryID** mithilfe der *Medien* auf die Werte in der folgenden Tabelle fest. **setItemInfo-Methode:**



| attribute                    | Wert                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

Sie können diese Werte auch verwenden, um mithilfe der *Medien* zu bestimmen, ob ein bestimmtes digitales Medienelement TV-Inhalte enthält. **getItemInfo** oder *medien*. **getItemInfoByType-Methoden.**

Denken Sie daran, die **GUID-Werte** als **Zeichenfolgenwerte** zu verwenden, wenn Sie diese Werte angeben oder abrufen.

Im folgenden C#-Beispielcode werden die Medienklassenattribute so festgelegt, dass ein Medienelement als TV-Inhalt identifiziert wird.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Weitere Informationen zu den möglichen Werten für die Medienklassenattribute finden Sie unter Windows Richtlinien zur [Verwendung von Medienmetadaten.](/previous-versions/ms867702(v=msdn.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medienelementattribute**](media-item-attributes.md)
</dt> <dt>

[**Bibliothekszugriff**](library-access.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> </dl>

 

 




