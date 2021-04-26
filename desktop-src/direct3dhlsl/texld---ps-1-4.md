---
title: texld – ps_1_4
description: Lädt das Zielregister mit Farbdaten (RGBA), die mit dem Inhalt des Quellregisters als Texturkoordinaten entnommen wurden. Die Textur mit Stichproben ist die Textur, die der Zielregisternummer zugeordnet ist.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996867"
---
# <a name="texld---ps_1_4"></a>texld - ps \_ 1 \_ 4

Lädt das Zielregister mit Farbdaten (RGBA), die mit dem Inhalt des Quellregisters als Texturkoordinaten entnommen wurden. Die Textur mit Stichproben ist die Textur, die der Zielregisternummer zugeordnet ist.



| texld dst, src |
|----------------|



 

## <a name="registers"></a>Register



|          |                      | vn        | Cn  | Tn  | Rn  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| dst      | Zielregister |           |     |     | x   | 1\_4         |
| src      | Quellregister      |           |     | x   |     | 1 \_ 4. Phase 1 |
|          |                      |           |     | x   | x   | 1 \_ 4 Phase   |



 

Wenn Sie r(n) als Quellregister verwenden, müssen die ersten drei Komponenten (XYZ) in der vorherigen Phase des Shaders initialisiert worden sein.

Weitere Informationen zu Registern finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)

## <a name="remarks"></a>Hinweise

Diese Anweisung erfasst die Textur in der Texturphase, die der Zielregisternummer zugeordnet ist. Die Textur wird mithilfe von Texturkoordinatendaten aus dem Quellregister entnommen.

Die Syntax für die Texld- und Texcrd-Anweisungen macht Unterstützung für eine projektive Division mit einem Texturregistermodifizierer verfügbar. Für die Pixelshaderversion 1.4 wird das D3DTTFF \_ PROJECTED-Texturtransformationsflag immer ignoriert.

Regeln für die Verwendung von texld:

1.  Der gleiche .xyz- oder .xyw-Modifizierer muss auf jeden Lese- eines einzelnen t(n)-Registers in texcrd- oder texld-Anweisungen angewendet werden. Wenn .xyw für t(n)-Registerleseungen verwendet wird, kann dies mit anderen Lesezeichen desselben t(n)-Registers mit .xyw dw kombiniert \_ werden.
2.  Der \_ dz-Quellmodifizierer ist nur für texld mit r(n) source register (also nur Phase 2) gültig.
3.  Der \_ dz-Quellmodifizierer kann nicht mehr als zweimal pro Shader verwendet werden.



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Beispiele

Die texld-Anweisung bietet eine gewisse Kontrolle darüber, welche Komponenten der Quelltexturkoordinatendaten verwendet werden. Der vollständige Satz zulässiger Syntax für texld folgt und enthält alle gültigen Quellregistermodifizierer, Selektoren und Schreibmaskenkombinationen.


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

 

 




