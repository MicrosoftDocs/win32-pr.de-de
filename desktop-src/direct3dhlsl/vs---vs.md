---
title: vs
description: Diese Anweisung gibt die Versionsnummer des Shaders an. Diese Anweisung funktioniert für alle Shaderversionen.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3977e77c685adb3a181804c0db5b281ae3e54c6f085586023855259f532dde8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484230"
---
# <a name="vs"></a>vs

Diese Anweisung gibt die Versionsnummer des Shaders an. Diese Anweisung funktioniert für alle Shaderversionen.

## <a name="syntax"></a>Syntax


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Eingabeargumente

Eingabeargumente enthalten eine einzelne Hauptversionsnummer mit einer einzelnen Unterversionsnummer. Die zulässigen Kombinationen sind in der folgenden Tabelle aufgeführt.



| Hauptversionen | Unterversionen                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, sw (Software), x (erweitert) |
| 3             | 0, sw (Software)               |



 

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung muss die erste Nichtkommentaranweisung in einem Vertex-Shader sein.

Diese Anweisung wird in allen Vertex-Shaderversionen unterstützt.

Hardwarebeschleunigte Versionen der Software (Versionen ohne \_ SW in der Versionsnummer) können Scheitelpunkte mit Hardware-Beschleunigung verarbeiten oder die Verarbeitung von Softwarevertex verwenden. Softwareversionen (Versionen mit \_ sw in der Versionsnummer) verarbeiten Scheitelpunkte nur mit Software.

## <a name="examples"></a>Beispiele

In diesem Teilbeispiel wird ein \_ Vertex-Shader der Version 1 1 deklariert.


```
vs_1_1
```



In diesem Teilbeispiel wird ein Softwarevertex-Shader der Version 2 deklariert.


```
vs_2_sw
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




