---
title: glGetString-Funktion (Gl.h)
description: Die glGetString-Funktion gibt eine Zeichenfolge zurück, die die aktuelle OpenGL-Verbindung beschreibt.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cbc5a1add320d711c92020074b3de810d134e88953a8413c0efd2e6b6fdd954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359909"
---
# <a name="glgetstring-function"></a>glGetString-Funktion

Die **glGetString-Funktion** gibt eine Zeichenfolge zurück, die die aktuelle OpenGL-Verbindung beschreibt.

## <a name="syntax"></a>Syntax


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Eine der folgenden symbolischen Konstanten.



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**GL \_ VENDOR**</dt> </dl>             | Gibt das Unternehmen zurück, das für diese OpenGL-Implementierung verantwortlich ist. Dieser Name ändert sich nicht von Release zu Release.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**\_GL-RENDERER**</dt> </dl>       | Gibt den Namen des Renderers zurück. Dieser Name ist in der Regel spezifisch für eine bestimmte Konfiguration einer Hardwareplattform. Es ändert sich nicht von Release zu Release.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**\_GL-VERSION**</dt> </dl>          | Gibt eine Version oder Releasenummer zurück.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**\_GL-ERWEITERUNGEN**</dt> </dl> | Gibt eine durch Leerzeichen getrennte Liste der unterstützten Erweiterungen für OpenGL zurück.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *name* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetString-Funktion** gibt einen Zeiger auf eine statische Zeichenfolge zurück, die einen Aspekt der aktuellen OpenGL-Verbindung beschreibt.

Da OpenGL keine Abfragen für die Leistungsmerkmale einer Implementierung enthält, wird erwartet, dass einige Anwendungen geschrieben werden, um bekannte Plattformen zu erkennen, und ihre OpenGL-Nutzung basierend auf bekannten Leistungsmerkmalen dieser Plattformen ändern. Die Zeichenfolgen GL VENDOR und GL RENDERER geben zusammen eindeutig eine Plattform an und ändern sich nicht \_ \_ von Release zu Release. Sie sollten als solche von Plattformerkennungsalgorithmen verwendet werden.

Das Format und der Inhalt der Zeichenfolge, die **glGetString** zurückgibt, hängen von der Implementierung ab, mit der Ausnahme, dass:

-   Erweiterungsnamen enthalten keine Leerzeichen und werden durch Leerzeichen in der GL \_ EXTENSIONS-Zeichenfolge getrennt.
-   Die GL \_ VERSION-Zeichenfolge beginnt mit einer Versionsnummer. Die Versionsnummer verwendet eine der folgenden Formen:

    *\_ Hauptnummer*. *\_ Nebennummer*

    *\_ Hauptnummer*. *\_ Nebennummer*. *\_ Releasenummer*

-   Anbieterspezifische Informationen können der Versionsnummer folgen. Das Format hängt von der Implementierung ab, aber ein Leerzeichen trennt immer die Versionsnummer und die herstellerspezifischen Informationen.
-   Alle Zeichenfolgen werden mit NULL beendet.

Wenn ein Fehler generiert wird, **gibt glGetString 0** (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





