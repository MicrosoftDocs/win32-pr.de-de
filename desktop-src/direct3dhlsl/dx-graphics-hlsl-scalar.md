---
title: Skalare Typen
description: Skalare Typen
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Skalartypen HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 39097dd358fcf9da1685be517742291ef96332f2307f255274445da70e4fc050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725934"
---
# <a name="scalar-types"></a>Skalare Typen


HLSL unterstützt mehrere skalare Datentypen:

-   **bool:** true oder false.
-   **int** : 32-Bit-Ganzzahl mit Vorzeichen.
-   **uint:** 32-Bit-Ganzzahl ohne Vorzeichen.
-   **dword:** 32-Bit-Ganzzahl ohne Vorzeichen.
-   **half** – 16-Bit-Gleitkommawert. Dieser Datentyp wird nur aus Gründen der Sprachkompatibilität bereitgestellt. Direct3D 10-Shaderziele ordnen alle halben Datentypen float-Datentypen zu. Ein halber Datentyp kann nicht für eine einheitliche globale Variable verwendet werden (verwenden Sie das /Gec-Flag, wenn diese Funktionalität gewünscht ist).
-   **float:** 32-Bit-Gleitkommawert.
-   **double** : 64-Bit-Gleitkommawert. Sie können keine Werte mit doppelter Genauigkeit als Eingaben und Ausgaben für einen Stream verwenden. Um Werte mit doppelter Genauigkeit zwischen Shadern zu übergeben, deklarieren Sie jeden **Double-Wert** als paarweise **uint-Datentypen.** Verwenden Sie dann die [**asuint-Funktion,**](asuint.md) um jedes **Double** in das Paar von **uint** s zu packen, und die [**Asdouble-Funktion,**](asdouble.md) um das Paar von **uint** s wieder in das **doppelte** zu entpacken.

Ab Windows 8 UNTERSTÜTZT HLSL auch Skalardatentypen mit minimaler Genauigkeit. Grafiktreiber können skalare Datentypen mit minimaler Genauigkeit implementieren, indem sie eine beliebige Genauigkeit verwenden, die größer oder gleich der angegebenen Bitgenauigkeit ist. Es wird empfohlen, sich nicht auf das Klammer- oder Umbruchverhalten zu verlassen, das von einer bestimmten zugrunde liegenden Genauigkeit abhängt. Beispielsweise kann der Grafiktreiber arithmetische Arithmetik für einen **min16float-Wert** mit vollständiger 32-Bit-Genauigkeit ausführen.

-   **min16float:** Mindestens 16-Bit-Gleitkommawert.
-   **min10float:** mindester 10-Bit-Gleitkommawert.
-   **min16int:** mindestens 16-Bit-Ganzzahl mit Vorzeichen.
-   **min12int:** mindestens 12-Bit-Ganzzahl mit Vorzeichen.
-   **min16uint:** mindestens 16-Bit-Ganzzahl ohne Vorzeichen.

Weitere Informationen zu skalaren Literalen finden Sie unter [Grammatik.](dx-graphics-hlsl-appendix-grammar.md)



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 10 sind die folgenden Typen Modifizierer für den Float-Typ.<br/>
<ul>
<li><strong>snorm float</strong> - IEEE 32-Bit-Gleitkommawert mit Vorzeichen im Bereich von -1 bis einschließlich 1.</li>
<li><strong>unorm float</strong> - IEEE 32-Bit unsigned-normalized float im Bereich von 0 bis einschließlich 1.</li>
</ul>
Hier sehen Sie beispielsweise eine Deklaration mit 4 Komponenten mit Vorzeichen und normalisierter Floatvariable.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a>Zeichenfolgentyp

HLSL unterstützt auch einen **Zeichenfolgentyp,** bei dem es sich um eine ASCII-Zeichenfolge handelt. Es gibt keine Vorgänge oder Zustände, die Zeichenfolgen akzeptieren, aber Effekte können Zeichenfolgenparameter und Anmerkungen abfragen.

## <a name="example"></a>Beispiel

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a>Weitere Informationen



* [Deklarieren von Skalartypen](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)