---
title: ps
description: Diese Anweisung gibt die shaderversionsnummer an und funktioniert für alle shaderversionen.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993191"
---
# <a name="ps"></a>ps

Diese Anweisung gibt die shaderversionsnummer an und funktioniert für alle shaderversionen.

## <a name="syntax"></a>Syntax


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>Eingabeargumente

Eingabeargumente enthalten eine einzelne Hauptversionsnummer mit einer einzelnen unter Versionsnummer. Die zulässigen Kombinationen sind in der folgenden Tabelle aufgeführt.



| Hauptversionen | Unter Versionen                   |
|---------------|--------------------------------|
| 1             | 1, 2, 3, 4                     |
| 2             | 0, x (erweitert), SW (Software) |
| 3             | 0, SW (Software)               |



 

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung muss die erste nicht-Kommentar Anweisung in einem Pixelshader sein.

Hardwarebeschleunigte Versionen der Software (Versionen ohne \_ SW in der Versionsnummer) können Scheitel Punkte mit Hardware-accelearation verarbeiten oder die Verarbeitung von Software Scheitel Punkten verwenden. Softwareversionen (Versionen mit \_ SW in der Versionsnummer) verarbeiten Vertices nur mit Software.

## <a name="examples"></a>Beispiele

Dieses partielle Beispiel deklariert einen Pixel-Shader der Version 1 \_ .


```
ps_1_1
```



In diesem partiellen Beispiel wird ein 1-Pixel-Shader der Version 1 deklariert \_ .


```
ps_1_4
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




