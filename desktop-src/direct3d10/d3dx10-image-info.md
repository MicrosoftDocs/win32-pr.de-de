---
description: 'D3DX10_IMAGE_INFO-Struktur: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.'
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO-Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: bf3aa2eeb3e908a76e05588940927fff53dd1583c937d95a1c862f6021bd630f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989520"
---
# <a name="d3dx10_image_info-structure"></a>D3DX10 \_ IMAGE \_ INFO-Struktur

Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tiefe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**ArraySize**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des Texturarrays. *ArraySize* ist für ein einzelnes Bild 1.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Mipmapebenen im ursprünglichen Bild.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Verschiedene Ressourceneigenschaften (siehe [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Ein Wert aus dem enumerierten [**DXGI \_ FORMAT-Typ,**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) der die Daten im ursprünglichen Bild am genauesten beschreibt.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Typ: **[ **D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Stellt den Typ der in der Datei gespeicherten Textur dar. Weitere Informationen finden Sie unter [**D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Typ: **[ **D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md)**

</dd> <dd>

Stellt das Format der Bilddatei dar. Weitere Informationen finden Sie unter [**D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
