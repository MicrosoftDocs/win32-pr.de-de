---
title: Effects-Element
description: Effects-Element
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Windows Media Player Skins, Effects-Element
- Skins, Effects-Element
- Effects-Element
- Verweis für Skins, Effects-Element
- Elemente, Effekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b6fdcde74288b0dd4215732d1e5b6a281154f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387985"
---
# <a name="effects-element"></a>Effects-Element

Das **Effects** -Element bietet eine Möglichkeit, Visualisierungen mithilfe der folgenden Attribute und Methoden zu organisieren und zu bearbeiten. Ein vordefiniertes **Effekte** -Element wird auch zur einfacheren Bereitstellung geboten.

Das **Effects** -Element unterstützt die folgenden Attribute.



| Attribut                                                        | BESCHREIBUNG                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Zuordnung](effects-allowall.md)                                 | Gibt einen Wert an, der angibt, ob alle Visualisierungen in die Registrierung eingeschlossen werden sollen, oder ruft ihn ab.                                                                                                                                                 |
| [Ereignis-ffect](effects-currenteffect.md)                       | Gibt die aktuelle Visualisierung an oder ruft Sie ab.                                                                                                                                                                                                    |
| ["seteffectpresetcount"](effects-currenteffectpresetcount.md) | Ruft die Anzahl der verfügbaren Voreinstellungen für die aktuelle Visualisierung ab.                                                                                                                                                                                 |
| ["Currency-ffecttitle"](effects-currenteffecttitle.md)             | Ruft den anzeigen Titel der aktuellen Visualisierung ab.                                                                                                                                                                                            |
| ["happteffecttype"](effects-currenteffecttype.md)               | Ruft den Registrierungs Namen der aktuellen Visualisierung ab.                                                                                                                                                                                            |
| [currentvoreinstellung](effects-currentpreset.md)                       | Gibt die aktuelle Voreinstellung der aktuellen Visualisierung an oder ruft diese ab.                                                                                                                                                                              |
| [currentpresettitle](effects-currentpresettitle.md)             | Ruft den Titel der aktuellen Voreinstellung der aktuellen Visualisierung ab.                                                                                                                                                                              |
| [effectcangofullscreen](effects-effectcangofullscreen.md)       | Ruft einen Wert ab, der angibt, ob die aktuelle Visualisierung voll Bildschirm angezeigt werden kann.                                                                                                                                                         |
| [effectcount](effects-effectcount.md)                           | Ruft die Anzahl der verfügbaren Visualisierungen ab.                                                                                                                                                                                                    |
| [effecthaspropertypage](effects-effecthaspropertypage.md)       | Ruft einen Wert ab, der angibt, ob die aktuelle Visualisierung über eine Eigenschaften Seite verfügt.                                                                                                                                                                  |
| [Vollbild](effects-fullscreen.md)                             | Gibt einen Wert an, der angibt, ob die aktuelle Visualisierung voll Bildschirm angezeigt wird, oder ruft diesen ab. Kann nur zur Laufzeit festgelegt werden.                                                                                                                   |
| [Fenster](effects-windowed.md)                                 | Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob die Visualisierung Fenster Weise angezeigt wird, d. h. ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist, oder ob es abgeschnitten werden kann. Kann nur zur Entwurfszeit festgelegt werden. |



 

Das **Effects** -Element unterstützt die folgenden Methoden.



| Methode                                       | BESCHREIBUNG                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [EffectTitle](effects-effecttitle.md)       | Ruft den anzeigen amen der Visualisierung mit dem angegebenen Registrierungs Index ab.                               |
| [EffectType](effects-effecttype.md)         | Ruft den Registrierungs Namen der Visualisierung mit dem angegebenen Registrierungs Index ab.                               |
| [Weiter](effects-next.md)                     | Zeigt die nächste Visualisierungs Voreinstellung an und wechselt bei Bedarf zur nächsten Visualisierung.                            |
| [nexteffect](effects-nexteffect.md)         | Zeigt die erste Voreinstellung der nächsten Visualisierung an und überspringt die dazwischenliegenden Voreinstellungen.                                |
| [nextvoreinstellung](effects-nextpreset.md)         | Zeigt die nächste Voreinstellung der aktuellen Visualisierung an.                                                            |
| [previous](effects-previous.md)             | Zeigt die vorherige Visualisierungs Voreinstellung an und wechselt ggf. zur letzten Voreinstellung der vorherigen Visualisierung. |
| [previouabffect](effects-previouseffect.md) | Zeigt die vorherige Visualisierung an und überspringt Voreinstellungen.                                                            |
| [previoustreuset](effects-previouspreset.md) | Zeigt die vorherige Voreinstellung der aktuellen Visualisierung an.                                                        |
| [settings](effects-settings.md)             | Zeigt die Attribut Seite für die aktuelle Visualisierung an (sofern vorhanden).                                            |



 

Das **Effects** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).

Vordefinierte Effekte sind normale **Effekte** Elemente mit verschiedenen allgemeinen Attribut Einstellungen, die standardmäßig angegeben werden. Die folgenden vordefinierten Effekte sind verfügbar.



| Vordefinierte Effekte           | BESCHREIBUNG                                                         |
|------------------------------|---------------------------------------------------------------------|
| [Wmpeffects](wmpeffects.md) | Ein **Effects** -Element, das die verfügbaren Effekte durchläuft. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




