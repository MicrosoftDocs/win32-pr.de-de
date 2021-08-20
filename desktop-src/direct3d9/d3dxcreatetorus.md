---
description: Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das einen Torus enthält.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: D3DXCreateTorus-Funktion (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1671641a5088535777cb78bf3773f4c1e56e1c3d35e70d345a39df2dad7bd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526192"
---
# <a name="d3dxcreatetorus-function"></a>D3DXCreateTorus-Funktion

Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das einen Torus enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das dem erstellten Torusgitternetz zugeordnet ist.

</dd> <dt>

*InnerRadius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Innerer Radius des Torus. Der Wert sollte größer oder gleich 0,0f sein.

</dd> <dt>

*OuterRadius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Äußerer Radius des Torus. Der Wert sollte größer oder gleich 0,0f sein.

</dd> <dt>

*Seiten* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Seiten in einem Kreuzabschnitt. Der Wert muss größer oder gleich 3 sein.

</dd> <dt>

*Ringe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Ringe, die den Torus bilden. Der Wert muss größer oder gleich 3 sein.

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

Der erstellte Torus ist am Ursprung zentriert, und seine Achse wird an der Z-Achse ausgerichtet. Der innere Radius des Torus ist der Radius des Kreuzabschnitts (der kleinere Radius), und der äußere Radius des Torus ist der Radius der zentralen Lücke.

Diese Funktion gibt ein Gitternetz zurück, das später zum Zeichnen oder Bearbeiten durch die Anwendung verwendet werden kann.

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

 

 
