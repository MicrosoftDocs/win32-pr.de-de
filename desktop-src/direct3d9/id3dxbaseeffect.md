---
description: Stellt Methoden zum erhalten und Festlegen von Effekt Parametern, wie z. b. Konstanten, Funktionen, Shadern und Techniken, bereit.
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: ID3DXBaseEffect-Schnittstelle (D3DX9Effect. h)
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
ms.openlocfilehash: e72fabf7db8341821885afb160fa73cb0fc9f395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132317"
---
# <a name="id3dxbaseeffect-interface"></a>ID3DXBaseEffect-Schnittstelle

Stellt Methoden zum erhalten und Festlegen von Effekt Parametern, wie z. b. Konstanten, Funktionen, Shadern und Techniken, bereit.

## <a name="members"></a>Member

Die **ID3DXBaseEffect** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXBaseEffect** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXBaseEffect** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnnotation**](id3dxbaseeffect--getannotation.md)                                   | Ruft das Handle einer Anmerkung ab. <br/>                                                                                                                                                                                     |
| [**Getannotationbyname**](id3dxbaseeffect--getannotationbyname.md)                       | Ruft das Handle einer Anmerkung ab, indem der zugehörige Name gesucht wird.<br/>                                                                                                                                                               |
| [**GetBool**](id3dxbaseeffect--getbool.md)                                               | Ruft einen booleschen Wert ab.<br/>                                                                                                                                                                                                     |
| [**Getboolarray**](id3dxbaseeffect--getboolarray.md)                                     | Ruft ein Array von booleschen Werten ab.<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | Ruft die Beschreibung des Effekts ab.<br/>                                                                                                                                                                                           |
| [**GetFloat**](id3dxbaseeffect--getfloat.md)                                             | Ruft einen Gleit Komma Wert ab.<br/>                                                                                                                                                                                           |
| [**Getfloatarray**](id3dxbaseeffect--getfloatarray.md)                                   | Ruft ein Array von Gleit Komma Werten ab.<br/>                                                                                                                                                                                |
| [**GetFunction**](id3dxbaseeffect--getfunction.md)                                       | Ruft das Handle einer Funktion ab.<br/>                                                                                                                                                                                         |
| [**Getfunctionbyname**](id3dxbaseeffect--getfunctionbyname.md)                           | Ruft das Handle einer Funktion ab, indem der zugehörige Name gesucht wird.<br/>                                                                                                                                                                  |
| [**Getfunctiondebug**](id3dxbaseeffect--getfunctiondesc.md)                               | Ruft eine Funktionsbeschreibung ab.<br/>                                                                                                                                                                                           |
| [**GetInt**](id3dxbaseeffect--getint.md)                                                 | Ruft eine ganze Zahl ab.<br/>                                                                                                                                                                                                       |
| [**Getintarray**](id3dxbaseeffect--getintarray.md)                                       | Ruft ein Array von ganzen Zahlen ab.<br/>                                                                                                                                                                                             |
| [**GetMatrix**](id3dxbaseeffect--getmatrix.md)                                           | Ruft eine nicht übersetzte Matrix ab.<br/>                                                                                                                                                                                           |
| [**Getmatrixarray**](id3dxbaseeffect--getmatrixarray.md)                                 | Ruft ein Array von nicht umsetzten Matrizen ab.<br/>                                                                                                                                                                               |
| [**Getmatrixpointerarray**](id3dxbaseeffect--getmatrixpointerarray.md)                   | Ruft ein Array von Zeigern auf nicht umgesetzte Matrizen ab.<br/>                                                                                                                                                                   |
| [**Getmatrixtransform**](id3dxbaseeffect--getmatrixtranspose.md)                         | Ruft eine umgesetzte Matrix ab.<br/>                                                                                                                                                                                              |
| [**Getmatrixtransposearray**](id3dxbaseeffect--getmatrixtransposearray.md)               | Ruft ein Array der übersetzten Matrizen ab.<br/>                                                                                                                                                                                  |
| [**Getmatrixtranspocpointerarray**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | Ruft ein Array von Zeigern auf umgesetzte Matrizen ab.<br/>                                                                                                                                                                      |
| [**GetParameter**](id3dxbaseeffect--getparameter.md)                                     | Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab.<br/>                                                                                                                                              |
| [**Getparameterbyname**](id3dxbaseeffect--getparameterbyname.md)                         | Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem der zugehörige Name gesucht wird.<br/>                                                                                                                       |
| [**Getparameterbysemantic**](id3dxbaseeffect--getparameterbysemantic.md)                 | Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem seine Semantik mit einer Suche ohne Berücksichtigung der Groß-/Kleinschreibung gesucht wird<br/>                                                                                    |
| [**Getparameterdebug**](id3dxbaseeffect--getparameterdesc.md)                             | Ruft eine Beschreibung des Parameters oder einer Anmerkung ab.<br/>                                                                                                                                                                            |
| [**Getparameterelement**](id3dxbaseeffect--getparameterelement.md)                       | Das Handle eines Array Element-Parameters erhalten.<br/>                                                                                                                                                                          |
| [**Getpass**](id3dxbaseeffect--getpass.md)                                               | Ruft das Handle eines Pass-ab.<br/>                                                                                                                                                                                             |
| [**Getpassbyname**](id3dxbaseeffect--getpassbyname.md)                                   | Ruft das Handle für einen Durchlauf ab, indem der zugehörige Name gesucht wird.<br/>                                                                                                                                                                      |
| [**Getpassde SC**](id3dxbaseeffect--getpassdesc.md)                                       | Ruft eine Pass Beschreibung ab.<br/>                                                                                                                                                                                               |
| [**Getpixelshader**](id3dxbaseeffect--getpixelshader.md)                                 | Ruft einen PixelShader ab.<br/>                                                                                                                                                                                                   |
| [**GetString**](id3dxbaseeffect--getstring.md)                                           | Ruft eine Zeichenfolge ab.<br/>                                                                                                                                                                                                         |
| [**Gettechnique**](id3dxbaseeffect--gettechnique.md)                                     | Ruft das Handle einer Technik ab.<br/>                                                                                                                                                                                        |
| [**Gettechniquebyname**](id3dxbaseeffect--gettechniquebyname.md)                         | Ruft das Handle einer Technik Durchsuchen des Namens ab.<br/>                                                                                                                                                                 |
| [**Gettechniquede SC**](id3dxbaseeffect--gettechniquedesc.md)                             | Ruft eine Technik Beschreibung ab.<br/>                                                                                                                                                                                          |
| [**GetTexture**](id3dxbaseeffect--gettexture.md)                                         | Ruft eine Textur ab.<br/>                                                                                                                                                                                                        |
| [**GetValue**](id3dxbaseeffect--getvalue.md)                                             | Den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen, erhalten. Diese Methode kann anstelle von fast allen GetXXX-aufrufen in **ID3DXBaseEffect** verwendet werden.<br/> |
| [**Getvector**](id3dxbaseeffect--getvector.md)                                           | Ruft einen Vektor ab.<br/>                                                                                                                                                                                                         |
| [**Getvector Array**](id3dxbaseeffect--getvectorarray.md)                                 | Ruft ein Array von Vektoren ab.<br/>                                                                                                                                                                                              |
| [**Getvertexshader**](id3dxbaseeffect--getvertexshader.md)                               | Ruft einen Scheitelpunkt-Shader ab.<br/>                                                                                                                                                                                                  |
| [**"Bereich"**](id3dxbaseeffect--setarrayrange.md)                                   | Legen Sie den Bereich eines Arrays fest, der an das Gerät übergeben werden soll.<br/>                                                                                                                                                                       |
| [**SetBool**](id3dxbaseeffect--setbool.md)                                               | Legt einen booleschen Wert fest.<br/>                                                                                                                                                                                                     |
| [**Setboolarray**](id3dxbaseeffect--setboolarray.md)                                     | Legt ein Array von booleschen Werten fest.<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | Legt einen Gleit Komma Wert fest.<br/>                                                                                                                                                                                           |
| [**Setfloatarray**](id3dxbaseeffect--setfloatarray.md)                                   | Legt ein Array von Gleit Komma Werten fest.<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | Legt eine ganze Zahl fest.<br/>                                                                                                                                                                                                       |
| [**"Tartintarray"**](id3dxbaseeffect--setintarray.md)                                       | Legt ein Array von ganzen Zahlen fest.<br/>                                                                                                                                                                                             |
| [**SetMatrix**](id3dxbaseeffect--setmatrix.md)                                           | Legt eine nicht übersetzte Matrix fest.<br/>                                                                                                                                                                                          |
| [**Setmatrixarray**](id3dxbaseeffect--setmatrixarray.md)                                 | Legt ein Array nicht umsetzbarer Matrizen fest.<br/>                                                                                                                                                                               |
| [**Setmatrixpointerarray**](id3dxbaseeffect--setmatrixpointerarray.md)                   | Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.<br/>                                                                                                                                                                   |
| [**Setmatrixtransform**](id3dxbaseeffect--setmatrixtranspose.md)                         | Legt eine übersetzte Matrix fest.<br/>                                                                                                                                                                                              |
| [**Setmatrixtransposearray**](id3dxbaseeffect--setmatrixtransposearray.md)               | Legt ein Array von umsetzten Matrizen fest.<br/>                                                                                                                                                                                  |
| [**Setmatrixtransposepointerarray**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | Legt ein Array von Zeigern auf umgesetzte Matrizen fest.<br/>                                                                                                                                                                      |
| [**SetString**](id3dxbaseeffect--setstring.md)                                           | Legt eine Zeichenfolge fest.<br/>                                                                                                                                                                                                         |
| [**SetTexture**](id3dxbaseeffect--settexture.md)                                         | Legt eine Textur fest.<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen. <br/>                                                                                        |
| [**Setvector**](id3dxbaseeffect--setvector.md)                                           | Legt einen Vektor fest.<br/>                                                                                                                                                                                                         |
| [**Setvector Array**](id3dxbaseeffect--setvectorarray.md)                                 | Legt ein Array von Vektoren fest.<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXBASEEFFECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Schnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
