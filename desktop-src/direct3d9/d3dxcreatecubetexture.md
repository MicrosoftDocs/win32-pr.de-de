---
description: Erstellt eine leere Cubetextur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: D3DXCreateCubeTexture-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 86518a98f9ac78c4c6410d6ff5aa76640dbd04c0d5e50158e4432b7fa5ab79ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045198"
---
# <a name="d3dxcreatecubetexture-function"></a>D3DXCreateCubeTexture-Funktion

Erstellt eine leere Cubetextur und passt die aufrufenden Parameter nach Bedarf an.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*Größe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite und Höhe der Cubetextur in Pixel. Wenn es sich bei der Cubetextur beispielsweise um einen Cube mit 8 x 8 Pixeln handelt, sollte der Wert für diesen Parameter 8 sein.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET oder D3DUSAGE \_ DYNAMIC. Durch Festlegen dieses Flags auf D3DUSAGE \_ RENDERTARGET wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode**](/windows/desktop/api) übergeben werden. Wenn D3DUSAGE \_ RENDERTARGET angegeben ist, sollte die Anwendung überprüfen, ob das Gerät diesen Vorgang unterstützt, indem [**sie CheckDeviceFormat aufruft.**](/windows/desktop/api) Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen.](performance-optimizations.md)

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das angeforderte Pixelformat für die Cubetextur beschreibt. Die zurückgegebene Cubetextur hat möglicherweise ein anderes Format als das von *Format* angegebene Format. Anwendungen sollten das Format der zurückgegebenen Cubetextur überprüfen.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Cubetextur platziert werden soll.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) die das erstellte Cubetexturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Cubetexturen unterscheiden sich von anderen Oberflächen darin, dass sie Auflistungen von Oberflächen sind.

Intern verwendet D3DXCreateCubeTexture [**D3DXCheckCubeTextureRequirements,**](d3dxcheckcubetexturerequirements.md) um die aufrufenden Parameter anzupassen. Daher sind Aufrufe von D3DXCreateCubeTexture häufig erfolgreich, wenn Aufrufe von [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) fehlschlagen würden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
