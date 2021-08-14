---
title: Ausblenden des Windows Media Player-Steuerelements
description: Ausblenden des Windows Media Player-Steuerelements
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player,Einbetten ActiveX Steuerelements
- Windows Media Player Objektmodell, Einbetten ActiveX Steuerelements
- Objektmodell, Einbetten ActiveX Steuerelements
- Windows Media Player Mobil, Einbetten ActiveX Steuerelements
- Windows Media Player ActiveX-Steuerelement, Einbetten
- Windows Media Player Mobiles ActiveX-Steuerelement, Einbetten
- ActiveX-Steuerelement, Einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobiles ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Einbetten,Webseiten
- Windows Media Player,Ausblenden ActiveX Steuerelements
- Windows Media Player Objektmodell, Ausblenden ActiveX Steuerelements
- Objektmodell,Ausblenden ActiveX Steuerelements
- Windows Media Player Mobiles, ausblendendesActiveX-Steuerelement
- Windows Media Player ActiveX-Steuerelement, Ausblenden
- Windows Media Player Mobile ActiveX-Steuerelement, Ausblenden
- ActiveX-Steuerelement, Ausblenden
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobiles ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Einbetten von Webseiten, Ausblenden ActiveX Steuerelements
- Ausblenden Windows Media Player ActiveX Steuerelements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb0b29bbbc1b2eb978c5bd9f29a58aa02bf629d5c6befe9f1dc68bbc92d280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339181"
---
# <a name="hiding-the-windows-media-player-control"></a>Ausblenden des Windows Media Player-Steuerelements

Das Windows Media Player ActiveX -Objekt wird mithilfe des OBJECT-Elements in eine Webseite eingebettet. Im Gegensatz zu früheren Versionen muss das OBJECT-Element, das Windows Media Player definiert, im BODY-Abschnitt einer Webseite zwischen platziert werden. <BODY> und </BODY> Schilder. Das Platzieren des Windows Media Player ActiveX-Objekts im HEAD-Abschnitt einer Webseite, um die Benutzeroberfläche auszublenden, kann zu unerwarteten Ergebnissen führen.

Wenn Sie das Windows Media Player ActiveX-Steuerelement im Body-Abschnitt einer Webseite setzen, wird die Benutzeroberfläche des Steuerelements angezeigt. Wenn sie nicht angezeigt werden soll und Sie eine eigene Benutzeroberfläche erstellen möchten, legen Sie die Höhen- und Breitenattribute des OBJECT-Elements auf 0 (null) fest.

Das Steuerelement kann auch unsichtbar gemacht werden, indem der *Player* festgelegt wird. **uiMode-Eigenschaft** zu "unsichtbar". Dies kann mithilfe eines PARAM-Tags erfolgen, wie im nächsten Abschnitt erläutert. In diesem Fall ist der Platz für das Steuerelement mithilfe von Höhe und Breite reserviert, aber im reservierten Bereich wird nichts angezeigt, bis **uiMode** in etwas anderes als "unsichtbar" geändert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuerelements auf einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




