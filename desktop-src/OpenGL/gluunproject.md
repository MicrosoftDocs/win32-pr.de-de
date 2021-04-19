---
title: gluunproject-Funktion (glu. h)
description: Die Funktion "gluunproject" ordnet den Objekt Koordinaten Fenster Koordinaten zu.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluunproject-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345928"
---
# <a name="gluunproject-function"></a>gluunproject-Funktion

Die Funktion " **gluunproject** " ordnet den Objekt Koordinaten Fenster Koordinaten zu.

## <a name="syntax"></a>Syntax


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Winx* 
</dt> <dd>

Die zuzuordnende x-Fenster Koordinate.

</dd> <dt>

*Winy* 
</dt> <dd>

Die zuzuordnende y-Fenster Koordinate.

</dd> <dt>

*Winz* 
</dt> <dd>

Die zu zugeordnete z-Fenster Koordinate.

</dd> <dt>

*modelmatrix* 
</dt> <dd>

Die Modelview-Matrix (wie bei einem [**glgetdoublev**](glgetdoublev.md) -Befehl).

</dd> <dt>

*projmatrix* 
</dt> <dd>

Die Projektions Matrix (wie bei einem **glgetdoublev** -Befehl).

</dd> <dt>

*Viewport* 
</dt> <dd>

Der Viewport (wie bei einem [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) -Befehl).

</dd> <dt>

*objX* 
</dt> <dd>

Die berechnete x-Objekt Koordinate.

</dd> <dt>

*objy* 
</dt> <dd>

Die berechnete y-Objekt Koordinate.

</dd> <dt>

*objz* 
</dt> <dd>

Die berechnete z-Objekt Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true".

Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluunproject** " ordnet die angegebenen Fenster Koordinaten mithilfe von " *modelmatrix*", " *projmatrix*" und " *Viewport*" den Objekt Koordinaten zu. Das Ergebnis wird in *objX*, *objy* und *objz* gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgetdoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluproject**](gluproject.md)
</dt> </dl>

 

 





