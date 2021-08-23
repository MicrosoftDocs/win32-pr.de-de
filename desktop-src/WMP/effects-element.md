---
title: EFFECTS-Element
description: EFFECTS-Element
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Windows Media Player Skins,EFFECTS-Element
- skins,EFFECTS-Element
- EFFECTS-Element
- Referenz für Skins, EFFECTS-Element
- Elements,EFFECTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a859414ffae934cafaa0c35b6b364eb42a5795bbeeef637857a0d81f47623379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651140"
---
# <a name="effects-element"></a>EFFECTS-Element

Das **EFFECTS-Element** bietet eine Möglichkeit, Visualisierungen mithilfe der folgenden Attribute und Methoden zu organisieren und zu bearbeiten. Der Einfachheit halber wird auch ein vordefiniertes **EFFECTS-Element** bereitgestellt.

Das **EFFECTS-Element** unterstützt die folgenden Attribute.



| attribute                                                        | Beschreibung                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Gibt einen Wert an, der angibt, ob alle Visualisierungen in die Registrierung enthalten sein werden, oder ruft diesen ab.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Gibt die aktuelle Visualisierung an oder ruft sie ab.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Ruft die Anzahl der verfügbaren Voreinstellungen für die aktuelle Visualisierung ab.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Ruft den Anzeigetitel der aktuellen Visualisierung ab.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Ruft den Registrierungsnamen der aktuellen Visualisierung ab.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Gibt die aktuelle Voreinstellung der aktuellen Visualisierung an oder ruft sie ab.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Ruft den Titel der aktuellen Voreinstellung der aktuellen Visualisierung ab.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Ruft einen Wert ab, der angibt, ob die aktuelle Visualisierung im Vollbildmodus angezeigt werden kann.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Ruft die Anzahl der verfügbaren Visualisierungen ab.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Ruft einen Wert ab, der angibt, ob die aktuelle Visualisierung über eine Eigenschaftenseite verfügt.                                                                                                                                                                  |
| [Fullscreen](effects-fullscreen.md)                             | Gibt einen Wert an, der angibt, ob die aktuelle Visualisierung im Vollbildmodus angezeigt wird, oder ruft einen Wert ab. Kann nur zur Laufzeit festgelegt werden.                                                                                                                   |
| [Fenstermodus](effects-windowed.md)                                 | Gibt einen Wert an bzw. ruft einen Wert ab, der angibt, ob die Visualisierung fensterlos oder fensterlos ist, d. b. ob das gesamte Rechteck des Steuerelements jederzeit sichtbar ist oder abgeschnitten werden kann. Kann nur zur Entwurfszeit festgelegt werden. |



 

Das **EFFECTS-Element** unterstützt die folgenden Methoden.



| Methode                                       | Beschreibung                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Ruft den Anzeigenamen der Visualisierung mit dem angegebenen Registrierungsindex ab.                               |
| [effectType](effects-effecttype.md)         | Ruft den Registrierungsnamen der Visualisierung mit dem angegebenen Registrierungsindex ab.                               |
| [Weiter](effects-next.md)                     | Zeigt die nächste Visualisierungsvoreinstellung an und geht bei Bedarf zur nächsten Visualisierung über.                            |
| [nextEffect](effects-nexteffect.md)         | Zeigt die erste Voreinstellung der nächsten Visualisierung an und überspringt die intervening-Voreinstellungen.                                |
| [nextPreset](effects-nextpreset.md)         | Zeigt die nächste Voreinstellung der aktuellen Visualisierung an.                                                            |
| [previous](effects-previous.md)             | Zeigt die vorherige Visualisierungsvoreinstellung an und bewegt sich bei Bedarf zur letzten Voreinstellung der vorherigen Visualisierung. |
| [previousEffect](effects-previouseffect.md) | Zeigt die vorherige Visualisierung an und überspringt Voreinstellungen.                                                            |
| [previousPreset](effects-previouspreset.md) | Zeigt die vorherige Voreinstellung der aktuellen Visualisierung an.                                                        |
| [settings](effects-settings.md)             | Zeigt die Attributseite für die aktuelle Visualisierung an, sofern vorhanden.                                            |



 

Das **EFFECTS-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient Attributes (Umgebungsattribute)](ambient-attributes.md) [und Ambient Event Handlers (Umgebungsereignishandler).](ambient-event-handlers.md)

Vordefinierte Effekte sind normale **EFFECTS-Elemente** mit verschiedenen allgemeinen Attributeinstellungen, die standardmäßig angegeben sind. Die folgenden vordefinierten Effekte sind verfügbar.



| Vordefinierte EFFEKTE           | Beschreibung                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Ein  EFFECTS-Element, das die verfügbaren Effekte durch iteriert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




