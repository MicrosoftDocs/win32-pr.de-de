---
title: Speichern eines 64-Bit-Werts
description: Verwenden Sie ULONG PTR, um einen 64-Bit-Zeigerwert \_ zu speichern. Ein ULONG-PTR-Wert beträgt 32 Bits, wenn er mit einem 32-Bit-Compiler kompiliert wird, und 64 Bit, wenn er mit einem \_ 64-Bit-Compiler kompiliert wird.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- Speichern von 64-Bit-Werten mit 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469067"
---
# <a name="storing-a-64-bit-value"></a>Speichern eines 64-Bit-Werts

Verwenden Sie **ULONG \_ PTR,** um einen 64-Bit-Zeigerwert zu speichern. Ein **\_ ULONG-PTR-Wert** beträgt 32 Bits, wenn er mit einem 32-Bit-Compiler kompiliert wird, und 64 Bit, wenn er mit einem 64-Bit-Compiler kompiliert wird.

In den folgenden Beispielen wird realer Code verwendet, der auf 64-Bit-Windows. Eine Ausführliche Erläuterung der Schritte zum 64-Bit-Kompatiblen des Codes ist enthalten.

## <a name="example-1-getting-an-address"></a>Beispiel 1: Abrufen einer Adresse

Der folgende Code veranschaulicht eine portable Möglichkeit, eine Adresse zu erhalten.




| | | Verwenden von ULONG (eine 32-Bit-Methode) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | | Verwenden ULONG_PTR (portable Methode) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>Beispiel 2: Berechnen einer Adresse

Der folgende Code veranschaulicht eine portable Methode zum Berechnen einer Adresse.




| | | Verwenden von ULONG (eine 32-Bit-Methode) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | | Verwenden ULONG_PTR (portable Methode) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




