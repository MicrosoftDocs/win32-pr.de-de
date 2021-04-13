---
title: Ausblenden des Windows Media Player-Steuer Elements
description: Ausblenden des Windows Media Player-Steuer Elements
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Einbettungen, Webseiten
- Windows Media Player, Ausblenden des ActiveX-Steuer Elements
- Windows Media Player-Objektmodell, Ausblenden des ActiveX-Steuer Elements
- Objektmodell, Ausblenden des ActiveX-Steuer Elements
- Windows Media Player Mobile, hidingactivex-Steuerelement
- Windows Media Player ActiveX-Steuerelement, ausblenden
- Windows Media Player Mobile ActiveX-Steuerelement, ausblenden
- ActiveX-Steuerelement, ausblenden
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Seiten Einbettung, Ausblenden des ActiveX-Steuer Elements
- Ausblenden von Windows Media Player ActiveX-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310768"
---
# <a name="hiding-the-windows-media-player-control"></a>Ausblenden des Windows Media Player-Steuer Elements

Das Windows-Media Player ActiveX-Objekt wird mit dem Object-Element in eine Webseite eingebettet. Im Gegensatz zu früheren Versionen muss das Object-Element, das Windows-Media Player definiert, im body-Abschnitt einer Webseite zwischen den Tags <BODY> und </BODY> abgelegt werden. Das Platzieren des Windows-Media Player ActiveX-Objekts im Head-Abschnitt einer Webseite, um die Benutzeroberfläche auszublenden, kann zu unerwarteten Ergebnissen führen.

Wenn Sie das Windows Media Player ActiveX-Steuerelement im body-Abschnitt einer Webseite ablegen, wird die Benutzeroberfläche des Steuer Elements angezeigt. Wenn Sie nicht möchten, dass Sie angezeigt wird, und Sie eine eigene Benutzeroberfläche erstellen möchten, legen Sie die Attribute height und Width des Object-Elements auf NULL fest.

Das Steuerelement kann auch durch Festlegen des *Players* unsichtbar gemacht werden. **uiMode** -Eigenschaft auf "unsichtbar". Dies kann mithilfe eines param-Tags erfolgen, wie im nächsten Abschnitt erläutert. In diesem Fall ist der Speicherplatz für das Steuerelement mit Höhe und Breite reserviert, aber im reservierten Bereich wird nichts angezeigt, bis **uiMode** in etwas anderes als "unsichtbar" geändert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




