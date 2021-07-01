---
title: ps_1_1__ps_1_2__ps_1_3__ps_1_4 Register
description: Pixel-Shader sind von Registern abhängig, um Scheitelpunktdaten zu erhalten, Pixeldaten ausausgaben, temporäre Ergebnisse während Berechnungen zu enthalten und Texturstichprobenstufen zu identifizieren.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- 'Register: ps_1_1, um ps_1_4'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 68e3645c3e634c4e9cd886600977882dcc3e2018
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129858"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register

Pixel-Shader sind von Registern abhängig, um Scheitelpunktdaten zu erhalten, Pixeldaten ausausgaben, temporäre Ergebnisse während Berechnungen zu enthalten und Texturstichprobenstufen zu identifizieren. Es gibt mehrere Arten von Registern, die jeweils eine eindeutige Funktionalität haben. Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Der Pixel-Shader Version 1 \_ X implementiert werden.

Register halten Daten für die Verwendung durch den Pixel-Shader. Register werden in den folgenden Abschnitten vollständig beschrieben.

-   Registertypen beschreibt die vier verfügbaren Registertypen und deren Zwecke.
-   Lesen Sie port limit (Portlimit lesen), um die Einschränkungen für die Verwendung mehrerer Register in einer einzelnen Anweisung zu erfahren.
-   Read only Read Write beschreibt, welche Register zum Lesen, Schreiben oder beides verwendet werden können.
-   Bereich gibt den Bereich der Komponentendaten an.

## <a name="register-types"></a>Registertypen



| Name |  Typ              | Version 1 \_ 1 | Version 1 \_ 2      | Version 1 \_ 3     | Version 1 \_ 4             |
|------|--------------------|----------|------|------|--------------|
| c\#  | Konstantes Register  | 8        | 8    | 8    | 8            |
| R\#  | Temporäres Register | 2        | 2    | 2    | 6            |
| T\#  | Texturregister   | 4        | 4    | 4    | 6            |
| V\#  | Farbregister     | 2        | 2    | 2    | 2 in Phase 2 |



 

-   Konstante Register enthalten konstante Daten. Daten können mit [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) in ein konstantes Register geladen oder mit [def - ps definiert werden.](def---ps.md) Konstante Register können nicht von Texturadressenanweisungen verwendet werden. Die einzige Ausnahme ist die [texm3x3spec -](texm3x3spec---ps.md) ps-Anweisung, die ein konstantes Register verwendet, um einen Augenstrahlvektor zu liefern.
-   Temporäre Register werden verwendet, um Zwischenergebnisse zu speichern. r0 dient darüber hinaus als Pixel-Shaderausgabe. Der Wert in r0 am Ende des Shaders ist die Pixelfarbe für den Shader.

    Bei der Shaderüberprüfung ist [**createPixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) für jeden Shader, der versucht, aus einem temporären Register zu lesen, das nicht von einer vorherigen Anweisung geschrieben wurde, nicht erfolgreich. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) ist auf ähnliche Weise nicht erfolgreich, vorausgesetzt, die Validierung ist aktiviert (verwenden Sie D3DXSHADER \_ SKIPVALIDATION nicht).

-   Texturregister

    Für Die Pixel-Shaderversion 1 \_ 1 bis 1 3 enthalten \_ Texturregister Texturdaten oder Texturkoordinaten. Texturdaten werden in ein Texturregister geladen, wenn eine Textur entnommen wird. Bei der Texturstichprobe werden Texturkoordinaten verwendet, um einen Farbwert an den angegebenen Koordinaten (u,v,w,q) zu suchen oder zu beproben, während die Zustandsattribute der Texturphase berücksichtigt werden. Die Texturkoordinatendaten werden aus den Koordinatendaten der Scheitelpunkttextur interpoliert und einer bestimmten Texturstufe zugeordnet. Es gibt eine standardmäßige 1:1-Zuordnung zwischen der Texturstufennummer und der Reihenfolge der Texturkoordinatendeklaration. Standardmäßig wird der erste Satz von Texturkoordinaten, die im Scheitelpunktformat definiert sind, textur stage 0 zugeordnet.

    Für diese Pixel-Shaderversionen verhalten sich Texturregister wie temporäre Register, wenn sie von arithmetischen Anweisungen verwendet werden.

    Für Pixel-Shader Version 1 \_ 4 enthalten Texturregister (t \# ) schreibgeschützte Texturkoordinatendaten. Dies bedeutet, dass der Texturkoordinatensatz und die Texturphasennummer voneinander unabhängig sind. Die Texturphasennummer (aus der eine Textur entnommen werden soll) wird durch die Zielregisternummer (r0 bis r5) bestimmt. Für die texld-Anweisung wird der Texturkoordinatensatz vom Quellregister (t0 bis t5) bestimmt, sodass der Texturkoordinatensatz jeder Texturstufe zugeordnet werden kann. Darüber hinaus kann das Quellregister (mit Texturkoordinaten) für texld auch ein temporäres Register (r) sein. In diesem Fall werden die Inhalte des temporären Registers als \# Texturkoordinaten verwendet.

-   Farbregister enthalten Farbwerte pro Pixel. Die Werte werden durch eine Pixeliteration der diffusen und specularen Farbwerte in den Scheitelpunktdaten ermittelt. Bei Shadern der Pixel-Shaderversion 1 4 sind Farbregister nur in der \_ zweiten Phase verfügbar.

    Wenn der Shade-Modus auf D3DSHADE FLAT festgelegt ist, wird die Iteration der Scheitelpunktfarben \_ (diffus und specular) deaktiviert. Unabhängig vom Schattierungsmodus wird der Farbton weiterhin von der Pipeline iteriert, wenn Pixelpixel aktiviert sind. Beachten Sie, dass Die Ziehpunkte später in der Pipeline angewendet werden als das Pixelhader.

    Es ist üblich, das v0-Register mit den diffusen Vertexfarbdaten zu laden. Es ist auch üblich, das v1-Register mit den Scheitelpunkt-Farbdaten zu laden.

    Eingabefarbdatenwerte werden an den Bereich 0 bis 1 geklammert ,da dies der gültige Eingabebereich für Farbregister im Pixel-Shader ist.

    Pixel-Shader haben schreibgeschützten Zugriff auf Farbregister. Der Inhalt dieser Register sind iterierte Werte, aber die Iteration kann mit viel geringerer Genauigkeit als Texturkoordinaten ausgeführt werden.

## <a name="read-port-limit"></a>Portlimit lesen

Der Grenzwert für den Leseport gibt die Anzahl der verschiedenen Register jedes Registertyps an, die als Quellregister in einer einzelnen Anweisung verwendet werden können.



| Name     | Typ                   | Version 1 \_ 1 | Version 1 \_ 2      | Version 1 \_ 3     | Version 1 \_ 4             |
|------|--------------------|----------|------|------|--------------|
| c\#  | Konstantes Register  | 2        | 2    | 2    | 2            |
| R\#  | Temporäres Register | 2        | 2    | 2    | 3            |
| T\#  | Texturregister   | 2        | 3    | 3    | 1            |
| V\#  | Farbregister     | 2        | 2    | 2    | 2 in Phase 2 |



 

Die Farbregister für fast alle Versionen haben z. B. ein Leseportlimit von zwei. Dies bedeutet, dass eine einzelne Anweisung maximal zwei verschiedene Farbregister (z. B. v0 und v1) als Quellregister verwenden kann. In diesem Beispiel werden zwei Farbregister in derselben Anweisung verwendet:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Schreibgeschützt, Lesen/Schreiben

Die Registertypen werden gemäß der schreibgeschützten Funktion (RO) oder der Lese-/Schreibfunktion (RW) in der folgenden Tabelle identifiziert. Schreibgeschützte Register können nur als Quellregister in einer Anweisung verwendet werden. sie können nie als Zielregister verwendet werden.



| Name     |  Typ                  | Version 1 \_ 1 | Version 1 \_ 2     | Version 1 \_ 3     | Version 1 \_ 4 |
|------|--------------------|----------|------|------|--------------------|
| Name | Typ               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Konstantes Register  | RO       | RO   | RO   | RO                 |
| R\#  | Temporäres Register | RW       | RW   | RW   | RW                 |
| T\#  | Texturregister   | RW       | RW   | RW   | Weitere Informationen finden Sie unter folgendem Hinweis: |
| V\#  | Farbregister     | RO       | RO   | RO   | RO                 |



 

Register, die RW-fähig sind, können zum Speichern von Zwischenergebnissen verwendet werden. Dies schließt die temporären Register und Texturregister für einige der Shaderversionen ein.

> [!Note]  
>
> -   Für Die Pixel-Shaderversion 1 4 sind Texturregister RO für Anweisungen zur Textur adressierung, und Texturregister können weder von arithmetischen Anweisungen gelesen noch in sie geschrieben \_ werden. Da Texturregister zu Texturkoordinatenregistern geworden sind, ist der RO-Zugriff auch keine Regression vorheriger Funktionen.

 

## <a name="range"></a>Range

Der Bereich ist der maximale und minimale Registerdatenwert. Die Bereiche variieren je nach Typ des Registers. Die Bereiche für einige der Register können mit [**getDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)über die Geräteobergrenze abgefragt werden.



| Name | Typ               | Range                                               | Versionen     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Konstantes Register  | -1 bis +1                                            | Alle Versionen |
| R\#  | Temporäres Register | \- PixelShader1xMaxValue bis + PixelShader1xMaxValue | Alle Versionen |
| T\#  | Texturregister   | \- MaxTextureRepeat auf + MaxTextureRepeat           | Alle Versionen |
| V\#  | Farbregister     | 0 bis 1                                              | Alle Versionen |



 

Frühe Pixel-Shaderhardware stellt Daten in Registern mithilfe einer Festen Punktzahl dar. Dadurch wird die Genauigkeit für den Bruchteil einer Zahl auf maximal acht Bits beschränkt. Beachten Sie dies beim Entwerfen eines Shaders.

Für die Pixel-Shaderversion \_ 1 1 bis 1 3 muss \_ MaxTextureRepeat mindestens eins sein. Für 1 \_ 4 muss MaxTextureRepeat mindestens acht sein.

Weitere Informationen zu PixelShader1xMaxValue finden Sie unter [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
