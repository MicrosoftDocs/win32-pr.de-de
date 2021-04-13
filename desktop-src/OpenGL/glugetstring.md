---
title: glugetstring-Funktion (glu. h)
description: Die Funktion "glugetstring" Ruft eine Zeichenfolge ab, die die glu-Versionsnummer oder unterstützte glu-Erweiterungs Aufrufe beschreibt.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- glugetstring-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391813"
---
# <a name="glugetstring-function"></a>glugetstring-Funktion

Die Funktion " **glugetstring** " Ruft eine Zeichenfolge ab, die die glu-Versionsnummer oder unterstützte glu-Erweiterungs Aufrufe beschreibt.

## <a name="syntax"></a>Syntax


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Entweder die Versionsnummer von Glu (GLU \_ Version) oder die verfügbaren herstellerspezifischen Erweiterungs Aufrufe (GLU \_ Extensions).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glugetstring** " gibt einen Zeiger auf eine statische, auf NULL endenden Zeichenfolge zurück. Wenn *Name* den Wert "- \_ Version" hat, ist die zurückgegebene Zeichenfolge ein Wert, der die Versionsnummer von Glu darstellt. Das Format der Versionsnummer lautet wie folgt:

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

Die Versionsnummer hat das Format "Haupt \_ Nummer. neben \_ Nummer" oder "Haupt \_ Nummer. neben \_ Version. \_ Releasenummer". Die anbieterspezifischen Informationen sind optional, und das Format und der Inhalt hängen von der Implementierung ab.

Wenn *Name* der Wert "-Erweiterungen" ist \_ , enthält die zurückgegebene Zeichenfolge eine Liste mit Namen unterstützter glu-Erweiterungen, die durch Leerzeichen getrennt sind. Das Format der zurückgegebenen Liste von Namen lautet wie folgt:

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

Die Erweiterungs Namen dürfen keine Leerzeichen enthalten.

Die Funktion " **glugetstring** " ist gültig für die Version 1,1 oder höher.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





