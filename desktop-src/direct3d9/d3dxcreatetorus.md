---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das einen "Tor" enthält.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: D3DXCreateTorus-Funktion (D3dx9shape. h)
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
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219520"
---
# <a name="d3dxcreatetorus-function"></a>D3DXCreateTorus-Funktion

Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das einen "Tor" enthält.

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das dem erstellten Tor-Mesh zugeordnete Gerät darstellt.

</dd> <dt>

*Innerradius* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Innerer Radius des "Tor". Der Wert muss größer oder gleich 0,0 f sein.

</dd> <dt>

*Outerradius* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Äußerer Radius des "Tor". Der Wert muss größer oder gleich 0,0 f sein.

</dd> <dt>

*Seiten* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Seiten in einem Querschnitt. Der Wert muss größer oder gleich 3 sein.

</dd> <dt>

*Ringe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Ringen, die den Tor bilden. Der Wert muss größer oder gleich 3 sein.

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

Der erstellte ' Tor ' wird am Ursprung zentriert, und seine Achse ist an der z-Achse ausgerichtet. Der innere Radius des "Tor" ist der Radius des Kreuz Abschnitts (der kleinere Radius), und der äußere Radius des "Tor" ist der Radius der zentralen Lücke.

Diese Funktion gibt ein Mesh zurück, das später zum Zeichnen oder manipulieren durch die Anwendung verwendet werden kann.

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

 

 
