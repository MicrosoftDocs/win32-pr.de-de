---
title: glViewport-Funktion (GL. h)
description: Die Funktion "glViewport" legt den Viewport fest.
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
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104559284"
---
# <a name="glviewport-function"></a>glViewport-Funktion

Die Funktion " **glViewport** " legt den Viewport fest.

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

Die Breite des Viewports. Wenn ein OpenGL-Kontext zum ersten Mal an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Viewports. Wenn ein OpenGL-Kontext zum ersten Mal an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glViewport** " gibt die affine Transformation von *x* und *y* von normalisierten Geräte Koordinaten zu Fenster Koordinaten an. Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sind normalisierte Geräte Koordinaten. Die Fenster Koordinaten (*x*<sub>w</sub> , *y*<sub>w</sub> ) werden dann wie folgt berechnet:

![Gleichung, die die Berechnung der Fenster Koordinaten anzeigt.](images/view01.png)

Breite und Höhe des Viewports werden automatisch an einen Bereich gebunden, der von der Implementierung abhängt. Dieser Bereich wird durch Aufrufen von **glget** mit dem Argument GL \_ Max \_ Viewport \_ DiMS abgefragt.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glViewport** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Viewport

**glget** mit dem Argument GL \_ Max \_ Viewport \_ DiMS

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

[**gldepthrange**](gldepthrange.md)
</dt> </dl>

 

 





