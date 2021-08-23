---
title: gluProject-Funktion (Glu.h)
description: Die gluProject-Funktion ordnet Objektkoordinaten Fensterkoordinaten zu.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324f6c896c225453bfc8bf2ebb4b8619707c498c75e1309ea24fc6557cdd3deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488809"
---
# <a name="gluproject-function"></a>gluProject-Funktion

Die **gluProject-Funktion** ordnet Objektkoordinaten Fensterkoordinaten zu.

## <a name="syntax"></a>Syntax


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objx* 
</dt> <dd>

Die x-Objektkoordinate.

</dd> <dt>

*objy* 
</dt> <dd>

Die y-Objektkoordinate.

</dd> <dt>

*objz* 
</dt> <dd>

Die z-Objektkoordinate.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Die aktuelle ModelView-Matrix (wie bei einem [**glGetDoublev-Aufruf).**](glgetdoublev.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

Die aktuelle Projektionsmatrix (wie bei einem **glGetDoublev-Aufruf).**

</dd> <dt>

*Ansichtsfenster* 
</dt> <dd>

Der aktuelle Viewport (wie bei einem [**glGetIntegerv-Aufruf).**](glgetintegerv.md)

</dd> <dt>

*Winx* 
</dt> <dd>

Die berechnete x-Fensterkoordinate.

</dd> <dt>

*winy* 
</dt> <dd>

Die berechnete y-Fensterkoordinate.

</dd> <dt>

*winz* 
</dt> <dd>

Die berechnete Z-Fensterkoordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert GL \_ TRUE.

Wenn die Funktion fehlschlägt, ist der Rückgabewert GL \_ FALSE.

## <a name="remarks"></a>Hinweise

Die **gluProject-Funktion** transformiert die angegebenen Objektkoordinaten mithilfe von *modelMatrix,* *projMatrix* und viewport in *Fensterkoordinaten.* Das Ergebnis wird in *winx*, *winy* und *winz gespeichert.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





