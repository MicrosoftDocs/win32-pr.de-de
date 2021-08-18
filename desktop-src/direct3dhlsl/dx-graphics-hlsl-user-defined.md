---
title: Benutzerdefinierter Typ
description: Verwenden Sie die folgende Syntax, um einen benutzerdefinierten Typ zu deklarieren.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee73cd5afcda15bcc821d7fea5b648924829d483a33b9c67c140eed0b100e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789310"
---
# <a name="user-defined-type"></a>Benutzerdefinierter Typ

Verwenden Sie die folgende Syntax, um einen benutzerdefinierten Typ zu deklarieren.



|                                           |
|-------------------------------------------|
| typedef **\[ const \] Type Name \[ Index \]**; |



 

## <a name="parameters"></a>Parameter



| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[Const\]**<br/>                 | Optional. Dieses Schlüsselwort markiert den Typ explizit als Konstante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Typ**<br/>     | Identifiziert den Datentyp. muss einer der systeminternen HLSL-Datentypen sein.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**<br/> | Optionale Arraygröße. Muss eine ganze Zahl ohne Vorzeichen zwischen 1 und 4 (einschließlich) sein.<br/> |



 

Zusätzlich zu den integrierten systeminternen Datentypen unterstützt HLSL benutzerdefinierte oder benutzerdefinierte Typen, die dieser Syntax folgen:

## <a name="remarks"></a>Hinweise

Bei benutzerdefinierten Typen wird die Groß-/Kleinschreibung nicht beachtet. Der Einfachheit halber werden die folgenden Typen automatisch im globalen Bereich definiert.


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



Das Nummernzeichen ( \# ) stellt eine ganzzahlige Ziffer zwischen 1 und 4 dar.

Aus Gründen der Kompatibilität mit DirectX 8-Effekten werden die folgenden Typen automatisch im globalen Bereich definiert:


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





