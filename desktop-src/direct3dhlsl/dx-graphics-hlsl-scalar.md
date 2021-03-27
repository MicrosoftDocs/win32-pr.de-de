---
title: Skalare Typen
description: Skalare Typen
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Skalare Typen HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103761895"
---
# <a name="scalar-types"></a>Skalare Typen


HLSL unterstützt mehrere skalare Datentypen:

-   **bool** -true oder false.
-   **int** -32-Bit-Ganzzahl mit Vorzeichen.
-   **uint** -32-Bit-Ganzzahl ohne Vorzeichen.
-   **DWORD** -32-Bit-Ganzzahl ohne Vorzeichen.
-   **halb** -16-Bit-Gleit Komma Wert. Dieser Datentyp wird nur für die sprach Kompatibilität bereitgestellt. Direct3D 10-Shader-Ziele ordnen alle halb Datentypen float-Datentypen zu. Ein halber Datentyp kann nicht für eine einheitliche globale Variable verwendet werden (verwenden Sie das/GEC-Flag, wenn diese Funktion gewünscht ist).
-   Gleit Komma Wert **float** -32-Bit.
-   **Double** -64-Bit-Gleit Komma Wert. Werte mit doppelter Genauigkeit können nicht als Eingaben und Ausgaben für einen Stream verwendet werden. Um Werte mit doppelter Genauigkeit zwischen Shadern zu übergeben, deklarieren Sie jedes **Double** als Paar von **uint** -Datentypen. Verwenden Sie dann die [**asuint**](asuint.md) -Funktion, um jedes **Double** in das Paar **von uint** s und die [**AsDouble**](asdouble.md) -Funktion zu packen, um das Paar von **uint** s wieder in den **Double**-Typ zu entpacken.

Ab Windows 8 unterstützt HLSL auch skalare Datentypen mit minimaler Genauigkeit. Grafiktreiber können Skalardatentypen mit minimaler Genauigkeit implementieren, indem Sie eine beliebige Genauigkeit angeben, die größer oder gleich der angegebenen bitgenauigkeit ist. Es wird empfohlen, sich nicht auf das Spannen-oder Wrapping Verhalten zu verlassen, das von einer bestimmten zugrunde liegenden Genauigkeit abhängt Beispielsweise kann der Grafiktreiber Arithmetik für einen **min16float** -Wert mit vollständiger 32-Bit-Genauigkeit ausführen.

-   **min16float** -minimaler 16-Bit-Gleit Komma Wert.
-   **min10float** -minimaler 10-Bit-Gleit Komma Wert.
-   **min16int** -minimale 16-Bit-Ganzzahl mit Vorzeichen.
-   **min12int** -minimale 12-Bit-Ganzzahl mit Vorzeichen.
-   **min16uint** -minimale 16-Bit-Ganzzahl ohne Vorzeichen.

Weitere Informationen zu skalaren literalen finden Sie unter [Grammatik](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 10 sind die folgenden Typen Modifizierer für den float-Typ.<br/>
<ul>
<li><strong>snorm float</strong> - IEEE 32-Bit mit Vorzeichen-normalisierter Gleit Komma Zahl im Bereich von 1 bis 1 einschließlich.</li>
<li><strong>unorm float</strong> - IEEE 32-Bit ohne Vorzeichen-normalisierte Gleit Komma Zahl im Bereich von 0 bis 1 einschließlich.</li>
</ul>
Hier sehen Sie z. b. eine 4-komponentendeklaration mit Vorzeichen und normalisierte float-Variablen.<br/> <span data-codelanguage=""></span>
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

HLSL unterstützt auch einen **Zeichen** Folgentyp, der eine ASCII-Zeichenfolge ist. Es sind keine Vorgänge oder Zustände vorhanden, die Zeichen folgen akzeptieren, aber Effekte können Zeichen folgen Parameter und Anmerkungen Abfragen.

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



* [Deklarieren von skalaren Typen](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)