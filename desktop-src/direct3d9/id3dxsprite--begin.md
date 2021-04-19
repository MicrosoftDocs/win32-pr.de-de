---
description: Bereitet ein Gerät zum Zeichnen von Sprites vor.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite:: Begin-Methode (D3dx9core. h)'
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
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366658"
---
# <a name="id3dxspritebegin-method"></a>ID3DXSprite:: Begin-Methode

Bereitet ein Gerät zum Zeichnen von Sprites vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus null oder mehr Flags, die Sprite-Renderingoptionen beschreiben. Für diese Methode sind die gültigen Flags:

-   D3DXSPRITE \_ AlphaBlend
-   D3DXSPRITE- \_ \_ Billboard
-   D3DXSPRITE \_ donotmodify \_ renderstate
-   D3DXSPRITE \_ DoNotSaveState
-   D3DXSPRITE \_ ObjectSpace
-   D3DXSPRITE \_ \_ Sortier \_ Tiefe zurück \_ wechseln
-   D3DXSPRITE- \_ \_ \_ Detail- \_ frontbackback
-   D3DXSPRITE \_ \_ Sortier \_ Textur

Eine Beschreibung der Flags und Informationen zum Steuern der Transformation für Gerätestatus Erfassung und Geräte Ansicht finden Sie unter [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DERR \_ ouesfvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode muss innerhalb von [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) aufgerufen werden. . . [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) -Sequenz. **ID3DXSprite:: begin** kann nicht als Ersatz für **IDirect3DDevice9:: BeginScene** oder [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md)verwendet werden.

Mit dieser Methode werden die folgenden Zustände auf dem Gerät festgelegt.

Rendering-Zustände:



| Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Wert                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ AlphaBlendEnable                                       | TRUE                                                                                                              |
| D3DRS \_ alphafunc                                              | D3DCMP \_ größer                                                                                                   |
| D3DRS \_ Alpha Aref                                               | 0x00                                                                                                              |
| D3DRS \_ Alpha atestenable                                        | Alpha acmpcaps                                                                                                      |
| D3DRS \_ blendop                                                | D3DBLENDOP \_ Hinzufügen                                                                                                   |
| D3DRS \_ Clipping                                               | TRUE                                                                                                              |
| D3DRS \_ clipplaneenable                                        | false                                                                                                             |
| D3DRS \_ colorschreiteenable                                       | D3DCOLORWRITEENABLE \_ alpha \| D3DCOLORWRITEENABLE \_ blau \| D3DCOLORWRITEENABLE \_ grün \| D3DCOLORWRITEENABLE \_ rot |
| D3DRS \_ CullMode                                               | D3DCULL \_ None                                                                                                     |
| D3DRS \_ destblend                                              | D3DBLEND- \_ invsrcalpha                                                                                             |
| D3DRS \_ DiffuseMaterialSource                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ enableadaptivetess                             | false                                                                                                             |
| D3DRS \_ FillMode                                               | D3DFILL \_ Solid                                                                                                    |
| D3DRS \_ fogenable                                              | false                                                                                                             |
| D3DRS \_ indexedvertexblendenable                               | false                                                                                                             |
| D3DRS- \_ Beleuchtung                                               | false                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | false                                                                                                             |
| D3DRS \_ separatealphablendenable                               | false                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE- \_ Gouraud                                                                                                 |
| D3DRS \_ specularenable                                         | false                                                                                                             |
| D3DRS \_ srcblend                                               | D3DBLEND \_ srcalpha                                                                                                |
| D3DRS \_ srgbschreiteenable                                        | false                                                                                                             |
| D3DRS \_ Schablone                                          | false                                                                                                             |
| D3DRS \_ vertexblend                                            | false                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Textur Stufen Zustände:



| Phasen Bezeichner | Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Wert            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | D3DTA- \_ Textur   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ diffuses   |
| 0                | D3DTSS \_ alphaop                                                           | D3DTOP \_ modulate |
| 0                | D3DTSS \_ COLORARG1                                                         | D3DTA- \_ Textur   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ diffuses   |
| 0                | D3DTSS \_ colorop                                                           | D3DTOP \_ modulate |
| 0                | D3DTSS \_ texcoordindex                                                     | 0                |
| 0                | D3DTSS \_ texturetransformflags                                             | D3DTTFF \_ Deaktivieren |
| 1                | D3DTSS \_ alphaop                                                           | D3DTOP \_ Deaktivieren  |
| 1                | D3DTSS \_ colorop                                                           | D3DTOP \_ Deaktivieren  |



 

Samplerzustände:



| Sampler-Phasen Index | Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Wert                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ adressu                                               | D3DTADDRESS- \_ Klammer                                                                                             |
| 0                   | D3DSAMP \_ adressssv                                               | D3DTADDRESS- \_ Klammer                                                                                             |
| 0                   | D3DSAMP- \_ MagFilter                                              | D3DTEXF \_ anisotrope, wenn TextureFilterCaps D3DPTFILTERCAPS \_ magfanisotrope enthält; andernfalls D3DTEXF \_ linear |
| 0                   | D3DSAMP \_ MaxMipLevel                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MaxAnisotropy                                          | Maxanisotropie                                                                                                  |
| 0                   | D3DSAMP \_ MinFilter                                              | D3DTEXF \_ anisotrope, wenn TextureFilterCaps D3DPTFILTERCAPS \_ minfanisotrope enthält; andernfalls D3DTEXF \_ linear |
| 0                   | D3DSAMP \_ MipFilter                                              | D3DTEXF \_ linear, wenn TextureFilterCaps D3DPTFILTERCAPS \_ mipflinear enthält; andernfalls D3DTEXF \_ Point            |
| 0                   | D3DSAMP \_ mipmaplodbias                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ srgbtexture                                            | 0                                                                                                              |



 

> [!Note]  
> Diese Methode deaktiviert N-Patches.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
