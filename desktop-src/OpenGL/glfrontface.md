---
title: glFrontFace-Funktion (Gl.h)
description: Die glFrontFace-Funktion definiert nach vorne gerichtete und zurück gerichtete Polygone.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d288b4e6380ab845af9a05381963444e28ddf50739ecd3f5563d9f2dc729fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580160"
---
# <a name="glfrontface-function"></a>glFrontFace-Funktion

Die **glFrontFace-Funktion** definiert nach vorne gerichtete und zurück gerichtete Polygone.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die Ausrichtung von polygonen nach vorn gerichteten Polygonen. GL \_ CW und GL \_ CCW werden akzeptiert. Der Standardwert ist GL \_ CCW.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

In einer Szene, die vollständig aus undurchsichtigen geschlossenen Oberflächen besteht, sind hintere Polygone nie sichtbar. Das Beseitigen dieser unsichtbaren Polygone hat den offensichtlichen Vorteil, dass das Rendern des Bilds beschleunigt wird. Sie aktivieren und deaktivieren die Beseitigung von nach hinten gerichteten Polygonen mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ CULL \_ FACE.

Die Projektion eines Polygons auf Fensterkoordinaten wird als im Uhrzeigersinn gewindet bezeichnet, wenn ein imaginäres Objekt, das dem Pfad vom ersten Scheitelpunkt, dem zweiten Scheitelpunkt und so weiter folgt, bis zum letzten Scheitelpunkt und schließlich zurück zum ersten Vertex im Uhrzeigersinn um das Innere des Polygons bewegt wird. Die Windung des Polygons wird als gegen den Uhrzeigersinn bezeichnet, wenn sich das imaginäre Objekt, das demselben Pfad folgt, gegen den Uhrzeigersinn um das Innere des Polygons bewegt. Die **glFrontFace-Funktion** gibt an, ob Polygone mit im Uhrzeigersinn in Fensterkoordinaten oder gegen den Uhrzeigersinn gerichteten Windungen in Fensterkoordinaten nach vorne gerichtet werden. Beim Übergeben von GL \_ CCW *an den Modus* werden Polygone gegen den Uhrzeigersinn als front-facing ausgewählt. GL \_ CW wählt Polygone im Uhrzeigersinn als front-facing aus. Standardmäßig werden Polygone gegen den Uhrzeigersinn als front-orientierte Polygone verwendet.

Die folgende Funktion ruft Informationen zu **glFrontface ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ FRONT \_ FACE

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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





