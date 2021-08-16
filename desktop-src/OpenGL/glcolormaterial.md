---
title: glColorMaterial-Funktion (Gl.h)
description: Die glColorMaterial-Funktion bewirkt, dass eine Materialfarbe die aktuelle Farbe nachverfolgt.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55cc846cfbc400d2372186f9af4a09db08e5ad769d1e8fec5f5f6f757e1ff447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360471"
---
# <a name="glcolormaterial-function"></a>glColorMaterial-Funktion

Die **glColorMaterial-Funktion** bewirkt, dass eine Materialfarbe die aktuelle Farbe nachverfolgt.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Gibt an, ob die materiale Parameter front, back oder front und back die aktuelle Farbe nachverfolgen sollen. Akzeptierte Werte sind GL \_ FRONT, GL \_ BACK und GL FRONT AND \_ \_ \_ BACK. Der Standardwert ist GL \_ FRONT \_ AND \_ BACK.

</dd> <dt>

*mode* 
</dt> <dd>

Gibt an, welcher von mehreren Materialparametern die aktuelle Farbe nachverfolgt. Akzeptierte Werte sind GL \_ AMBIENT, GL \_ AMBIENT, GL \_ DIFFUSE, GL \_ SPECULAR und GL \_ AMBIENT UND \_ \_ DIFFUSE. Der Standardwert ist GL \_ AMBIENT \_ UND \_ DIFFUSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *face* oder *mode* war kein akzeptierter Wert.<br/>                                                                                |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glColorMaterial-Funktion** gibt an, welche Materialparameter die aktuelle Farbe nachverfolgen. Wenn Sie GL COLOR MATERIAL aktivieren, wird die aktuelle Farbe für jedes material oder material, das bzw. das durch das Gesicht angegeben wird, durch den vom Modus angegebenen Materialparameter oder Parameter \_ \_ jederzeit nachverfolgt.   Aktivieren und deaktivieren Sie GL COLOR MATERIAL mit den Funktionen \_ \_ [**glEnable**](glenable.md) und [**glDisable**](gldisable.md), die Sie mit GL \_ COLOR MATERIAL als Argument \_ aufrufen. Standardmäßig ist GL \_ COLOR \_ MATERIAL deaktiviert.

Mit **glColorMaterial** können Sie eine Teilmenge von Materialparametern für jeden Scheitelpunkt ändern, indem Sie nur die [**glColor-Funktion**](glcolor-functions.md) verwenden, ohne [**glMaterial auf aufruft.**](glmaterial-functions.md) Wenn Sie nur eine solche Teilmenge von Parametern für jeden Scheitelpunkt angeben möchten, ist es besser, **glColorMaterial** als **glMaterial zu verwenden.**

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glColorMaterial ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ COLOR \_ MATERIAL \_ PARAMETER

**glGet** mit argument GL \_ COLOR \_ MATERIAL \_ FACE

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ COLOR \_ MATERIAL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





