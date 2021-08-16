---
title: glGenLists-Funktion (Gl.h)
description: Die glGenLists-Funktion generiert einen zusammenhängenden Satz leerer Anzeigelisten.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- glGenLists-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a916b163f2ec04e51da06263aed0f76f5e4dd6b51b7eca9fdbca8965644fdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360397"
---
# <a name="glgenlists-function"></a>glGenLists-Funktion

Die **glGenLists-Funktion** generiert einen zusammenhängenden Satz leerer Anzeigelisten.

## <a name="syntax"></a>Syntax


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*range* 
</dt> <dd>

Die Anzahl der zusammenhängenden leeren Anzeigelisten, die generiert werden sollen.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *bereich* war negativ.<br/>                                                                                                      |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGenLists-Funktion** verfügt über ein Argument, *den Bereich*. Sie gibt eine ganze *Zahl n zurück,* die den Bereich *zusammenhängender* leerer Anzeigelisten mit den Namen *n*, *n* + 1, angibt. . ., *n* + (*Bereich* - 1) werden erstellt. Wenn *der* Bereich 0 (null) ist, keine Gruppe zusammenhängender Bereichsnamen verfügbar ist oder ein Fehler generiert wird, werden keine Anzeigelisten generiert und 0 (null) zurückgegeben. 

Die folgende Funktion ruft Informationen im Zusammenhang mit **glGenLists ab:**

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





