---
title: vs
description: Diese Anweisung gibt die Shader-Versionsnummer an. Diese Anweisung funktioniert für alle shaderversionen.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389588"
---
# <a name="vs"></a>vs

Diese Anweisung gibt die Shader-Versionsnummer an. Diese Anweisung funktioniert für alle shaderversionen.

## <a name="syntax"></a>Syntax


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Eingabeargumente

Eingabeargumente enthalten eine einzelne Hauptversionsnummer mit einer einzelnen unter Versionsnummer. Die zulässigen Kombinationen sind in der folgenden Tabelle aufgeführt.



| Hauptversionen | Unter Versionen                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, SW (Software), x (erweitert) |
| 3             | 0, SW (Software)               |



 

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung muss die erste Anweisung sein, die kein Kommentar in einem Scheitelpunkt-Shader ist.

Diese Anweisung wird in allen Scheitelpunkt-Shader-Versionen unterstützt.

Hardwarebeschleunigte Versionen der Software (Versionen ohne \_ SW in der Versionsnummer) können Scheitel Punkte mit Hardware-accelearation verarbeiten oder die Verarbeitung von Software Scheitel Punkten verwenden. Softwareversionen (Versionen mit \_ SW in der Versionsnummer) verarbeiten Vertices nur mit Software.

## <a name="examples"></a>Beispiele

In diesem partiellen Beispiel wird ein \_ Vertex-Shader der Version 1 deklariert.


```
vs_1_1
```



In diesem partiellen Beispiel wird ein Software-Vertex-Shader der Version 2 deklariert.


```
vs_2_sw
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




