---
description: Stellt Methoden zum Abrufen und Festlegen von Effektparametern wie Konstanten, Funktionen, Shadern und Techniken zur Verfügung.
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: ID3DXBaseEffect-Schnittstelle (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8525a8139cd769a59886576f8ec32c7dab333a2903ffdb0fba1abc8ffbe27d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848550"
---
# <a name="id3dxbaseeffect-interface"></a>ID3DXBaseEffect-Schnittstelle

Stellt Methoden zum Abrufen und Festlegen von Effektparametern wie Konstanten, Funktionen, Shadern und Techniken zur Verfügung.

## <a name="members"></a>Member

Die **ID3DXBaseEffect-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXBaseEffect** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXBaseEffect-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnnotation**](id3dxbaseeffect--getannotation.md)                                   | Ruft das Handle einer Anmerkung ab. <br/>                                                                                                                                                                                     |
| [**GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md)                       | Ruft das Handle einer Anmerkung ab, indem ihr Name gesucht wird.<br/>                                                                                                                                                               |
| [**GetBool**](id3dxbaseeffect--getbool.md)                                               | Ruft einen BOOL-Wert ab.<br/>                                                                                                                                                                                                     |
| [**GetBoolArray**](id3dxbaseeffect--getboolarray.md)                                     | Ruft ein Array von BOOL-Werten ab.<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | Ruft die Beschreibung des Effekts ab.<br/>                                                                                                                                                                                           |
| [**Getfloat**](id3dxbaseeffect--getfloat.md)                                             | Ruft einen Gleitkommawert ab.<br/>                                                                                                                                                                                           |
| [**GetFloatArray**](id3dxbaseeffect--getfloatarray.md)                                   | Ruft ein Array von Gleitkommawerten ab.<br/>                                                                                                                                                                                |
| [**GetFunction**](id3dxbaseeffect--getfunction.md)                                       | Ruft das Handle einer Funktion ab.<br/>                                                                                                                                                                                         |
| [**GetFunctionByName**](id3dxbaseeffect--getfunctionbyname.md)                           | Ruft das Handle einer Funktion ab, indem ihr Name gesucht wird.<br/>                                                                                                                                                                  |
| [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)                               | Ruft eine Funktionsbeschreibung ab.<br/>                                                                                                                                                                                           |
| [**GetInt**](id3dxbaseeffect--getint.md)                                                 | Ruft eine ganze Zahl ab.<br/>                                                                                                                                                                                                       |
| [**GetIntArray**](id3dxbaseeffect--getintarray.md)                                       | Ruft ein Array von ganzen Zahlen ab.<br/>                                                                                                                                                                                             |
| [**GetMatrix**](id3dxbaseeffect--getmatrix.md)                                           | Ruft eine nicht übersetzte Matrix ab.<br/>                                                                                                                                                                                           |
| [**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)                                 | Ruft ein Array von nicht übersetzten Matrizen ab.<br/>                                                                                                                                                                               |
| [**GetMatrixPointerArray**](id3dxbaseeffect--getmatrixpointerarray.md)                   | Ruft ein Array von Zeigern auf nicht übersetzte Matrizen ab.<br/>                                                                                                                                                                   |
| [**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)                         | Ruft eine transponierte Matrix ab.<br/>                                                                                                                                                                                              |
| [**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)               | Ruft ein Array von transponierten Matrizen ab.<br/>                                                                                                                                                                                  |
| [**GetMatrixTransposePointerArray**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | Ruft ein Array von Zeigern auf transponierte Matrizen ab.<br/>                                                                                                                                                                      |
| [**Dbparametercollection.getparameter**](id3dxbaseeffect--getparameter.md)                                     | Ruft das Handle eines Parameters der obersten Ebene oder eines Struktur-Memberparameters ab.<br/>                                                                                                                                              |
| [**GetParameterByName**](id3dxbaseeffect--getparameterbyname.md)                         | Ruft das Handle eines Parameters der obersten Ebene oder eines Struktur-Memberparameters ab, indem nach dessen Namen gesucht wird.<br/>                                                                                                                       |
| [**GetParameterBySemantic**](id3dxbaseeffect--getparameterbysemantic.md)                 | Ruft das Handle eines Parameters der obersten Ebene oder eines Struktur-Memberparameters ab, indem seine Semantik mit einer Suche gesucht wird, bei der die Groß-/Kleinschreibung nicht beachtet wird.<br/>                                                                                    |
| [**GetParameterDesc**](id3dxbaseeffect--getparameterdesc.md)                             | Ruft eine Parameter- oder Anmerkungsbeschreibung ab.<br/>                                                                                                                                                                            |
| [**GetParameterElement**](id3dxbaseeffect--getparameterelement.md)                       | Gibt das Handle eines Arrayelementparameters an.<br/>                                                                                                                                                                          |
| [**GetPass**](id3dxbaseeffect--getpass.md)                                               | Ruft das Handle eines Durchgangs ab.<br/>                                                                                                                                                                                             |
| [**GetPassByName**](id3dxbaseeffect--getpassbyname.md)                                   | Ruft das Handle eines Durchgangs ab, indem nach dessen Namen gesucht wird.<br/>                                                                                                                                                                      |
| [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)                                       | Ruft eine Passbeschreibung ab.<br/>                                                                                                                                                                                               |
| [**GetPixelShader**](id3dxbaseeffect--getpixelshader.md)                                 | Ruft einen Pixel-Shader ab.<br/>                                                                                                                                                                                                   |
| [**Getstring**](id3dxbaseeffect--getstring.md)                                           | Ruft eine Zeichenfolge ab.<br/>                                                                                                                                                                                                         |
| [**GetTechnique**](id3dxbaseeffect--gettechnique.md)                                     | Ruft das Handle einer Technik ab.<br/>                                                                                                                                                                                        |
| [**GetTechniqueByName**](id3dxbaseeffect--gettechniquebyname.md)                         | Ruft das Handle einer Technik ab, indem ihr Name gesucht wird.<br/>                                                                                                                                                                 |
| [**GetTechniqueDesc**](id3dxbaseeffect--gettechniquedesc.md)                             | Ruft eine Technikbeschreibung ab.<br/>                                                                                                                                                                                          |
| [**GetTexture**](id3dxbaseeffect--gettexture.md)                                         | Ruft eine Textur ab.<br/>                                                                                                                                                                                                        |
| [**GetValue**](id3dxbaseeffect--getvalue.md)                                             | Hier erhalten Sie den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichenfolgen, Shader und Texturen. Diese Methode kann statt fast aller Getxxx-Aufrufe in **ID3DXBaseEffect verwendet werden.**<br/> |
| [**GetVector**](id3dxbaseeffect--getvector.md)                                           | Ruft einen Vektor ab.<br/>                                                                                                                                                                                                         |
| [**GetVectorArray**](id3dxbaseeffect--getvectorarray.md)                                 | Ruft ein Array von Vektoren ab.<br/>                                                                                                                                                                                              |
| [**GetVertexShader**](id3dxbaseeffect--getvertexshader.md)                               | Ruft einen Vertex-Shader ab.<br/>                                                                                                                                                                                                  |
| [**SetArrayRange**](id3dxbaseeffect--setarrayrange.md)                                   | Legen Sie den Bereich eines Arrays fest, das an das Gerät übergeben werden soll.<br/>                                                                                                                                                                       |
| [**SetBool**](id3dxbaseeffect--setbool.md)                                               | Legt einen BOOL-Wert fest.<br/>                                                                                                                                                                                                     |
| [**SetBoolArray**](id3dxbaseeffect--setboolarray.md)                                     | Legt ein Array von booleschen Werten fest.<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | Legt einen Gleitkommawert fest.<br/>                                                                                                                                                                                           |
| [**SetFloatArray**](id3dxbaseeffect--setfloatarray.md)                                   | Legt ein Array von Gleitkommawerten fest.<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | Legt eine ganze Zahl fest.<br/>                                                                                                                                                                                                       |
| [**SetIntArray**](id3dxbaseeffect--setintarray.md)                                       | Legt ein Array von ganzen Zahlen fest.<br/>                                                                                                                                                                                             |
| [**SetMatrix**](id3dxbaseeffect--setmatrix.md)                                           | Legt eine nicht transponierte Matrix fest.<br/>                                                                                                                                                                                          |
| [**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)                                 | Legt ein Array von nicht transposierten Matrizen fest.<br/>                                                                                                                                                                               |
| [**SetMatrixPointerArray**](id3dxbaseeffect--setmatrixpointerarray.md)                   | Legt ein Array von Zeigern auf nicht transposte Matrizen fest.<br/>                                                                                                                                                                   |
| [**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)                         | Legt eine transponierte Matrix fest.<br/>                                                                                                                                                                                              |
| [**SetMatrixTransposeArray**](id3dxbaseeffect--setmatrixtransposearray.md)               | Legt ein Array von transponierten Matrizen fest.<br/>                                                                                                                                                                                  |
| [**SetMatrixTransposePointerArray**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | Legt ein Array von Zeigern auf transponierte Matrizen fest.<br/>                                                                                                                                                                      |
| [**Setstring**](id3dxbaseeffect--setstring.md)                                           | Legt eine Zeichenfolge fest.<br/>                                                                                                                                                                                                         |
| [**SetTexture**](id3dxbaseeffect--settexture.md)                                         | Legt eine Textur fest.<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | Legen Sie den Wert eines beliebigen Parameters oder einer beliebigen Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichenfolgen, Shader und Texturen. <br/>                                                                                        |
| [**SetVector**](id3dxbaseeffect--setvector.md)                                           | Legt einen Vektor fest.<br/>                                                                                                                                                                                                         |
| [**SetVectorArray**](id3dxbaseeffect--setvectorarray.md)                                 | Legt ein Array von Vektoren fest.<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>Hinweise

Der LPD3DXBASEEFFECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektschnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
