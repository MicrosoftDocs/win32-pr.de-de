---
description: Compilerdirektiven optimieren die Funktionalität, die von der DirectXMath-Bibliothek verwendet wird.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: DirectXMath Library-Compilerdirektiven
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261b4d7dec2c9c3fda7413c0559ad95b7b6a46d31ad2f273c04c8e2bd4c30054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118210"
---
# <a name="directxmath-library-compiler-directives"></a>DirectXMath Library-Compilerdirektiven

Compilerdirektiven optimieren die Funktionalität, die von der DirectXMath-Bibliothek verwendet wird.



| Anweisung                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ KEINE \_ SYSTEMINTERNEN FUNKTIONEN\_        | Wenn \_ XM \_ NO \_ INTRINSICS definiert \_ ist, werden DirectXMath-Vorgänge implementiert, ohne plattformspezifische systeminterne Funktionen zu verwenden. Stattdessen verwendet DirectXMath nur Standard-Gleitkommaoperationen.<br/> Standardmäßig \_ ist XM \_ NO \_ INTRINSICS nicht \_ definiert.<br/> Diese Direktive überschreibt alle anderen -Direktiven. Daher empfiehlt es sich, XM NO INTRINSICS zu überprüfen, \_ bevor Sie den Status von \_ \_ \_ \_ XM ARM NEON \_ \_ \_ INTRINSICS oder \_ \_ XM \_ SSE \_ INTRINSICS \_ ermitteln.<br/>                                                                              |
| \_\_ \_ SYSTEMINTERNE XM-SSE-FUNKTIONEN\_       | Wenn \_ XM \_ SSE \_ INTRINSICS \_ definiert ist, wird Code kompiliert, um SSE und SSE2 auf Plattformen zu verwenden, die diese Anweisungssätze unterstützen.<br/> Die Windows Versionen, die systeminterne SSE-Funktionen bereitstellen, unterstützen sowohl SSE als auch SSE2.<br/> \_XM \_ SSE \_ INTRINSICS \_ hat keine Auswirkungen auf Systeme, die SSE und SSE2 nicht unterstützen.<br/> Standardmäßig \_ wird XM \_ SSE \_ INTRINSICS \_ definiert, wenn Benutzer für eine Windows Plattform kompilieren.<br/> DirectXMath verwendet den Standardcompiler, der \_ (M \_ IX86/M \_ \_ AMD64) definiert, um Windows x86- oder Windows x64-Ziele zu bestimmen.<br/> |
| \_SYSTEMINTERNE XM \_ ARM \_ \_ NEON-FUNKTIONEN\_ | Dies gibt die DirectXMath-Implementierungsverwendungen der systeminternen ARM-NEON-Funktionen an. Standardmäßig \_ wird XM \_ ARM NEON \_ \_ INTRINSICS \_ definiert, wenn Benutzer für eine Windows auf der ARM/ARM64-Plattform kompilieren. DirectXMath verwendet den Standardcompiler define \_ (M \_ ARM, \_ M \_ ARM64), um dieses binäre Ziel zu bestimmen.<br/> Die systeminterne ARM-NEON-Unterstützung ist neu in DirectXMath und wird von XNAMath 2.x nicht unterstützt.<br/>                                                                                                                                                                             |
| \_\_SYSTEMINTERNE XM \_ SSE3-FUNKTIONEN\_      | Neu für DirectXMath 3.10. <br/> Wenn Sie diese Compilerdirektive angeben, werden DirectXMath-Funktionen implementiert, um ggf. systeminterne SSE3-Funktionen zu verwenden. andernfalls wird SSE/SSE2 verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_\_SYSTEMINTERNE XM \_ SSE4-FUNKTIONEN\_      | Neu für DirectMath 3.09. <br/> Wenn Sie diese Compilerdirektive angeben, werden DirectXMath-Funktionen implementiert, um ggf. die systeminternen Funktionen SSE3 und SSE4.1 zu nutzen. andernfalls wird SSE/SSE2 verwendet. Wenn Sie diese Compilerdirektive angeben, impliziert dies auch \_ XM \_ SSE3 \_ INTRINSICS \_ und \_ XM \_ SSE \_ INTRINSICS \_ .<br/>                                                                                                                                                                                                                                |
| \_\_SYSTEMINTERNE XM \_ AVX-FUNKTIONEN\_       | Neu für DirectXMath 3.09. <br/> Die Verwendung von /arch:AVX aktiviert diese Direktive. <br/> Wenn Sie diese Compilerdirektive angeben, werden DirectXMath-Funktionen implementiert, um die systeminternen Funktionen SSE3, SSE4.1 und AVX 128-Bit zu verwenden, sofern zutreffend. Andernfalls verwendet DirectXMath SSE/SSE2. Wenn Sie diese Compilerdirektive angeben, impliziert sie auch \_ XM \_ SSE3 \_ INTRINSICS, \_ XM \_ SSE4 \_ INTRINSICS \_ und \_ XM \_ SSE \_ INTRINSICS \_ und enthält eine kleine Teilmenge der SSE3-Anweisungen. <br/>                                                                    |
| SYSTEMINTERNE XM \_ \_ AVX2-FUNKTIONEN\_        | Neu für DirectXMath 3.11. <br/> Die Verwendung von /arch:AVX2 aktiviert diese Direktive. Wenn Sie diese Compilerdirektive angeben, verwenden DirectXMath-Funktionen die systeminternen Funktionen AVX2, F16C/CVT16, FMA3, AVX 128-Bit, SSE4.1 und SSE3. Wenn Sie \_ XM \_ AVX2 \_ INTRINSICS \_ verwenden, impliziert \_ dies XM \_ F16C \_ INTRINSICS \_ , \_ XM \_ FMA3 \_ INTRINSICS , \_ \_ XM \_ AVX \_ INTRINSICS , \_ \_ XM \_ SSE \_ INTRINSICS , \_ \_ XM \_ SSE3 \_ INTRINSICS und \_ \_ XM \_ SSE4 \_ INTRINSICS \_ .<br/>                                                                                       |
| \_SYSTEMINTERNE XM \_ F16C-FUNKTIONEN \_\_      | Neu für DirectXMath 3.09. <br/> Wenn Sie diese Compilerdirektive angeben, werden DirectXMath-Funktionen implementiert, um die systeminternen Funktionen SSE3, SSE4.1, AVX 128 Bit und F16C/CVT16 zu verwenden, sofern zutreffend. Andernfalls verwendet DirectXMath SSE/SSE2. Wenn Sie \_ XM \_ F16C \_ INTRINSICS \_ verwenden, impliziert dies \_ XM \_ AVX \_ INTRINSICS \_ , \_ XM \_ SSE \_ INTRINSICS , \_ \_ XM \_ SSE3 \_ INTRINSICS und \_ \_ XM \_ SSE4 \_ INTRINSICS \_ .<br/>                                                                                                                                                 |
| \_\_SYSTEMINTERNE XM-FMA3-FUNKTIONEN \_\_      | Neu für DirectXMath 3.11. <br/> Wenn Sie diese Compilerdirektive angeben, verwenden DirectXMath-Funktionen die systeminternen Funktionen SSE3, SSE4.1, AVX 128-Bit und FMA3, sofern zutreffend. Andernfalls verwendet DirectXMath SSE/SSE2. Wenn Sie \_ XM \_ FMA3 \_ INTRINSICS \_ verwenden, impliziert \_ dies XM \_ AVX \_ INTRINSICS \_ , \_ XM \_ SSE \_ INTRINSICS , \_ \_ XM \_ SSE3 \_ INTRINSICS und \_ \_ XM \_ SSE4 \_ INTRINSICS \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Dies ermöglicht die Verwendung der \_ \_ Vectorcall-Aufrufkonvention für Windows x86- oder Windows x64-Ziele. Standardmäßig wird \_ XM \_ VECTORCALL \_ =1 verwendet, wenn der Compiler dieses Feature unterstützt. Sie können sie manuell auf \_ XM \_ VECTORCALL \_ =0 festlegen, um sie immer zu deaktivieren. <br/> \_\_vectorcall wird für die Windows auf der ARM/ARM64-Plattform oder verwalteten C++ nicht unterstützt. <br/>                                                                                                                                                                                                                 |
| \_SYSTEMINTERNE XM \_ \_ SVML-FUNKTIONEN\_     | Neu für DirectXMath 3.16. <br/> Mit VS 2019 oder höher ermöglicht dies der Bibliothek die Verwendung der Intel &reg; Short Vector Matrix Library für x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierreferenz](ovw-xnamath-reference.md)
</dt> </dl>

 

 
