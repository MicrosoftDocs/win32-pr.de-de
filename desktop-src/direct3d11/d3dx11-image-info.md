---
title: D3DX11_IMAGE_INFO-Struktur (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. | D3DX11_IMAGE_INFO-Struktur (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO Struktur Direct3D 11
- LPD3DX11_IMAGE_INFO Struktur Zeiger Direct3D 11
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
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982557"
---
# <a name="d3dx11_image_info-structure"></a>Bibliothek d3dx11 \_ Image- \_ Informationsstruktur

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. Der Wert Bibliothek d3dx11 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.

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

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Ziel Breite der Textur. Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um dieser Ziel Breite gerecht zu werden.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zielhöhe der Textur. Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um an diese Zielhöhe angepasst zu werden.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Tiefe der Textur. Dies gilt nur für Volumentexturen.

</dd> <dt>

**ArraySize**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Elemente im Array.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die maximale Anzahl von MipMap-Ebenen in der Textur. Weitere Informationen finden Sie in den Hinweisen unter [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Die Verwendung von 0 oder Bibliothek d3dx11 \_ default bewirkt, dass eine vollständige MipMap-Kette erstellt wird.

</dd> <dt>

**Fehlflags**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Verschiedene Ressourcen Eigenschaften, die mit [**dem \_ Flag "D3D11 Resource \_ misc \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) " angegeben werden.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Eine [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , die das Format angibt, in dem sich die Textur befindet, nachdem Sie geladen wurde.

</dd> <dt>

**Resourcedimension**
</dt> <dd>

Type: **[ **D3D11- \_ Ressourcen \_ Dimension**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Ein [**D3D11- \_ Ressourcen \_ Dimensions**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) Wert, der den Typ der Ressource identifiziert.

</dd> <dt>

**Imagefileformat**
</dt> <dd>

Type: **[ **Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**

</dd> <dd>

Ein [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md) -Wert, der das Bildformat angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von Methoden wie z. b. [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)oder [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

