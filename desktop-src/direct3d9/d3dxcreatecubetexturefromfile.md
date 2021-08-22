---
description: Erstellt eine Cubetextur aus einer Datei.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: D3DXCreateCubeTextureFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e25b6692fc22eed1695b1d60b019a595826de15af87e4ca70f2610a621abc532
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279890"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a>D3DXCreateCubeTextureFromFile-Funktion

Erstellt eine Cubetextur aus einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
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

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) die das erstellte Cubetexturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in **D3DXCreateCubeTextureFromFileW auflösen.** Andernfalls wird der Funktionsaufruf in **D3DXCreateCubeTextureFromFileA** auflösen, da ANSI-Zeichenfolgen verwendet werden.

Die Funktion entspricht D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL,** ppCubeTexture).

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicherklasse platziert wird, die von D3DPOOL MANAGED bezeichnet \_ wird. Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicherklasse platziert, die durch D3DPOOL DEFAULT bezeichnet \_ wird.

Die Filterung wird automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde. Die Filterung entspricht D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

**D3DXCreateCubeTextureFromFile** verwendet das DirectDraw-Oberflächendateiformat (DDS). Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine Cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern. Sie können sich Dxtex.exe DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXCreateCubeTextureFromFileEx**](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
