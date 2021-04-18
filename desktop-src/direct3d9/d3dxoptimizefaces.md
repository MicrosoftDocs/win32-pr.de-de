---
description: Generiert eine optimierte Gesichts Zuordnung für eine Dreiecks Liste.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: D3DXOptimizeFaces-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351918"
---
# <a name="d3dxoptimizefaces-function"></a>D3DXOptimizeFaces-Funktion

Generiert eine optimierte Gesichts Zuordnung für eine Dreiecks Liste.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PIndizes* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf Dreiecks Listenindizes, die zum Anordnen von Scheitel Punkten verwendet werden sollen.

</dd> <dt>

*Numerische Werte* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Gesichter in der Dreiecks Liste. Bei 16-Bit-Meshes ist dies auf 2 ^ 16-1 (65535) oder weniger Gesichter beschränkt.

</dd> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte, auf die durch die Dreiecks Liste verwiesen wird.

</dd> <dt>

*Indices32Bit* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Flag, das den Indextyp angibt: **true** , wenn Indizes 32-Bit (mehr als 65535 Indizes) sind, **false** , wenn Indizes 16-Bit (65535 oder weniger Indizes) sind.

</dd> <dt>

*pfakeremap* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf das ursprüngliche Gitter Gesicht, das geteilt wurde, um die aktuelle Seite zu generieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Die Optimierungs Prozedur dieser Funktion ist funktional äquivalent zum Aufrufen von [**ID3DXMesh::**](id3dxmesh--optimize.md) Optimization mit dem D3DXMESHOPT \_ deviceindependent-Flag. diese Funktion ermöglicht jedoch eine effizientere Verwendung von Scheitelpunkt Caches.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
