---
description: Gibt die Größe eines Scheitel Punkts für ein flexibles Vertex-Format (FVF) zurück.
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: D3DXGetFVFVertexSize-Funktion (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353724"
---
# <a name="d3dxgetfvfvertexsize-function"></a>D3DXGetFVFVertexSize-Funktion

Gibt die Größe eines Scheitel Punkts für ein flexibles Vertex-Format (FVF) zurück.

## <a name="syntax"></a>Syntax


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*F-VF* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

FVF, die abgefragt werden soll. Eine Kombination aus [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die vertexgröße des-Vertex in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
