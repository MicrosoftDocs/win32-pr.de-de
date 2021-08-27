---
title: SUBVIEW-Element
description: SUBVIEW-Element
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player Skins, SUBVIEW-Element
- skins,SUBVIEW-Element
- SUBVIEW-Element
- Referenz für Skins, SUBVIEW-Element
- elements,SUBVIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef4f7860d1db04991a35ffeff2903e7a16a5d7bd84929313c296006f6f1c092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122910"
---
# <a name="subview-element"></a>SUBVIEW-Element

Das **SUBVIEW-Element** bietet eine Möglichkeit, einen Teil einer Skin zu bearbeiten, z. B. um eine Systemsteuerung bereitzustellen, die ausgeblendet werden kann, wenn sie nicht verwendet wird. **SUBVIEW-Elemente** sind immer untergeordnete Elemente übergeordneter **VIEW-Elemente** und können andere Skinelemente mit Ausnahme von **VIEW,** **THEME** und anderen **SUBVIEW-Elementen** enthalten.

Das **SUBVIEW-Element** unterstützt die folgenden Attribute, die unter dem **VIEW-Element** definiert sind.



| attribute                                                       | Beschreibung                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](view-backgroundcolor.md)                     | Gibt die Hintergrundfarbe des **SUBVIEW-Steuerelements** an oder ruft sie ab. Der Standardwert ist "none".        |
| [backgroundImage](view-backgroundimage.md)                     | Gibt das Hintergrundbild des **SUBVIEW-Steuerelements** an oder ruft es ab.                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Gibt die Menge an, um die der Farbton des Hintergrundbilds verschoben wird, oder ruft sie ab.                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Gibt den Sättigungswert des Hintergrundbilds an oder ruft den Sättigungswert ab.                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | Gibt einen Wert an, der angibt, ob das Hintergrundbild des **SUBVIEW-Steuerelements** gekachelt ist, oder ruft einen Wert ab. |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Gibt einen Wert an, der angibt, ob die Größe des Hintergrundbilds geändert werden kann, oder ruft einen Wert ab.                      |
| [transparencyColor](view-transparencycolor.md)                 | Gibt die Transparenzfarbe des Hintergrundbilds an oder ruft sie ab.                                      |



 

Das **SUBVIEW-Element** unterstützt die Ambient-Attribute, sofern nicht angegeben. Weitere Informationen finden Sie unter [Ambient Attributes](ambient-attributes.md).

Das **SUBVIEW-Element** kann die folgenden Ambient-Ereignishandler implementieren: [onendmove](onendmove.md) und [onresize](onresize.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> <dt>

[**VIEW-Element**](view-element.md)
</dt> </dl>

 

 




