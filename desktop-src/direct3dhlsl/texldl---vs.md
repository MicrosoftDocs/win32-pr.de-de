---
title: texldl – vs
description: Beispiel für eine Textur mit einem bestimmten Sampler. Die bestimmte mipmap-Detailebene, für die Stichproben entnommen werden, muss als vierte Komponente der Texturkoordinate angegeben werden. | texldl – vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b06d9529d4f7e6bf8e44339290855d50e6668d67f56305fbc3bbeb77ad4b217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787850"
---
# <a name="texldl---vs"></a>texldl – vs

Beispiel für eine Textur mit einem bestimmten Sampler. Die bestimmte mipmap-Detailebene, für die Stichproben entnommen werden, muss als vierte Komponente der Texturkoordinate angegeben werden.

## <a name="syntax"></a>Syntax



| texldl dst, src0, src1 |
|------------------------|



 

Hierbei gilt:

-   dst ist ein Zielregister.
-   src0 ist ein Quellregister, das die Texturkoordinaten für das Texturbeispiel enthält.
-   src1 identifiziert das Quell-Samplerregister (s), wobei angibt, welche \# \# Texturs samplernummer entnommen werden soll. Der Sampler hat ihm eine Textur und einen Steuerelementzustand zugeordnet, die durch die [**D3DSAMPLERSTATETYPE-Enumeration**](/windows/desktop/direct3d9/d3dsamplerstatetype) definiert sind (z. B. D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| texldl                 |      |      |      |       | x    | x     |



 

texldl sucht den Textursatz in der Samplerphase, auf die src1 verweist. Die Detailebene wird in src0.w ausgewählt. Dieser Wert kann negativ sein. In diesem Fall ist die ausgewählte Detailebene die "nullte" (größte Karte) mit dem MAGFILTER. Da src0.w ein Gleitkommawert ist, wird der Bruchwert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren (wenn MIPFILTER LINEAR ist). Der Sampler gibt an, dass MIPMAPLODBIAS und MAXMIPLEVEL verwendet werden. Weitere Informationen zu Samplerzuständen finden Sie unter [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Wenn ein Shaderprogramm Stichproben von einem Sampler ohne Textursatz entnommen hat, wird 0001 im Zielregister ermittelt.

Dies ist eine Näherung an den Referenzgerätealgorithmus.


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



Beschränkungen:

-   Die Texturkoordinaten sollten nicht nach Texturgröße skaliert werden.
-   dst muss ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r) \# sein.
-   dst kann eine Schreibmaske akzeptieren. Weitere Informationen [finden Sie unter Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).
-   Die Standardwerte für fehlende Komponenten sind entweder 0 oder 1 und hängen vom Texturformat ab.
-   src1 muss ein [Sampler (Direct3D 9 asm-vs) (s)](dx9-graphics-reference-asm-vs-registers-sampler.md) \# sein. src1 darf keinen Negatmodifizierer verwenden. src1 kann Swizzle verwenden, das nach der Stichprobenentnahme angewendet wird, bevor die Schreibmaske verwendet wird. Der Sampler muss am Anfang des Shaders deklariert worden sein [(mit dcl \_ samplerType (sm3 – vs asm)](dcl-samplertype---vs.md)).
-   Die Anzahl der Koordinaten, die zum Ausführen der Texturstichprobe erforderlich sind, hängt davon ab, wie der Sampler deklariert wurde. Wenn er als Cube deklariert wurde, ist eine Texturkoordinate mit drei Komponenten erforderlich (RGB). Die Validierung erzwingt, dass koordinaten, die für texldl bereitgestellt werden, für die für den Sampler deklarierte Texturdimension ausreichend sind. Es ist jedoch nicht garantiert, dass die Anwendung tatsächlich eine Textur (über die API) mit Dimensionen festgelegt hat, die der für den Sampler deklarierten Dimension entspricht. In einem solchen Fall versucht die Runtime, Nichtübereinstimmungen zu erkennen (möglicherweise nur beim Debuggen). Das Sampling einer Textur mit weniger Dimensionen als in der Texturkoordinate ist zulässig, und es wird davon ausgegangen, dass die zusätzlichen Texturkoordinatenkomponenten ignoriert werden. Umgekehrt ist das Sampling einer Textur mit mehr Dimensionen als in der Texturkoordinate zulässig.
-   Wenn src0 (Texturkoordinate) ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r) ist, müssen die für die Suche erforderlichen Komponenten \# (oben beschrieben) bereits geschrieben worden sein.
-   Das Sampling von RGB-Texturen ohne Vorzeichen führt zu Gleitkommawerten zwischen 0,0 und 1,0.
-   Das Sampling signierter Texturen führt zu Gleitkommawerten zwischen -1,0 und 1,0.
-   Beim Sampling von Gleitkommatexturen bedeutet Float16, dass die Daten innerhalb von MAX \_ FLOAT16 liegen. Float32 bedeutet, dass der maximale Bereich der Pipeline verwendet wird. Die Stichprobenentnahme außerhalb eines bereichs ist nicht definiert.
-   Es gibt kein abhängiges Leselimit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
