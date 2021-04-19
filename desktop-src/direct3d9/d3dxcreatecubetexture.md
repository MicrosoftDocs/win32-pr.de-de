---
description: Erstellt eine leere cubetextur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: D3DXCreateCubeTexture-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367478"
---
# <a name="d3dxcreatecubetexture-function"></a>D3DXCreateCubeTexture-Funktion

Erstellt eine leere cubetextur und passt die aufrufenden Parameter nach Bedarf an.

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*Größe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Breite und Höhe der cubetextur in Pixel. Wenn es sich bei der cubetextur z. b. um einen 8-Pixel-Cube mit 8 Pixel handelt, sollte der Wert für diesen Parameter 8 lauten.

</dd> <dt>

*Miplevels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der angeforderten Mip-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic. Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden. Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die cubetextur beschreibt. Die zurückgegebene cubetextur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird. Anwendungen sollten das Format der zurückgegebenen cubetextur überprüfen.

</dd> <dt>

*Pool* \[ in\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Cubestruktur platziert werden soll.

</dd> <dt>

*ppcubetexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von

Intern verwendet D3DXCreateCubeTexture [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) , um die aufrufenden Parameter anzupassen. Daher sind Aufrufe von D3DXCreateCubeTexture oft erfolgreich, wenn Aufrufe von " [**anatecubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) " fehlschlagen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
