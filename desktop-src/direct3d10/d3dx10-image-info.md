---
description: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO-Struktur (d3dx10. h)
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
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354437"
---
# <a name="d3dx10_image_info-structure"></a>D3dx10 \_ Image- \_ Informationsstruktur

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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tiefe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**ArraySize**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des Textur Arrays. *ArraySize* ist 1 für ein einzelnes Image.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von MipMap-Ebenen im ursprünglichen Bild.

</dd> <dt>

**Fehlflags**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Verschiedene Ressourcen Eigenschaften (siehe [**d3d10 \_ Resource \_ misc- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Ein Wert aus dem enumerierten [**DXGI- \_ Formattyp**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , der die Daten im ursprünglichen Bild am ehesten beschreibt.

</dd> <dt>

**Resourcedimension**
</dt> <dd>

Type: **[ **d3d10- \_ Ressourcen \_ Dimension**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Stellt den Typ der Textur dar, die in der Datei gespeichert ist. Siehe [**d3d10 \_ Resource- \_ Dimension**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**Imagefileformat**
</dt> <dd>

Type: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**

</dd> <dd>

Stellt das Format der Bilddatei dar. Siehe [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
