---
title: Neue Ressourcentypen
description: In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Byte Adress Puffer (Übersicht)
- Lese-/Schreibpuffer (Übersicht)
- Strukturierter Puffer (Übersicht)
- Ungeordneter Zugriffs Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390652"
---
# <a name="new-resource-types"></a>Neue Ressourcentypen

In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.

-   [Puffer und Texturen mit Lese-/Schreibzugriff](#readwrite-buffers-and-textures)
-   [Strukturierter Puffer](#structured-buffer)
-   [Byte Adress Puffer](#byte-address-buffer)
-   [Ungeordneter Zugriffs Puffer oder Textur](#unordered-access-buffer-or-texture)
    -   [Puffer anfügen und nutzen](#append-and-consume-buffer)
-   [Zugehörige Themen](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Puffer und Texturen mit Lese-/Schreibzugriff

Shadermodell 4-Ressourcen sind schreibgeschützt. Shader Model 5 implementiert einen neuen entsprechenden Satz von Lese-/Schreibressourcen:

-   [Rwbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Diese Ressourcen erfordern eine Ressourcen Variable für den Zugriff auf den Arbeitsspeicher (durch Indizierung), da keine Methoden für den direkten Zugriff auf den Speicher vorhanden sind. Eine Ressourcen Variable kann auf der linken und der rechten Seite einer Gleichung verwendet werden. Wenn Sie auf der rechten Seite verwendet wird, muss es sich bei dem Vorlagentyp um eine einzelne Komponente (float, int oder uint) handeln.

## <a name="structured-buffer"></a>Strukturierter Puffer

Ein strukturierter Puffer ist ein Puffer, der Elemente gleicher Größen enthält. Verwenden Sie eine Struktur mit einem oder mehreren Elementtypen, um ein Element zu definieren. Im folgenden finden Sie eine Struktur mit drei Membern.


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



Verwenden Sie diese Struktur, um einen strukturierten Puffer wie den folgenden zu deklarieren:


```
StructuredBuffer<MyStruct> mySB;
```



Zusätzlich zur Indizierung unterstützt ein strukturierter Puffer den Zugriff auf einen einzelnen Member wie den folgenden:


```
float4 myColor = mySb[27].Color;
```



Verwenden Sie die folgenden Objekttypen, um auf einen strukturierten Puffer zuzugreifen:

-   [Structuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) ist ein strukturierter Schreib geschützter Puffer.
-   [Rwstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) ist ein strukturierter Lese-/Schreib-Puffer.

[Atomarische Funktionen](direct3d-11-advanced-stages-cs-atomic-functions.md) , die Interlocked-Vorgänge implementieren, sind für int-und uint-Elemente in einem **rwstructuredbuffer** zulässig.

## <a name="byte-address-buffer"></a>Byte Adress Puffer

Ein Byte Adress Puffer ist ein Puffer, dessen Inhalt durch einen Byte Offset adressierbar ist. Normalerweise wird der Inhalt eines [Puffers](overviews-direct3d-11-resources-buffers-intro.md) pro Element mithilfe eines Stride-Elements für jedes Element und der Element Nummer (n) indiziert, wie von S \* N angegeben. Ein Byte Adress Puffer, der auch als Rohdaten Puffer bezeichnet werden kann, verwendet einen Byte-Wert Offset vom Anfang des Puffers für den Zugriff auf Daten. Der Bytewert muss ein Vielfaches von vier sein, damit er mit DWORD ausgerichtet ist. Wenn ein anderer Wert angegeben wird, ist das Verhalten nicht definiert.

Mit Shader Model 5 werden Objekte für den Zugriff auf einen schreibgeschützten [Byte Adress Puffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) sowie einen [Byte Adress Puffer mit Lese-/Schreibzugriff](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)eingeführt. Der Inhalt eines Byte Adress Puffers ist als 32-Bit-Ganzzahl ohne Vorzeichen konzipiert. Wenn der Wert im Puffer nicht wirklich eine Ganzzahl ohne Vorzeichen ist, verwenden Sie eine Funktion wie [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) , um Sie zu lesen.

## <a name="unordered-access-buffer-or-texture"></a>Ungeordneter Zugriffs Puffer oder Textur

Eine unsorderte Zugriffs Ressource (einschließlich Puffer, Texturen und Textur Arrays ohne Multisampling) ermöglicht Temporale ungeordnete Lese-/Schreibzugriffe aus mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Arbeitsspeicher Konflikte durch die Verwendung von [atomaren Funktionen](direct3d-11-advanced-stages-cs-atomic-functions.md)entstehen.

Erstellen Sie einen ungeordneten Zugriffs Puffer oder eine Textur, indem Sie eine Funktion wie z. b. [**ID3D11Device:: createbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) oder [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) aufrufen und in der Enumeration [**D3D11 \_ Bind- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) das Flag **D3D11 \_ Bind \_ ungeordnete \_ Zugriffe** übergeben.

Ungeordnete Zugriffs Ressourcen können nur an Pixel-Shader und Compute-Shader gebunden werden. Während der Ausführung verfügen Pixel-Shader oder COMPUTE-Shader, die parallel ausgeführt werden, über die gleichen unbestellten Zugriffs Ressourcen.

### <a name="append-and-consume-buffer"></a>Puffer anfügen und nutzen

Ein Anfüge-und-Wert-Puffer ist ein spezieller Typ einer ungeordneten Ressource, der das Hinzufügen und Entfernen von Werten am Ende eines Puffers unterstützt, ähnlich der Art und Weise, wie ein Stapel funktioniert.

Ein Anfüge-und-Verb-Puffer muss ein strukturierter Puffer sein:

-   [Appendstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [Consumestructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Diese Ressourcen werden über ihre Methoden verwendet, von denen diese Ressourcen keine Ressourcenvariablen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 