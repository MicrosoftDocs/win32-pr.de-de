---
title: call (sm4 - asm)
description: Ruft eine mit gekennzeichnete Unterroutine auf, in der die Bezeichnung l\ im Programm angezeigt wird.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c55ce1c0005014928c006e29c9d7d08c3cadc3d11fee870ea1c9fa39df514fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516653"
---
# <a name="call-sm4---asm"></a>call (sm4 - asm)

Ruft eine mit gekennzeichnete Unterroutine auf, wobei die Bezeichnung **l \#** im Programm angezeigt wird.



| call l\# |
|----------|



 



| Element                                                       | Beschreibung                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[in \] Die Bezeichnung der Unterroutine.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein [Ret](ret--sm4---asm-.md) gefunden wird, wird die Ausführung nach diesem Aufruf an die Anweisung zurückgegeben.

Das Tokenformat enthält zur Vereinfachung den Offset der entsprechenden Bezeichnung im Shader.

Das folgende Beispiel zeigt die Aufrufanweisung.


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a>Beschränkungen

-   Unterroutinen können 32 Tiefe schachteln.
-   Der Rückgabeadressstapel wird von der Implementierung transparent verwaltet.
-   Wenn bereits 32 Einträge im Rückgabeadressstapel vorhanden sind und ein **Aufruf** ausgegeben wird, wird der Aufruf übersprungen.
-   Es gibt keinen automatischen Parameterstapel. Die Anwendung kann ein indizierbares temporäres Registerarray (x \# \[ \] ) verwenden, um einen Stapel manuell zu implementieren. Die Rückgabeadressen der Unterroutinenaufrufe sind jedoch nicht sichtbar und für jede manuelle Stapelverwaltung, die von der Anwendung durchgeführt wird, orthogonal.
-   Die Indizierung des *\# l-Parameters* ist nicht zulässig.
-   Rekursion ist nicht zulässig.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





