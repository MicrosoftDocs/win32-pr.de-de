---
description: Diese Konstanten gelten für Auswirkung-Variablen.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE Konstanten
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343965"
---
# <a name="d3d10_effect_variable-constants"></a>D3d10 \_ Effect- \_ Variablen Konstanten

Diese Konstanten gelten für Auswirkung-Variablen.



| \#definieren                                       | BESCHREIBUNG  | Wert                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10 \_ Effect- \_ Variablen \_ Anmerkung            | 1 << 0 | Gibt an, dass dies eine Anmerkung oder eine globale Variable ist.                                                                                                                                                                                                        |
| D3d10 \_ Effect- \_ Variable in \_ Pooled                | 1 << 1 | Gibt an, dass sich diese Variable oder der Konstantenpuffer in einem Effekt Pool befindet. Wenn dieses Flag nicht festgelegt ist, befindet sich die Variable in einem eigenständigen Effekt oder einem untergeordneten Effekt (eigenständige Effekte geben false aus [**ID3D10Effect:: ispool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)zurück. |
| D3d10 \_ - \_ Variable ( \_ expliziter \_ Bindungs \_ Punkt) | 1 << 2 | Gibt an, dass die Variable mithilfe des Register-Schlüssel Worts explizit gebunden wurde.                                                                                                                                                                                 |



 

Diese Flags sind in d3d10effect. h als Makros definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Konstanten (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



