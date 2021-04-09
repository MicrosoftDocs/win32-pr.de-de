---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das ein n-seitiges Polygon enthält.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: D3DXCreatePolygon-Funktion (D3dx9shape. h)
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
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050858"
---
# <a name="d3dxcreatepolygon-function"></a>D3DXCreatePolygon-Funktion

Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das ein n-seitiges Polygon enthält.

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Polygonnetz zugeordnet ist.

</dd> <dt>

*Länge* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Länge jeder Seite.

</dd> <dt>

*Seiten* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Seiten für das Polygon. Der Wert muss größer oder gleich 3 sein.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.

</dd> <dt>

*ppency* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle. Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben. **Null** kann angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Das erstellte Polygon wird am Ursprung zentriert.

Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Formen Zeichnungsfunktionen](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
