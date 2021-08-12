---
title: glPolygonOffset-Funktion (Gl.h)
description: Die glPolygonOffset-Funktion legt die Von OpenGL zum Berechnen von Tiefenwerten verwendeten Skalierungs- und Einheiten fest.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 314372c0ce87ef5b75db24e4482d6b621422546abe0c71a34cc9821cb4391997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614916"
---
# <a name="glpolygonoffset-function"></a>glPolygonOffset-Funktion

Die **glPolygonOffset-Funktion** legt die Von OpenGL zum Berechnen von Tiefenwerten verwendeten Skalierungs- und Einheiten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Faktor* 
</dt> <dd>

Gibt einen Skalierungsfaktor an, der zum Erstellen eines variablen Tiefenoffsets für jedes Polygon verwendet wird. Der Anfangswert ist 0 (null).

</dd> <dt>

*Einheiten* 
</dt> <dd>

Gibt einen Wert an, der mit einem implementierungsspezifischen Wert multipliziert wird, um einen konstanten Tiefenoffset zu erstellen. Der Anfangswert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Wenn GL POLYGON OFFSET aktiviert ist, wird der Tiefenwert jedes Fragments versetzt, nachdem er aus den Tiefenwerten der entsprechenden \_ \_ Scheitelungen interpoliert wurde. Der Wert des  Offsets ist faktor ?z + r Einheiten, wobei ?z eine Messung der Tiefenänderung relativ zum Bildschirmbereich des Polygons ist und r der kleinste Wert ist, der garantiert einen auflösbaren Offset für eine bestimmte Implementierung \* \* erzeugt. Der Offset wird hinzugefügt, bevor der Tiefentest ausgeführt wird und bevor der Wert in den Tiefenpuffer geschrieben wird.

Die **glPolygonOffset-Funktion** ist nützlich für das Rendern ausgeblendeter Linienbilder, das Anwenden von Decals auf Oberflächen und das Rendern von Festkörpern mit hervorgehobenen Kanten.

Die **funktion glPolygonOffset** hat keine Auswirkungen auf Tiefenkoordinaten, die im Feedbackpuffer platziert werden. Sie hat auch keine Auswirkungen auf die Auswahl.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPolygonOffset ab:**

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ POLYGON \_ OFFSET \_ FACTOR
-   [**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ POLYGON OFFSET \_ \_ UNITS
-   [**glIsEnabled mit Argument**](glisenabled.md) GL \_ POLYGON OFFSET \_ \_ FILL
-   [**glIsEnabled mit Argument**](glisenabled.md) GL \_ POLYGON OFFSET \_ \_ LINE
-   [**glIsEnabled mit Argument**](glisenabled.md) GL \_ POLYGON OFFSET \_ \_ POINT

> [!Note]  
> Die **glPolygonOffset-Funktion** ist nur in OpenGl Version 1.1 oder höher verfügbar.

 

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





