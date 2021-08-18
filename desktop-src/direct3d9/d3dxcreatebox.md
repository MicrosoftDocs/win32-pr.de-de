---
description: Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das ein an einer Achse ausgerichtetes Feld enthält.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: D3DXCreateBox-Funktion (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66afc489611936a122e05e8a797997d11e5073429834f8f1b534b03b02c2de4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526544"
---
# <a name="d3dxcreatebox-function"></a>D3DXCreateBox-Funktion

Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das ein an einer Achse ausgerichtetes Feld enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das dem erstellten Box mesh zugeordnet ist.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Breite des Felds entlang der X-Achse.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Höhe des Felds entlang der y-Achse.

</dd> <dt>

*Tiefe* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Tiefe des Felds entlang der Z-Achse.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf die Ausgabeform, eine [**ID3DXMesh-Schnittstelle.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md) Wenn die Methode zurückgegeben wird, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben. **NULL** kann angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Das erstellte Feld wird am Ursprung zentriert.

Diese Funktion erstellt ein Gitternetz mit der Erstellungsoption D3DXMESH MANAGED und dem flexiblen \_ Vertexformat (FVF) [ \_ \| D3DFVF XYZ D3DFVF \_ NORMAL.](d3dfvf.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Formzeichnungsfunktionen](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
