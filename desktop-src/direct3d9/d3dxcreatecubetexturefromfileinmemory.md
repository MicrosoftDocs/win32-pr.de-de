---
description: Erstellt eine Cubetextur aus einer Datei im Arbeitsspeicher.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: D3DXCreateCubeTextureFromFileInMemory-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c39e3aa96445ddfd6e2aee9df90c16bf52aee6f70759eb310288276ff8b9531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631550"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a>D3DXCreateCubeTextureFromFileInMemory-Funktion

Erstellt eine Cubetextur aus einer Datei im Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Cubetextur zugeordnet werden soll.

</dd> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Datei im Arbeitsspeicher, aus der die Cubemap erstellt werden soll. Siehe Hinweise.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Größe der Datei im Arbeitsspeicher in Bytes.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) die das erstellte Cubetexturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Die Funktion entspricht D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL,** ppCubeTexture).

Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicherklasse platziert wird, die von D3DPOOL MANAGED bezeichnet \_ wird. Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicherklasse platziert, die durch D3DPOOL DEFAULT bezeichnet \_ wird.

Diese Methode ist für das Laden von Bilddateien konzipiert, die als RT RCDATA gespeichert sind. Dabei handelt es sich um eine anwendungsdefinierte \_ Ressource (Rohdaten). Andernfalls kann diese Methode nicht verwendet werden.

Die Filterung wird automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde. Die Filterung entspricht D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

**D3DXCreateCubeTextureFromFileInMemory** verwendet das DirectDraw-Oberflächendateiformat (DDS). Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine Cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern. Sie können sich Dxtex.exe DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
