---
title: texldl - ps
description: Beispiel für eine Textur mit einem bestimmten Sampler. Die bestimmte mipmap-Detailebene, für die Stichproben entnommen werden, muss als vierte Komponente der Texturkoordinate angegeben werden. | texldl - ps
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f66bc54f00e5eb560589429f1cb116183e165a36d90f5d560d8895678a2d5bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723177"
---
# <a name="texldl---ps"></a>texldl - ps

Beispiel für eine Textur mit einem bestimmten Sampler. Die bestimmte mipmap-Detailebene, für die Stichproben entnommen werden, muss als vierte Komponente der Texturkoordinate angegeben werden.

## <a name="syntax"></a>Syntax



| texldl dst, src0, src1 |
|------------------------|



 

Hierbei gilt:

-   dst ist ein Zielregister.
-   src0 ist ein Quellregister, das die Texturkoordinaten für das Texturbeispiel enthält. Weitere Informationen [finden Sie unter Texturkoordinatenregister.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifiziert das Quell-Samplerregister (s), wobei angibt, welche \# \# Texturs samplernummer entnommen werden soll. Der Sampler hat ihm eine Textur und einen Steuerelementzustand zugeordnet, die durch die [**D3DSAMPLERSTATETYPE-Enumeration**](/windows/desktop/direct3d9/d3dsamplerstatetype) definiert sind (z. B. D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl sucht den Textursatz in der Samplerphase, auf die src1 verweist. Die Detailebene wird in src0.w ausgewählt. Dieser Wert kann negativ sein. In diesem Fall ist die ausgewählte Detailebene die nullte (größte Karte) mit dem MAGFILTER. Da src0.w ein Gleitkommawert ist, wird der Bruchwert verwendet, um zwischen zwei Mip-Ebenen zu interpolieren (wenn MIPFILTER LINEAR ist). Der Sampler gibt an, dass MIPMAPLODBIAS und MAXMIPLEVEL verwendet werden. Weitere Informationen zu Samplerzuständen finden Sie unter [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Wenn ein Shaderprogramm Stichproben von einem Sampler ohne Textursatz entnommen hat, wird 0001 im Zielregister erhalten.

Im Folgenden finden Sie einen groben Algorithmus, dem das Referenzgerät folgt:


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
   LOD = MAX( MAXMIPLEVEL, LOD );
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
-   dst muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r) \# sein.
-   dst kann eine Schreibmaske akzeptieren. Weitere Informationen finden [Sie unter Zielregister-Schreibmaske.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)
-   Die Standardwerte für fehlende Komponenten sind entweder 0 oder 1 und hängen vom Texturformat ab.
-   src1 muss ein [Sampler (Direct3D 9 asm-ps) (s)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# sein. src1 verwendet möglicherweise keinen Negatmodifizierer (siehe [Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)). src1 kann Swizzle verwenden (siehe Quellregister [Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), das nach der Stichprobenentnahme angewendet wird, aber bevor die Schreibmaske (siehe Zielregister-Schreibmaske) verwendet wird. Der Sampler muss am Anfang des Shaders deklariert worden sein [(mit dcl \_ samplerType (sm2, sm3 - ps asm).](dcl-samplertype---ps.md)
-   Die Anzahl der Koordinaten, die zum Ausführen der Texturstichprobe erforderlich sind, hängt davon ab, wie der Sampler deklariert wurde. Wenn er als Cube deklariert wurde, ist eine Texturkoordinate mit drei Komponenten erforderlich (RGB). Die Validierung erzwingt, dass koordinaten, die für tex ldl bereitgestellt werden, für die \_ Texturdimension ausreichen, die für den Sampler deklariert wurde. Es ist jedoch nicht garantiert, dass die Anwendung tatsächlich eine Textur (über die API) mit Dimensionen fest legt, die der für den Sampler deklarierten Dimension entspricht. In einem solchen Fall versucht die Runtime, Nichtübereinstimmungen zu erkennen (möglicherweise nur beim Debuggen). Das Sampling einer Textur mit weniger Dimensionen als in der Texturkoordinate ist zulässig und wird davon ausgegangen, dass die zusätzlichen Texturkoordinatenkomponenten ignoriert werden. Umgekehrt ist das Sampling einer Textur mit mehr Dimensionen als in der Texturkoordinate unzulässig.
-   Wenn src0 (Texturkoordinate) ["Temporary Register"](dx9-graphics-reference-asm-ps-registers-temporary.md)ist, müssen die komponenten, die für die Suche erforderlich sind (oben beschrieben), zuvor geschrieben worden sein.
-   Das Sampling von RGB-Texturen ohne Vorzeichen führt zu Gleitkommawerten zwischen 0,0 und 1,0.
-   Das Sampling signierter Texturen führt zu Gleitkommawerten zwischen -1,0 und 1,0.
-   Beim Sampling von Gleitkommatexturen bedeutet Float16, dass die Daten innerhalb von MAX \_ FLOAT16 liegen. Float32 bedeutet, dass der maximale Bereich der Pipeline verwendet wird. Die Stichprobenentnahme außerhalb eines bereichs ist nicht definiert.
-   Es gibt kein abhängiges Leselimit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
