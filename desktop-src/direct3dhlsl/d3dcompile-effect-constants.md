---
title: D3DCOMPILE_EFFECT Konstanten (D3DCompiler. h)
description: Diese Konstanten leiten direkt, wie der Compiler eine Effekt Datei kompiliert oder wie die Laufzeit die Effekt Datei verarbeitet.
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
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982120"
---
# <a name="d3dcompile_effect-constants"></a>D3DCOMPILE \_ Effect-Konstanten

Diese Konstanten leiten direkt, wie der Compiler eine Effekt Datei kompiliert oder wie die Laufzeit die Effekt Datei verarbeitet.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**Untergeordneter Effekt von D3DCOMPILE \_ Effect \_ \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Kompilieren Sie die Effekt Datei (. fx) in einen untergeordneten Effekt. Untergeordnete Effekte verfügen über keine Initialisierer für freigegebene Werte, da diese untergeordneten Effekte im Haupteffekt (dem Effekt Pool) initialisiert werden.

> [!Note]  
> Effekt Pools werden von Effekten 10 (FX10) unterstützt, aber nicht durch Effekte 11 (FX11). Weitere Informationen zu Unterschieden zwischen den Effekts-Pools in Direct3D 10-und Effect-Gruppen in Direct3D 11 finden Sie unter [Auswirkungen von Pools und Gruppen](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ Effekt \_ \_ langsame \_ Ops zulassen**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Deaktiviert den Leistungsmodus und ermöglicht änderbare Zustands Objekte.

Standardmäßig ist der Leistungsmodus aktiviert. Der Leistungsmodus lässt änderbare Zustands Objekte nicht zu, indem verhindert wird, dass nicht literale Ausdrücke in Zustands Objekt Definitionen angezeigt werden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DCompiler-Konstanten](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

