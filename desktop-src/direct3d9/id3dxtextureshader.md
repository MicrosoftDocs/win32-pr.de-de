---
description: Die ID3DXTextureShader-Schnittstelle.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: ID3DXTextureShader-Schnittstelle (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366456"
---
# <a name="id3dxtextureshader-interface"></a>ID3DXTextureShader-Schnittstelle

Die ID3DXTextureShader-Schnittstelle.

## <a name="members"></a>Member

Die **ID3DXTextureShader** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXTextureShader** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXTextureShader** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                       | BESCHREIBUNG                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**Getconstant**](id3dxtextureshader--getconstant.md)                                       | Ruft eine Konstante ab, indem ihr Index gesucht wird.<br/>                         |
| [**Getconstantbuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Einen Zeiger auf die Konstante Tabelle erhalten.<br/>                             |
| [**Getconstantbyname**](id3dxtextureshader--getconstantbyname.md)                           | Ruft eine Konstante ab, indem Ihr Name gesucht wird.<br/>                          |
| [**Getconstantdebug**](id3dxtextureshader--getconstantdesc.md)                               | Ruft einen Zeiger auf das Array von Konstanten in der Konstanten Tabelle ab.<br/>  |
| [**Getconstantelements**](id3dxtextureshader--getconstantelement.md)                         | Eine Konstante aus der Konstanten Tabelle erhalten.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Ruft eine Beschreibung der Konstanten Tabelle ab.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Ruft einen Zeiger auf die Funktion DWORD-Stream ab.<br/>                     |
| [**SetBool**](id3dxtextureshader--setbool.md)                                               | Legt einen booleschen Wert fest.<br/>                                               |
| [**Setboolarray**](id3dxtextureshader--setboolarray.md)                                     | Legt ein Array von booleschen Werten fest.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Legt die Konstanten auf die im Shader deklarierten Standardwerte fest.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Legt eine Gleit Komma Zahl fest.<br/>                                    |
| [**Setfloatarray**](id3dxtextureshader--setfloatarray.md)                                   | Legt ein Array von Gleit Komma Zahlen fest.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Legt einen ganzzahligen Wert fest.<br/>                                           |
| [**"Tartintarray"**](id3dxtextureshader--setintarray.md)                                       | Legt ein Array von ganzen Zahlen fest.<br/>                                       |
| [**SetMatrix**](id3dxtextureshader--setmatrix.md)                                           | Legt eine nicht übersetzte Matrix fest.<br/>                                    |
| [**Setmatrixarray**](id3dxtextureshader--setmatrixarray.md)                                 | Legt ein Array von nicht übersetzten Matrizen fest.<br/>                        |
| [**Setmatrixpointerarray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.<br/>            |
| [**Setmatrixtransform**](id3dxtextureshader--setmatrixtranspose.md)                         | Legt eine übersetzte Matrix fest.<br/>                                        |
| [**Setmatrixtransposearray**](id3dxtextureshader--setmatrixtransposearray.md)               | Legt ein Array von umsetzten Matrizen fest.<br/>                            |
| [**Setmatrixtransposepointerarray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Legt ein Array von Zeigern auf umgesetzte Matrizen fest.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Legt die Konstante Tabelle mit den Daten im Puffer fest.<br/>             |
| [**Setvector**](id3dxtextureshader--setvector.md)                                           | Legt einen 4D-Vektor fest.<br/>                                                |
| [**Setvector Array**](id3dxtextureshader--setvectorarray.md)                                 | Legt ein Array von 4D-Vektoren fest.<br/>                                     |



 

## <a name="remarks"></a>Bemerkungen

Die **ID3DXTextureShader** -Schnittstelle wird durch Aufrufen der [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) -Funktion abgerufen.

Die **ID3DXTextureShader** -Schnittstelle erbt wie alle COM-Schnittstellen die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.

Der LPD3DXTEXTURESHADER-Typ wird als Zeiger auf die **ID3DXTextureShader** -Schnittstelle definiert.


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
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

 

 
