---
description: In dieser Tabelle sind die Direct3D 9-Formate aufgeführt, die einem Direct3D 10-Format zugeordnet werden können.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Legacyformate: Zuordnen von Direct3D 9-Formaten zu Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40a437ef42b4ce24b468c39d169b39db7fb9cb7951c825da38bb63f85b9dba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895300"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Legacyformate: Zuordnen von Direct3D 9-Formaten zu Direct3D 10

In dieser Tabelle sind die Direct3D 9-Formate aufgeführt, die einem Direct3D 10-Format zugeordnet werden können. Die Direct3D 10-Formate unterscheiden sich von den Direct3D 9-Formaten, sodass Scheitelpunkt- und Texturformate zusammengeführt werden können, um Cross-Endian-Anwendungen zu ermöglichen.



| Direct3D 9 Texture/Vertex/Index Format | Entsprechendes Direct3D 10-Format                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                        | \_DXGI-FORMAT \_ UNBEKANNT                                                |
| D3DFMT \_ R8G8B8                         | Nicht verfügbar                                                        |
| D3DFMT \_ A8R8G8B8                       | \_DXGI-FORMAT \_ B8G8R8A8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ X8R8G8B8                       | DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ R5G6B5                         | \_DXGI-FORMAT \_ B5G6R5 \_ UNORM (DXGI 1.2)                               |
| D3DFMT \_ X1R5G5B5                       | Nicht verfügbar                                                        |
| D3DFMT \_ A1R5G5B5                       | \_DXGI-FORMAT \_ B5G5R5A1 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ A4R4G4B4                       | \_DXGI-FORMAT \_ B4G4R4A4 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ R3G3B2                         | Nicht verfügbar                                                        |
| D3DFMT \_ A8                             | \_DXGI-FORMAT \_ A8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | Nicht verfügbar                                                        |
| D3DFMT \_ X4R4G4B4                       | Nicht verfügbar                                                        |
| D3DFMT \_ A2B10G10R10                    | \_DXGI-FORMAT \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM oder DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB |
| D3DFMT \_ X8B8G8R8                       | Nicht verfügbar                                                        |
| D3DFMT \_ G16R16                         | \_DXGI-FORMAT \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | Nicht verfügbar                                                        |
| D3DFMT \_ A16B16G16R16                   | \_DXGI-FORMAT \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | Nicht verfügbar                                                        |
| D3DFMT \_ P8                             | Nicht verfügbar                                                        |
| D3DFMT \_ L8                             | DXGI \_ FORMAT \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | Nicht verfügbar                                                        |
| D3DFMT \_ A4L4                           | Nicht verfügbar                                                        |
| D3DFMT \_ V8U8                           | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | Nicht verfügbar                                                        |
| D3DFMT \_ X8L8V8U8                       | Nicht verfügbar                                                        |
| D3DFMT \_ Q8W8V8U8                       | DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | \_DXGI-FORMAT \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | Nicht verfügbar                                                        |
| D3DFMT \_ A2W10V10U10                    | Nicht verfügbar                                                        |
| D3DFMT \_ UYVY                           | Nicht verfügbar                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | \_DXGI-FORMAT \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | Nicht verfügbar                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | \_DXGI-FORMAT \_ R8G8 \_ B8G8 \_ UNORM zep                                    |
| D3DFMT \_ DXT1                           | DXGI \_ FORMAT \_ BC1 \_ UNORM oder DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT2                           | DXGI \_ FORMAT \_ BC2 \_ UNORM oder DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB gis         |
| D3DFMT \_ DXT3                           | DXGI \_ FORMAT \_ BC2 \_ UNORM oder DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT4                           | DXGI \_ FORMAT \_ BC3 \_ UNORM oder DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB gb         |
| D3DFMT \_ DXT5                           | DXGI \_ FORMAT \_ BC3 \_ UNORM oder DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB           |
| D3DFMT \_ D16 und D3DFMT \_ D16 \_ LOCKABLE  | DXGI \_ FORMAT \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | Nicht verfügbar                                                        |
| D3DFMT \_ D15S1                          | Nicht verfügbar                                                        |
| D3DFMT \_ D24S8                          | Nicht verfügbar                                                        |
| D3DFMT \_ D24X8                          | Nicht verfügbar                                                        |
| D3DFMT \_ D24X4S4                        | Nicht verfügbar                                                        |
| D3DFMT \_ D16                            | DXGI \_ FORMAT \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ LOCKABLE                 | DXGI \_ FORMAT \_ D32 \_ FLOAT                                             |
| D3DFMT \_ D24FS8                         | Nicht verfügbar                                                        |
| D3DFMT \_ S1D15                          | Nicht verfügbar                                                        |
| D3DFMT \_ S8D24                          | DXGI \_ FORMAT \_ D24 \_ UNORM \_ S8 \_ UINT                                   |
| D3DFMT \_ X8D24                          | Nicht verfügbar                                                        |
| D3DFMT \_ X4S4D24                        | Nicht verfügbar                                                        |
| D3DFMT \_ L16                            | DXGI \_ FORMAT \_ R16 \_ UNORM                                           |
| D3DFMT \_ INDEX16                        | DXGI \_ FORMAT \_ R16 \_ UINT                                              |
| D3DFMT \_ INDEX32                        | DXGI \_ FORMAT \_ R32 \_ UINT                                              |
| D3DFMT \_ Q16W16V16U16                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | Nicht verfügbar                                                        |
| D3DFMT \_ R16F                           | DXGI \_ FORMAT \_ R16 \_ FLOAT                                             |
| D3DFMT \_ G16R16F                        | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                          |
| D3DFMT \_ A16B16G16R16F                  | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                    |
| D3DFMT \_ R32F                           | DXGI \_ FORMAT \_ R32 \_ FLOAT                                             |
| D3DFMT \_ G32R32F                        | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                          |
| D3DFMT \_ A32B32G32R32F                  | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                    |
| D3DFMT \_ CxV8U8                         | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ FLOAT1                    | DXGI \_ FORMAT \_ R32 \_ FLOAT                                             |
| D3DDECLTYPE \_ FLOAT2                    | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT3                    | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                       |
| D3DDECLTYPE \_ FLOAT4                    | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                    |
| D3DDECLTYPED3DCOLOR                    | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ UBYTE4                    | DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | DXGI \_ FORMAT \_ R16G16 \_ SINT                                           |
| D3DDECLTYPE \_ SHORT4                    | DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT                                     |
| D3DDECLTYPE \_ UBYTE4N                   | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ DEC3N                     | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                    |



 

1.  Verwenden Sie .r swizzle in einem Shader, um Rot auf andere Komponenten zu duplizieren, um das Direct3D 9-Verhalten zu erhalten.
2.  In Direct3D 9 wurden die Daten um 255,0f hochskaliert, was stattdessen im Shadercode erfolgen kann.
3.  DXT2 und DXT3 sind aus API-Sicht identisch. DXT4 und DXT5 sind aus API-Sicht identisch. Der einzige Unterschied war das prämultipliierte Alpha, das von einer Anwendung nachverfolgt werden kann und kein separates Format benötigt.
4.  Ein Shader ruft UINT-Werte ab, aber wenn integrale Gleitkommawerte im Direct3D 9-Stil (0,0f, 1,0f... 255.f) erforderlich, UINT kann in einem Shader in float32 konvertiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



