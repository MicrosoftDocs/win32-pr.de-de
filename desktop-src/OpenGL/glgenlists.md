---
title: glgenlists-Funktion (GL. h)
description: Die Funktion "glgenlists" generiert einen zusammenhängenden Satz leerer Anzeigelisten.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- glgenlists-Funktion OpenGL
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
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740480"
---
# <a name="glgenlists-function"></a>glgenlists-Funktion

Die Funktion " **glgenlists** " generiert einen zusammenhängenden Satz leerer Anzeigelisten.

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

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | der *Bereich* war negativ.<br/>                                                                                                      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgenlists** " weist ein Argument *auf.* Er gibt eine ganze Zahl *n* zurück, die den *Bereich* zusammenhängender leerer Anzeigelisten mit dem Namen *n*, *n* + 1, enthält. . ., *n* + (*Bereich* -1), werden erstellt. Wenn *Range* gleich 0 (null) ist, wenn keine *Gruppe von zusammen* hängenden Namen verfügbar ist oder wenn ein Fehler generiert wird, werden keine anzeigen Listen generiert und NULL zurückgegeben.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glgenlists** ab:

[**glislist**](glislist.md)

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

[**glislist**](glislist.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> </dl>

 

 





