---
title: texldl-vs
description: Beispiel für eine Textur mit einem bestimmten Sampler. Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050768"
---
# <a name="texldl---vs"></a>texldl-vs

Beispiel für eine Textur mit einem bestimmten Sampler. Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden.

## <a name="syntax"></a>Syntax



| texldl DST, src0, Quelle1 |
|------------------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register.
-   src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.
-   Quelle1 identifiziert die Quell-Samplerregister \# , bei der \# angibt, welche Textur samplingnummer Stichproben geben soll. Der Sampler hat ihm eine Textur und einen Steuerelement Zustand zugeordnet, der durch die [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) -Enumeration definiert ist (z \_ . b. D3DSAMP MinFilter).

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| texldl                 |      |      |      |       | x    | x     |



 

texldl sucht den Textur Satz in der Samplingphase, auf die von Quelle1 verwiesen wird. Die Detailebene wird aus src0. w ausgewählt. Dieser Wert kann negativ sein. in diesem Fall ist die ausgewählte Detailstufe die "nullte 1" (größte Zuordnung) mit dem "MagFilter". Da src0. w ein Gleit Komma Wert ist, wird der Bruchteil-Wert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren (wenn MipFilter linear ist). Die samplerzustände mipmaplodbias und MaxMipLevel werden berücksichtigt. Weitere Informationen zu samplerzuständen finden Sie unter [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Wenn ein Shader-Programm eine Stichprobe von einem Sampler erstellt, der keinen Textur Satz hat, wird 0001 im Ziel Register abgerufen.

Dies ist eine Näherung zum Referenzgeräte Algorithmus.


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



Begrenzungen

-   Die Texturkoordinaten sollten nicht nach Textur Größe skaliert werden.
-   DST muss ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ) sein.
-   DST kann eine Schreib Maske akzeptieren. Siehe [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).
-   Die Standardwerte für fehlende Komponenten sind entweder 0 oder 1 und hängen vom Textur Format ab.
-   Quelle1 muss ein [Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) sein \# . Quelle1 darf keinen Negation-Modifizierer verwenden. Quelle1 verwendet möglicherweise Swizzle, das nach der Stichprobenentnahme angewendet wird, bevor die Schreib Maske berücksichtigt wird. Der Sampler muss am Anfang des Shader (mit [DCL \_ -samplertype (SM3-vs ASM)](dcl-samplertype---vs.md)) deklariert worden sein.
-   Die Anzahl der Koordinaten, die zum Ausführen des Textur Beispiels erforderlich sind, hängt davon ab, wie der Sampler deklariert wurde. Wenn Sie als Cube deklariert wurde, ist eine Textur Koordinate mit drei Komponenten erforderlich (. RGB). Die Validierung erzwingt, dass die für texldl bereitgestellten Koordinaten für die für den Sampler deklarierte Textur Dimension ausreichend sind. Es ist jedoch nicht garantiert, dass die Anwendung tatsächlich eine Textur (über die API) mit Dimensionen festgelegt, die der für den Sampler deklarierten Dimension entsprechen. In einem solchen Fall versucht die Laufzeit, Konflikte zu erkennen (möglicherweise nur im Debugmodus). Das Sampling einer Textur mit weniger Dimensionen als in der Textur Koordinate vorhanden ist zulässig, und es wird davon ausgegangen, dass die zusätzlichen Texturkoordinaten Komponenten ignoriert werden. Umgekehrt ist das Sampling einer Textur mit mehr Dimensionen als in der Textur Koordinate nicht zulässig.
-   Wenn src0 (Textur Koordinate) ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ) ist, müssen die für die Suche (oben beschriebenen) erforderlichen Komponenten bereits geschrieben worden sein.
-   Die Stichprobenentnahme nicht signierter RGB-Texturen führt zu float-Werten zwischen 0,0 und 1,0.
-   Die Stichproben signierter Texturen führen zu float-Werten zwischen-1,0 und 1,0.
-   Beim Sampling von Gleit Komma Texturen bedeutet Float16, dass die Daten innerhalb von Max \_ . Float16 liegen. Float32 bedeutet, dass der maximale Bereich der Pipeline verwendet wird. Die Stichprobenentnahme außerhalb eines Bereichs ist nicht definiert.
-   Es gibt keine abhängige Lese Beschränkung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
