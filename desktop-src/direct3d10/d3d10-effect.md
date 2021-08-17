---
description: Diese Konstanten werden beim Erstellen eines Effekts verwendet, um das Kompilierungsverhalten oder das Laufzeiteffektverhalten zu definieren.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT Konstanten
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3738a95a843020f7c0f8af30e8c5d035f0a86ac7098d36cae422eb01ed4dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736049"
---
# <a name="d3d10_effect-constants"></a>D3D10 \_ EFFECT-Konstanten

Diese Konstanten werden beim Erstellen eines Effekts verwendet, um das Kompilierungsverhalten oder das Laufzeiteffektverhalten zu definieren.



| \#Definieren                                 | Wert        | Beschreibung                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UNTERGEORDNETER D3D10 \_ EFFECT \_ \_ \_ COMPILE-EFFEKT    | 1 << 0 | Kompilieren Sie die FX-Datei in einen untergeordneten Effekt. Untergeordnete Effekte haben keine Initialisierungen für freigegebene Werte, da diese im Effektpool initialisiert werden.                                                                                                           |
| D3D10 \_ EFFECT COMPILE ERMÖGLICHT \_ \_ \_ \_ LANGSAME OPS | 1 << 1 | Standardmäßig ist der Leistungsmodus aktiviert. Der Leistungsmodus verhindert, dass veränderliche Zustandsobjekte in Zustandsobjektdefinitionen angezeigt werden, da nicht literale Ausdrücke nicht angezeigt werden. Wenn Sie dieses Flag angeben, wird der Modus deaktiviert, und es können veränderliche Zustandsobjekte verwendet werden. |
| D3D10 \_ EFFECT \_ SINGLE \_ THREADED          | 1 << 3 | Versuchen Sie nicht, eine Synchronisierung mit anderen Threads zu versuchen, die Auswirkungen in denselben Pool laden.                                                                                                                                                                        |



 

Diese Konstanten werden in d3d10effect.h als Makros definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektkonst constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



