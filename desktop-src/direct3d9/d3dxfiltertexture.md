---
description: Filtert MipMap-Ebenen einer Textur.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: D3DXFilterTexture-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355012"
---
# <a name="d3dxfiltertexture-function"></a>D3DXFilterTexture-Funktion

Filtert MipMap-Ebenen einer Textur.

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

*pbasetexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Zeiger auf eine [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle, die das zu filternde Textur Objekt darstellt.

</dd> <dt>

*pPalette* \[ vorgenommen\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null** für nicht paletformatierte Formate. Wenn keine Palette angegeben ist, wird die standardmäßige Direct3D-Palette (eine alle nicht transparenten weißen Palette) bereitgestellt. Siehe Hinweise.

</dd> <dt>

*Srclevel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ebene, mit deren Bild die nachfolgenden Ebenen generiert werden. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von 0.

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie die MipMap gefiltert wird. Das angeben \_ von D3DX default für diesen Parameter entspricht dem Angeben des \_ D3DX \_ -Filter Felds, wenn die Textur Größe eine Potenz von zwei ist, und D3DX \_ Filter \_ Box \| D3DX \_ filtert \_ andernfalls.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Ein Filter wird rekursiv auf jede Textur Ebene angewendet, um die nächste Textur Ebene zu generieren.

Das Schreiben in eine Oberfläche ohne Ebene der Textur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXFilterTexture** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit für die Textur aufrufen.

Texturen, die im Standard Pool (D3DPOOL \_ Default) erstellt werden, können nicht mit **D3DXFilterTexture** verwendet werden (es sei denn, Sie werden mit D3DUSAGE \_ Dynamic erstellt), da ein Sperr Vorgang für das Objekt erforderlich ist. Beachten Sie, dass Sperren für Texturen im Standard Pool nicht zulässig sind (es sei denn, Sie sind dynamisch).

Ausführliche Informationen zu [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)finden Sie unter Platform SDK. Beachten Sie, dass der Member "Peer Flags" der **PaletteEntry** -Struktur ab DirectX 8,0 nicht wie im Platform SDK dokumentiert funktioniert. Der peflags-Member ist nun der Alphakanal für 8-Bit-Paletten-Formate.

Es gibt nur eine Textur Filterungs Funktion, aber zwei Makros, die diese Methode aufruft.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
