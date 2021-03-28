---
title: ps_1_1__ps_1_2__ps_1_3__ps_1_4 Register
description: Pixel-Shader sind von Registern abhängig, um Vertexdaten zu erhalten, die Pixeldaten auszugeben, temporäre Ergebnisse während der Berechnungen zu speichern und Textur-Samplings zu identifizieren.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- Register-ps_1_1 für ps_1_4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4525b6d3be2e9287f53edc1da0cd2fb188184a69
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473421"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register

Pixel-Shader sind von Registern abhängig, um Vertexdaten zu erhalten, die Pixeldaten auszugeben, temporäre Ergebnisse während der Berechnungen zu speichern und Textur-Samplings zu identifizieren. Es gibt mehrere Arten von Registern, von denen jede über eine eindeutige Funktionalität verfügt. Dieser Abschnitt enthält Referenzinformationen zu den von Pixel Shader Version 1 X implementierten Eingabe-und Ausgabe Registern \_ .

Registriert haltendaten für die Verwendung durch den Pixelshader. Register werden in den folgenden Abschnitten vollständig beschrieben.

-   Register Typen beschreibt die vier verfügbaren Register Typen und deren Zwecke.
-   Über Port Limit lesen werden die Einschränkungen bei der Verwendung mehrerer Register in einer einzigen Anweisung ausführlich erläutert.
-   Schreib geschützter Lese-/Schreibzugriff beschreibt, welche Register zum Lesen, schreiben oder beides verwendet werden können.
-   Bereich Details der Bereich der Komponenten Daten.

## <a name="register-types"></a>Register Typen



|      |                    | Versionen |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Name | type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Konstantes Register  | 8        | 8    | 8    | 8            |
| r\#  | Temporäres Register | 2        | 2    | 2    | 6            |
| t\#  | Textur Register   | 4        | 4    | 4    | 6            |
| Ramelow\#  | Farbregister     | 2        | 2    | 2    | 2 in Phase 2 |



 

-   Konstante Register enthalten Konstante Daten. Daten können mithilfe von [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) in ein konstantes Register geladen werden, oder Sie können mit [DEF-PS](def---ps.md)definiert werden. Konstante Register können nicht durch Textur Adress Anweisungen verwendet werden. Die einzige Ausnahme ist die [texm3x3spec-PS-](texm3x3spec---ps.md) Anweisung, die ein konstantes Register verwendet, um einen Augen Strahl Vektor bereitzustellen.
-   Temporäre Register werden verwendet, um Zwischenergebnisse zu speichern. R0 fungiert außerdem als Pixel-Shader-Ausgabe. Der Wert in R0 am Ende des Shaders ist die Pixelfarbe für den Shader.

    Bei der shaderüberprüfung tritt für einen Shader, der versucht, aus einem temporären [**Register zu lesen**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) , das nicht von einer vorherigen Anweisung geschrieben wurde, ein Fehler auf. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) führt zu einem Fehler, wenn die Überprüfung aktiviert ist (D3DXSHADER \_ skipvalidation nicht verwenden).

-   Textur Register

    Bei Pixel-Shader Version 1 \_ 1 bis 1 \_ 3 enthalten Textur Register Textur Daten oder Texturkoordinaten. Textur Daten werden in ein Textur Register geladen, wenn eine Textur als Stichprobe erstellt wird. Bei der Textur Stichprobe werden Texturkoordinaten verwendet, um einen Farbwert bei den angegebenen (u, v, w, q)-Koordinaten zu suchen, während die Attribute des Textur Stufen Zustands berücksichtigt werden. Die Texturkoordinaten Daten werden aus den vertextextur-Koordinatendaten interpoliert und einer bestimmten Textur Phase zugeordnet. Zwischen der Reihenfolge der Textur Stufen und der Reihenfolge der Texturkoordinaten wird eine 1-zu-eins-Standard Zuordnung angezeigt. Standardmäßig ist der erste Satz von Texturkoordinaten, der im Vertex-Format definiert ist, der Textur Phase 0 zugeordnet.

    Bei diesen Pixel-Shader-Versionen Verhalten sich Textur Register bei Verwendung von arithmetischen Anweisungen wie bei temporären Registern.

    Bei Pixel-Shader Version 1 \_ 4 enthalten Textur Register (t) schreibgeschützte \# Texturkoordinaten Daten. Dies bedeutet, dass der Texturkoordinaten Satz und die Textur Phasen Nummer voneinander unabhängig sind. Die Textur Phasen Nummer (aus der ein Beispiel für eine Textur besteht) wird von der Ziel Registernummer (R0 bis R5) bestimmt. Bei der texld-Anweisung wird der Texturkoordinaten Satz durch das Quell Register (t0 bis T5) bestimmt, sodass der Texturkoordinaten Satz beliebigen Textur Stufen zugeordnet werden kann. Außerdem kann das Quell Register (das Angeben von Texturkoordinaten) für texld auch ein temporäres Register (r \# ) sein. in diesem Fall wird der Inhalt des temporären Registers als Texturkoordinaten verwendet.

-   Farbregister enthalten Farbwerte pro Pixel. Die Werte werden durch die Iteration pro Pixel der diffusen und Glanz Farbwerte in den Scheitelpunkt Daten abgerufen. Für Pixel Shader, Version 1 \_ 4, sind Farbregister nur in der zweiten Phase verfügbar.

    Wenn der Schattierung-Modus auf D3DSHADE Flat festgelegt ist \_ , wird die Iteration beider Scheitelpunkt Farben (diffs und spectex) deaktiviert. Der Nebel wird unabhängig vom schattierten Modus immer noch durch die Pipeline durchlaufen, wenn Pixel Nebel aktiviert ist. Denken Sie daran, dass der Nebel später in der Pipeline als der Pixelshader angewendet wird.

    Es ist üblich, das Register "v0" mit den diffusen Farbdaten zu laden. Es ist auch üblich, das v1-Register mit den Glanz Farben der Scheitelpunkt Daten zu laden.

    Die Datenwerte für die Eingabe Farbe werden mit dem Bereich von 0 bis 1 geklammert (ausgelastet), da dies der gültige Eingabebereich für Farbregister im Pixelshader ist.

    Pixel-Shader haben Lese geschützten Zugriff auf Farbregister. Der Inhalt dieser Register ist Iterierte Werte, aber die Iterationen werden möglicherweise mit einer deutlich niedrigeren Genauigkeit als Texturkoordinaten ausgeführt.

## <a name="read-port-limit"></a>Grenzwert für Lese Port

Der Grenzwert für den Lese Anschluss gibt die Anzahl verschiedener Register für jeden Registrierungstyp an, der in einer einzigen Anweisung als Quell Register verwendet werden kann.



|      |                    | Versionen |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Name | type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Konstantes Register  | 2        | 2    | 2    | 2            |
| r\#  | Temporäres Register | 2        | 2    | 2    | 3            |
| t\#  | Textur Register   | 2        | 3    | 3    | 1            |
| Ramelow\#  | Farbregister     | 2        | 2    | 2    | 2 in Phase 2 |



 

Beispielsweise haben die Farbregister für fast alle Versionen eine Lese Port Beschränkung von zwei. Dies bedeutet, dass eine einzelne Anweisung maximal zwei verschiedene Farbregister (z. a. V0 und v1) als Quell Register verwenden kann. Dieses Beispiel zeigt zwei Farbregister, die in derselben Anweisung verwendet werden:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Schreibgeschützt, Lese-/Schreibzugriff

Die Register Typen werden in der folgenden Tabelle gemäß Schreib geschützter Funktion (RO) oder Lese-/Schreibfunktion (RW) identifiziert. Schreibgeschützte Register können nur als Quell Register in einer Anweisung verwendet werden. Sie können nie als Ziel Register verwendet werden.



|      |                    | Versionen |      |      |                    |
|------|--------------------|----------|------|------|--------------------|
| Name | type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Konstantes Register  | RO       | RO   | RO   | RO                 |
| r\#  | Temporäres Register | RW       | RW   | RW   | RW                 |
| t\#  | Textur Register   | RW       | RW   | RW   | Siehe folgenden Hinweis |
| Ramelow\#  | Farbregister     | RO       | RO   | RO   | RO                 |



 

Registrierungen, die als RW-fähig sind, können zum Speichern von Zwischenergebnissen verwendet werden. Dies schließt die temporären Register und Textur Register für einige der Shader-Versionen ein.

> [!Note]  
>
> -   Bei Pixel-Shader, Version 1 \_ 4, sind Textur Register für texturierungs-Anweisungen "ro", und Textur Register können weder aus einer arithmetischen Anleitung gelesen noch in Sie geschrieben werden. Da Textur Register auch Texturkoordinaten Register aufweisen, ist der Ro-Zugriff keine Regression vorheriger Funktionen.

 

## <a name="range"></a>Range

Der Bereich ist der maximale und minimale Registrierungs Datenwert. Die Bereiche variieren je nach Typ des Registers. Die Bereiche für einige der Register können mithilfe von [**getde vicecaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)von den Geräte Caps abgefragt werden.



| Name | type               | Range                                               | Versionen     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Konstantes Register  | -1 bis + 1                                            | Alle Versionen |
| r\#  | Temporäres Register | \- PixelShader1xMaxValue bis + PixelShader1xMaxValue | Alle Versionen |
| t\#  | Textur Register   | \- MaxTextureRepeat in + maxtextureretorf           | Alle Versionen |
| Ramelow\#  | Farbregister     | 0 bis 1                                              | Alle Versionen |



 

Die frühe Pixel-Shader-Hardware stellt Daten in Registern mit einer Festkomma Zahl dar. Dadurch wird die Genauigkeit für den Bruchteil einer Zahl auf maximal 8 Bits beschränkt. Beachten Sie dies beim Entwerfen eines Shaders.

Für die Pixel-Shader-Version 1 \_ 1 bis 1 \_ 3 muss MaxTextureRepeat mindestens eins aufweisen. Bei 1 \_ 4 muss MaxTextureRepeat mindestens acht sein.

Weitere Informationen zu PixelShader1xMaxValue finden Sie unter [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 