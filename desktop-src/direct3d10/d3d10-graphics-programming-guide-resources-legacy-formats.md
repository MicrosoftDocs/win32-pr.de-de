---
description: In dieser Tabelle werden die Direct3D 9-Formate aufgelistet, die einem Direct3D 10-Format zugeordnet werden können.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Legacy Formate: Zuordnen von Direct3D 9-Formaten zu Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344359"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Legacy Formate: Zuordnen von Direct3D 9-Formaten zu Direct3D 10

In dieser Tabelle werden die Direct3D 9-Formate aufgelistet, die einem Direct3D 10-Format zugeordnet werden können. Die Direct3D 10-Formate unterscheiden sich von den Formaten Direct3D 9, sodass Scheitelpunkt-und Textur Formate zusammengeführt werden können, um Kreuz endische Anwendungen zu ermöglichen.



| Direct3D 9 Textur/Scheitelpunkt/Index Format | Entsprechendes Direct3D 10-Format                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ unbekannt                        | DXGI- \_ Format \_ unbekannt                                                |
| D3DFMT \_ R8G8B8                         | Nicht verfügbar                                                        |
| D3DFMT \_ A8R8G8B8                       | DXGI- \_ Format \_ B8G8R8A8 \_ unorm (DXGI 1,1)                             |
| D3DFMT \_ X8R8G8B8                       | DXGI- \_ Format \_ B8G8R8X8 \_ unorm (DXGI 1,1)                             |
| D3DFMT \_ R5G6B5                         | DXGI- \_ Format \_ B5G6R5 \_ unorm (DXGI 1,2)                               |
| D3DFMT \_ X1R5G5B5                       | Nicht verfügbar                                                        |
| D3DFMT \_ A1R5G5B5                       | DXGI- \_ Format \_ B5G5R5A1 \_ unorm (DXGI 1,2)                             |
| D3DFMT \_ A4R4G4B4                       | DXGI- \_ Format \_ B4G4R4A4 \_ unorm (DXGI 1,2)                             |
| D3DFMT \_ R3G3B2                         | Nicht verfügbar                                                        |
| D3DFMT \_ a8                             | DXGI- \_ Format \_ a8 \_ unorm                                              |
| D3DFMT \_ A8R3G3B2                       | Nicht verfügbar                                                        |
| D3DFMT \_ X4R4G4B4                       | Nicht verfügbar                                                        |
| D3DFMT \_ A2B10G10R10                    | DXGI- \_ Format \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | DXGI- \_ Format \_ R8G8B8A8 \_ unorm-oder DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB |
| D3DFMT \_ X8B8G8R8                       | Nicht verfügbar                                                        |
| D3DFMT \_ G16R16                         | DXGI- \_ Format \_ R16G16 \_ unorm                                          |
| D3DFMT \_ A2R10G10B10                    | Nicht verfügbar                                                        |
| D3DFMT \_ A16B16G16R16                   | DXGI- \_ Format \_ R16G16B16A16 \_ unorm                                    |
| D3DFMT \_ A8P8                           | Nicht verfügbar                                                        |
| D3DFMT \_ P8                             | Nicht verfügbar                                                        |
| D3DFMT \_ L8                             | DXGI- \_ Format \_ R8 \_ unorm ¹                                            |
| D3DFMT \_ A8L8                           | Nicht verfügbar                                                        |
| D3DFMT \_ A4L4                           | Nicht verfügbar                                                        |
| D3DFMT \_ V8U8                           | DXGI- \_ Format \_ R8G8 \_ snorm                                            |
| D3DFMT \_ L6V5U5                         | Nicht verfügbar                                                        |
| D3DFMT \_ X8L8V8U8                       | Nicht verfügbar                                                        |
| D3DFMT \_ Q8W8V8U8                       | DXGI- \_ Format \_ R8G8B8A8 \_ snorm                                        |
| D3DFMT \_ V16U16                         | DXGI- \_ Format \_ R16G16 \_ snorm                                          |
| D3DFMT \_ W11V11U10                      | Nicht verfügbar                                                        |
| D3DFMT \_ A2W10V10U10                    | Nicht verfügbar                                                        |
| D3DFMT \_ UYVY                           | Nicht verfügbar                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | DXGI- \_ Format \_ G8R8 \_ G8B8 \_ unorm ²                                    |
| D3DFMT \_ im YUY2                           | Nicht verfügbar                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm ²                                    |
| D3DFMT \_ DXT1                           | DXGI- \_ Format \_ BC1 \_ unorm-oder DXGI- \_ Format \_ BC1 \_ unorm \_ sRGB           |
| D3DFMT \_ DXT2                           | DXGI- \_ Format \_ BC2 \_ unorm-oder DXGI- \_ Format \_ BC2 \_ unorm \_ sRGB ³         |
| D3DFMT \_ DXT3                           | DXGI- \_ Format \_ BC2 \_ unorm-oder DXGI- \_ Format \_ BC2 \_ unorm \_ sRGB           |
| D3DFMT \_ DXT4                           | DXGI- \_ Format \_ BC3 \_ unorm-oder DXGI- \_ Format \_ BC3 \_ unorm \_ sRGB ³         |
| D3DFMT \_ DXT5                           | DXGI- \_ Format \_ BC3 \_ unorm-oder DXGI- \_ Format \_ BC3 \_ unorm \_ sRGB           |
| D3DFMT \_ D16 und D3DFMT \_ D16 \_ Lockable  | DXGI- \_ Format \_ D16 \_ unorm                                             |
| D3DFMT \_ d32                            | Nicht verfügbar                                                        |
| D3DFMT \_ D15S1                          | Nicht verfügbar                                                        |
| D3DFMT \_ D24S8                          | Nicht verfügbar                                                        |
| D3DFMT \_ D24X8                          | Nicht verfügbar                                                        |
| D3DFMT \_ D24X4S4                        | Nicht verfügbar                                                        |
| D3DFMT \_ D16                            | DXGI- \_ Format \_ D16 \_ unorm                                             |
| D3DFMT \_ D32F \_ Lockable                 | DXGI- \_ Format \_ d32 \_ float                                             |
| D3DFMT \_ D24FS8                         | Nicht verfügbar                                                        |
| D3DFMT \_ S1D15                          | Nicht verfügbar                                                        |
| D3DFMT \_ S8D24                          | DXGI- \_ Format \_ D24 \_ unorm \_ S8 \_ uint                                   |
| D3DFMT \_ X8D24                          | Nicht verfügbar                                                        |
| D3DFMT \_ X4S4D24                        | Nicht verfügbar                                                        |
| D3DFMT \_ L16                            | DXGI- \_ Format \_ R16 \_ unorm ¹                                           |
| D3DFMT \_ INDEX16                        | DXGI- \_ Format \_ R16 \_ uint                                              |
| D3DFMT \_ INDEX32                        | DXGI- \_ Format \_ R32 \_ uint                                              |
| D3DFMT \_ Q16W16V16U16                   | DXGI- \_ Format \_ R16G16B16A16 \_ snorm                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | Nicht verfügbar                                                        |
| D3DFMT \_ R16F                           | DXGI- \_ Format \_ R16 \_ float                                             |
| D3DFMT \_ G16R16F                        | DXGI- \_ Format \_ R16G16 \_ float                                          |
| D3DFMT \_ A16B16G16R16F                  | DXGI- \_ Format \_ R16G16B16A16 \_ float                                    |
| D3DFMT \_ R32F                           | DXGI- \_ Format \_ R32 \_ float                                             |
| D3DFMT \_ G32R32F                        | DXGI- \_ Format \_ R32G32 \_ float                                          |
| D3DFMT \_ A32B32G32R32F                  | DXGI- \_ Format \_ R32G32B32A32 \_ float                                    |
| D3DFMT \_ CxV8U8                         | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ FLOAT1                    | DXGI- \_ Format \_ R32 \_ float                                             |
| D3DDECLTYPE \_ FLOAT2                    | DXGI- \_ Format \_ R32G32 \_ float                                          |
| D3DDECLTYPE \_ FLOAT3                    | DXGI- \_ Format \_ R32G32B32 \_ float                                       |
| D3DDECLTYPE \_ float4                    | DXGI- \_ Format \_ R32G32B32A32 \_ float                                    |
| D3DDECLTYPED3DCOLOR                    | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ UBYTE4                    | DXGI- \_ Format \_ R8G8B8A8 \_ uint ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | DXGI- \_ Format \_ R16G16 \_ Sint                                           |
| D3DDECLTYPE \_ SHORT4                    | DXGI- \_ Format \_ R16G16B16A16 \_ Sint                                     |
| D3DDECLTYPE \_ UBYTE4N                   | DXGI- \_ Format \_ R8G8B8A8 \_ unorm                                        |
| D3DDECLTYPE \_ SHORT2N                   | DXGI- \_ Format \_ R16G16 \_ snorm                                          |
| D3DDECLTYPE \_ SHORT4N                   | DXGI- \_ Format \_ R16G16B16A16 \_ snorm                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI- \_ Format \_ R16G16 \_ unorm                                          |
| D3DDECLTYPE \_ USHORT4N                  | DXGI- \_ Format \_ R16G16B16A16 \_ unorm                                    |
| D3DDECLTYPE \_ UDEC3                     | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ DEC3N                     | Nicht verfügbar                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | DXGI- \_ Format \_ R16G16 \_ float                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | DXGI- \_ Format \_ R16G16B16A16 \_ float                                    |



 

1.  Verwenden Sie. r Swizzle in einem Shader, um rot zu anderen Komponenten zu duplizieren, um das Direct3D 9-Verhalten zu erhalten.
2.  In Direct3D 9 wurden die Daten von 255.0 f zentral hochskaliert, was stattdessen im Shader-Code erfolgen kann.
3.  DXT2 und DXT3 sind aus API-Sicht identisch. DXT4 und DXT5 sind aus API-Sicht identisch. Der einzige Unterschied war ein prämultipliziertes Alpha, das von einer Anwendung nachverfolgt werden kann und kein separates Format benötigt.
4.  Ein Shader ruft uint-Werte ab, aber wenn Direct3D 9-Format ganzzahlige Gleit Komma Zahlen (0,0 f, 1.0 f... 255. f) erforderlich, uint kann in einen Shader in float32 konvertiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



