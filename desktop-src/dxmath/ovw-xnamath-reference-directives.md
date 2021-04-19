---
description: Compilerdirektiven optimieren die Funktionen, die von der directxmath-Bibliothek verwendet werden.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Directxmath-Bibliotheks-Compilerdirektiven
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f1d67ecd4772116a3bf29f802c39b2e348fd5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348500"
---
# <a name="directxmath-library-compiler-directives"></a>Directxmath-Bibliotheks-Compilerdirektiven

Compilerdirektiven optimieren die Funktionen, die von der directxmath-Bibliothek verwendet werden.



| Anweisung                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ keine \_ intrinsie\_        | Wenn \_ XM \_ keine systeminternen \_ \_ Funktionen definiert sind, werden directxmath-Vorgänge implementiert, ohne dass plattformspezifische systeminterne Funktionen verwendet werden. Stattdessen verwendet directxmath nur standardmäßige Gleit Komma Operationen.<br/> Standardmäßig \_ ist XM \_ \_ \_ nicht definiert.<br/> Diese Direktive überschreibt alle anderen-Direktiven. Daher wird empfohlen, dass Sie nach XM keine systeminternen Funktionen suchen, \_ \_ \_ \_ bevor Sie den Status von XM-Arm-Neon-Funktionen oder systeminternen \_ \_ \_ \_ \_ \_ XM- \_ SSE \_ \_ -Funktionen ermitteln.<br/>                                                                              |
| \_intrinsie systeminterne XM- \_ SSE \_\_       | Wenn die systeminternen Funktionen \_ von XM \_ SSE \_ definiert sind \_ , wird Code für die Verwendung von SSE und SSE2 auf Plattformen kompiliert, die diese Anweisungs Sätze unterstützen.<br/> Die Windows-Versionen mit den systeminternen SSE-Funktionen unterstützen SSE und SSE2.<br/> \_Die systeminternen Funktionen von XM \_ SSE \_ \_ wirken sich nicht auf Systeme aus, die SSE und SSE2 nicht unterstützen.<br/> Standardmäßig wird die systeminternen Funktionen von \_ XM \_ SSE \_ definiert, \_ Wenn Benutzer für eine Windows-Plattform kompilieren.<br/> Directxmath verwendet den Standard Compiler definiert ( \_ M \_ IX86/ \_ m \_ amd64), um Windows x86-oder Windows x64-Ziele zu bestimmen.<br/> |
| \_intrinsie systeminterne XM-Arm-Funktionen \_ \_ \_\_ | Dies gibt an, dass die directxmath-Implementierung die systeminternen Arm-Neon-Funktionen verwendet. Standardmäßig werden \_ XM-Arm-Neon-Funktionen \_ \_ definiert, \_ \_ Wenn Benutzer für eine Windows RT-Plattform kompilieren. Directxmath verwendet die standardmäßige compilerdefinition ( \_ m \_ Arm, \_ m \_ ARM64), um dieses binäre Ziel zu ermitteln.<br/> Die Unterstützung von systeminternen Arm-Neon-Funktionen ist neu in directxmath und wird von xnamath 2. x nicht unterstützt.<br/>                                                                                                                                                                             |
| \_XM- \_ SSE3 \_ intrinsie\_      | Neues für das Windows 10 Creators Update SDK. <br/> Wenn Sie diese Compilerdirektive angeben, werden directxmath-Funktionen implementiert, um die SSE3-systeminternen Funktionen zu verwenden, sofern zutreffend. Andernfalls wird SSE/SSE2 verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_XM- \_ SSE4 \_ intrinsie\_      | Neues für das Windows 10 Anniversary SDK.<br/> Wenn Sie diese Compilerdirektive angeben, werden directxmath-Funktionen implementiert, um die systeminternen Funktionen SSE3 und SSE 4.1 zu verwenden, sofern zutreffend. Andernfalls wird SSE/SSE2 verwendet. Wenn Sie diese Compilerdirektive angeben, impliziert Sie auch \_ XM \_ \_ -SSE3 Intrinsics und systeminterne \_ \_ XM- \_ SSE \_ \_ .<br/>                                                                                                                                                                                                                                |
| \_systeminterne XM- \_ Verfügbarkeit \_\_       | Neues für das Windows 10 Anniversary SDK.<br/> Die Verwendung von/Arch: AVX aktiviert diese Direktive. <br/> Wenn Sie diese Compilerdirektive angeben, werden directxmath-Funktionen implementiert, um die systeminternen Funktionen SSE3, SSE 4.1 und AVX 128-Bit zu verwenden, sofern zutreffend. Andernfalls verwendet directxmath SSE/SSE2. Wenn Sie diese Compilerdirektive angeben, impliziert Sie auch \_ XM \_ SSE3 \_ Intrinsics, \_ XM \_ SSE4 \_ Intrinsics und systeminterne \_ \_ XM- \_ SSE \_ -Funktionen \_ und enthält eine kleine Teilmenge von SSE3-Anweisungen. <br/>                                                                    |
| XM- \_ AVX2 \_ intrinsie\_        | Neues für Windows 10 Fall Creators Update SDK<br/> Verwendung von/Arch: AVX2 aktiviert diese Direktive. Wenn Sie diese Compilerdirektive angeben, nutzen directxmath-Funktionen ggf. AVX2, F16C/CVT16, FMA3, AVX 128-Bit, SSE 4.1 und SSE3 intrinsie. Wenn Sie die systeminternen Funktionen von \_ XM \_ AVX2 verwenden \_ \_ , impliziert dies \_ XM \_ F16C \_ Intrinsics \_ , \_ XM \_ FMA3 \_ Intrinsics \_ , \_ XM \_ AVX \_ Intrinsics \_ , \_ XM \_ SSE \_ Intrinsics \_ , \_ XM \_ SSE3 \_ Intrinsics \_ und \_ XM \_ SSE4 \_ Intrinsics \_ .<br/>                                                                                       |
| \_XM- \_ F16C \_ intrinsie\_      | Neues für das Windows 10 Anniversary SDK.<br/> Wenn Sie diese Compilerdirektive angeben, werden directxmath-Funktionen implementiert, um die systeminternen Funktionen SSE3, SSE 4.1, AVX 128-Bit und F16C/CVT16 zu verwenden, sofern zutreffend. Andernfalls verwendet directxmath SSE/SSE2. Wenn Sie die systeminternen Funktionen von \_ XM F16C verwenden, werden systeminterne XM-Funktionen, systeminterne \_ \_ \_ \_ \_ \_ \_ \_ XM \_ \_ -SSE-Funktionen \_ , \_ XM \_ SSE3-Funktionen \_ \_ und \_ XM-SSE4- \_ \_ \_ Funktionen impliziert.<br/>                                                                                                                                                 |
| \_XM- \_ FMA3 \_ intrinsie\_      | Neues für Windows 10 Fall Creators Update SDK<br/> Wenn Sie diese Compilerdirektive angeben, nutzen directxmath-Funktionen ggf. die systeminternen Funktionen SSE3, SSE 4.1, AVX 128-Bit und FMA3. Andernfalls verwendet directxmath SSE/SSE2. Wenn Sie die systeminternen Funktionen von \_ XM FMA3 verwenden, werden systeminterne XM-Funktionen, systeminterne \_ \_ \_ \_ \_ \_ \_ \_ XM \_ \_ -SSE-Funktionen \_ , \_ XM \_ SSE3-Funktionen \_ \_ und \_ XM-SSE4- \_ \_ \_ Funktionen impliziert. <br/>                                                                                                                                                            |
| \_XM- \_ vectorcallcenter\_            | Dies ermöglicht die Verwendung der neuen \_ \_ vectorcall-Aufruf Konvention für Windows x86-oder Windows x64-Ziele. Der Standardwert ist \_ XM \_ vectorcallcenter \_ = 1, wenn der Compiler dieses Feature unterstützt. Sie können Sie manuell auf \_ XM \_ vectorcallcenter \_ = 0 festlegen, um Sie immer zu deaktivieren. <br/> \_\_vectorcallcenter wird für Windows RT Platform oder Managed C++ nicht unterstützt. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Referenz](ovw-xnamath-reference.md)
</dt> </dl>

 

 




