---
title: gluerrorstring-Funktion (glu. h)
description: Die Funktion "gluerrorstring" erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode. Die Fehler Zeichenfolge ist nur ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluerrorstring-Funktion OpenGL
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
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741120"
---
# <a name="gluerrorstring-function"></a>gluerrorstring-Funktion

Die Funktion " **gluerrorstring** " erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode. Die Fehler Zeichenfolge ist nur ANSI.

## <a name="syntax"></a>Syntax


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Errcode* 
</dt> <dd>

Ein OpenGL-oder glu-Fehlercode.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluerrorstring** " erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode. Die Zeichenfolge weist ein ISO Latin 1-Format auf. Beispielsweise gibt " **gluerrorstring**(GL \_ out \_ of \_ Memory)" die Zeichenfolge "nicht genügend Arbeitsspeicher" zurück.

Die standardmäßigen glu-Fehlercodes lauten "glu \_ invalid \_ enum", "glu \_ invalid value" und "glu" aus dem Arbeits \_ \_ \_ \_ Speicher. Bestimmte andere glu-Funktionen können spezielle Fehlercodes durch Rückrufe zurückgeben. Eine Liste der OpenGL-Fehlercodes finden Sie unter [**glgeterror**](glgeterror.md).

Die Funktion " **gluerrorstring** " erzeugt Fehler Zeichenfolgen nur in ANSI. Verwenden Sie nach Möglichkeit " **gluerrorstringwin**", das ANSI-oder Unicode-Fehler Zeichenfolgen zulässt. Dadurch ist es einfacher, Ihr Programm für die Verwendung mit einer anderen Sprache zu lokalisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glgeterror**](glgeterror.md)
</dt> <dt>

[*glunurbscallback*](glunurbs.md)
</dt> <dt>

[*gluvierccallback*](gluquadric.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> </dl>

 

 





