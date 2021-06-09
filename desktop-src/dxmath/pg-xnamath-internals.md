---
description: In diesem Thema wird der interne Entwurf der DirectXMath-Bibliothek beschrieben.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Bibliotheksinternes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7c1843a83a81e7acac241c66dd18ff26217569
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827234"
---
# <a name="library-internals"></a>Bibliotheksinternes

In diesem Thema wird der interne Entwurf der DirectXMath-Bibliothek beschrieben.

-   [Aufrufkonventionen](#calling-conventions)
-   [Äquivalenz des Grafikbibliothekstyps](#graphics-library-type-equivalence)
-   [Globale Konstanten in der DirectXMath-Bibliothek](#global-constants-in-the-directxmath-library)
-   [Windows-SSE im Vergleich zu SSE2](#windows-sse-versus-sse2)
-   [Routinevarianten](#routine-variants)
-   [Plattforminkonsistenzen](#platform-inconsistencies)
-   [Plattformspezifische Erweiterungen](#platform-specific-extensions)
-   [Verwandte Themen](#related-topics)

## <a name="calling-conventions"></a>Aufrufkonventionen

Um die Portabilität zu verbessern und das Datenlayout zu optimieren, müssen Sie die entsprechenden Aufrufkonventionen für jede Plattform verwenden, die von der DirectXMath-Bibliothek unterstützt wird. Wenn Sie [**XMVECTOR-Objekte**](xmvector-data-type.md) als Parameter übergeben, die als an einer 16-Byte-Grenze ausgerichtet definiert sind, gibt es je nach Zielplattform unterschiedliche Aufrufanforderungen:

**Für 32-Bit-Windows**

Für 32-Bit-Windows sind zwei Aufrufkonventionen für die effiziente Übergabe von [ \_ \_ m128-Werten](/cpp/cpp/m128) verfügbar (die [**XMVECTOR**](xmvector-data-type.md) auf dieser Plattform implementieren). Der Standard ist [ \_ \_ fastcall,](https://docs.microsoft.com/cpp/cpp/fastcall)der die ersten drei [ \_ \_ m128-Werte](/cpp/cpp/m128) **(XMVECTOR-Instanzen)** als Argumente an eine Funktion in einem *SSE/SSE2-Register übergeben* kann. [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall) übergibt verbleibende Argumente über den Stapel.

Neuere Microsoft Visual Studio-Compiler unterstützen eine neue Aufrufkonvention, vectorcall, die bis zu sechs \_ \_ [ \_ \_ m128-Werte](/cpp/cpp/m128) [**(XMVECTOR-Instanzen)**](xmvector-data-type.md) als Argumente an eine Funktion in einem *SSE/SSE2-Register* übergeben kann. Sie kann auch heterogene Vektoraggregate (auch [**als XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)bezeichnet) über *SSE/SSE2-Register* übergeben, wenn ausreichend Platz vorhanden ist.

**Für 64-Bit-Editionen von Windows**

Für 64-Bit-Windows stehen zwei Aufrufkonventionen für die effiziente Übergabe von [ \_ \_ m128-Werten zur](/cpp/cpp/m128) Verfügung. Der Standard ist [ \_ \_ fastcall,](https://docs.microsoft.com/cpp/cpp/fastcall)der alle [ \_ \_ m128-Werte](/cpp/cpp/m128) auf dem Stapel übergibt.

Neuere Visual Studio unterstützen die Vectorcall-Aufrufkonvention, die bis zu sechs \_ \_ [ \_ \_ m128-Werte](/cpp/cpp/m128) [**(XMVECTOR-Instanzen)**](xmvector-data-type.md) als Argumente an eine Funktion in einem *SSE/SSE2-Register* übergeben kann. Sie kann auch heterogene Vektoraggregate (auch [**als XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)bezeichnet) über *SSE/SSE2-Register* übergeben, wenn ausreichend Platz vorhanden ist.

**Für Windows auf ARM**

Windows unter ARM & ARM64 unterstützt die Übergabe der ersten \_ \_ vier n128-Werte [**(XMVECTOR-Instanzen)**](xmvector-data-type.md) im Register.

**DirectXMath-Lösung**

Die **Aliase FXMVECTOR,** **GXMVECTOR,** **HXMVECTOR** und **CXMVECTOR** unterstützen diese Konventionen:

-   Verwenden Sie **den FXMVECTOR-Alias,** um an die ersten drei Instanzen von [**XMVECTOR**](xmvector-data-type.md) zu übergeben, die als Argumente an eine Funktion verwendet werden.
-   Verwenden Sie **den GXMVECTOR-Alias,** um die 4. Instanz einer [**XMVECTOR-Instanz**](xmvector-data-type.md) zu übergeben, die als Argument an eine Funktion verwendet wird.
-   Verwenden Sie **den HXMVECTOR-Alias,** um die 5. und 6. Instanz eines [**XMVECTOR-Steuerelements**](xmvector-data-type.md) zu übergeben, das als Argument an eine Funktion verwendet wird. Weitere Informationen zu weiteren Überlegungen finden Sie in der \_ \_ Vectorcall-Dokumentation.
-   Verwenden Sie **den CXMVECTOR-Alias,** um alle weiteren Instanzen von [**XMVECTOR**](xmvector-data-type.md) zu übergeben, die als Argumente verwendet werden.

> [!Note]  
> Verwenden Sie für Ausgabeparameter immer XMVECTOR oder XMVECTOR& und ignorieren Sie sie in Bezug auf die oben genannten Regeln \* für Eingabeparameter.

 

Aufgrund von Einschränkungen bei \_ \_ vectorcall wird empfohlen, **GXMVECTOR** oder **HXMVECTOR** nicht für C++-Konstruktoren zu verwenden. Verwenden Sie **einfach FXMVECTOR** für die ersten drei [**XMVECTOR-Werte,**](xmvector-data-type.md) und verwenden Sie **dann CXMVECTOR** für den Rest.

Die **Aliase FXMMATRIX** und **CXMMATRIX** unterstützen die Nutzung des HVA-Arguments, das mit \_ \_ vectorcall übergeben wird.

-   Verwenden Sie **den FXMMATRIX-Alias,** um die erste [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) als Argument an die Funktion zu übergeben. Dabei wird davon ausgegangen, dass Sie nicht mehr als zwei **FXMVECTOR-Argumente** oder mehr als zwei float-, double- oder **FXMVECTOR-Argumente** rechts von der Matrix haben. Weitere Informationen zu weiteren Überlegungen finden Sie in der \_ \_ Vectorcall-Dokumentation.
-   Verwenden Sie **andernfalls den CXMMATRIX-Alias.**

Aufgrund von Einschränkungen bei \_ \_ vectorcall wird empfohlen, **fxmmatrix** niemals für C++-Konstruktoren zu verwenden. Verwenden Sie einfach **CXMMATRIX**.

Zusätzlich zu den Typaliasen müssen Sie auch die XM CALLCONV-Anmerkung verwenden, um sicherzustellen, dass die Funktion die entsprechende Aufrufkonvention ( fastcall im Vergleich zu \_ \_ \_ \_ vectorcall) basierend auf Ihrem Compiler und Ihrer Architektur \_ verwendet. Aufgrund von Einschränkungen bei \_ \_ vectorcall wird empfohlen, XM \_ CALLCONV für C++-Konstruktoren nicht zu verwenden.

Im Folgenden finden Sie Beispieldeklarationen, die diese Konvention veranschaulichen:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Um diese Aufrufkonventionen zu unterstützen, werden diese Typaliase wie folgt definiert (Parameter müssen als Wert übergeben werden, damit der Compiler sie für die In-Register-Übergabe berücksichtigen kann):

**Für 32-Bit-Windows-Apps**

Bei Verwendung von \_ \_ fastcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Bei Verwendung von \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Für native 64-Bit-Windows-Apps**

Bei Verwendung von \_ \_ fastcall:


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Bei Verwendung von \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows unter ARM**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Obwohl alle Funktionen inline deklariert werden und der Compiler in vielen Fällen keine Aufrufkonventionen für diese Funktionen verwenden muss, gibt es Fälle, in denen der Compiler entscheiden kann, dass es effizienter ist, die Funktion nicht inline zu verwenden, und in diesen Fällen wünschen wir die bestmögliche Aufrufkonvention für jede Plattform.

 

## <a name="graphics-library-type-equivalence"></a>Typäquivalenz der Grafikbibliothek

Um die Verwendung der DirectXMath-Bibliothek zu unterstützen, entsprechen viele DirectXMath Library-Typen und -Strukturen den Windows-Implementierungen der **Typen D3DDECLTYPE** und **D3DFORMAT** sowie den [**DXGI \_ FORMAT-Typen.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | \_DXGI-FORMAT                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | DXGI \_ FORMAT \_ R8G8 \_ SINT                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (nur Xbox)                                                        | D3DFMT \_ x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8 \_ SINT                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (nur Xbox)                                                       | D3DFMT \_ x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ SNORM                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM (DXGI 1.1+)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (nur Xbox)                                                         | D3DDECLTYPE \_ DEC3 (nur Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (nur Xbox)                                                        | D3DDECLTYPE \_ DEC3N (nur Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | \_DXGI-FORMAT \_ R11G11B10 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | \_DXGI-FORMAT \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | \_DXGI-FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | \_DXGI-FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | \_DXGI-FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | \_DXGI-FORMAT \_ R32G32 \_ SINT                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | \_DXGI-FORMAT \_ R32G32B32 \_ SINT                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | \_DXGI-FORMAT \_ R32G32B32A32 \_ SINT                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | \_DXGI-FORMAT \_ R16G16 \_ SINT                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | \_DXGI-FORMAT \_ R16G16B16A16 \_ SINT                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | \_DXGI-FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | DXGI \_ FORMAT \_ R8G8 \_ UINT                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | DXGI \_ FORMAT \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | DXGI \_ FORMAT \_ R32G32 \_ UINT                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | \_DXGI-FORMAT \_ R32G32B32 \_ UINT                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | DXGI \_ FORMAT \_ R32G32B32A32 \_ UINT                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | \_DXGI-FORMAT \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | \_DXGI-FORMAT \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UINT                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ FORMAT \_ R10G10B10 \_ XR BIAS \_ \_ A2 \_ UNORM (XMLoadUDecN4 [**\_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) und [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)verwenden.)<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (nur Xbox)<br/> D3DDECLTYPE \_ UDEC3 (nur Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (nur Xbox)<br/> D3DDECLTYPE \_ UDEC3N (nur Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM (DXGI 1.2+)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | DXGI \_ FORMAT \_ R16G16 \_ UINT                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (nur Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | DXGI \_ FORMAT \_ R16G16B16A16 \_ UINT                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | \_DXGI-FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Globale Konstanten in der DirectXMath-Bibliothek

Um die Größe des Datensegments zu reduzieren, verwendet die DirectXMath-Bibliothek das [XMGLOBALCONST-Makro,](xmglobalconst.md) um eine Reihe von globalen internen Konstanten in der Implementierung zu verwenden. Standardmäßig wird solchen internen globalen Konstanten g **\_ XM vorangestellt.** In der Regel handelt es sich dabei um einen der folgenden Typen: [**XMVECTORU32,**](xmvectoru32-data-type.md) [**XMVECTORF32**](xmvectorf32-data-type.md)oder **XMVECTORI32**.

Diese internen globalen Konstanten können sich in zukünftigen Revisionen der DirectXMath-Bibliothek ändern. Verwenden Sie öffentliche Funktionen, die die Konstanten nach Möglichkeit kapseln, anstatt globale **g \_ XM-Werte** direkt zu verwenden. Sie können auch eigene globale Konstanten mit [XMGLOBALCONST deklarieren.](xmglobalconst.md)

## <a name="windows-sse-versus-sse2"></a>Windows-SSE im Vergleich zu SSE2

Der SSE-Anweisungssatz bietet nur Unterstützung für Gleitkommavektoren mit einzelner Genauigkeit. DirectXMath muss den SSE2-Anweisungssatz verwenden, um ganzzahlige Vektorunterstützung zu bieten. SSE2 wird von allen Intel-Prozessoren seit der Einführung von Pentium 4, allen AMD K8- und höher-Prozessoren sowie allen x64-fähigen Prozessoren unterstützt.

> [!Note]  
> Windows 8 für x86 oder höher erfordert Unterstützung für SSE2. Alle Versionen von Windows x64 erfordern Unterstützung für SSE2. Windows unter ARM/ARM64 erfordert ARM \_ NEON.

 

## <a name="routine-variants"></a>Routinevarianten

Es gibt mehrere Varianten von DirectXMath-Funktionen, die ihnen die Arbeit erleichtern:

-   Vergleichsfunktionen zum Erstellen komplizierter bedingter Verzweigung basierend auf einer kleineren Anzahl von Vektorvergleichsvorgängen. Der Name dieser Funktionen endet auf "R", z. B. XMVector3InBoundsR. Die Funktionen geben einen Vergleichsdatensatz als UINT-Rückgabewert oder als UINT out-Parameter zurück. Sie können die **XMComparision-Makros verwenden, \*** um den Wert zu testen.
-   Batchfunktionen zum Ausführen von Batchvorgängen für größere Vektorarrays. Der Name dieser Funktionen endet mit "Stream", z. B. [**XMVector3TransformStream.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream) Die Funktionen arbeiten mit einem Array von Eingaben und generieren ein Array von Ausgaben. In der Regel wird ein Eingabe- und Ausgabeschritt verwendet.
-   Schätzfunktionen, die eine schnellere Schätzung statt eines langsameren, genaueren Ergebnisses implementieren. Der Name dieser Funktionen endet auf "Est", z. B. [**XMVector3NormalizeEst.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest) Die Auswirkungen der Verwendung von Schätzwert auf Qualität und Leistung variieren von Plattform zu Plattform. Es wird jedoch empfohlen, für leistungsempfindlichen Code Schätzvarianten zu verwenden.

## <a name="platform-inconsistencies"></a>Plattforminkonsistenzen

Die DirectXMath-Bibliothek ist für die Verwendung in leistungssensiblen Grafikanwendungen und Spielen vorgesehen. Daher ist die Implementierung für eine optimale Geschwindigkeit bei der normalen Verarbeitung auf allen unterstützten Plattformen konzipiert. Ergebnisse an Begrenzungsbedingungen, insbesondere solche, die Gleitkomma-Specials generieren, variieren wahrscheinlich von Ziel zu Ziel. Dieses Verhalten hängt auch von anderen Laufzeiteinstellungen ab, z. B. dem x87-Steuerwort für das Windows 32-Bit-No-Intrinsics-Ziel oder dem SSE-Steuerelementwort für Windows 32-Bit und 64-Bit. Darüber hinaus gibt es Unterschiede bei den Begrenzungsbedingungen zwischen verschiedenen CPU-Anbietern.

Verwenden Sie DirectXMath nicht in wissenschaftlichen oder anderen Anwendungen, in denen die numerische Genauigkeit von entscheidender Bedeutung ist. Diese Einschränkung spiegelt sich auch in der fehlenden Unterstützung für Berechnungen mit doppelter oder anderer erweiterter Genauigkeit wider.

> [!Note]  
> Die \_ XM \_ NO INTRINSICS-Skalarcodepfade werden in der Regel aus \_ \_ Compliance- und nicht aus Leistungs- und Nicht-Leistungs-Anforderungen geschrieben. Die Ergebnisse der Begrenzungsbedingung variieren ebenfalls.

 

## <a name="platform-specific-extensions"></a>Plattformspezifische Erweiterungen

Die DirectXMath-Bibliothek soll die C++-SIMD-Programmierung vereinfachen und bietet hervorragende Unterstützung für x86-, x64- und Windows RT-Plattformen mithilfe von allgemein unterstützten systeminternen Anweisungen (SSE2 und ARM-NEON).

Es gibt jedoch Zeiten, in denen plattformspezifische Anweisungen sich als nützlich erweisen können. Aufgrund der Art und Weise, wie DirectXMath implementiert wird, ist es in vielen Fällen einfach, DirectXMath-Typen direkt in systeminternen Standardanweisungen zu verwenden, die vom Compiler unterstützt werden, und DirectXMath als Fallbackpfad für Plattformen zu verwenden, die die erweiterte Anweisung nicht unterstützen.

Hier sehen Sie beispielsweise ein vereinfachtes Beispiel für die Nutzung der Punktproduktanweisung SSE 4.1. Beachten Sie, dass Sie den Codepfad explizit schützen müssen, um zu vermeiden, dass zur Laufzeit ungültige Anweisungsausnahmen generiert werden. Stellen Sie sicher, dass die Codepfade genügend Arbeit ausführen, um die zusätzlichen Kosten der Verzweigung, die Komplexität der Verwaltung mehrerer Codepfade und so weiter zu rechtfertigen.


```
#include <Windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ...

   return 0;
}
```



Weitere Informationen zu plattformspezifischen Erweiterungen finden Sie unter:

<dl>

[DirectXMath: SSE, SSE2 und ARM-NEON](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath: SSE3 und SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath: SSE4.1 und SSE4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath: AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath: F16C und FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
