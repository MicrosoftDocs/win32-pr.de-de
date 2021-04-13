---
description: Diese Konstanten werden beim Erstellen eines Effekts verwendet, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT Konstanten
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342159"
---
# <a name="d3d10_effect-constants"></a>D3d10 \_ Effect-Konstanten

Diese Konstanten werden beim Erstellen eines Effekts verwendet, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren.



| \#definieren                                 | Wert        | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10 \_ Effekt \_ Kompilieren des untergeordneten \_ \_ Effekts    | 1 << 0 | Kompilieren Sie die FX-Datei mit einem untergeordneten Effekt. Untergeordnete Effekte haben keine Initialisiert für freigegebene Werte, da diese im Effekt Pool initialisiert werden.                                                                                                           |
| D3d10 \_ Effekt- \_ Kompilierung \_ \_ langsame \_ Ops zulassen | 1 << 1 | Standardmäßig ist der Leistungsmodus aktiviert. Der Leistungsmodus lässt änderbare Zustands Objekte nicht zu, indem verhindert wird, dass nicht literale Ausdrücke in Zustands Objekt Definitionen angezeigt werden. Wenn Sie dieses Flag angeben, wird der Modus deaktiviert, und es werden änderbare Zustands Objekte zugelassen. |
| D3d10 \_ Effect \_ Single \_ Thread          | 1 << 3 | Versuchen Sie nicht, mit anderen Threads zu synchronisieren, die Auswirkungen in denselben Pool laden.                                                                                                                                                                        |



 

Diese Konstanten werden in d3d10effect. h als Makros definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Konstanten (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



