---
title: gluproject-Funktion (glu. h)
description: Die Funktion "gluproject" ordnet den Fenster Koordinaten Objekt Koordinaten zu.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluproject-Funktion OpenGL
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
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478024"
---
# <a name="gluproject-function"></a>gluproject-Funktion

Die Funktion " **gluproject** " ordnet den Fenster Koordinaten Objekt Koordinaten zu.

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

*objX* 
</dt> <dd>

Die x-Objekt Koordinate.

</dd> <dt>

*objy* 
</dt> <dd>

Die y-Objekt Koordinate.

</dd> <dt>

*objz* 
</dt> <dd>

Die z-Objekt Koordinate.

</dd> <dt>

*modelmatrix* 
</dt> <dd>

Die aktuelle Modelview-Matrix (wie von einem [**glgetdoublev**](glgetdoublev.md) -Befehl).

</dd> <dt>

*projmatrix* 
</dt> <dd>

Die aktuelle Projektions Matrix (wie bei einem **glgetdoublev** -Befehl).

</dd> <dt>

*Viewport* 
</dt> <dd>

Der aktuelle Viewport (wie bei einem [**glgetintegerv**](glgetintegerv.md) -Befehl).

</dd> <dt>

*Winx* 
</dt> <dd>

Die berechnete x-Fenster Koordinate.

</dd> <dt>

*Winy* 
</dt> <dd>

Die berechnete y-Fenster Koordinate.

</dd> <dt>

*Winz* 
</dt> <dd>

Die berechnete z-Fenster Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true".

Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluproject** " wandelt die angegebenen Objekt Koordinaten mithilfe von " *modelmatrix*", " *projmatrix*" und " *Viewport*" in Fenster Koordinaten um. Das Ergebnis wird in *Winx*, *Winy* und *Winz* gespeichert.

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

[**glgetdoublev**](glgetdoublev.md)
</dt> <dt>

[**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**"gluunproject"**](gluunproject.md)
</dt> </dl>

 

 





