---
title: texld – ps_1_4
description: Lädt das Zielregister mit Farbdaten (RGBA), die mithilfe des Inhalts des Quellregisters als Texturkoordinaten entnommen wurden. Die entnommene Textur ist die Textur, die der Zielregisternummer zugeordnet ist.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d956d9176a6356dc3837ee4f4d13b5bb700dda98
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118825"
---
# <a name="texld---ps_1_4"></a>texld – ps \_ 1 \_ 4

Lädt das Zielregister mit Farbdaten (RGBA), die mithilfe des Inhalts des Quellregisters als Texturkoordinaten entnommen wurden. Die entnommene Textur ist die Textur, die der Zielregisternummer zugeordnet ist.



| texld dst, src |
|----------------|



 

## <a name="registers"></a>Register



| Wert         | Beschreibung                     | vn        | Cn  | Tn  | Rn  | Pixel-Shaderversion              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| dst      | Zielregister |           |     |     | x   | 1\_4         |
| src      | Quellregister      |           |     | x   |     | 1 \_ 4 Phase 1 |
|          |                      |           |     | x   | x   | 1 \_ 4 Phase   |



 

Bei Verwendung von r(n) als Quellregister müssen die ersten drei Komponenten (XYZ) in der vorherigen Phase des Shaders initialisiert worden sein.

Weitere Informationen zu Registern finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)

## <a name="remarks"></a>Bemerkungen

Diese Anweisung untersucht die Textur in der Texturphase, die der Zielregisternummer zugeordnet ist. Die Textur wird mithilfe von Texturkoordinatendaten aus dem Quellregister entnommen.

Die Syntax für die Anweisungen texld und texcrd macht Unterstützung für eine projektive Division mit einem Texturregistermodifizierer verfügbar. Für Die Pixel-Shaderversion 1.4 wird das D3DTTFF \_ PROJECTED-Texturtransformationsflag immer ignoriert.

Regeln für die Verwendung von texld:

1.  Der gleiche MODIFI-Modifizierer ".xyz" oder ".xyw" muss sowohl in texcrd- als auch in texld-Anweisungen auf jeden Leses eines einzelnen t(n)-Registers angewendet werden. Wenn .xyw für t(n)-Registerlesedaten verwendet wird, kann dies mit anderen Lesezeichen desselben t(n)-Registers mithilfe von .xyw dw gemischt \_ werden.
2.  Der \_ Quellcodemodifizierer ist nur für texld mit dem Quellregister r(n) gültig (daher nur Phase 2).
3.  Der \_ Quellmodifizierer kann nicht mehr als zweimal pro Shader verwendet werden.



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
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

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




