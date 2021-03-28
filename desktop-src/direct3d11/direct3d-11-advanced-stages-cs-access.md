---
title: Zugreifen auf Ressourcen
description: Es gibt mehrere Möglichkeiten, auf Ressourcen zuzugreifen.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993495"
---
# <a name="accessing-resources"></a>Zugreifen auf Ressourcen

Es gibt mehrere Möglichkeiten, auf [Ressourcen](overviews-direct3d-11-resources-types.md)zuzugreifen. Unabhängig davon garantiert Direct3D, dass NULL für alle Ressourcen zurückgegeben wird, auf die außerhalb der Grenzen zugegriffen wird.

-   [Zugriff nach Byte Offset](#access-by-byte-offset)
-   [Zugriff nach Index](#access-by-index)
-   [Zugriff über die MIPS-Methode](#access-by-mips-method)
-   [Zugehörige Themen](#related-topics)

## <a name="access-by-byte-offset"></a>Zugriff nach Byte Offset

Auf zwei neue Puffer Typen kann mithilfe eines Byte Offsets zugegriffen werden:

-   [**Byteaddressbuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) ist ein Schreib geschützter Puffer.
-   [**Rwbyteaddressbuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) ist ein Lese-oder Schreibpuffer.

## <a name="access-by-index"></a>Zugriff nach Index

Ressourcentypen können einen Index verwenden, um auf eine bestimmte Position in der Ressource zu verweisen. Betrachten Sie das folgende Beispiel:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



In diesem Beispiel werden die 4 float-Werte, die an der Position " *POS* " in der Textur Ressource " *MyTexture* 2D" gespeichert sind, der *myVar* -Variablen zugewiesen.

> [!Note]  
> Der Standardwert für den Zugriff auf eine Textur auf diese Weise ist MipMap Level Zero (die ausführlichste Ebene).

 

> [!Note]  
> Die Zeile "float4 MyVar = MyTexture \[ POS \] ;" entspricht "float4 MyVar = MyTexture. Load (uint3 (POS, 0));". Der Zugriff nach Index ist eine neue HLSL-Syntax Erweiterung.

 

> [!Note]  
> Mit dem Compiler in der Version vom Juni 2010 des DirectX SDK und höher können Sie alle Ressourcentypen außer für [Byte Adress Puffer](direct3d-11-advanced-stages-cs-resources.md)indizieren.

 

> [!Note]  
> Mit dem Compiler vom Juni 2010 und höher können Sie lokale Ressourcenvariablen deklarieren. Sie können diesen Variablen global definierte Ressourcen (z. b. *MyTexture*) zuweisen und Sie auf die gleiche Weise wie Ihre globalen Gegenstücke verwenden.

 

## <a name="access-by-mips-method"></a>Zugriff über die MIPS-Methode

Textur Objekte verfügen über eine **MIPS** -Methode (z [**. b. Texture2D. mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), die Sie verwenden können, um die MipMap-Ebene anzugeben. In diesem Beispiel wird die Farbe, die unter (7, 16) auf MipMap-Ebene 2 gespeichert ist, in einer 2D-Textur gelesen:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Dies ist eine Erweiterung des Compilers vom Juni 2010 und höher. Der Ausdruck "MyTexture. mips \[ 2 \] \[ uint2 (x, y) \] " entspricht "MyTexture. Load (uint3 (x, y, 2))".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 