---
title: D3DCOMPILE_EFFECT Konstanten (D3DCompiler.h)
description: Diese Konstanten leiten an, wie der Compiler eine Effektdatei kompiliert oder wie die Laufzeit die Effektdatei verarbeitet.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d5c31efb17d2f852ac3903a5946ce5fb72fcef86ef083c474328859472c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286914"
---
# <a name="d3dcompile_effect-constants"></a>D3DCOMPILE \_ EFFECT-Konstanten

Diese Konstanten leiten an, wie der Compiler eine Effektdatei kompiliert oder wie die Laufzeit die Effektdatei verarbeitet.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**UNTERGEORDNETER D3DCOMPILE \_ \_ \_ EFFECT-EFFEKT**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Kompilieren Sie die Effektdatei (.fx) in einen untergeordneten Effekt. Untergeordnete Effekte verfügen über keine Initialisierer für freigegebene Werte, da diese untergeordneten Effekte im Mastereffekt (dem Effektpool) initialisiert werden.

> [!Note]  
> Effektpools werden von Effekten 10 (FX10), aber nicht von Effekten 11 (FX11) unterstützt. Weitere Informationen zu den Unterschieden zwischen Effektpools in Direct3D 10 und Effektgruppen in Direct3D 11 finden Sie unter [Effektpools und -gruppen.](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences)

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ EFFECT \_ ALLOW \_ SLOW \_ OPS**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Deaktiviert den Leistungsmodus und ermöglicht veränderliche Zustandsobjekte.

Standardmäßig ist der Leistungsmodus aktiviert. Der Leistungsmodus verhindert veränderliche Zustandsobjekte, indem verhindert wird, dass nicht literale Ausdrücke in Zustandsobjektdefinitionen angezeigt werden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DCompiler.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DCompiler-Konstanten](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

