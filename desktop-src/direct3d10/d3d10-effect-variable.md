---
description: Diese Konstanten gelten für Effektvariablen.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE Konstanten
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7541253fffd6671e01a8da38c06fd15924d45b461d5acc0e468fd17660746f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736069"
---
# <a name="d3d10_effect_variable-constants"></a>D3D10 \_ EFFECT \_ VARIABLE-Konstanten

Diese Konstanten gelten für Effektvariablen.



| \#Definieren                                       | Beschreibung  | Wert                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANMERKUNG ZU D3D10 \_ \_ \_ EFFECT-VARIABLEN            | 1 << 0 | Gibt an, dass es sich um eine Anmerkung oder eine globale Variable handelt.                                                                                                                                                                                                        |
| D3D10 \_ EFFECT \_ VARIABLE \_ POOLED                | 1 << 1 | Gibt an, dass sich diese Variable oder dieser konstante Puffer in einem Effektpool befindet. Wenn dieses Flag nicht festgelegt ist, befindet sich die Variable in einem eigenständigen Effekt oder einem untergeordneten Effekt (eigenständige Effekte geben FALSE von [**ID3D10Effect::IsPool zurück.**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool) |
| D3D10 \_ EFFECT \_ VARIABLE \_ EXPLICIT \_ BIND \_ POINT | 1 << 2 | Gibt an, dass die Variable explizit mithilfe des Register-Schlüsselworts gebunden wurde.                                                                                                                                                                                 |



 

Diese Flags werden als Makros in d3d10effect.h definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektkonst constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



