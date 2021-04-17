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
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388105"
---
# <a name="user-defined-type"></a>Benutzerdefinierter Typ

Verwenden Sie die folgende Syntax, um einen benutzerdefinierten Typ zu deklarieren.



|                                           |
|-------------------------------------------|
| typedef konstanter **\[ \] Typname \[ \] Index**; |



 

## <a name="parameters"></a>Parameter



| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[const\]**<br/>                 | Optional. Dieses Schlüsselwort kennzeichnet den Typ explizit als Konstante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**<br/>     | Identifiziert den Datentyp. muss einer der systeminternen HLSL-Datentypen sein.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Sin**<br/> | Optionale Array Größe. Muss eine ganze Zahl ohne Vorzeichen zwischen 1 und 4 sein.<br/> |



 

Neben den integrierten systeminternen Datentypen unterstützt HLSL benutzerdefinierte oder benutzerdefinierte Typen, die dieser Syntax folgen:

## <a name="remarks"></a>Bemerkungen

Bei benutzerdefinierten Typen wird die Groß-/Kleinschreibung nicht beachtet. Die folgenden Typen werden aus Gründen der Unterstützung automatisch in einem Superglobalen Gültigkeitsbereich definiert.


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



Das Nummern Zeichen ( \# ) stellt eine ganzzahlige Ziffer zwischen 1 und 4 dar.

Aus Kompatibilitätsgründen mit DirectX 8-Effekten werden die folgenden Typen automatisch im superglobalen Bereich definiert:


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

 

 





