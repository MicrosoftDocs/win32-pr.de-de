---
title: Pixel-Shader-quellregistrierungs Modifizierern
description: Verwenden Sie die quellregistrierungs modifiziererer, um den Wert zu ändern, der aus einem Register gelesen wird, bevor eine Anweisung
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311490"
---
# <a name="pixel-shader-source-register-modifiers"></a>Pixel-Shader-quellregistrierungs Modifizierern

Verwenden Sie die quellregistrierungs modifiziererer, um den Wert zu ändern, der aus einem Register gelesen wird, bevor eine Anweisung Der Inhalt eines Quell Registers bleibt unverändert. Modifizierer sind nützlich, um den Bereich der Register Daten zur Vorbereitung der Anweisung anzupassen. Ein Satz von Modifizierern, die als Selektoren bezeichnet werden, kopiert oder repliziert die Daten von einem einzelnen Kanal (r, g, b, a) in die anderen Kanäle.

## <a name="ps_1_1---ps_1_4"></a>PS \_ 1 \_ 1-PS \_ 1 \_ 4

Diese Tabelle identifiziert die Versionen, die die einzelnen Modifizierer unterstützen:



| Quellregistrierungs modifiziererer                                                                                    | Syntax         | Version |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |     |     |
| [eingenommen](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | \_Befangenheit registrieren | X       | X    | X    | X    |     |     |
| [umkehren](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1: registrieren   | X       | X    | X    | X    |     |     |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- sich    | X       | X    | X    | X    |     |     |
| [Skalieren um 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | Registrieren von \_ x2   |         |      |      | X    |     |     |
| [signierte Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | \_bx2 registrieren  | X       | X    | X    | X    |     |     |
| [texld-und texcrd-Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | Registrieren von \_ d\*  | X       | X    | X    | X    |     |     |
| [Quellen Register (swizzelnder)](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | Register. xyzw  | X       | X    | X    | X    |     |     |



 

Modifizierermodifiziererer für die Quelle können nur in arithmetischen Anweisungen verwendet werden. Sie können nicht für Textur Adress Anweisungen verwendet werden. Eine Ausnahme bildet der " [Scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) "-Modifizierer. Bei Version 1 \_ 1 kann die signierte Skala für das Quell Argument einer beliebigen texm- \* Anweisung verwendet werden. Bei Version 1 \_ 2 oder 1 \_ 3 kann die signierte Skala für das Quell Argument einer beliebigen Textur Adress Anweisung verwendet werden.

Bestimmte Einschränkungen für den Modifizierer:

-   Negate können entweder mit dem-Modifizierer "Bias", "signed Scaling" oder "scalex2" kombiniert werden. Wenn Sie kombiniert werden, wird Negation zuletzt ausgeführt.
-   Invert kann nicht mit einem anderen Modifizierer kombiniert werden.
-   Invert, Negate, Bias, signierte Skalierung und scalex2 können mit jedem der Selektoren kombiniert werden.
-   Modifizierermodifiziererer für die Quelle dürfen nicht in konstanten Registern verwendet werden, da Sie zu nicht definierten Ergebnissen führen. Bei Version 1 \_ 4 sind modifiziererer für Konstanten nicht zulässig, und die Überprüfung wird fehlschlagen.

## <a name="ps_2_0-and-above"></a>PS \_ 2 \_ 0 und höher

Bei Version PS \_ 2 \_ 0 und höher wurde die Anzahl der modifiziererer vereinfacht.

### <a name="negate"></a>Negate

Negieren Sie den Inhalt des Quell Registers.



| Komponentenmodifizierer | BESCHREIBUNG     |
|--------------------|-----------------|
| \- r               | Quell Negation |



 

Der Negation-Modifizierer kann nicht für das zweite Quell Register dieser Anweisungen verwendet werden: [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)und [M4x4-PS](m4x4---ps.md).



| Pixel-Shader-Versionen | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Absoluter Wert

Nehmen Sie den absoluten Wert des Register.



| Pixel-Shader-Versionen | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Wenn ein Shader der Version 3 aus mindestens einem konstanten float-Register (c \# ) liest, muss einer der folgenden Werte zutreffen.

-   Alle Konstanten Gleit Komma Register müssen den ABS-Modifizierer verwenden.
-   Keines der Konstanten Gleit Komma Register kann den ABS-Modifizierer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshadermodifizierern](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




