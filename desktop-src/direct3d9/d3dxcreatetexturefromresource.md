---
description: Erstellt eine Textur aus einer Ressource.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: D3DXCreateTextureFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870103"
---
# <a name="d3dxcreatetexturefromresource-function"></a>D3DXCreateTextureFromResource-Funktion

Erstellt eine Textur aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*hsrcmodule* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.

</dd> <dt>

*psrkresource* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*pptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextureFromResourceW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateTextureFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Die-Funktion entspricht D3DXCreateTextureFromResourceEx (pdevice, hsrcmodule, psrkresource, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, pptexture).

Die Ressource, die geladen wird, muss den Typ RT \_ Bitmap oder RT \_ RCDATA aufweisen. Der Ressourcentyp RT \_ RCDATA dient zum Laden von anderen Formaten als Bitmaps (z. b. TGA, JPG und DDS).

Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA. Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .

Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde. Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
