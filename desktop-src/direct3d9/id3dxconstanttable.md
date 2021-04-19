---
description: Die ID3DXConstantTable-Schnittstelle wird verwendet, um auf die Konstante Tabelle zuzugreifen. Diese Tabelle enthält die Variablen, die von den sprach-Shadern und-Effekten auf hoher Ebene verwendet werden.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: ID3DXConstantTable-Schnittstelle (D3DX9Shader. h)
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
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366648"
---
# <a name="id3dxconstanttable-interface"></a>ID3DXConstantTable-Schnittstelle

Die ID3DXConstantTable-Schnittstelle wird verwendet, um auf die Konstante Tabelle zuzugreifen. Diese Tabelle enthält die Variablen, die von den sprach-Shadern und-Effekten auf hoher Ebene verwendet werden.

## <a name="members"></a>Member

Die **ID3DXConstantTable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXConstantTable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXConstantTable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                       | BESCHREIBUNG                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Getbufferpointer**](id3dxconstanttable--getbufferpointer.md)                             | Ruft einen Zeiger auf den Puffer ab, der die Konstante Tabelle enthält.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Ruft die Puffergröße der Konstanten Tabelle ab.<br/>                                                                             |
| [**Getconstant**](id3dxconstanttable--getconstant.md)                                       | Ruft eine Konstante ab, indem ihr Index gesucht wird.<br/>                                                                                |
| [**Getconstantbyname**](id3dxconstanttable--getconstantbyname.md)                           | Ruft eine Konstante ab, indem Ihr Name gesucht wird.<br/>                                                                                 |
| [**Getconstantdebug**](id3dxconstanttable--getconstantdesc.md)                               | Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstanten Tabelle ab.<br/>                                              |
| [**Getconstantelements**](id3dxconstanttable--getconstantelement.md)                         | Ruft eine Konstante von einem Array von Konstanten ab. Ein Array besteht aus Elementen.<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Ruft eine Beschreibung der Konstanten Tabelle ab.<br/>                                                                               |
| [**Getsamplerindex**](id3dxconstanttable--getsamplerindex.md)                               | Gibt den samplerindex zurück.<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | Legt einen booleschen Wert fest.<br/>                                                                                                   |
| [**Setboolarray**](id3dxconstanttable--setboolarray.md)                                     | Legt ein Array von booleschen Werten fest.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Legt die Konstanten auf ihre Standardwerte fest. Die Standardwerte werden in den Variablen Deklarationen im Shader deklariert.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Legt eine Gleit Komma Zahl fest.<br/>                                                                                           |
| [**Setfloatarray**](id3dxconstanttable--setfloatarray.md)                                   | Legt ein Array von Gleit Komma Zahlen fest.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Legt einen ganzzahligen Wert fest.<br/>                                                                                                  |
| [**"Tartintarray"**](id3dxconstanttable--setintarray.md)                                       | Legt ein Array von ganzen Zahlen fest.<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | Legt eine nicht übersetzte Matrix fest.<br/>                                                                                            |
| [**Setmatrixarray**](id3dxconstanttable--setmatrixarray.md)                                 | Legt ein Array nicht umsetzbarer Matrizen fest.<br/>                                                                                |
| [**Setmatrixpointerarray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.<br/>                                                                    |
| [**Setmatrixtransform**](id3dxconstanttable--setmatrixtranspose.md)                         | Legt eine übersetzte Matrix fest.<br/>                                                                                               |
| [**Setmatrixtransposearray**](id3dxconstanttable--setmatrixtransposearray.md)               | Legt ein Array von umsetzten Matrizen fest.<br/>                                                                                   |
| [**Setmatrixtransposepointerarray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Legt ein Array von Zeigern auf umgesetzte Matrizen fest.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Legt den Inhalt des Puffers auf die Konstante Tabelle fest.<br/>                                                                  |
| [**Setvector**](id3dxconstanttable--setvector.md)                                           | Legt einen 4D-Vektor fest.<br/>                                                                                                       |
| [**Setvector Array**](id3dxconstanttable--setvectorarray.md)                                 | Legt ein Array von 4D-Vektoren fest.<br/>                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXCONSTANTTABLE-Typ wird als Zeiger auf die **ID3DXConstantTable** -Schnittstelle definiert.


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
