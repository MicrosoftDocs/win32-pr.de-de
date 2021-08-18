---
description: Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das ein n-seiteniges Polygon enthält.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: D3DXCreatePolygon-Funktion (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf3694bb247fb95e654452c8db3887fcebc2832ac28ec0b2ac920b28f285e22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045148"
---
# <a name="d3dxcreatepolygon-function"></a>D3DXCreatePolygon-Funktion

Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das ein n-seiteniges Polygon enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das dem erstellten Polygonnetz zugeordnet ist.

</dd> <dt>

*Länge* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Länge der einzelnen Seiten.

</dd> <dt>

*Seiten* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Seiten für das Polygon. Der Wert muss größer oder gleich 3 sein.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf die Ausgabeform, eine [**ID3DXMesh-Schnittstelle.**](id3dxmesh.md)

</dd> <dt>

*ppAdencyency* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md) Wenn die Methode zurückgegeben wird, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Netz angeben. **NULL** kann angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Das erstellte Polygon wird am Ursprung zentriert.

Diese Funktion erstellt ein Netz mit der Erstellungsoption D3DXMESH \_ MANAGED und [D3DFVF \_ XYZ \| D3DFVF \_ NORMAL](d3dfvf.md) Flexible Vertex format (FVF).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeichnen von Formenfunktionen](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
