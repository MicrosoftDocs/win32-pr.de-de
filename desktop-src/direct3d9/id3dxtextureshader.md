---
description: Die ID3DXTextureShader-Schnittstelle.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: ID3DXTextureShader-Schnittstelle (D3DX9Shader.h)
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
ms.openlocfilehash: 95e6a8feb35ea5d1e38a5cb63bb1379e4995e7562839cc1b582ee8efd8550212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846980"
---
# <a name="id3dxtextureshader-interface"></a>ID3DXTextureShader-Schnittstelle

Die ID3DXTextureShader-Schnittstelle.

## <a name="members"></a>Member

Die **ID3DXTextureShader-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXTextureShader** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXTextureShader-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                       | Beschreibung                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**GetConstant**](id3dxtextureshader--getconstant.md)                                       | Ruft eine Konstante ab, indem der index nach oben gesucht wird.<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Abrufen eines Zeigers auf die konstante Tabelle.<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | Ruft eine Konstante ab, indem deren Name nach gesucht wird.<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | Ruft einen Zeiger auf das Array von Konstanten in der Konstantentabelle ab.<br/>  |
| [**GetConstantElement**](id3dxtextureshader--getconstantelement.md)                         | Abrufen einer Konstante aus der Konstantentabelle.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Ruft eine Beschreibung der konstanten Tabelle ab.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Ruft einen Zeiger auf den DWORD-Funktionsstream ab.<br/>                     |
| [**SetBool**](id3dxtextureshader--setbool.md)                                               | Legt einen BOOL-Wert fest.<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | Legt ein Array von BOOL-Werten fest.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Legt die Konstanten auf die Standardwerte fest, die im Shader deklariert sind.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Legt eine Gleitkommazahl fest.<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | Legt ein Array von Gleitkommazahlen fest.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Legt einen ganzzahligen Wert fest.<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | Legt ein Array von ganzen Zahlen fest.<br/>                                       |
| [**SetMatrix**](id3dxtextureshader--setmatrix.md)                                           | Legt eine nicht transponierte Matrix fest.<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | Legt ein Array von nicht transponierten Matrizen fest.<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Legt ein Array von Zeigern auf nicht transponierte Matrizen fest.<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | Legt eine transponierte Matrix fest.<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | Legt ein Array von transponierten Matrizen fest.<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Legt ein Array von Zeigern auf transponierte Matrizen fest.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Legt die konstante Tabelle mit den Daten im Puffer fest.<br/>             |
| [**SetVector**](id3dxtextureshader--setvector.md)                                           | Legt einen 4D-Vektor fest.<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | Legt ein Array von 4D-Vektoren fest.<br/>                                     |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXTextureShader-Schnittstelle** wird durch Aufrufen der [**D3DXCreateTextureShader-Funktion**](d3dxcreatetextureshader.md) abgerufen.

Die **ID3DXTextureShader-Schnittstelle** erbt wie alle COM-Schnittstellen die [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Der LPD3DXTEXTURESHADER-Typ wird als Zeiger auf die **ID3DXTextureShader-Schnittstelle** definiert.


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
