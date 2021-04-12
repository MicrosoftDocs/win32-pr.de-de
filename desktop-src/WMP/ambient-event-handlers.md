---
title: Ambient-Ereignishandler
description: Ambient-Ereignishandler
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Windows Media Player Skins, Ambient-Ereignishandler
- Skins, Ambient-Ereignishandler
- Referenz für Skins, Ambient-Ereignishandler
- Ambient-Ereignishandler
- Ereignisse, Ambient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388086"
---
# <a name="ambient-event-handlers"></a>Ambient-Ereignishandler

Die folgenden Ereignishandler können für die meisten Skin-Elemente implementiert werden. Die Ambient-Ereignis Attribute, auf die mit dem **Ereignis** Schlüsselwort zugegriffen wird, können innerhalb eines Ereignis Handlers verwendet werden, um den Zustand der Tastatur und der Maus zum Zeitpunkt des Ereignisses zu bestimmen.



| Ereignishandler                                   | BESCHREIBUNG                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Attribut* \_ OnChange](attribute-onchange.md) | Wenn ein Skin-Attribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignis Handlers ist der Name des Attributs, gefolgt von einem Unterstrich und "OnChange", z. b. "Value \_ OnChange". |
| [onblur](onblur.md)                            | Behandelt ein Ereignis, das auftritt, wenn das Element den Tastaturfokus verliert.                                                                                                                                                       |
| [OnClick](onclick.md)                          | Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf das Element klickt.                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf das Element doppelklickt.                                                                                                                                                         |
| [onendalphablend](onendalphablend.md)          | Behandelt ein Ereignis, das auftritt, wenn ein Element einen **alphablendto** -Vorgang abschließt.                                                                                                                                         |
| [onendmove](onendmove.md)                      | Behandelt ein Ereignis, das auftritt, **Wenn ein Element einen Vorgang vom** Typ "Vorgang" abgeschlossen hat.                                                                                                                                                |
| [onfocus](onfocus.md)                          | Behandelt ein Ereignis, das auftritt, wenn das Element den Tastaturfokus erhält.                                                                                                                                                    |
| [OnKeyDown](onkeydown.md)                      | Behandelt ein Ereignis, das auftritt, wenn eine Taste gedrückt wird.                                                                                                                                                                           |
| [OnKeyPress](onkeypress.md)                    | Behandelt ein Ereignis, das auftritt, wenn der Benutzer einen alphanumerischen Schlüssel drückt.                                                                                                                                                       |
| [OnKeyUp](onkeyup.md)                          | Behandelt ein Ereignis, das auftritt, wenn eine Taste losgelassen wird.                                                                                                                                                                          |
| ["OnMouseDown"](onmousedown.md)                  | Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf eine Maustaste klickt.                                                                                                                                                             |
| [OnMouseMove](onmousemove.md)                  | Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger bewegt, während er sich über einem Element befindet.                                                                                                                               |
| [onmouout](onmouseout.md)                    | Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger vom Element bewegt.                                                                                                                                                 |
| ["onmouseover](onmouseover.md)                  | Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger über das Element platziert.                                                                                                                                         |
| [OnMouseUp](onmouseup.md)                      | Behandelt ein Ereignis, das auftritt, wenn der Benutzer eine Maustaste loslässt, während sich der Mauszeiger über dem Element befindet.                                                                                                                     |
| [OnResize](onresize.md)                        | Behandelt ein Ereignis, das auftritt, wenn die Größe eines Steuer Elements geändert wird.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ambient-Ereignis Attribute**](ambient-event-attributes.md)
</dt> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




