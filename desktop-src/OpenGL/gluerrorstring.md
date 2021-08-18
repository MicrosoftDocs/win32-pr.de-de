---
title: gluErrorString-Funktion (Glu.h)
description: Die funktion gluErrorString erzeugt eine Fehlerzeichenfolge aus einem OpenGL- oder GLU-Fehlercode. Die Fehlerzeichenfolge ist nur ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beef90cfced2b33b612e15c1ef6918de81997520483acfb141f3a307ad64096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777650"
---
# <a name="gluerrorstring-function"></a>gluErrorString-Funktion

Die **funktion gluErrorString** erzeugt eine Fehlerzeichenfolge aus einem OpenGL- oder GLU-Fehlercode. Die Fehlerzeichenfolge ist nur ANSI.

## <a name="syntax"></a>Syntax


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errCode* 
</dt> <dd>

Ein OpenGL- oder GLU-Fehlercode.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **funktion gluErrorString** erzeugt eine Fehlerzeichenfolge aus einem OpenGL- oder GLU-Fehlercode. Die Zeichenfolge hat ein ISO Latin 1-Format. Beispielsweise gibt **gluErrorString**(GL \_ OUT OF \_ \_ MEMORY) die Zeichenfolge "nicht genügend Arbeitsspeicher" zurück.

Die Standardmäßigen GLU-Fehlercodes sind GLU \_ INVALID \_ ENUM, GLU \_ INVALID VALUE und GLU OUT OF \_ \_ \_ \_ MEMORY. Bestimmte andere GLU-Funktionen können spezielle Fehlercodes über Rückrufe zurückgeben. Die Liste der OpenGL-Fehlercodes finden Sie unter [**glGetError**](glgeterror.md).

Die **funktion gluErrorString** erzeugt nur Fehlerzeichenfolgen in ANSI. Verwenden Sie nach Möglichkeit **gluErrorStringWIN,** wodurch ANSI- oder Unicode-Fehlerzeichenfolgen zulässig sind. Dadurch ist es einfacher, Ihr Programm für die Verwendung mit einer anderen Sprache zu lokalisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





