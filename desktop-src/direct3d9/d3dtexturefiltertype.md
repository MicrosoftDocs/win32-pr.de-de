---
description: Definiert Texturfilterungsmodi für eine Texturphase.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: D3DTEXTUREFILTERTYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: a9a55632ee1f1b8f2e40b1be1272411c7c24b3b18c576563ff9c0de7c79bc413
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069370"
---
# <a name="d3dtexturefiltertype-enumeration"></a>D3DTEXTUREFILTERTYPE-Enumeration

Definiert Texturfilterungsmodi für eine Texturphase.

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

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**
</dt> <dd>

Bei Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md)deaktiviert mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ POINT**
</dt> <dd>

Gibt bei Verwendung mit [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)an, dass die Punktfilterung als Texturvergrößerungs- bzw. Vergrößerungsfilter verwendet werden soll. Bei Verwendung mit **D3DSAMP \_ MIPFILTER** aktiviert mipmapping und gibt an, dass der Rasterizer die Farbe aus dem Texel der nächsten Mipebene ausgibt.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ LINEAR**
</dt> <dd>

Gibt bei Verwendung mit [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)an, dass die lineare Filterung als Texturvergrößerungs- bzw. Vergrößerungsfilter verwendet werden soll. Bei Verwendung mit **D3DSAMP \_ MIPFILTER** ermöglicht mipmapping und trilineare Filterung. Es gibt an, dass der Rasterizer zwischen den beiden nächsten Mip-Ebenen interpoliert.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROP**
</dt> <dd>

Bei Verwendung mit [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)gibt an, dass die Anisotrope Texturfilterung als Texturvergrößerungs- bzw. Vergrößerungsfilter verwendet wird. Kompensiert die Verzerrung, die durch den Unterschied im Winkel zwischen dem Texturpolygon und der Bildschirmebene verursacht wird. Die Verwendung mit **D3DSAMP \_ MIPFILTER** ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Ein 4-Stichproben-Festzeltfilter, der als Texturvergrößerungs- oder Vergrößerungsfilter verwendet wird. Die Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

Ein 4-Stichproben-Filter, der als Texturvergrößerungs- oder Vergrößerungsfilter verwendet wird. Die Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

Konvolutionsfilter für monocolore Texturen. Weitere Informationen finden Sie unter [D3DFMT \_ A1.](d3dformat.md)

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- Dieses Flag ist nur in Direct3D 9Ex verfügbar.



 

Die Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) ist nicht definiert.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DTEXTUREFILTERTYPE wird von [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) zusammen mit [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) verwendet, um Texturfilterungsmodi für eine Texturphase zu definieren.

Um zu überprüfen, ob ein Format andere Texturfiltertypen als D3DTEXF POINT unterstützt \_ (was immer unterstützt wird), rufen Sie [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ QUERY FILTER \_ auf.

Legen Sie den Vergrößerungsfilter einer Texturphase fest, indem [**Sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MAGFILTER-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.

Legen Sie den Qualifizierungsfilter einer Texturstufe fest, indem [**Sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MINFILTER-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.

Legen Sie den Texturfilter für die Verwendung zwischen MIPMAP-Ebenen fest, indem [**Sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MIPFILTER-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.

Nicht alle gültigen Filtermodi für ein Gerät gelten für Volumezuordnungen. Im Allgemeinen werden D3DTEXF \_ POINT- und D3DTEXF \_ LINEAR-Vergrößerungsfilter für Volumezuordnungen unterstützt. Wenn D3DPTEXTURECAPS \_ MIPVOLUMEMAP festgelegt ist, werden die Mipmapfilter D3DTEXF POINT und die \_ Filter D3DTEXF \_ POINT und D3DTEXF \_ LINEAR minification für Volumezuordnungen unterstützt. Das Gerät unterstützt möglicherweise den D3DTEXF \_ LINEAR-Mipmapfilter für Volumezuordnungen. Geräte, die die Anisotrope Filterung für 2D-Karten unterstützen, unterstützen nicht unbedingt die Anisotrope Filterung für Volumezuordnungen. Anwendungen, die die Anisotrope Filterung aktivieren, erhalten jedoch die beste verfügbare Filterung (wahrscheinlich linear), wenn die Anisotrope Filterung nicht unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
