---
title: Ziel Registrierungs-Schreib Maske
description: Eine Schreib Maske steuert, welche Komponenten eines Ziel Registers geschrieben werden, nachdem eine Anweisung abgeschlossen wurde.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948085"
---
# <a name="destination-register-write-mask"></a>Ziel Registrierungs-Schreib Maske

Eine Schreib Maske steuert, welche Komponenten eines Ziel Registers geschrieben werden, nachdem eine Anweisung abgeschlossen wurde. Eine Ausgabe Schreib Maske ist zulässig, solange die Komponenten in der Reihenfolge von. RGBA oder. xyzw vorliegen. Das heißt, dass RBA und XW gültige Masken sind. Textur Register verfügen über einen Regelsatz, und nicht Textur Register verfügen über einen anderen Satz von Regeln.

## <a name="syntax"></a>Syntax



| DST. Write-Ask |
|---------------|



 

where

-   DST ist ein Ziel Register.
-   beim Schreiben von Schreib Vorwörtern handelt es sich um eine Sequenz von Masken, die entweder festgelegt sind: (x, y, z, w) oder (rot, grün, blau, Alpha).

## <a name="remarks"></a>Bemerkungen

Die folgenden Ziel Schreib Masken sind verfügbar.



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| . xyzw (Standard)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . XYZ                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| beliebige Maske        |      |      |      | x    | x    | x    | x     | x    | x     |



 

Mit der beliebigen Maske können alle Kanäle kombiniert werden, um eine Maske zu bilden. Die Kanäle müssen in der Reihenfolge r, g, b, a aufgeführt werden, z. b. "Register. RBA", mit der die roten, blauen und Alphakanäle des Ziels aktualisiert werden. Die beliebige Maske ist in Version 1 \_ 4 oder höher verfügbar.

Wenn keine Ziel Schreib Maske angegeben ist, wird die Ziel Schreib Maske standardmäßig auf den RGBA-Fall festgelegt. Anders ausgedrückt: alle Kanäle im Ziel Register werden aktualisiert.

Für die Versionen 1 \_ 0 bis 1 \_ 3 kann die arithmetische Anweisung [DP3-PS](dp3---ps.md) DP3 nur die. RGB-oder. RGBA-Ausgabe Schreib Masken verwenden.

Ziel Register-Schreib Masken werden nur für arithmetische Operationen unterstützt. Sie können nicht für Textur Adressierungs Anweisungen verwendet werden, mit Ausnahme der Anweisungen der Version 1 \_ 4, [texcrd-PS](texcrd---ps.md) und [texld-PS \_ 2 \_ 0 und höher](texld---ps-2-0.md).

Standardmäßig werden alle vier Farbkanäle geschrieben.


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



Die Alpha-Schreib Maske wird auch als skalare Schreib Maske bezeichnet, da Sie die skalare Pipeline verwendet.


```
add r0.a, t1, v1
```



Mit dieser Anweisung wird die Summe der Alpha Komponente von T1 und der Alpha Komponente V1 in r0. a eingefügt.

Die Farb Schreib Maske wird verwendet, um das Schreiben in die Farbkanäle zu steuern.


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



Für Version 1 \_ 4 können Ziel Schreib Masken in jeder beliebigen Kombination verwendet werden, solange die Masken nach r, g, b, a geordnet sind.


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



Eine gemeinsam ausgestellte Anweisung ermöglicht es, zwei möglicherweise unterschiedliche Anweisungen gleichzeitig auszuführen. Dies wird durch Ausführen der Anweisungen in der Alpha Pipeline und der RGB-Pipeline erreicht.


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



Der Vorteil von paarweise Einfügeanweisungen besteht darin, dass es möglich ist, verschiedene Vorgänge parallel in der Vektor-und skalarpipeline durchzuführen.

Diese Vertex-Shader-Ausgabe Register sind auf die folgenden Schreib Masken beschränkt:



| Registriungstyp | Erforderliche Schreib Maske                                              |
|---------------|------------------------------------------------------------------|
| onebel          | für dieses skalarregister ist keine explizite Schreib Maske zulässig.        |
| oPts          | für dieses skalarregister ist keine explizite Schreib Maske zulässig.        |
| OPOS          | . xyzw (Standardeinstellung)                                      |
| TS\#          | kombinierte Maske:. x \| . XY \| . XYZ \| . xyzw (Standardeinstellung) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshadermodifizierern](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




