---
description: Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das eine Kugel enthält.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: D3DXCreateSphere-Funktion (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c1cea000071f0d097f29138b4e5f2db554f2214d8ca6343c16a39740d82c29e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119350"
---
# <a name="d3dxcreatesphere-function"></a>D3DXCreateSphere-Funktion

Verwendet ein linkshändiges Koordinatensystem, um ein Gitternetz zu erstellen, das eine Kugel enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das dem erstellten Kugelgitternetz zugeordnet ist.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der Kugel. Dieser Wert sollte größer oder gleich 0,0f sein.

</dd> <dt>

*Slices* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Slices über die Hauptachse.

</dd> <dt>

*Stapel* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Stapel entlang der Hauptachse.

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

Die erstellte Kugel wird am Ursprung zentriert, und ihre Achse wird an der Z-Achse ausgerichtet.

Diese Funktion erstellt ein Netz mit der Erstellungsoption D3DXMESH \_ MANAGED und [D3DFVF \_ XYZ \| D3DFVF \_ NORMAL](d3dfvf.md) Flexible Vertex format (FVF).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeichnen von Formenfunktionen](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
