---
description: Definiert die Textur Filtermodi für eine Textur Phase.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: D3DTEXTUREFILTERTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366626"
---
# <a name="d3dtexturefiltertype-enumeration"></a>D3DTEXTUREFILTERTYPE-Enumeration

Definiert die Textur Filtermodi für eine Textur Phase.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ None**
</dt> <dd>

Deaktiviert bei Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md)Mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ Punkt**
</dt> <dd>

Gibt bei Verwendung mit [**D3DSAMP \_ MagFilter**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MinFilter**](./d3dsamplerstatetype.md)an, dass die Punkt Filterung als Textur Vergrößerung bzw. minierungs Filter verwendet werden soll. Bei Verwendung mit **D3DSAMP \_ MipFilter** aktiviert Mipmapping und gibt an, dass der Raster die Farbe aus dem textsder nächstgelegenen MIP-Ebene auswählt.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ linear**
</dt> <dd>

Gibt bei Verwendung mit [**D3DSAMP \_ MagFilter**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MinFilter**](./d3dsamplerstatetype.md)an, dass die lineare Filterung als Textur Vergrößerung bzw. minierungs Filter verwendet werden soll. Bei Verwendung mit **D3DSAMP \_ MipFilter** aktiviert Mipmapping und die drei lineare Filterung. es gibt an, dass der Raster zwischen den beiden nächsten MIP-Ebenen interpoliert.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotrope**
</dt> <dd>

Gibt bei Verwendung mit [**D3DSAMP \_ MagFilter**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MinFilter**](./d3dsamplerstatetype.md)an, dass die anisotrope Textur Filterung als Textur Vergrößerung bzw. minierungs Filter verwendet wird. Kompensiert die Verzerrung, die durch den Unterschied in der Spitze zwischen dem Textur Polygon und der Ebene des Bildschirms verursacht wird. Die Verwendung mit **D3DSAMP \_ MipFilter** ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ pyramidalquad**
</dt> <dd>

Ein vier-Stichproben-Zelt Filter, der als Textur Vergrößerungs-oder minierungs Filter verwendet wird. Die Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md) ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ gausianquad**
</dt> <dd>

Ein Gaußscher vier-Stichproben Filter, der als Textur Vergrößerungs-oder minierungs Filter verwendet wird. Die Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md) ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ -Konstante**
</dt> <dd>

Der Konfigurations Filter für monochrome Texturen. Siehe [D3DFMT \_ a1](d3dformat.md).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |



 

Die Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md) ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

D3DTEXTUREFILTERTYPE wird von [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) zusammen mit [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) verwendet, um die Textur Filtermodi für eine Textur Phase zu definieren.

Um zu überprüfen, ob ein Format andere Textur Filtertypen als D3DTEXF Point unterstützt \_ (was immer unterstützt wird), wenden Sie [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit dem D3DUSAGE- \_ Abfrage \_ Filter an.

Legen Sie den Vergrößerungs Filter einer Textur Phase fest, indem Sie [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MagFilter-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.

Legen Sie den Minimierung Filter für die Textur Phase fest, indem Sie [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MinFilter-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.

Legen Sie den Textur Filter so fest, dass er zwischen-MipMap-Ebenen verwendet wird, indem Sie [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MipFilter-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.

Nicht alle gültigen Filtermodi für ein Gerät gelten für volumenmaps. Im Allgemeinen werden D3DTEXF \_ Punkt-und D3DTEXF- \_ lineare Vergrößerungs Filter für Volume Maps unterstützt. Wenn D3DPTEXTURECAPS \_ mipvolumemap festgelegt ist, werden die \_ Filter D3DTEXF Point MipMap und D3DTEXF \_ Point und D3DTEXF \_ linear Minimierung für Volume Maps unterstützt. Das Gerät unterstützt den linearen D3DTEXF- \_ Mipmap-Filter für Volume Maps möglicherweise nicht. Geräte, die die anisotrope Filterung für 2D-Zuordnungen unterstützen, unterstützen nicht notwendigerweise die anisotrope Filterung für Volume Maps. Anwendungen, die die anisotrope Filterung aktivieren, erhalten jedoch die beste verfügbare Filterung (wahrscheinlich linear), wenn die anisotrope Filterung nicht unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh:: getverdräneparam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh:: setverdräneparam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
