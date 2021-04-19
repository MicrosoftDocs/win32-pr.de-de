---
description: Generiert eine optimierte Vertex-Neuzuordnung für eine Dreiecks Liste. Diese Funktion wird in der Regel nach dem Anwenden der von D3DXOptimizeFaces generierten Gesichts Neuzuordnung verwendet.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: D3DXOptimizeVertices-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 734c2224ae29e7ab166010d59859d00355e5400e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355159"
---
# <a name="d3dxoptimizevertices-function"></a>D3DXOptimizeVertices-Funktion

Generiert eine optimierte Vertex-Neuzuordnung für eine Dreiecks Liste. Diese Funktion wird in der Regel nach dem Anwenden der von [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)generierten Gesichts Neuzuordnung verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
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

Anzahl der Gesichter in der Dreiecks Liste.

</dd> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte, auf die durch die Dreiecks Liste verwiesen wird.

</dd> <dt>

*Indices32Bit* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Flag, das den Indextyp angibt: **true** , wenn Indizes 32-Bit (mehr als 65535 Scheitel Punkte) sind, **false** , wenn Indizes 16-Bit (65535 oder weniger Scheitel Punkte) sind.

</dd> <dt>

*pvertexremap* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf einen Ziel Puffer, der den neuen Index für jeden Scheitelpunkt enthält. Der in " *pvertexremap* " für ein bestimmtes Element gespeicherte Wert ist der Quell Vertex-Speicherort in der neuen Scheitelpunkt Reihenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Standardmäßig verwendet ein Mesh bei der Erstellung 16-Bit-Indizes, es sei denn, die Anwendung gibt andernfalls an. Um zu überprüfen, ob ein vorhandenes Mesh 16-Bit-oder 32-Bit-Indizes verwendet, müssen Sie [**ID3DXBaseMesh:: GetOptions**](id3dxbasemesh--getoptions.md) aufrufen und das D3DXMESH 32-Bit-Flag überprüfen \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
