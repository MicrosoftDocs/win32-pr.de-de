---
title: glHint-Funktion (Gl.h)
description: Die glHint-Funktion gibt implementierungsspezifische Hinweise an.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint-Funktion OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7602b4f0af35c8bc9aeb38cdcb613e30ded907ced75e2241c8ed9e23b57fd98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359646"
---
# <a name="glhint-function"></a>glHint-Funktion

Die **glHint-Funktion** gibt implementierungsspezifische Hinweise an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Eine symbolische Konstante, die das zu steuernde Verhalten angibt. Die folgenden symbolischen Konstanten werden zusammen mit vorgeschlagener Semantik akzeptiert.



| Wert                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**\_ \_ GL-HINWEIS**</dt> </dl>                                                           | Gibt die Genauigkeit der Berechnung des Berechnungszeichens an. Wenn die Berechnung des Pro-Pixel-Knotens von der OpenGL-Implementierung nicht effizient unterstützt wird, kann ein Hinweis auf GL \_ DONT \_ CARE oder GL FASTEST zu einer \_ Pro-Scheitelpunkt-Berechnung von Effekten führen.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**GL \_ LINE \_ SMOOTH \_ HINT**</dt> </dl>                                  | Gibt die Stichprobenqualität von Antialiasinglinien an. Ein Hinweis auf GL \_ NICEST kann dazu führen, dass während der Rasterung mehr Pixelfragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**GL \_ PERSPECTIVE \_ CORRECTION \_ HINT**</dt> </dl> | Gibt die Qualität der Farb- und Texturkoordinateninterpolation an. Wenn die perspektivisch korrigierte Parameterinterpolation von der OpenGL-Implementierung nicht effizient unterstützt wird, kann das Angeben von GL \_ DONT \_ CARE oder GL FASTEST zu einer \_ einfachen linearen Interpolation von Farben und/oder Texturkoordinaten führen.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**GL \_ POINT \_ SMOOTH \_ HINT**</dt> </dl>                               | Gibt die Stichprobenqualität von Antialiasingpunkten an. Ein Hinweis auf GL \_ NICEST kann dazu führen, dass während der Rasterung mehr Pixelfragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**GL \_ POLYGON \_ SMOOTH \_ HINT**</dt> </dl>                         | Gibt die Stichprobenqualität von antialiasierten Polygonen an. Ein Hinweis auf GL \_ NICEST kann dazu führen, dass während der Rasterung mehr Pixelfragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Eine symbolische Konstante, die das gewünschte Verhalten angibt. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                       | Bedeutung                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ FASTEST**</dt> </dl>        | Die effizienteste Option sollte ausgewählt werden.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL \_ NICEST**</dt> </dl>           | Die richtige oder höchste Qualität sollte ausgewählt werden.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL \_ DONT \_ CARE**</dt> </dl> | Der Client hat keine Präferenz.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *mode* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Wenn Interpretationsmöglichkeiten vorhanden sind, können Sie bestimmte Aspekte des OpenGL-Verhaltens mit Hinweisen steuern. Sie geben einen Hinweis mit zwei Argumenten an. Der *Zielparameter* ist eine symbolische Konstante, die das zu steuernde Verhalten angibt, und *mode* ist eine weitere symbolische Konstante, die das gewünschte Verhalten angibt.

Obwohl die Implementierungsaspekte, die hinweise können, klar definiert sind, hängt die Interpretation der Hinweise von der Implementierung ab.

Die **glHint-Funktion** kann ignoriert werden.

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

[**glEnd**](glend.md)
</dt> </dl>

 

 





