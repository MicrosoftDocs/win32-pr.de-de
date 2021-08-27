---
description: Gibt die Größe eines Scheitelpunkts für ein flexibles Scheitelpunktformat (FVF) zurück.
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: D3DXGetFVFVertexSize-Funktion (D3dx9mesh.h)
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
ms.openlocfilehash: f00faa489481faf436a30fe6e6313429d446cd8000173131d823442e960b5a08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119210"
---
# <a name="d3dxgetfvfvertexsize-function"></a>D3DXGetFVFVertexSize-Funktion

Gibt die Größe eines Scheitelpunkts für ein flexibles Scheitelpunktformat (FVF) zurück.

## <a name="syntax"></a>Syntax


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FVF* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

FVF, die abgefragt werden soll. Eine Kombination aus [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die FVF-Scheitelpunktgröße in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
