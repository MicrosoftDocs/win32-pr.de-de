---
description: Gibt die Größe des Shader-Bytecodes in Bytes zurück.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: D3DXGetShaderSize-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7354431fa8f9e8a177b8ccc63ef434a3f0a88add8e9e4736e3fd5fffb0cea811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564820"
---
# <a name="d3dxgetshadersize-function"></a>D3DXGetShaderSize-Funktion

Gibt die Größe des Shader-Bytecodes in Bytes zurück.

## <a name="syntax"></a>Syntax


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Datenstrom der Funktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Gibt die Größe des Shader-Bytecodes in Bytes zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
