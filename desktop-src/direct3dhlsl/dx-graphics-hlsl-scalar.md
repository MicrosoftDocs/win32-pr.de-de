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
ms.openlocfilehash: 7ddfbc679d95ca0a2c6fce0710b5de37f677fe0f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626726"
---
# <a name="scalar-types"></a>Skalare Typen


HLSL unterstützt mehrere skalare Datentypen:

-   **bool:** true oder false.
-   **int:** 32-Bit-Ganzzahl mit Vorzeichen.
-   **uint:** 32-Bit-Ganzzahl ohne Vorzeichen.
-   **dword:** 32-Bit-Ganzzahl ohne Vorzeichen.
-   **half** – 16-Bit-Gleitkommawert. Dieser Datentyp wird nur zur Sprachkompatibilität bereitgestellt. Direct3D 10-Shaderziele ordnen alle halbierten Datentypen float-Datentypen zu. Ein halber Datentyp kann nicht für eine einheitliche globale Variable verwendet werden (verwenden Sie das Flag /Gec, wenn diese Funktionalität gewünscht ist).
-   **float:** 32-Bit-Gleitkommawert.
-   **double:** 64-Bit-Gleitkommawert. Sie können keine Werte mit doppelter Genauigkeit als Eingaben und Ausgaben für einen Stream verwenden. Um Werte mit doppelter Genauigkeit  zwischen Shadern zu übergeben, deklarieren Sie jedes Double als paar **uint-Datentypen.** Verwenden Sie dann die [**asuint-Funktion,**](asuint.md) um jedes Double in das Paar **von uint** s und die [**asdouble-Funktion**](asdouble.md) zu packen, um das **UINT-Paar** wieder in das doppelte zu **entpacken.** 

Ab Windows 8 unterstützt HLSL auch skalare Datentypen mit minimaler Genauigkeit. Grafiktreiber können skalare Datentypen mit minimaler Genauigkeit implementieren, indem sie eine genauigkeit verwenden, die größer oder gleich der angegebenen Bitgenauigkeit ist. Es wird empfohlen, sich nicht auf das Schließ- oder Umbruchverhalten zu verlassen, das von einer bestimmten zugrunde liegenden Genauigkeit abhängt. Beispielsweise kann der Grafiktreiber arithmetische Anweisungen für einen **min16float-Wert** mit voller 32-Bit-Genauigkeit ausführen.

-   **min16float:** Mindestens 16-Bit-Gleitkommawert.
-   **min10float:** Mindestens 10-Bit-Gleitkommawert.
-   **min16int:** mindestens eine 16-Bit-Ganzzahl mit Vorzeichen.
-   **min12int :** mindestens eine 12-Bit-Ganzzahl mit Vorzeichen.
-   **min16uint:** mindestens eine 16-Bit-Ganzzahl ohne Vorzeichen.

Weitere Informationen zu Skalarliteralen finden Sie unter [Grammatik.](dx-graphics-hlsl-appendix-grammar.md)



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 10 sind die folgenden Typen Modifizierer für den float-Typ.<br/>
<ul>
<li><strong>snorm float</strong> - IEEE 32-Bit signed-normalized float in range -1 to 1 inclusive.</li>
<li><strong>unorm float</strong> - IEEE 32-Bit unsigned-normalized float in range 0 to 1 inclusive.</li>
</ul>
Hier ist z. B. eine 4-Komponenten-Deklaration mit signierter normalisierter float-variable.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
