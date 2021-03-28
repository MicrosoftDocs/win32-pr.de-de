---
title: texld-ps_1_4
description: Lädt das Ziel Register mit Farbdaten (RGBA), wobei der Inhalt des Quell Registers als Texturkoordinaten verwendet wird. Die Stichproben Textur ist die Textur, die der Ziel Registernummer zugeordnet ist.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993143"
---
# <a name="texld---ps_1_4"></a>texld-PS \_ 1 \_ 4

Lädt das Ziel Register mit Farbdaten (RGBA), wobei der Inhalt des Quell Registers als Texturkoordinaten verwendet wird. Die Stichproben Textur ist die Textur, die der Ziel Registernummer zugeordnet ist.



| texld DST, src |
|----------------|



 

## <a name="registers"></a>Register



| Argument | BESCHREIBUNG          | Register |     |     |     | Version      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | VN        | 2.300  | TN  | Mar  |              |
| DST      | Ziel Register |           |     |     | x   | 1\_4         |
| src      | Quell Register      |           |     | x   |     | 1 \_ 4 Phase 1 |
|          |                      |           |     | x   | x   | 1 \_ 4-Phase   |



 

Wenn Sie r (n) als Quell Register verwenden, müssen die ersten drei Komponenten (XYZ) in der vorherigen Phase des Shaders initialisiert worden sein.

Weitere Informationen zu Registern finden Sie unter [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Bemerkungen

Diese Anweisung gibt eine Stichprobe der Textur in der Textur Phase aus, die der Ziel Registernummer zugeordnet ist. Die Textur wird mithilfe von Texturkoordinaten Daten aus dem Quell Register entnommen.

Die Syntax für die Anweisungen texld und texcrd macht die Unterstützung für eine Projective Teilung mit einem Textur Register-Modifizierer verfügbar. Für die Pixel-Shader-Version 1,4 \_ wird das Flag D3DTTFF projiziertes Textur Transform immer ignoriert.

Regeln für die Verwendung von texld:

1.  Der gleiche. XYZ-oder. xyw-Modifizierer muss auf jeden Lesevorgang eines einzelnen t (n)-Registers in texcrd-oder texld-Anweisungen angewendet werden. Wenn ". xyw" für t (n)-Registrierungs Lesevorgänge verwendet wird, kann dies mit anderen Lesevorgängen desselben t-Registers (n) mithilfe von. xyw DW gemischt werden \_ .
2.  Der- \_ Modifizierer für die DZ-Quelle ist nur für texld mit r (n)-Quell Register gültig (daher nur Phase 2).
3.  Der- \_ Modifizierer für die DZ-Quelle darf nicht mehr als zwei Mal pro Shader verwendet werden.



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Beispiele

Die texld-Anweisung bietet eine gewisse Kontrolle darüber, welche Komponenten der Quell Textur Daten verwendet werden. Der vollständige Satz zulässiger Syntax für texld folgt und enthält alle gültigen Quell Registrierungs Modifizierern, Selektoren und Schreib Masken Kombinationen.


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




