---
title: glDeleteLists-Funktion (Gl.h)
description: Die glDeleteLists-Funktion löscht eine zusammenhängende Gruppe von Anzeigelisten.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ec0ffac68119f6f2080ef6ca96ec63fbd35176d3541464a89b6c31f4941b4c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081660"
---
# <a name="gldeletelists-function"></a>glDeleteLists-Funktion

Die **glDeleteLists-Funktion** löscht eine zusammenhängende Gruppe von Anzeigelisten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*list* 
</dt> <dd>

Der ganzzahlige Name der ersten zu löschende Anzeigeliste.

</dd> <dt>

*range* 
</dt> <dd>

Die Anzahl der zu löschende Anzeigelisten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *der Bereich* war negativ.<br/>                                                                                                      |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glDeleteLists-Funktion** bewirkt, dass eine zusammenhängende Gruppe von Anzeigelisten gelöscht wird. Der *list-Parameter* ist der Name der ersten zu löschenden Anzeigeliste, und *range* ist die Anzahl der zu löschenden Anzeigelisten. Alle Anzeigelisten *d* mit *list*  =  *d*  =  *list*  +  *range* - 1 werden gelöscht.

Alle Speicherorte, die den angegebenen Anzeigelisten zugeordnet sind, werden freigegeben, und die Namen können zu einem späteren Zeitpunkt wiederverwendet werden. Namen innerhalb des Bereichs, denen keine Anzeigeliste zugeordnet ist, werden ignoriert. Wenn *der Bereich* 0 (null) ist, geschieht nichts.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





