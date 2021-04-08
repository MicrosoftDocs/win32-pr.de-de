---
title: glgetstring-Funktion (GL. h)
description: Die glgetstring-Funktion gibt eine Zeichenfolge zurück, die die aktuelle OpenGL-Verbindung beschreibt.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glgetstring-Funktion OpenGL
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
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957079"
---
# <a name="glgetstring-function"></a>glgetstring-Funktion

Die **glgetstring** -Funktion gibt eine Zeichenfolge zurück, die die aktuelle OpenGL-Verbindung beschreibt.

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
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**GL- \_ Hersteller**</dt> </dl>             | Gibt das für diese OpenGL-Implementierung verantwortliche Unternehmen zurück. Dieser Name ändert sich nicht von Release zu Release.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**GL- \_ Renderer**</dt> </dl>       | Gibt den Namen des Renderers zurück. Dieser Name ist in der Regel spezifisch für eine bestimmte Konfiguration einer Hardwareplattform. Es ändert sich nicht von Release zu Release.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**GL- \_ Version**</dt> </dl>          | Gibt eine Version oder eine Releasenummer zurück.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**GL- \_ Erweiterungen**</dt> </dl> | Gibt eine durch Leerzeichen getrennte Liste der unterstützten Erweiterungen für OpenGL zurück.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Name* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetstring** " gibt einen Zeiger auf eine statische Zeichenfolge zurück, die einen Aspekt der aktuellen OpenGL-Verbindung beschreibt.

Da OpenGL keine Abfragen für die Leistungsmerkmale einer Implementierung enthält, wird erwartet, dass einige Anwendungen so geschrieben werden, dass Sie bekannte Plattformen erkennen und ihre OpenGL-Verwendung basierend auf bekannten Leistungsmerkmalen dieser Plattformen verändern. Der Hersteller der Zeichen folgen GL \_ und der GL- \_ Renderer geben eine Plattform eindeutig an und werden nicht von Release zu Release geändert. Sie sollten wie bei Platt Form Erkennungsalgorithmen verwendet werden.

Das Format und der Inhalt der Zeichenfolge, die von " **glgetstring** " zurückgegeben wird, hängt von der Implementierung ab, ausgenommen:

-   Erweiterungs Namen enthalten keine Leerzeichen und werden durch Leerzeichen in der GL- \_ Erweiterungs Zeichenfolge getrennt.
-   Die Zeichenfolge der GL- \_ Version beginnt mit einer Versionsnummer. Die Versionsnummer verwendet eines der folgenden Formen:

    *Haupt \_ Nummer*. *neben \_ Nummer*

    *Haupt \_ Nummer*. *neben \_ Nummer*. *Freigabe \_ Nummer*

-   Herstellerspezifische Informationen können der Versionsnummer folgen. Das Format hängt von der Implementierung ab, aber ein Speicherplatz trennt immer die Versionsnummer und die herstellerspezifischen Informationen.
-   Alle Zeichen folgen werden mit Null beendet.

Wenn ein Fehler generiert wird, gibt " **glgetstring** " 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





