---
title: Zugreifen auf Ressourcen
description: Es gibt mehrere Möglichkeiten, auf Ressourcen zu zugreifen.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b66ae5ad0f3a49f51281d12ba5e3c2c52cd822aadd5097485b571533ae1a04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677170"
---
# <a name="accessing-resources"></a>Zugreifen auf Ressourcen

Es gibt mehrere Möglichkeiten, auf Ressourcen [zu zugreifen.](overviews-direct3d-11-resources-types.md) Unabhängig davon garantiert Direct3D, dass 0 (null) für jede Ressource zurückgesetzt wird, auf die über grenzenlose Grenzen zugegriffen wird.

-   [Zugriffs-Byteoffset](#access-by-byte-offset)
-   [Zugriff nach Index](#access-by-index)
-   [Access By Mips-Methode](#access-by-mips-method)
-   [Zugehörige Themen](#related-topics)

## <a name="access-by-byte-offset"></a>Zugriffs-Byteoffset

Auf zwei neue Puffertypen kann mithilfe eines Byteoffsets zugegriffen werden:

-   [**ByteAddressBuffer ist**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) ein schreibgeschützter Puffer.
-   [**RWByteAddressBuffer ist**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) ein Lese- oder Schreibpuffer.

## <a name="access-by-index"></a>Zugriff nach Index

Ressourcentypen können einen Index verwenden, um auf einen bestimmten Speicherort in der Ressource zu verweisen. Betrachten Sie das folgende Beispiel:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



In diesem Beispiel werden die vier float-Werte, die  am Texel an der Pos-Position in der *Texturressource myTexture* 2D gespeichert sind, der *Variablen myVar* zugewiesen.

> [!Note]  
> Der Standardwert für den Zugriff auf eine Textur auf diese Weise ist Mipmap-Ebene 0 (die ausführlichste Ebene).

 

> [!Note]  
> Die Zeile "float4 myVar = myTexture pos ;" entspricht \[ \] "float4 myVar = myTexture.Load(uint3(pos,0));". Der Zugriff nach Index ist eine neue HLSL-Syntaxerweiterung.

 

> [!Note]  
> Mit dem Compiler in der Version vom Juni 2010 des DirectX SDK und höher können Sie alle Ressourcentypen mit Ausnahme von [Byteadressenpuffern indizieren.](direct3d-11-advanced-stages-cs-resources.md)

 

> [!Note]  
> Mit dem Compiler vom Juni 2010 und höher können Sie lokale Ressourcenvariablen deklarieren. Sie können diesen Variablen global definierte Ressourcen (z. B. *myTexture)* zuweisen und sie auf die gleiche Weise wie ihre globalen Entsprechungen verwenden.

 

## <a name="access-by-mips-method"></a>Access By Mips-Methode

Texturobjekte verfügen über eine **mips-Methode** (z. B. [**Texture2D.mips),**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))mit der Sie die Mipmap-Ebene angeben können. In diesem Beispiel wird die Farbe gelesen, die bei (7,16) auf Mipmap-Ebene 2 in einer 2D-Textur gespeichert ist:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Dies ist eine Erweiterung des Compilers vom Juni 2010 und höher. Der Ausdruck "myTexture.mips \[ 2 \] \[ uint2(x,y) " entspricht \] "myTexture.Load(uint3(x,y,2))".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 