---
description: Legt einen Albedo-Wert für jeden Texttyp fest, wobei vorherige Albedo-Werte überschrieben werden.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'ID3DXPRTEngine:: setpertexelalbedo-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394166"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>ID3DXPRTEngine:: setpertexelalbedo-Methode

Legt einen Albedo-Wert für jeden Texttyp fest, wobei vorherige Albedo-Werte überschrieben werden.

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

*palbedotexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt, in dem Albedo-Werte gespeichert werden.

</dd> <dt>

*Numchannels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der festzulegenden Farbkanäle. Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.

</dd> <dt>

*pgh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Optionaler Zeiger auf ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt. Wenn nicht angegeben, wird ein Textur-bundbundhilfsobjekt intern erstellt und zerstört.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DERR \_ NOTAVAILABLED3DERR \_ oudefvideomemory, D3DERR \_ wasstilldrawing, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
