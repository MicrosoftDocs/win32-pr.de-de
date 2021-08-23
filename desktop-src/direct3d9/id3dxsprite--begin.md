---
description: Bereitet ein Gerät für das Zeichnen von Sprites vor.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: ID3DXSprite::Begin-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94d3ee659937508f52e38513006701494a01ed4ff95fe6c75c56bd9638137160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277830"
---
# <a name="id3dxspritebegin-method"></a>ID3DXSprite::Begin-Methode

Bereitet ein Gerät für das Zeichnen von Sprites vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von null oder mehr Flags, die Sprite-Renderingoptionen beschreiben. Für diese Methode sind die folgenden Flags gültig:

-   D3DXSPRITE \_ ALPHABLEND
-   D3DXSPRITE \_ \_ PLAYLIST
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   D3DXSPRITE \_ DONOTSAVESTATE
-   D3DXSPRITE \_ OBJECTSPACE
-   D3DXSPRITE \_ \_ SORT \_ DEPTH \_ BACKTOFRONT
-   D3DXSPRITE \_ \_ SORT \_ DEPTH \_ FRONTTOBACK
-   D3DXSPRITE \_ \_ SORT \_ TEXTURE

Eine Beschreibung der Flags und Informationen zum Steuern der Gerätestatuserfassung und geräteansichtstransformationen finden Sie unter [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode muss innerhalb einer [**IDirect3DDevice9::BeginScene aufgerufen werden.**](/windows/desktop/api) . . [**IDirect3DDevice9::EndScene-Sequenz.**](/windows/desktop/api) **ID3DXSprite::Begin** kann nicht als Ersatz für **IDirect3DDevice9::BeginScene** oder [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md)verwendet werden.

Mit dieser Methode werden die folgenden Zustände auf dem Gerät festgelegt.

Renderzustände:



| Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Wert                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | TRUE                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ GREATER                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| D3DRS \_ BLENDOP                                                | D3DBLENDOP \_ ADD                                                                                                   |
| D3DRS \_ CLIPPING                                               | TRUE                                                                                                              |
| D3DRS \_ CLIPPLANEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ ALPHA \| D3DCOLORWRITEENABLE \_ BLUE \| D3DCOLORWRITEENABLE \_ GREEN \| D3DCOLORWRITEENABLE \_ RED |
| D3DRS \_ CULLMODE                                               | D3DCULL \_ NONE                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DIFFUSEMATERIALSOURCE                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | FALSE                                                                                                             |
| D3DRS \_ FILLMODE                                               | D3DFILL \_ SOLID                                                                                                    |
| D3DRS \_ – WARTEBAR                                              | FALSE                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | FALSE                                                                                                             |
| D3DRS-BELEUCHTUNG \_                                               | FALSE                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE \_ GOURAUD                                                                                                 |
| D3DRS \_ SPECULARENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | FALSE                                                                                                             |
| D3DRS \_ VERTEXBLEND                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Texturphasenzustände:



| Phasenbezeichner | Typ ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Wert            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | D3DTA-TEXTUR \_   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ DIFFUSE   |
| 0                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ MODULATE |
| 0                | D3DTSS \_ COLORARG1                                                         | D3DTA-TEXTUR \_   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ DIFFUSE   |
| 0                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ MODULATE |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | D3DTSS \_ TEXTURETRANSFORMFLAGS                                             | D3DTTFF \_ DISABLE |
| 1                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ DISABLE  |
| 1                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ DISABLE  |



 

Samplerzustände:



| Sampler-Phasenindex | Typ ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Wert                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ ADDRESSU                                               | D3DTADDRESS-KLAMMER \_                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | D3DTADDRESS-KLAMMER \_                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | D3DTEXF \_ ANISOTROP, wenn TextureFilterCaps D3DPTFILTERCAPS \_ MAGFANISOTROPE enthält, andernfalls D3DTEXF \_ LINEAR |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropie                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | D3DTEXF \_ ANISOTROP, wenn TextureFilterCaps D3DPTFILTERCAPS \_ MINFANISOTROPE enthält, andernfalls D3DTEXF \_ LINEAR |
| 0                   | D3DSAMP \_ MIPFILTER                                              | D3DTEXF \_ LINEAR, wenn TextureFilterCaps D3DPTFILTERCAPS \_ MIPFLINEAR enthält, andernfalls D3DTEXF \_ POINT            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> Diese Methode deaktiviert N-Patches.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
