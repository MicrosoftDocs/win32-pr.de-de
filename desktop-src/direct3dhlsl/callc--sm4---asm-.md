---
title: callc (SM4-ASM)
description: Ruft bedingt eine durch markierte Unterroutine auf, wobei die Bezeichnung l \ im Programm angezeigt wird.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993071"
---
# <a name="callc-sm4---asm"></a>callc (SM4-ASM)

Ruft bedingt eine durch markierte Unterroutine auf, wobei die Bezeichnung **l \#** im Programm angezeigt wird.



| callc { \_ z \|\_NZ} src0. Select- \_ Komponente, l\# |
|----------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Komponente, für die die Bedingung getestet werden soll.<br/> |
| <span id="l_"></span><span id="L_"></span>*int\#*<br/>      | \[in \] der Bezeichnung der Unterroutine.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein [ret](ret--sm4---asm-.md) gefunden wird, wird die Ausführung an die Anweisung nach diesem-Befehl zurückgegeben.

Das tokenformat enthält den Offset der entsprechenden Bezeichnung im Shader.

Im folgenden Beispiel wird die-Anweisung aufgerufen.


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

-   Unterroutinen können 32 tief Schachteln.
-   Der Rückgabe Adress Stapel wird von der-Implementierung transparent verwaltet.
-   Wenn im Rückgabe Adress Stapel bereits 32 Einträge vorhanden sind und ein-Befehl ausgegeben wird **, wird der** -Vorgang übersprungen.
-   Es ist kein automatischer Parameter Stapel vorhanden. Die Anwendung kann ein indizierbares temporäres Registrierungs Array (x \# \[ \] ) verwenden, um einen Stapel manuell zu implementieren. Allerdings sind die Rückgabe Adressen der Unterroutine Aufrufe nicht sichtbar und für jede manuelle Stapel Verwaltung, die von der Anwendung ausgeführt wird, orthogonal.
-   Die Indizierung *des \# l* -Parameters ist nicht zulässig.
-   Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, führt **callc \_ NZ** den Aufruf aus. Wenn alle Bits NULL sind, führt **callc \_ z** den Aufruf aus.
-   Rekursion ist nicht zulässig.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





