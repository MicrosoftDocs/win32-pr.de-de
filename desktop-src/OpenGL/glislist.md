---
title: glislist-Funktion (GL. h)
description: Die gllslist-Funktion testet, ob die Anzeigeliste vorhanden ist.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- glislist-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341037"
---
# <a name="glislist-function"></a>glislist-Funktion

Die **gllslist** -Funktion testet, ob die Anzeigeliste vorhanden ist.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*list* 
</dt> <dd>

Ein potenzieller Anzeigelisten Name.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **gllslist** -Funktion gibt "GL true" zurück, \_ Wenn " *List* " der Name einer Anzeigeliste ist und andernfalls "GL false" zurückgibt \_ .

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

[**gldelta etelists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgenlists**](glgenlists.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> </dl>

 

 





