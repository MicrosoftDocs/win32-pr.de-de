---
description: In diesem Thema wird der interne Entwurf der directxmath-Bibliothek beschrieben.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Internale für die Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccac708934c393a526fdb46d73f819d6557107f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348859"
---
# <a name="library-internals"></a>Internale für die Bibliothek

In diesem Thema wird der interne Entwurf der directxmath-Bibliothek beschrieben.

-   [Aufrufkonventionen](#calling-conventions)
-   [Äquivalenz von Grafik Bibliothekstypen](#graphics-library-type-equivalence)
-   [Globale Konstanten in der directxmath-Bibliothek](#global-constants-in-the-directxmath-library)
-   [Windows SSE im Vergleich zu SSE2](#windows-sse-versus-sse2)
-   [Routine Varianten](#routine-variants)
-   [Platform](#platform-inconsistencies)
-   [Plattformspezifische Erweiterungen](#platform-specific-extensions)
-   [Zugehörige Themen](#related-topics)

## <a name="calling-conventions"></a>Aufrufkonventionen

Um die Portabilität zu verbessern und das Datenlayout zu optimieren, müssen Sie die entsprechenden Aufruf Konventionen für jede Plattform verwenden, die von der directxmath-Bibliothek unterstützt wird. Insbesondere bei der Übergabe von [**xmvector**](xmvector-data-type.md) -Objekten als Parameter, die auf einer 16-Byte-Grenze als ausgerichtet definiert sind, gibt es je nach Zielplattform unterschiedliche Sätze von Aufruf Anforderungen:

**Für 32-Bit-Windows**

Bei 32-Bit-Fenstern gibt es zwei Aufruf Konventionen, die für die effiziente Übergabe von [ \_ \_ M128](/cpp/cpp/m128) -Werten (die [**xmvector**](xmvector-data-type.md) auf dieser Plattform implementiert) verfügbar sind. Der Standardwert ist [ \_ \_ fastcallcenter](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), der die ersten drei [ \_ \_ M128](/cpp/cpp/m128) -Werte (**xmvector** -Instanzen) als Argumente an eine Funktion in einem *SSE/SSE2-* Register übergeben kann. [ \_ \_ fastcallübergibt](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx) verbleibende Argumente über den Stapel.

Neuere Microsoft Visual Studio Compiler unterstützen eine neue Aufruf Konvention \_ \_ (vectorcall), die bis zu sechs [ \_ \_ M128](/cpp/cpp/m128) -Werte ([**xmvector**](xmvector-data-type.md) -Instanzen) als Argumente an eine Funktion in einem *SSE/SSE2* -Register übergeben kann. Sie kann auch heterogene Vektor Aggregate (auch als [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)bezeichnet) über *SSE/SSE2* -Register übergeben, wenn ausreichend Platz vorhanden ist.

**Für 64-Bit-Editionen von Windows**

Bei 64-Bit-Fenstern gibt es zwei Aufruf Konventionen, die für die effiziente Übergabe von [ \_ \_ M128](/cpp/cpp/m128) -Werten verfügbar sind. Der Standardwert ist [ \_ \_ fastcallcenter](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), der alle [ \_ \_ M128](/cpp/cpp/m128) -Werte im Stapel übergibt.

Neuere Visual Studio-Compiler unterstützen die \_ \_ vectorcall-Aufruf Konvention, die bis zu sechs [ \_ \_ M128](/cpp/cpp/m128) -Werte ([**xmvector**](xmvector-data-type.md) -Instanzen) als Argumente an eine Funktion in einem *SSE/SSE2* -Register übergeben kann. Sie kann auch heterogene Vektor Aggregate (auch als [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)bezeichnet) über *SSE/SSE2* -Register übergeben, wenn ausreichend Platz vorhanden ist.

**Für Windows RT**

Das Windows RT-Betriebssystem unterstützt das übergeben der ersten vier \_ \_ n128-Werte ([**xmvector**](xmvector-data-type.md) -Instanzen) in-Register.

**Directxmath-Lösung**

Die Aliase " **fxmvector**", " **gxmvector**", " **hxmvector**" und " **cxmvector** " unterstützen diese Konventionen:

-   Verwenden Sie den **fxmvector** -Alias, um an die ersten drei [**xmvector**](xmvector-data-type.md) -Instanzen zu übergeben, die als Argumente für eine Funktion verwendet werden.
-   Verwenden Sie den **gxmvector** -Alias, um die vierte Instanz eines [**xmvector**](xmvector-data-type.md) zu übergeben, die als Argument an eine Funktion verwendet wird.
-   Verwenden Sie den **hxmvector** -Alias, um die fünften und sechsten Instanzen eines [**xmvector**](xmvector-data-type.md) zu übergeben, die als Argument an eine Funktion verwendet werden. Weitere Informationen zu weiteren Überlegungen finden Sie in der \_ \_ vectorcallcenter-Dokumentation.
-   Verwenden Sie den **cxmvector** -Alias, um alle weiteren Instanzen von [**xmvector**](xmvector-data-type.md) zu übergeben, die als Argumente verwendet werden.

> [!Note]  
> Verwenden Sie für Ausgabeparameter immer xmvector \* oder xmvector&, und ignorieren Sie diese in Bezug auf die vorangehenden Regeln für Eingabeparameter.

 

Aufgrund von Einschränkungen bei \_ \_ vectorcallcenter empfiehlt es sich, **gxmvector** oder **hxmvector** nicht für C++-Konstruktoren zu verwenden. Verwenden Sie einfach **fxmvector** für die ersten drei [**xmvector**](xmvector-data-type.md) -Werte, und verwenden Sie dann **cxmvector** für den Rest.

Die **fxmmatrix** -und **cxmmatrix** -Aliase helfen bei der Unterstützung der Verwendung des HVA-Arguments, das mit \_ \_ vectorcallübergibt.

-   Verwenden Sie den **fxmmatrix** -Alias, um die erste [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) als Argument an die Funktion zu übergeben. Dabei wird davon ausgegangen, dass Sie nicht mehr als zwei **fxmvector** -Argumente oder mehr als zwei float-, Double-oder **fxmvector** -Argumente für das "Right" der Matrix haben. Weitere Informationen zu weiteren Überlegungen finden Sie in der \_ \_ vectorcallcenter-Dokumentation.
-   Verwenden Sie andernfalls den **cxmmatrix** -Alias.

Aufgrund von Einschränkungen bei \_ \_ vectorcallcenter empfiehlt es sich nicht, **fxmmatrix** für C++-Konstruktoren zu verwenden. Verwenden Sie einfach " **cxmmatrix**".

Zusätzlich zu den typaliasen müssen Sie auch die XM callkonv-Anmerkung verwenden, \_ um sicherzustellen, dass die Funktion die entsprechende Aufruf Konvention ( \_ \_ fastcall anstelle \_ \_ von vectorcall) auf Grundlage Ihres Compilers und ihrer Architektur verwendet. Aufgrund von Einschränkungen bei \_ \_ vectorcallcenter wird empfohlen, dass Sie XM \_ callkonv nicht für C++-Konstruktoren verwenden.

Im folgenden finden Sie Beispiel Deklarationen, die diese Konvention veranschaulichen:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Um diese Aufruf Konventionen zu unterstützen, werden diese Typaliase wie folgt definiert (Parameter müssen als Wert übergeben werden, damit der Compiler Sie für die in-Register-Übergabe berücksichtigt):

**Für 32-Bit-Windows-apps**

Wenn Sie \_ \_ fast-Befehl verwenden:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Bei Verwendung von \_ \_ vectorcallcenter:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Für Native 64-Bit-Windows-apps**

Wenn Sie \_ \_ fast-Befehl verwenden:


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Bei Verwendung von \_ \_ vectorcallcenter:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows RT**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Obwohl alle Funktionen Inline deklariert sind und der Compiler in vielen Fällen keine Aufruf Konventionen für diese Funktionen verwenden muss, gibt es Fälle, in denen der Compiler entscheiden kann, dass es effizienter ist, die Funktion nicht Inline zu verwenden. in diesen Fällen soll die beste Aufruf Konvention für jede Plattform verwendet werden.

 

## <a name="graphics-library-type-equivalence"></a>Äquivalenz von Grafik Bibliothekstypen

Um die Verwendung der directxmath-Bibliothek zu unterstützen, entsprechen viele directxmath-Bibliothekstypen und-Strukturen den Windows-Implementierungen der Typen **D3DDECLTYPE** und **D3DFORMAT** sowie den [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Typen. 

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | DXGI- \_ Format                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | DXGI- \_ Format \_ R8G8 \_ Sint                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (nur Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | DXGI- \_ Format \_ x8x8x8x8 \_ Sint                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | DXGI- \_ Format \_ R8G8 \_ snorm                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (nur Xbox)                                                       | D3DFMT \_ x8x8x8x8                                              | DXGI- \_ Format \_ x8x8x8x8 \_ snorm                                                                                                                                                                           |
| [**Xmcolor**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | DXGI- \_ Format \_ B8G8R8A8 \_ unorm (DXGI 1.1 und höher)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (nur Xbox)                                                         | D3DDECLTYPE \_ DEC3 (nur Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (nur Xbox)                                                        | D3DDECLTYPE \_ DEC3N (nur Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI- \_ Format \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI- \_ Format \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI- \_ Format \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI- \_ Format \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | DXGI- \_ Format \_ R11G11B10 \_ float                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | DXGI- \_ Format \_ R9G9B9E5 \_ sharedexp                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ float4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI- \_ Format \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ float4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI- \_ Format \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | DXGI- \_ Format \_ R16G16 \_ float                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | DXGI- \_ Format \_ R16G16B16A16 \_ float                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | DXGI- \_ Format \_ R32G32 \_ Sint                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | DXGI- \_ Format \_ R32G32B32 \_ Sint                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | DXGI- \_ Format \_ R32G32B32A32 \_ Sint                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | DXGI- \_ Format \_ R16G16 \_ Sint                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | DXGI- \_ Format \_ R16G16 \_ snorm                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | DXGI- \_ Format \_ R16G16B16A16 \_ Sint                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | DXGI- \_ Format \_ R16G16B16A16 \_ snorm                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | DXGI- \_ Format \_ R8G8 \_ uint                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | DXGI- \_ Format \_ R8G8 \_ unorm                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | DXGI- \_ Format \_ R32G32 \_ uint                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | DXGI- \_ Format \_ R32G32B32 \_ uint                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | DXGI- \_ Format \_ R32G32B32A32 \_ uint                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | DXGI- \_ Format \_ B5G5R5A1 \_ unorm                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | DXGI- \_ Format \_ B5G6R5 \_ unorm                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI- \_ Format \_ x8x8x8x8 \_ uint                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI- \_ Format \_ x8x8x8x8 \_ unorm<br/> DXGI- \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm (verwenden Sie [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) und [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr).)<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (nur Xbox)<br/> D3DDECLTYPE \_ UDEC3 (nur Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI- \_ Format \_ R10G10B10A2 \_ uint                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (nur Xbox)<br/> D3DDECLTYPE \_ UDEC3N (nur Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI- \_ Format \_ R10G10B10A2 \_ unorm                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | DXGI- \_ Format \_ B4G4R4A4 \_ unorm (DXGI 1.2 und höher)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | DXGI- \_ Format \_ R16G16 \_ uint                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI- \_ Format \_ R16G16 \_ unorm                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (nur Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | DXGI- \_ Format \_ R16G16B16A16 \_ uint                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | DXGI- \_ Format \_ R16G16B16A16 \_ unorm                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Globale Konstanten in der directxmath-Bibliothek

Um die Größe des Datensegments zu reduzieren, verwendet die directxmath-Bibliothek das [xmglobalconst](xmglobalconst.md) -Makro, um eine Reihe globaler interner Konstanten in der Implementierung zu verwenden. Gemäß der Konvention werden solche internen globalen Konstanten mit **g \_ XM** vorangestellt. In der Regel handelt es sich dabei um einen der folgenden Typen: [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md)oder **XMVECTORI32**.

Diese internen globalen Konstanten können in zukünftigen Revisionen der directxmath-Bibliothek geändert werden. Verwenden Sie öffentliche Funktionen, die die Konstanten einschließen, wenn möglich, anstelle der direkten Verwendung von globalen **g \_ XM** -Werten. Sie können auch Ihre eigenen globalen Konstanten mithilfe von [xmglobalconst](xmglobalconst.md)deklarieren.

## <a name="windows-sse-versus-sse2"></a>Windows SSE im Vergleich zu SSE2

Der SSE-Anweisungs Satz bietet nur Unterstützung für Gleit Komma Vektoren mit einfacher Genauigkeit. Directxmath muss den SSE2-Anweisungs Satz verwenden, um die Unterstützung für ganzzahlige Vektor bereitzustellen. SSE2 wird von allen Intel-Prozessoren seit der Einführung von Pentium 4, allen AMD-und späteren Prozessoren und allen x64-fähigen Prozessoren unterstützt.

> [!Note]  
> Windows 8 für x86 erfordert Unterstützung für SSE2. Alle Versionen von Windows x64 benötigen Unterstützung für SSE2. Windows RT (auch als Windows auf Arm bezeichnet) erfordert Arm \_ Neon.

 

## <a name="routine-variants"></a>Routine Varianten

Es gibt mehrere Varianten von directxmath-Funktionen, mit denen Sie Ihre Arbeit vereinfachen können:

-   Vergleichsfunktionen, um komplizierte bedingte Verzweigungen basierend auf einer geringeren Anzahl von Vektor Vergleichs Vorgängen zu erstellen. Der Name dieser Funktionen endet in "R", z. b. XMVector3InBoundsR. Die-Funktionen geben einen Vergleichsdaten Satz als uint-Rückgabewert oder als uint-out-Parameter zurück. Sie können den *xmcomparision \** _-Makros verwenden, um den Wert zu testen.
-   Batch Funktionen zum Ausführen von Batch-Stil-Vorgängen für größere Vektor Arrays. Der Name dieser Funktionen endet mit "Stream", z. b. " [_ *XMVector3TransformStream* *](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)". Die-Funktionen arbeiten mit einem Array von Eingaben und generieren ein Array von Ausgaben. In der Regel nehmen Sie einen Eingabe-und Ausgabe Schritt in Anspruch.
-   Schätz Funktionen, die eine schnellere Schätzung anstelle eines langsameren, genaueren Ergebnisses implementieren. Der Name dieser Funktionen endet mit "EST", z. b. [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest). Die Qualitäts-und Leistungseinbußen bei der Verwendung der Schätzung variieren von Plattform zu Plattform, aber es wird empfohlen, dass Sie für leistungsabhängigen Code Schätz Varianten verwenden.

## <a name="platform-inconsistencies"></a>Platform

Die directxmath-Bibliothek ist für die Verwendung in Leistungs sensiblen Grafikanwendungen und spielen vorgesehen. Daher ist die Implementierung für die optimale Geschwindigkeit der normalen Verarbeitung auf allen unterstützten Plattformen konzipiert. Die Ergebnisse an begrenzungsbedingungen, insbesondere solche, die Gleit Komma-Sonderangebote generieren, unterscheiden sich wahrscheinlich von Ziel zu Ziel. Dieses Verhalten hängt auch von anderen Lauf Zeit Einstellungen ab, wie z. b. dem x87-Steuerwort für das Windows 32-Bit-No-Intrinsics-Ziel oder das SSE-Steuerwort für Windows 32-Bit und 64-Bit. Außerdem gibt es Unterschiede in den begrenzungsbedingungen zwischen verschiedenen CPU-Anbietern.

Verwenden Sie directxmath nicht in wissenschaftlichen oder anderen Anwendungen, in denen die numerische Genauigkeit von größter Bedeutung ist. Diese Einschränkung gilt auch für das Fehlen von Unterstützung für doppelte oder andere Berechnungen mit erweiterter Genauigkeit.

> [!Note]  
> Die \_ XM \_ - \_ \_ skalarcodepfade sind im Allgemeinen nicht für die Konformität geschrieben, nicht für die Leistung. Die Ergebnisse der Grenze sind ebenfalls unterschiedlich.

 

## <a name="platform-specific-extensions"></a>Plattformspezifische Erweiterungen

Die Bibliothek directxmath soll die C++ SIMD-Programmierung vereinfachen, die eine hervorragende Unterstützung für x86-, x64-und Windows RT-Plattformen mithilfe von umfassend unterstützten intrinsie-Anweisungen (SSE2 und Arm-Neon) bietet.

Es gibt jedoch Zeiten, in denen plattformspezifische Anweisungen sich als vorteilhaft erweisen können. Aufgrund der Art und Weise, wie directxmath implementiert wird, ist es in vielen Fällen trivial, directxmath-Typen direkt in standardmäßig vom Compiler unterstützten intrinsie-Anweisungen zu verwenden und directxmath als Fall Back Pfad für Plattformen zu verwenden, die die erweiterte Anweisung nicht unterstützen.

Hier ist beispielsweise ein vereinfachtes Beispiel für die Nutzung der SSE 4,1-Punkt-Produkt-Anweisung angegeben. Beachten Sie, dass Sie den Codepfad explizit schützen müssen, um zu vermeiden, dass zur Laufzeit ungültige Anweisungs Ausnahmen erzeugt werden. Stellen Sie sicher, dass die Codepfade erheblich genug arbeiten, um die zusätzlichen Kosten der Verzweigung, die Komplexität der Verwaltung mehrerer Codepfade usw. zu rechtfertigen.


```
#include <windows.h>
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
   __cpuid( CPUInfo, 0 );

   if ( CPUInfo[0] >= 1 )
   {
       __cpuid(CPUInfo, 1 );
 
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

[Directxmath: SSE, SSE2 und Arm-Neon](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[Directxmath: SSE3 und SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[Directxmath: SSE 4.1 und SSE 4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[Directxmath: AVX](https://walbourn.github.io/directxmath-avx/)  
[Directxmath: F16C und FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[Directxmath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[Directxmath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
