---
title: Subview-Element
description: Subview-Element
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player Skins, subview-Element
- Skins, subview-Element
- Subview-Element
- Verweis für Skins, subview-Element
- Elemente, unter Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310971"
---
# <a name="subview-element"></a>Subview-Element

Das **subview** -Element bietet eine Möglichkeit, einen Teil einer Skin zu bearbeiten, um z. b. eine Systemsteuerung bereitzustellen, die ausgeblendet werden kann, wenn Sie nicht verwendet wird. **Subview** -Elemente sind immer untergeordnete Elemente von übergeordneten **Ansichts** Elementen und können ein anderes Skin-Element enthalten, mit Ausnahme der Elemente **View**, **Theme** und other **subview** .

Das **subview** -Element unterstützt die folgenden Attribute, die unter dem **View** -Element definiert sind.



| Attribut                                                       | BESCHREIBUNG                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Background Color](view-backgroundcolor.md)                     | Gibt die Hintergrundfarbe des **unter Ansicht** -Steuer Elements an oder ruft diese ab. Der Standardwert ist "None".        |
| [backgroundImage](view-backgroundimage.md)                     | Gibt das Hintergrundbild des **unter Ansicht** -Steuer Elements an oder ruft es ab.                                     |
| [backgroundimagehueshift](view-backgroundimagehueshift.md)     | Gibt den Betrag an, um den der Farbton des Hintergrund Bilds verschoben wird, oder ruft diesen ab.                      |
| [backgroundimagesationations](view-backgroundimagesaturation.md) | Gibt den Sättigungswert des Hintergrund Bilds an oder ruft ihn ab.                                        |
| [backgroundkacheln](view-backgroundtiled.md)                     | Gibt einen Wert an, der angibt, ob das Hintergrundbild des **unter Ansicht** -Steuer Elements angezeigt wird, oder ruft diesen Wert ab. |
| [resizebackgroundimage](view-resizebackgroundimage.md)         | Gibt einen Wert an oder ruft ihn ab, der angibt, ob die Größe des Hintergrund Bilds geändert werden kann.                      |
| [transparendcolor](view-transparencycolor.md)                 | Gibt die Transparenz Farbe des Hintergrund Bilds an oder ruft diese ab.                                      |



 

Das **subview** -Element unterstützt die Ambient-Attribute, sofern nicht angegeben. Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md).

Das **subview** -Element kann die folgenden Ambient-Ereignishandler implementieren: [onendmove](onendmove.md) und [OnResize](onresize.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> <dt>

[**View-Element**](view-element.md)
</dt> </dl>

 

 




