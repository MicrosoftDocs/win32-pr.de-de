---
title: Ambient-Ereignishandler
description: Ambient-Ereignishandler
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Windows Media Player Skins,Ambient-Ereignishandler
- Skins, Ambient-Ereignishandler
- Referenz für Skins, Ambient-Ereignishandler
- Ambient-Ereignishandler
- Events,Ambient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff72739ec1791b79d6113415f1219a1ddee578b4b5a690ffaaac62bf6b3dbcfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865090"
---
# <a name="ambient-event-handlers"></a>Ambient-Ereignishandler

Die folgenden Ereignishandler können für die meisten Skinelemente implementiert werden. Die Ambient-Ereignisattribute, auf die mit dem **Event-Schlüsselwort** zugegriffen wird, können innerhalb eines Ereignishandlers verwendet werden, um den Zustand von Tastatur und Maus zum Zeitpunkt des Ereignisses zu bestimmen.



| Ereignishandler                                   | BESCHREIBUNG                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Attribut* \_ Onchange](attribute-onchange.md) | Wenn ein Skinattribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignishandlers ist der Name des Attributs, gefolgt von einem Unterstrich und "onchange", z. B. "value \_ onchange". |
| [Onblur](onblur.md)                            | Behandelt ein Ereignis, das auftritt, wenn das Element den Tastaturfokus verliert.                                                                                                                                                       |
| [Onclick](onclick.md)                          | Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf das Element klickt.                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf das Element doppelklickt.                                                                                                                                                         |
| [onendalphablend](onendalphablend.md)          | Behandelt ein Ereignis, das auftritt, wenn ein Element einen **alphaBlendTo-Vorgang** abwickelt.                                                                                                                                         |
| [onendmove](onendmove.md)                      | Behandelt ein Ereignis, das auftritt, wenn ein Element einen **moveTo-Vorgang** abwickelt.                                                                                                                                                |
| [Onfocus](onfocus.md)                          | Behandelt ein Ereignis, das auftritt, wenn das Element den Tastaturfokus erhält.                                                                                                                                                    |
| [Onkeydown](onkeydown.md)                      | Behandelt ein Ereignis, das auftritt, wenn eine Taste gedrückt wird.                                                                                                                                                                           |
| [Onkeypress](onkeypress.md)                    | Behandelt ein Ereignis, das auftritt, wenn der Benutzer eine alphanumerische Taste drückt.                                                                                                                                                       |
| [Onkeyup](onkeyup.md)                          | Behandelt ein Ereignis, das auftritt, wenn ein Schlüssel freigegeben wird.                                                                                                                                                                          |
| [Onmousedown](onmousedown.md)                  | Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf eine Maustaste klickt.                                                                                                                                                             |
| [Onmousemove](onmousemove.md)                  | Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger bewegt, während er sich über einem Element befindet.                                                                                                                               |
| [Onmouseout](onmouseout.md)                    | Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Zeiger vom Element verschiebt.                                                                                                                                                 |
| [Onmouseover](onmouseover.md)                  | Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Zeiger zum ersten Mal auf das Element setzt.                                                                                                                                         |
| [Onmouseup](onmouseup.md)                      | Behandelt ein Ereignis, das auftritt, wenn der Benutzer eine Maustaste loslässt, während sich der Zeiger über dem Element befindet.                                                                                                                     |
| [Onresize](onresize.md)                        | Behandelt ein Ereignis, das auftritt, wenn die Größe eines Steuerelements geändert wird.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ambient-Ereignisattribute**](ambient-event-attributes.md)
</dt> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




