---
title: glDepthRange-Funktion (Gl.h)
description: Die glDepthRange-Funktion gibt die Zuordnung von Z-Werten von normalisierten Gerätekoordinaten zu Fensterkoordinaten an.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac72155449e70a59265e4ffd2576245059a547906092df2a932e84f221e48fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081650"
---
# <a name="gldepthrange-function"></a>glDepthRange-Funktion

Die **glDepthRange-Funktion** gibt die Zuordnung von *Z-Werten* von normalisierten Gerätekoordinaten zu Fensterkoordinaten an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*zNear* 
</dt> <dd>

Die Zuordnung der Nahezu-Clippingebene zu Fensterkoordinaten. Der Standardwert ist 0 (null).

</dd> <dt>

*zFar* 
</dt> <dd>

Die Zuordnung der fernen Clippingebene zu Fensterkoordinaten. Der Standardwert ist 1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Nach dem Clipping und der Division durch *w* liegen *die Z-Koordinaten* zwischen 0,0 und 1,0, was den mittleren und fernen Clippingebenen entspricht. Die **glDepthRange-Funktion** gibt eine lineare Zuordnung der normalisierten *z-Koordinaten* in diesem Bereich zum Fenster *z*-coordinates an. Unabhängig von der tatsächlichen Implementierung des Tiefenpuffers werden Die Tiefenwerte der Fensterkoordinaten so behandelt, als ob sie zwischen 0,0 und 1,0 liegen (z. B. Farbkomponenten). Daher werden die von **glDepthRange** akzeptierten Werte an diesen Bereich gebunden, bevor sie akzeptiert werden.

Die Standardzuordnung von (0,1) ordnet die Nahebene 0 und die ferne Ebene 1 zu. Mit dieser Zuordnung wird der Tiefenpufferbereich vollständig ausgelastet.

Es ist nicht erforderlich, dass *zNear* kleiner als *zFar* ist. Umgekehrte Zuordnungen wie (1,0) sind akzeptabel.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glDepthRange** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ DEPTH \_ RANGE

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





