---
description: 'D3DXCreateVolumeTextureFromFile-Funktion: Erstellt eine Volumetextur aus einer Datei.'
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: D3DXCreateVolumeTextureFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094301"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a>D3DXCreateVolumeTextureFromFile-Funktion

Erstellt eine Volumetextur aus einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Volumetextur zugeordnet werden soll.

</dd> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*ppVolumeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) die das erstellte Texturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Funktion ein Fehler auftritt, kann der Rückgabewert einen der folgenden Werte haben: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateVolumeTextureFromFileW auflösen. Andernfalls wird der Funktionsaufruf in D3DXCreateVolumeTextureFromFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Die Funktion entspricht D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL,** ppVolumeTexture).

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Bei Mipmapped-Texturen wird jede Ebene automatisch mit der geladenen Textur gefüllt.

Beim Laden von Bildern in mipmapped Texturen können einige Geräte nicht zu einem 1x1-Bild wechseln, und diese Funktion schlägt fehl. In diesem Fall müssen die Images manuell geladen werden.

Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicherklasse platziert wird, die von D3DPOOL MANAGED bezeichnet \_ wird. Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicherklasse platziert, die durch D3DPOOL DEFAULT gekennzeichnet \_ wird.

Die Filterung wird automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde. Die Filterung entspricht D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
