---
title: Neue Ressourcentypen
description: In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Byte-Adresspuffer (Übersicht)
- Lese-/Schreibpuffer (Übersicht)
- Strukturierter Puffer (Übersicht)
- Ungeordneter Zugriffspuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ab9e6f1677770b1a40766b846f4675df9eaa3809b42838783ddb834044bfe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566300"
---
# <a name="new-resource-types"></a>Neue Ressourcentypen

In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.

-   [Lese-/Schreibpuffer und Texturen](#readwrite-buffers-and-textures)
-   [Strukturierter Puffer](#structured-buffer)
-   [Byteadressenpuffer](#byte-address-buffer)
-   [Ungeordneter Zugriffspuffer oder Ungeordnete Textur](#unordered-access-buffer-or-texture)
    -   [Puffer anfügen und nutzen](#append-and-consume-buffer)
-   [Zugehörige Themen](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Lese-/Schreibpuffer und Texturen

Shadermodell 4-Ressourcen sind schreibgeschützt. Shadermodell 5 implementiert einen neuen entsprechenden Satz von Lese-/Schreibressourcen:

-   [Rwbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Diese Ressourcen erfordern eine Ressourcenvariable für den Zugriff auf den Arbeitsspeicher (durch Indizierung), da es keine Methoden für den direkten Zugriff auf den Arbeitsspeicher gibt. Eine Ressourcenvariable kann auf der linken und rechten Seite einer Gleichung verwendet werden. Bei Verwendung auf der rechten Seite muss der Vorlagentyp eine einzelne Komponente (float, int oder uint) sein.

## <a name="structured-buffer"></a>Strukturierter Puffer

Ein strukturierter Puffer ist ein Puffer, der Elemente gleicher Größe enthält. Verwenden Sie eine -Struktur mit einem oder mehr Membertypen, um ein Element zu definieren. Hier ist eine Struktur mit drei Membern.


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



Verwenden Sie diese Struktur, um einen strukturierten Puffer wie diesen zu deklarieren:


```
StructuredBuffer<MyStruct> mySB;
```



Zusätzlich zur Indizierung unterstützt ein strukturierter Puffer den Zugriff auf einen einzelnen Member wie diesen:


```
float4 myColor = mySb[27].Color;
```



Verwenden Sie die folgenden Objekttypen für den Zugriff auf einen strukturierten Puffer:

-   [StructuredBuffer ist](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) ein schreibgeschützter strukturierter Puffer.
-   [RWStructuredBuffer ist](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) ein strukturierter Puffer mit Lese-/Schreibzugriff.

[Atomic-Funktionen,](direct3d-11-advanced-stages-cs-atomic-functions.md) die interlocked-Vorgänge implementieren, sind für int- und uint-Elemente in einem **RWStructuredBuffer zulässig.**

## <a name="byte-address-buffer"></a>Byteadressenpuffer

Ein Byteadressenpuffer ist ein Puffer, dessen Inhalt durch einen Byteoffset adressierbar ist. Normalerweise wird der [](overviews-direct3d-11-resources-buffers-intro.md) Inhalt eines Puffers pro Element mithilfe eines Schritts für jedes Element (S) und der Elementnummer (N) indiziert, wie von S \* N angegeben. Ein Byteadressenpuffer, der auch als Rohpuffer bezeichnet werden kann, verwendet einen Bytewertoffset vom Anfang des Puffers, um auf Daten zu zugreifen. Der Bytewert muss ein Vielfaches von vier sein, damit er DWORD-ausgerichtet ist. Wenn ein anderer Wert angegeben wird, ist das Verhalten nicht definiert.

Shadermodell 5 führt -Objekte für den Zugriff auf einen schreibgeschützten [Byteadressenpuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) sowie einen Byteadressenpuffer mit [Lese-/Schreibzugriff ein.](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) Der Inhalt eines Byteadressenpuffers ist als 32-Bit-Ganzzahl ohne Vorzeichen konzipiert. Wenn der Wert im Puffer keine ganze Zahl ohne Vorzeichen ist, verwenden Sie eine Funktion wie [**asfloat,**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) um ihn zu lesen.

## <a name="unordered-access-buffer-or-texture"></a>Ungeordneter Zugriffspuffer oder Ungeordnete Textur

Eine ungeordnete Zugriffsressource (einschließlich Puffern, Texturen und Texturarrays ohne Multisampling) ermöglicht temporal ungeordneten Lese-/Schreibzugriff aus mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne speicherkonflikte durch die Verwendung von [Atomic Functions zu generieren.](direct3d-11-advanced-stages-cs-atomic-functions.md)

Erstellen Sie einen ungeordneten Zugriffspuffer oder eine ungeordnete Textur, indem Sie eine Funktion wie [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) oder [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) aufrufen und das **FLAG D3D11 \_ BIND \_ UNORDERED \_ ACCESS** aus der [**D3D11 \_ BIND \_ FLAG-Enumeration**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) übergeben.

Ungeordnete Zugriffsressourcen können nur an Pixel-Shader und Compute-Shader gebunden werden. Während der Ausführung werden für Pixel-Shader oder Compute-Shader, die parallel ausgeführt werden, dieselben ungeordneten Zugriffsressourcen gebunden.

### <a name="append-and-consume-buffer"></a>Puffer anfügen und nutzen

Ein Puffer zum Anfügen und Nutzen ist ein spezieller Typ einer ungeordneten Ressource, der das Hinzufügen und Entfernen von Werten am Ende eines Puffers unterstützt, ähnlich wie ein Stapel funktioniert.

Ein Puffer zum Anfügen und Nutzen muss ein strukturierter Puffer sein:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Verwenden Sie diese Ressourcen über ihre Methoden. Diese Ressourcen verwenden keine Ressourcenvariablen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 