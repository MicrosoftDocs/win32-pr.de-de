---
description: Filtert Mipmapebenen einer Textur.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: D3DXFilterTexture-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc07336edb5f7bb8672fbbec415b0a3b312335a3a3a4b0de32aec4fdde558363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988500"
---
# <a name="d3dxfiltertexture-function"></a>D3DXFilterTexture-Funktion

Filtert Mipmapebenen einer Textur.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBaseTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Zeiger auf eine [**IDirect3DBaseTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) die das zu filternde Texturobjekt darstellt.

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine zu füllende 256-Farbpalette darstellt, oder **NULL** für nichtpalettierte Formate. Wenn keine Palette angegeben wird, wird die Direct3D-Standardpalette (eine nicht transparente weiße Palette) bereitgestellt. Siehe Hinweise.

</dd> <dt>

*SrcLevel* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ebene, deren Bild zum Generieren der nachfolgenden Ebenen verwendet wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe \_ von 0.

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus mindestens einem [D3DX-FILTER, \_ ](d3dx-filter.md) der steuert, wie die Mipmap gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER BOX, wenn die Texturgröße eine Zweierleistung hat, andernfalls \_ \_ \_ D3DX \_ FILTER \_ BOX \| D3DX \_ FILTER \_ DITHER.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Ein Filter wird rekursiv auf jede Texturebene angewendet, um die nächste Texturebene zu generieren.

Das Schreiben auf eine Texturoberfläche, die keine Ebene 0 (null) aufgibt, verursacht keine Aktualisierung des geänderten Rechtecks. Wenn **D3DXFilterTexture** aufgerufen wird und die Oberfläche noch nicht angepasst wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit für die Textur aufrufen.

Im Standardpool erstellte Texturen (D3DPOOL DEFAULT) können nicht mit \_ **D3DXFilterTexture** verwendet werden (es sei denn, sie werden mit D3DUSAGE DYNAMIC erstellt), da ein Sperrvorgang für das Objekt erforderlich \_ ist. Beachten Sie, dass Sperren für Texturen im Standardpool nicht zulässig sind (es sei denn, sie sind dynamisch).

Weitere Informationen zu [**PALETTEENTRY finden**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)Sie im Plattform-SDK. Beachten Sie, dass das peFlags-Member der **PALETTEENTRY-Struktur** ab DirectX 8.0 nicht wie im Platform SDK dokumentiert funktioniert. Das peFlags-Member ist jetzt der Alphakanal für palettierte 8-Bit-Formate.

Es gibt nur eine Texturfilterfunktion, aber zwei Makros, die diese Methode aufrufen.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
