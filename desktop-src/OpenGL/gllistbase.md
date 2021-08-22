---
title: glListBase-Funktion (Gl.h)
description: Die glListBase-Funktion legt die Basis der Anzeigeliste für glCallLists fest.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- glListBase-Funktion OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba7cbe7b179184efa739ac3492f4e74b36f56abe0f02498a0e1a688b85183a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938517"
---
# <a name="gllistbase-function"></a>glListBase-Funktion

Die **glListBase-Funktion** legt die Basis der Anzeigeliste für **glCallLists fest.**

## <a name="syntax"></a>Syntax


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*base* 
</dt> <dd>

Ein ganzzahliger Offset, der [**glCallLists-Offsets**](glcalllists.md) hinzugefügt wird, um Anzeigelistennamen zu generieren. Der Anfangswert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glListBase-Funktion** gibt ein Array von Offsets an. Anzeigelistennamen werden durch Hinzufügen der *Basis zu* jedem Offset generiert. Namen, die auf gültige Anzeigelisten verweisen, werden ausgeführt. andere werden ignoriert.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glListBase ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ LIST \_ BASE

## <a name="requirements"></a>Anforderungen



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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





