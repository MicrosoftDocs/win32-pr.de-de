---
description: Legt einen Albedo-Wert für jedes Texel fest und überschreiben vorherige Albedo-Werte.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: ID3DXPRTEngine::SetPerTexelAlbedo-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6f17e4d3d3922c8e9d54b880f969c14b781935da34eab29b4ec1eb5d4d5421c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985550"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>ID3DXPRTEngine::SetPerTexelAlbedo-Methode

Legt einen Albedo-Wert für jedes Texel fest und überschreiben vorherige Albedo-Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlbedoTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9-Texturobjekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) in dem Albedo-Werte gespeichert werden.

</dd> <dt>

*NumChannels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der farblich zu setzenden Kanäle. Legen Sie auf 1 fest, um graue Materialien anzugeben (R = G = B), oder 3, um Farbeffekte zu aktivieren.

</dd> <dt>

*pGH* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Optionaler Zeiger auf ein [**ID3DXTextureGutterHelper-Objekt.**](id3dxtexturegutterhelper.md) Wenn kein Hilfsobjekt angegeben wird, wird intern ein Hilfsobjekt für den Textur-Bundschreck erstellt und zerstört.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einen der folgenden Werte haben: \_ D3DERR INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASIERERDRAWING, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
