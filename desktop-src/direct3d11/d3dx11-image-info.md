---
title: D3DX11_IMAGE_INFO -Struktur (D3DX11tex.h)
description: 'Hinweis: Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Stellen Sie optional Informationen für Texturlader-APIs zur Verfügung, um zu steuern, wie Texturen geladen werden. | D3DX11_IMAGE_INFO -Struktur (D3DX11tex.h)'
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO-Struktur Direct3D 11
- LPD3DX11_IMAGE_INFO Strukturzeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64366755e9bb9398e8107d931ee5425d2fcee78fdd9d03487b9533270cc17c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536867"
---
# <a name="d3dx11_image_info-structure"></a>D3DX11 \_ IMAGE \_ INFO-Struktur

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Stellen Sie optional Informationen für Texturlader-APIs zur Verfügung, um zu steuern, wie Texturen geladen werden. Der Wert D3DX11 DEFAULT für einen dieser Parameter führt dazu, dass D3DX automatisch den Wert \_ aus der Quelldatei verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zielbreite der Textur. Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur hoch- oder herunterskaliert, um diese Zielbreite zu erreichen.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zielhöhe der Textur. Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur hoch- oder herunterskaliert, um diese Zielhöhe zu erreichen.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Tiefe der Textur. Dies gilt nur für Volumetexturen.

</dd> <dt>

**ArraySize**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Elemente im Array.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die maximale Anzahl von Mipmapebenen in der Textur. Weitere Informationen finden Sie in den Anmerkungen unter [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Wenn Sie 0 oder D3DX11 DEFAULT verwenden, wird \_ eine vollständige Mipmapkette erstellt.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Verschiedene Ressourceneigenschaften, die mit einem [**FLAG D3D11 \_ RESOURCE \_ MISC FLAG \_ angegeben**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) werden.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Eine [**DXGI \_ FORMAT-Enumeration,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) die das Format an gibt, in dem sich die Textur befindet, nachdem sie geladen wurde.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Typ: **[ **D3D11 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Ein [**D3D11 \_ RESOURCE \_ DIMENSION-Wert,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) der den Typ der Ressource identifiziert.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md)**

</dd> <dd>

Ein [**D3DX11 \_ IMAGE FILE \_ \_ FORMAT-Wert,**](d3dx11-image-file-format.md) der das Bildformat identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von Methoden wie [**D3DX11GetImageInfoFromFile,**](d3dx11getimageinfofromfile.md) [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)oder [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[D3DX-Strukturen](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

