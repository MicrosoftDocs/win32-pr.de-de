---
description: Die ID3DXConstantTable-Schnittstelle wird verwendet, um auf die konstante Tabelle zuzugreifen. Diese Tabelle enthält die Variablen, die von übergeordneten Sprach-Shadern und -Effekten verwendet werden.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: ID3DXConstantTable-Schnittstelle (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ead9e594e79daf8bd43bf4125b857030482028f7128c8063196413d52c9a8b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675480"
---
# <a name="id3dxconstanttable-interface"></a>ID3DXConstantTable-Schnittstelle

Die ID3DXConstantTable-Schnittstelle wird verwendet, um auf die konstante Tabelle zuzugreifen. Diese Tabelle enthält die Variablen, die von übergeordneten Sprach-Shadern und -Effekten verwendet werden.

## <a name="members"></a>Member

Die **ID3DXConstantTable-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXConstantTable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXConstantTable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                       | Beschreibung                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Ruft einen Zeiger auf den Puffer ab, der die konstante Tabelle enthält.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Ruft die Puffergröße der konstanten Tabelle ab.<br/>                                                                             |
| [**GetConstant**](id3dxconstanttable--getconstant.md)                                       | Ruft eine Konstante ab, indem der index nach oben gesucht wird.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Ruft eine Konstante ab, indem deren Name nach gesucht wird.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der konstanten Tabelle ab.<br/>                                              |
| [**GetConstantElement**](id3dxconstanttable--getconstantelement.md)                         | Ruft eine Konstante aus einem Array von Konstanten ab. Ein Array besteht aus Elementen.<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Ruft eine Beschreibung der konstanten Tabelle ab.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Gibt den Samplerindex zurück.<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | Legt einen booleschen Wert fest.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Legt ein Array von booleschen Werten fest.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Legt die Konstanten auf ihre Standardwerte fest. Die Standardwerte werden in den Variablendeklarationen im Shader deklariert.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Legt eine Gleitkommazahl fest.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Legt ein Array von Gleitkommazahlen fest.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Legt einen ganzzahligen Wert fest.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Legt ein Array von ganzen Zahlen fest.<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | Legt eine nicht transposed Matrix fest.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Legt ein Array von nicht transposierten Matrizen fest.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Legt ein Array von Zeigern auf nicht transposte Matrizen fest.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Legt eine transponierte Matrix fest.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Legt ein Array von transponierten Matrizen fest.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Legt ein Array von Zeigern auf transponierte Matrizen fest.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Legt den Inhalt des Puffers auf die konstante Tabelle fest.<br/>                                                                  |
| [**SetVector**](id3dxconstanttable--setvector.md)                                           | Legt einen 4D-Vektor fest.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Legt ein Array von 4D-Vektoren fest.<br/>                                                                                            |



 

## <a name="remarks"></a>Hinweise

Der LPD3DXCONSTANTTABLE-Typ wird als Zeiger auf die **ID3DXConstantTable-Schnittstelle** definiert.


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
