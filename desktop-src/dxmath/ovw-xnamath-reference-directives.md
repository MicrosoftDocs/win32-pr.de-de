---
description: Compiler-Direktiven optimieren die Funktionalität, die von der DirectXMath-Bibliothek verwendet wird.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: DirectXMath Library-Compilerrichtlinien
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7419afbab80d35feea135a25f7c5892b137a08
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826775"
---
# <a name="directxmath-library-compiler-directives"></a>DirectXMath Library-Compilerrichtlinien

Compiler-Direktiven optimieren die Funktionalität, die von der DirectXMath-Bibliothek verwendet wird.



| Anweisung                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ KEINE \_ SYSTEMINTERNEN\_        | Wenn \_ XM \_ NO \_ INTRINSICS definiert \_ ist, werden DirectXMath-Vorgänge implementiert, ohne plattformspezifische systeminterne Eigenschaften zu verwenden. Stattdessen verwendet DirectXMath nur Standard-Gleitkommavorgänge.<br/> Standardmäßig ist \_ XM \_ NO \_ INTRINSICS nicht \_ definiert.<br/> Diese Anweisung überschreibt alle anderen -Anweisungen. Daher wird empfohlen, vor der Bestimmung des Status von \_ \_ \_ \_ \_ XM \_ ARM NEON INTRINSICS oder \_ \_ \_ \_ XM SSE INTRINSICS auf XM NO \_ \_ INTRINSICS zu \_ prüfen.<br/>                                                                              |
| \_SYSTEMINTERNE \_ XM-SSE-EIGENSCHAFTEN \_\_       | Wenn XM SSE INTRINSICS definiert ist, wird Code kompiliert, um unterstützungs-SSE und SSE2 auf Plattformen zu verwenden, \_ \_ die diese \_ \_ Anweisungssätze unterstützen.<br/> Die Windows-Versionen, die systeminterne SSE-Versionen bereitstellen, unterstützen sowohl SSE als auch SSE2.<br/> \_XM \_ SSE \_ INTRINSICS \_ hat keine Auswirkungen auf Systeme, die SSE und SSE2 nicht unterstützen.<br/> Standardmäßig wird \_ XM \_ SSE \_ INTRINSICS \_ definiert, wenn Benutzer für eine Windows-Plattform kompilieren.<br/> DirectXMath verwendet den Standardcompiler defines ( \_ M \_ IX86 \_ /M \_ AMD64), um Windows x86- oder Windows x64-Ziele zu bestimmen.<br/> |
| \_SYSTEMINTERNE \_ XM ARM \_ \_ NEON-EIGENSCHAFTEN\_ | Dies gibt an, dass die DirectXMath-Implementierung die systeminternen ARM-NEON-Eigenschaften verwendet. Standardmäßig wird XM ARM NEON INTRINSICS definiert, wenn Benutzer für eine \_ \_ Windows auf \_ \_ \_ ARM-/ARM64-Plattform kompilieren. DirectXMath verwendet den Standardcompiler define ( \_ M \_ ARM, \_ M \_ ARM64), um dieses binäre Ziel zu bestimmen.<br/> Die systeminterne ARM-NEON-Unterstützung ist neu in DirectXMath und wird von XNAMath 2.x nicht unterstützt.<br/>                                                                                                                                                                             |
| \_SYSTEMINTERNE \_ XM SSE3-EIGENSCHAFTEN \_\_      | Neu für DirectXMath 3.10. <br/> Wenn Sie diese Compiler-Direktive angeben, werden DirectXMath-Funktionen implementiert, um ggf. systeminterne SSE3-Funktionen zu verwenden. Andernfalls wird SSE/SSE2 verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_SYSTEMINTERNE \_ XM-SSE4-EIGENSCHAFTEN \_\_      | Neu für DirectMath 3.09. <br/> Wenn Sie diese Compiler-Direktive angeben, werden DirectXMath-Funktionen implementiert, um ggf. die systeminternen Funktionen SSE3 und SSE4.1 zu verwenden. Andernfalls wird SSE/SSE2 verwendet. Wenn Sie diese Compiler-Direktive angeben, impliziert dies auch \_ XM \_ SSE3 \_ INTRINSICS \_ und \_ XM \_ SSE \_ INTRINSICS \_ .<br/>                                                                                                                                                                                                                                |
| \_SYSTEMINTERNE \_ XM-AVX-SYSTEME \_\_       | Neu für DirectXMath 3.09. <br/> Die Verwendung von /arch:AVX ermöglicht diese Direktive. <br/> Wenn Sie diese Compiler-Direktive angeben, werden DirectXMath-Funktionen implementiert, um ggf. die systeminternen Funktionen SSE3, SSE4.1 und AVX 128 Bit zu verwenden. Andernfalls verwendet DirectXMath SSE/SSE2. Wenn Sie diese Compileranweisung angeben, impliziert sie auch \_ XM \_ SSE3 \_ INTRINSICS, \_ XM SSE4 INTRINSICS und XM SSE INTRINSICS und enthält eine kleine Teilmenge der \_ \_ \_ \_ \_ \_ \_ SSE3-Anweisungen. <br/>                                                                    |
| SYSTEMINTERNE \_ XM AVX2-SYSTEME \_\_        | Neu für DirectXMath 3.11. <br/> Die Verwendung von /arch:AVX2 ermöglicht diese Direktive. Wenn Sie diese Compiler-Direktive angeben, verwenden DirectXMath-Funktionen ggf. die systeminternen Funktionen AVX2, F16C/CVT16, FMA3, AVX 128-Bit, SSE4.1 und SSE3. Wenn Sie \_ XM AVX2 INTRINSICS verwenden, impliziert dies \_ \_ \_ \_ XM \_ F16C \_ \_ \_ INTRINSICS, XM \_ FMA3 \_ \_ INTRINSICS, \_ XM \_ AVX \_ \_ INTRINSICS, \_ XM \_ SSE \_ \_ INTRINSICS, \_ XM \_ SSE3 \_ INTRINSICS und \_ \_ XM \_ SSE4 \_ INTRINSICS \_ .<br/>                                                                                       |
| \_SYSTEMINTERNE \_ XM F16C-EIGENSCHAFTEN \_\_      | Neu für DirectXMath 3.09. <br/> Wenn Sie diese Compiler-Direktive angeben, werden DirectXMath-Funktionen implementiert, um die systeminternen Funktionen SSE3, SSE4.1, AVX 128-Bit und F16C/CVT16 zu verwenden. Andernfalls verwendet DirectXMath SSE/SSE2. Wenn Sie \_ XM \_ F16C \_ INTRINSICS verwenden, impliziert \_ \_ dies XM \_ AVX \_ \_ INTRINSICS, \_ XM \_ SSE \_ \_ INTRINSICS, \_ XM \_ SSE3 \_ INTRINSICS und \_ \_ XM \_ SSE4 \_ INTRINSICS \_ .<br/>                                                                                                                                                 |
| \_SYSTEMINTERNE \_ XM FMA3-SYSTEMINTERNES \_\_      | Neu für DirectXMath 3.11. <br/> Wenn Sie diese Compiler-Direktive angeben, verwenden DirectXMath-Funktionen die systeminternen Funktionen SSE3, SSE4.1, AVX 128-Bit und FMA3, sofern zutreffend. Andernfalls verwendet DirectXMath SSE/SSE2. Wenn Sie \_ XM \_ FMA3 \_ INTRINSICS verwenden, impliziert \_ \_ dies XM \_ AVX \_ \_ INTRINSICS, \_ XM \_ SSE \_ \_ INTRINSICS, \_ XM \_ SSE3 \_ INTRINSICS und \_ \_ XM \_ SSE4 \_ INTRINSICS \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Dies ermöglicht die Verwendung der \_ \_ Vectorcall-Aufrufkonvention für Windows x86- oder Windows x64-Ziele. Der Standardwert ist \_ XM \_ VECTORCALL \_ =1, wenn der Compiler dieses Feature unterstützt. Sie können sie manuell auf \_ XM \_ VECTORCALL \_ =0 festlegen, um sie immer zu deaktivieren. <br/> \_\_vectorcall wird für windows on ARM/ARM64 platform oder Managed C++ nicht unterstützt. <br/>                                                                                                                                                                                                                 |
| \_SYSTEMINTERNE \_ XM-SVML-EIGENSCHAFTEN \_\_     | Neu für DirectXMath 3.16. <br/> Mit VS 2019 oder höher ermöglicht dies der Bibliothek die Verwendung der Intel &reg; Short Vector Matrix Library für x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierreferenz](ovw-xnamath-reference.md)
</dt> </dl>

 

 
