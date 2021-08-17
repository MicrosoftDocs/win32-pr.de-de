---
description: Erstellt eine Textur aus einer Datei.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: D3DXCreateTextureFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3ffce68a8044267e67d874412264d5a915c65b88ea5cc13b0cd8d2cd1400828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732159"
---
# <a name="d3dxcreatetexturefromfile-function"></a>D3DXCreateTextureFromFile-Funktion

Erstellt eine Textur aus einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die das erstellte Texturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateTextureFromFileW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXCreateTextureFromFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Die Funktion entspricht D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL**, **NULL**, ppTexture).

Bei Mipmapped-Texturen ist jede Ebene automatisch mit der geladenen Textur gefüllt.

Beim Laden von Bildern in mipmapped Texturen können einige Geräte nicht zu einem 1x1-Bild wechseln, und diese Funktion schlägt fehl. In diesem Fall müssen die Images manuell geladen werden.

Beachten Sie, dass eine mit dieser Funktion erstellte Ressource in der Speicherklasse platziert wird, die von D3DPOOL MANAGED bezeichnet \_ wird.

Die Filterung wird automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde. Die Filterung entspricht D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

Für die beste Leistung bei Verwendung von **D3DXCreateTextureFromFile:**

1.  Die Bildskalierung und Formatkonvertierung zur Ladezeit kann langsam sein. Store Bilder in dem Format und der Auflösung, in dem sie verwendet werden. Wenn die Zielhardware eine Leistung von zwei Dimensionen erfordert, erstellen und speichern Sie Bilder mit zwei Dimensionen.
2.  Erwägen Sie die Verwendung von DDS-Dateien (DirectDraw Surface). Da DDS-Dateien verwendet werden können, um jedes Direct3D 9-Texturformat darzustellen, sind sie für D3DX sehr einfach zu lesen. Außerdem können sie Mipmaps speichern, sodass alle Mipmap-Generierungsalgorithmen zum Erstellen der Bilder verwendet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
