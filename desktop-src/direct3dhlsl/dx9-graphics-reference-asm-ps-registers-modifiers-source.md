---
title: Quellregistermodifizierer für Pixelshader
description: Verwenden Sie Quellregistermodifizierer, um den Aus einem Register gelesenen Wert zu ändern, bevor eine Anweisung ausgeführt wird.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0626449e0a38cb695f5f3c9402969df3a25c192ad7a16ef3311053c7843e0667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673310"
---
# <a name="pixel-shader-source-register-modifiers"></a>Quellregistermodifizierer für Pixelshader

Verwenden Sie Quellregistermodifizierer, um den Aus einem Register gelesenen Wert zu ändern, bevor eine Anweisung ausgeführt wird. Der Inhalt eines Quellregisters bleibt unverändert. Modifizierer sind nützlich, um den Bereich der Registerdaten als Vorbereitung für die Anweisung anzupassen. Eine Reihe von Modifizierern, die als Selektoren bezeichnet werden, kopiert oder repliziert die Daten aus einem einzelnen Kanal (r,g,b,a) in die anderen Kanäle.

## <a name="ps_1_1---ps_1_4"></a>ps \_ 1 \_ 1 - ps \_ 1 \_ 4

In dieser Tabelle sind die Versionen aufgeführt, die die einzelnen Modifizierer unterstützen:



| Modifizierer für Quellregister                                                                                    | Syntax         | Version 1 \_ 1 | Version 1 \_ 2     | Version 1 \_ 3     | Version 1 \_ 4     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [Vorurteil](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | \_Registervoreingenommenheit | X       | X    | X    | X    |
| [Invertieren](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1– Registrieren   | X       | X    | X    | X    |
| [Negieren](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- Registrieren    | X       | X    | X    | X    |
| [Skalierung um 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | Registrieren \_ von x2   |         |      |      | X    |
| [Signierte Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | register \_ bx2  | X       | X    | X    | X    |
| [Texld- und Texcrd-Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | register \_ d\*  | X       | X    | X    | X    |
| [Quellenregister-Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | register.xyzw  | X       | X    | X    | X    |



 

Quellregistermodifizierer können nur für arithmetische Anweisungen verwendet werden. Sie können nicht für Texturadressanweisungen verwendet werden. Die Ausnahme ist der Modifizierer [Scale by 2.](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) Für Version 1 \_ 1 kann die signierte Skalierung für das Quellargument jeder texm-Anweisung verwendet \* werden. Für Version \_ 1 2 oder 1 \_ 3 kann die signierte Skala für das Quellargument einer beliebigen Texturadressanweisung verwendet werden.

Einige modifiziererspezifische Einschränkungen:

-   "Negate" kann entweder mit dem Modifizierer "Bias", "Signed Scaling" oder "scalex2" kombiniert werden. In kombination wird "negate" zuletzt ausgeführt.
-   Invert kann nicht mit einem anderen Modifizierer kombiniert werden.
-   Invertieren, Negieren, Voreingenommenheit, signierte Skalierung und Scalex2 können mit jedem der Selektoren kombiniert werden.
-   Quellregistermodifizierer sollten nicht für Konstantenregister verwendet werden, da sie nicht definierte Ergebnisse verursachen. Für Version 1 \_ 4 sind Modifizierer für Konstanten nicht zulässig und schlagen bei der Überprüfung fehl.

## <a name="ps_2_0-and-above"></a>ps \_ 2 \_ 0 und höher

Für Version ps \_ 2 \_ 0 und höher wurde die Anzahl der Modifizierer vereinfacht.

### <a name="negate"></a>Negate

Negieren Sie den Inhalt des Quellregisters.



| Komponentenmodifizierer | Beschreibung     |
|--------------------|-----------------|
| \- R               | Quell negation |



 

Der Modifizierer negate kann nicht im zweiten Quellregister dieser Anweisungen verwendet werden: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md)und [m4x4 - ps](m4x4---ps.md).



| Pixelshaderversionen | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Absoluter Wert

Nehmen Sie den absoluten Wert des Registers.



| Pixelshaderversionen | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Wenn ein Shader der Version 3 aus einem oder mehreren konstanten float-Registern (c) liest, \# muss eines der folgenden Punkte zutreffen.

-   Alle konstanten Gleitkommaregister müssen den Abs-Modifizierer verwenden.
-   Keiner der konstanten Gleitkommaregister kann den Abs-Modifizierer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registermodifizierer für Pixel-Shader](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




