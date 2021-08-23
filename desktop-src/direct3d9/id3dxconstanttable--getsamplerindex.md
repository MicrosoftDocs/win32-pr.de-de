---
description: Gibt den Samplerindex zurück.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: ID3DXConstantTable::GetSamplerIndex-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dac22cc15e93198e7d494986b2279ae7e1d11fdb3c8cb65b3caddf9b905595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987570"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a>ID3DXConstantTable::GetSamplerIndex-Methode

Gibt den Samplerindex zurück.

## <a name="syntax"></a>Syntax


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ out\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Das Samplerhand handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Gibt die Samplerindexnummer aus der konstanten Tabelle zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
