---
title: glPolygonStipple-Funktion (Gl.h)
description: Die glPolygonStipple-Funktion legt das Polygonausschnittmuster fest.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f9098ab91af5f258f97e0878ae8cbcb19863ec3bc82765c2664683830539fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614906"
---
# <a name="glpolygonstipple-function"></a>glPolygonStipple-Funktion

Die **funktion glPolygonStipple legt** das Polygonausschnittmuster fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Ein Zeiger auf ein 32x32-Ausschnittmuster, das auf die gleiche Weise aus dem Arbeitsspeicher entpackt wird, wie [**glDrawPixels**](gldrawpixels.md) Pixel entpackt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **funktion glPolygonStipple legt** das Polygonausschnittmuster fest. Polygonstipping, z. B. Zeilenausschnitt (siehe [**glLineStipple),**](gllinestipple.md)maskiert bestimmte Fragmente, die durch Rasterung erzeugt werden, und erstellt ein Muster. Das Ausschnitten ist unabhängig von Polygon-Antialiasing.

Der *Mask-Parameter* ist ein Zeiger auf ein 32x32-Ausschnittmuster, das im Arbeitsspeicher gespeichert wird,  genau  wie die Pixeldaten, die  **glDrawPixels** mit einer Höhe und Breite von 32, einem Pixelformat von GL COLOR INDEX und dem Datentyp GL BITMAP bereitgestellt \_ \_  \_ werden. Das heißt, das Ausschnittmuster wird als 32x32-Array von 1-Bit-Farbindizes dargestellt, die in Bytes ohne Vorzeichen gepackt sind. Die [**glPixelStore-Funktionsparameter**](glpixelstore-functions.md) wie GL UNPACK SWAP BYTES und GL UNPACK LSB FIRST wirken sich auf die \_ \_ \_ \_ \_ Assempel der Bits in einem \_ Ausschnittmuster aus. Pixelübertragungsvorgänge (Umschalt-, Offset- und Pixelzuordnung) werden jedoch nicht auf das Ausschnittbild angewendet.

Polygonausschnitte sind mit [**glEnable**](glenable.md) und **glDisable** aktiviert und deaktiviert, indem das Argument GL \_ POLYGON \_ STIPPLE verwendet wird. Wenn diese Option aktiviert ist, wird ein rasteriertes Polygonfragment mit den Fensterkoordinaten *x*<sub>w</sub> und *y*<sub>w</sub> nur dann an die nächste Phase von OpenGL gesendet, wenn das *(x*<sub>w</sub> mod 32)th-Bit in der (*y*<sub>w</sub> mod 32)-Zeile des Ausschnittmusters eins ist. Wenn Polygonausschnitte deaktiviert sind, ist dies so, als ob es sich bei dem Ausschnittmuster um alle handelte.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPolygonStipple ab:**

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ POLYGON \_ STIPPLE

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





