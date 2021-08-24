---
title: callc (sm4 - asm)
description: Ruft bedingt eine Unterroutine auf, die durch markiert ist, wobei die Bezeichnung l\ im Programm angezeigt wird.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb751b57a09704a2fec7a9c3afb69362873e3a1d2b43091efd984f67623188a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727160"
---
# <a name="callc-sm4---asm"></a>callc (sm4 - asm)

Ruft bedingt eine Unterroutine auf, die durch markiert ist, wobei die Bezeichnung **l \#** im Programm angezeigt wird.



| callc{ \_ z\|\_nz} src0.select \_ component, l\# |
|----------------------------------------------|



 



| Element                                                            | Beschreibung                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente, für die die Bedingung zu testen ist.<br/> |
| <span id="l_"></span><span id="L_"></span>*L\#*<br/>      | \[in \] Die Bezeichnung der Unterroutine.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Wenn ein [Ret gefunden wird,](ret--sm4---asm-.md) geben Sie die Ausführung an die Anweisung nach diesem Aufruf zurück.

Das Tokenformat enthält der Einfachheit halber den Offset der entsprechenden Bezeichnung im Shader.

Das folgende Beispiel zeigt die Aufrufanweisung.


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
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
-   Der Rückgabeadressenstapel wird transparent von der Implementierung verwaltet.
-   Wenn bereits 32 Einträge im Rückgabeadressenstapel vorhanden sind und ein Aufruf ausgegeben wird, wird der Aufruf übersprungen. 
-   Es gibt keinen automatischen Parameterstapel. Die Anwendung kann ein indizierbares temporäres Registerarray (x) verwenden, \# \[ \] um einen Stapel manuell zu implementieren. Die Rückrufadressen der Unterroutine sind jedoch nicht sichtbar und sind orthogonal zu jeder manuellen Stapelverwaltung, die von der Anwendung durchgeführt wird.
-   Die Indizierung des *l-Parameters \#* ist nicht zulässig.
-   Das von *src0* bereitgestellte 32-Bit-Register wird auf Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, führt **callc \_ nz** den Aufruf aus. Wenn alle Bits 0 (null) sind, führt **callc \_ z** den Aufruf aus.
-   Rekursion ist nicht zulässig.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





