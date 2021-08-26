---
description: Gibt die Größe eines Scheitelpunkts aus der Scheitelpunktdeklaration zurück.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: D3DXGetDeclVertexSize-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c120e0089c350133372526f1b030eb1a94ede5a511ba44fb21b5ae320aa7090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986860"
---
# <a name="d3dxgetdeclvertexsize-function"></a>D3DXGetDeclVertexSize-Funktion

Gibt die Größe eines Scheitelpunkts aus der Scheitelpunktdeklaration zurück.

## <a name="syntax"></a>Syntax


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDecl* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Ein Zeiger auf die Scheitelpunktdeklaration. Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*Streamen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der nullbasierte Streamindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Größe der Scheitelpunktdeklaration in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
