---
title: glViewport-Funktion (Gl.h)
description: Die glViewport-Funktion legt den Viewport fest.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport-Funktion OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70fc727265ce4af1db2be808ae7eee3f59246874659a815c66292bcab3d7ecfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035405"
---
# <a name="glviewport-function"></a>glViewport-Funktion

Die **glViewport-Funktion** legt den Viewport fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die linke untere Ecke des Viewportrechtecks in Pixel. Der Standardwert ist (0,0).

</dd> <dt>

*y* 
</dt> <dd>

Die linke untere Ecke des Viewportrechtecks in Pixel. Der Standardwert ist (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Viewports. Wenn ein OpenGL-Kontext zum ersten Mal an ein Fenster angefügt *wird,* werden Breite und *Höhe* auf die Abmessungen dieses Fensters festgelegt.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Viewports. Wenn ein OpenGL-Kontext zum ersten Mal an ein Fenster angefügt *wird,* werden Breite und *Höhe* auf die Abmessungen dieses Fensters festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Breite *oder* *Höhe waren* negativ.<br/>                                                                                   |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glViewport-Funktion** gibt die affine Transformation von *x* und *y* von normalisierten Gerätekoordinaten zu Fensterkoordinaten an. Lassen Sie (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) normalisierte Gerätekoordinaten sein. Die Fensterkoordinaten (*x*<sub>w</sub> , *y*<sub>w</sub> ) werden dann wie folgt berechnet:

![Gleichung, die die Berechnung der Fensterkoordinaten zeigt.](images/view01.png)

Breite und Höhe des Viewports werden im Hintergrund an einen Bereich geklammert, der von der Implementierung abhängt. Dieser Bereich wird abgefragt, indem **glGet mit dem** Argument GL \_ MAX \_ VIEWPORT \_ DIMSgefragt wird.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glViewport ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ VIEWPORT

**glGet** mit argument GL \_ MAX \_ VIEWPORT \_ DIMS

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

[**glDepthRange**](gldepthrange.md)
</dt> </dl>

 

 





