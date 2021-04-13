---
title: gldepthrange-Funktion (GL. h)
description: Die Funktion "gldepthrange" gibt die Zuordnung von z-Werten von normalisierten Geräte Koordinaten zu Fenster Koordinaten an.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- gldepthrange-Funktion OpenGL
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
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391710"
---
# <a name="gldepthrange-function"></a>gldepthrange-Funktion

Die Funktion " **gldepthrange** " gibt die Zuordnung von *z* -Werten von normalisierten Geräte Koordinaten zu Fenster Koordinaten an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*znear* 
</dt> <dd>

Die Zuordnung der Near Clipping-Ebene zu Fenster Koordinaten. Der Standardwert ist 0 (null).

</dd> <dt>

*zfar* 
</dt> <dd>

Die Zuordnung der weit entfernten Clippingebene zu den Fenster Koordinaten. Der Standardwert ist 1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Nach dem Abschneiden und der Division durch *w* reichen die *z* -Koordinaten zwischen 0,0 und 1,0. Dies entspricht den Near-und Far-Clipping-Ebenen. Die Funktion " **gldepthrange** " gibt eine lineare Zuordnung der normalisierten *z*-Koordinaten in diesem Bereich zu Windows *z*-Koordinaten an. Unabhängig von der tatsächlichen tiefen Puffer Implementierung werden Fenster Koordinaten tiefen Werte so behandelt, als wären Sie von 0,0 bis 1,0 (z. b. Farbkomponenten). Folglich werden die von **gldepthrange** akzeptierten Werte an diesen Bereich gebunden, bevor Sie akzeptiert werden.

Die Standard Zuordnung von (0,0) ordnet die Near-Ebene 0 und die weite Ebene 1 zu. Mit dieser Zuordnung wird der tiefen Pufferbereich vollständig genutzt.

Es ist nicht erforderlich, dass *znear* kleiner als *zfar* ist. Umgekehrte Zuordnungen wie (1, 0) sind zulässig.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **gldepthrange** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ tiefen \_ Bereich

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

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





