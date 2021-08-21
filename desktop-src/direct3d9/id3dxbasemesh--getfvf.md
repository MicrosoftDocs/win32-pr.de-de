---
description: 'ID3DXBaseMesh::GetFVF-Methode: Ruft den festen Funktionsvertexwert ab.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: ID3DXBaseMesh::GetFVF-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f14645e5e7f0aa883f04e689f0774441482b86223bf485fa1fc8a395618c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987620"
---
# <a name="id3dxbasemeshgetfvf-method"></a>ID3DXBaseMesh::GetFVF-Methode

Ruft den vertex-Wert der festen Funktion ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Codes des flexiblen Vertexformats (FVF) zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kann 0 zurückgeben, wenn das Scheitelpunktformat nicht direkt einem FVF-Code zugeordnet werden kann. Dies tritt bei einem Gitternetz auf, das aus einer Scheitelpunktdeklaration erstellt wurde, die nicht die gleiche Reihenfolge und elemente aufwies, die von den FVF-Codes unterstützt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
