---
title: Speichern eines 64-Bit-Werts
description: Verwenden Sie zum Speichern eines 64-Bit-Zeiger Werts ULONG \_ ptr. Ein ULONG- \_ ptr-Wert ist 32 Bits, wenn er mit einem 32-Bit-Compiler und 64 Bits kompiliert wird, wenn er mit einem 64-Bit-Compiler kompiliert wird.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- Speichern von 64-Bit-Werten für die Windows-Programmierung mit 64 Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310056"
---
# <a name="storing-a-64-bit-value"></a>Speichern eines 64-Bit-Werts

Verwenden Sie zum Speichern eines 64-Bit-Zeiger Werts **ulong \_ ptr**. Ein **ulong- \_ ptr** -Wert ist 32 Bits, wenn er mit einem 32-Bit-Compiler und 64 Bits kompiliert wird, wenn er mit einem 64-Bit-Compiler kompiliert wird.

In den folgenden Beispielen wird realer Code verwendet, der in 64-Bit-Windows portiert wurde. Kommentare zu den Schritten, mit denen der Code 64-Bit-kompatibel gemacht werden kann, sind enthalten.

## <a name="example-1-getting-an-address"></a>Beispiel 1: erhalten einer Adresse

Der folgende Code veranschaulicht eine Portier bare Methode, um eine Adresse zu erhalten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Verwenden von ULONG (eine 32-Bit-Methode)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td>Verwenden von ULONG_PTR (die Portable-Methode)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a>Beispiel 2: Berechnen einer Adresse

Der folgende Code veranschaulicht eine portablen Methode zum Berechnen einer Adresse.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Verwenden von ULONG (eine 32-Bit-Methode)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td>Verwenden von ULONG_PTR (die Portable-Methode)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




