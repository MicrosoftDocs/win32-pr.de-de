---
title: gldelta etelists-Funktion (GL. h)
description: Die Funktion "gldelta etelists" löscht eine zusammenhängende Gruppe von Anzeigelisten.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- gldelta etelists-Funktion OpenGL
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
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339335"
---
# <a name="gldeletelists-function"></a>gldelta etelists-Funktion

Die Funktion " **gldelta etelists** " löscht eine zusammenhängende Gruppe von Anzeigelisten.

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

Der ganzzahlige Name der ersten zu löschenden Anzeigeliste.

</dd> <dt>

*range* 
</dt> <dd>

Die Anzahl der zu löschenden Anzeigelisten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | der *Bereich* war negativ.<br/>                                                                                                      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **gldelta etelists** " bewirkt, dass eine zusammenhängende Gruppe von Anzeigelisten gelöscht wird. Der *List* -Parameter ist der Name der ersten zu löschenden Anzeigeliste, und *Range* steht für die Anzahl der zu löschenden Anzeigelisten. Alle Anzeigelisten *d* mit *Listen*  =    =    +  *Bereich* -1 werden gelöscht.

Alle Speicherorte, die den angegebenen anzeigen Listen zugeordnet sind, werden freigegeben, und die Namen können zu einem späteren Zeitpunkt wieder verwendet werden. Namen innerhalb des Bereichs, die keine zugeordnete Anzeigeliste aufweisen, werden ignoriert. Wenn *Range* gleich NULL ist, geschieht nichts.

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glcalllists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgenlists**](glgenlists.md)
</dt> <dt>

[**glislist**](glislist.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> </dl>

 

 





