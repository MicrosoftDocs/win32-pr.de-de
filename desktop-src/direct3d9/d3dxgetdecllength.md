---
description: Gibt die Anzahl der Elemente in der Scheitelpunktdeklaration zurück.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: D3DXGetDeclLength-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc6a44c73d9b7127bb382cfbf18587a84d8cc179feabf48da6e29b908204b1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857039"
---
# <a name="d3dxgetdecllength-function"></a>D3DXGetDeclLength-Funktion

Gibt die Anzahl der Elemente in der Scheitelpunktdeklaration zurück.

## <a name="syntax"></a>Syntax


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDecl* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Ein Zeiger auf die Scheitelpunktdeklaration. Siehe [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente in der Scheitelpunktdeklaration.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
