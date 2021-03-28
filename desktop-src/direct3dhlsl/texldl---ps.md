---
title: texldl-PS
description: Beispiel für eine Textur mit einem bestimmten Sampler. Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981137"
---
# <a name="texldl---ps"></a>texldl-PS

Beispiel für eine Textur mit einem bestimmten Sampler. Die jeweilige MipMap-Detailebene, für die ein Sampling durchgeführt wird, muss als vierte Komponente der Textur Koordinate angegeben werden.

## <a name="syntax"></a>Syntax



| texldl DST, src0, Quelle1 |
|------------------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register.
-   src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt. Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   Quelle1 identifiziert die Quell-Samplerregister \# , bei der \# angibt, welche Textur samplingnummer Stichproben geben soll. Der Sampler hat ihm eine Textur und einen Steuerelement Zustand zugeordnet, der durch die [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) -Enumeration definiert ist (z \_ . b. D3DSAMP MinFilter).

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl sucht den Textur Satz in der Samplingphase, auf die von Quelle1 verwiesen wird. Die Detailebene wird aus src0. w ausgewählt. Dieser Wert kann negativ sein. in diesem Fall handelt es sich bei der ausgewählten Detailebene um die nullten (größte Karte) mit dem MagFilter. Da src0. w ein Gleit Komma Wert ist, wird der Bruchteil-Wert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren (wenn MipFilter linear ist). Die samplerzustände mipmaplodbias und MaxMipLevel werden berücksichtigt. Weitere Informationen zu samplerzuständen finden Sie unter [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Wenn ein Shader-Programm eine Stichprobe von einem Sampler durchführt, der keinen Textur Satz hat, wird 0001 im Ziel Register abgerufen.

Im folgenden finden Sie einen groben Algorithmus, dem das Referenzgerät folgt:


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



Begrenzungen

-   Die Texturkoordinaten sollten nicht nach Textur Größe skaliert werden.
-   DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein.
-   DST kann einen Schreib Versuch akzeptieren. Siehe [Ziel Registrierung schreiben Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   Die Standardwerte für fehlende Komponenten sind entweder 0 oder 1 und hängen vom Textur Format ab.
-   Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# . Quelle1 darf keinen Negation-Modifizierer verwenden (siehe [Ziel-Register Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)). Quelle1 verwendet möglicherweise "Swizzle" (siehe [Quell Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)"), das nach dem Sampling angewendet wird, jedoch vor der Schreib Maske (siehe Ziel-Register Schreib Maske) berücksichtigt wird. Der Sampler muss am Anfang des Shader (mit [DCL- \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) deklariert worden sein.
-   Die Anzahl der Koordinaten, die zum Ausführen des Textur Beispiels erforderlich sind, hängt davon ab, wie der Sampler deklariert wurde. Wenn Sie als Cube deklariert wurde, ist eine Textur Koordinate mit drei Komponenten erforderlich (. RGB). Die Validierung erzwingt, dass für die Tex-LDL bereitgestellte Koordinaten \_ für die für den Sampler deklarierte Textur Dimension ausreichend sind. Es ist jedoch nicht sichergestellt, dass die Anwendung tatsächlich eine Textur (über die API) mit Dimensionen festlegt, die der für den Sampler deklarierten Dimension entsprechen. In einem solchen Fall versucht die Laufzeit, Konflikte zu erkennen (möglicherweise nur im Debugmodus). Das Sampling einer Textur mit weniger Dimensionen, als in der Textur Koordinate vorhanden sind, wird zugelassen, und es wird davon ausgegangen, dass die zusätzlichen Texturkoordinaten Komponenten ignoriert werden. Umgekehrt ist das Sampling einer Textur mit mehr Dimensionen als in der Textur Koordinate nicht zulässig.
-   Wenn src0 (Textur Koordinate) [temporär registriert](dx9-graphics-reference-asm-ps-registers-temporary.md)ist, müssen die für die Suche (oben beschriebenen) erforderlichen Komponenten bereits geschrieben worden sein.
-   Die Stichprobenentnahme nicht signierter RGB-Texturen führt zu float-Werten zwischen 0,0 und 1,0.
-   Die Stichproben signierter Texturen führen zu float-Werten zwischen-1,0 und 1,0.
-   Beim Sampling von Gleit Komma Texturen bedeutet Float16, dass die Daten innerhalb von Max \_ . Float16 liegen. Float32 bedeutet, dass der maximale Bereich der Pipeline verwendet wird. Die Stichprobenentnahme außerhalb eines Bereichs ist nicht definiert.
-   Es gibt keine abhängige Lese Beschränkung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
