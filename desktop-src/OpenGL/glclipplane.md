---
title: glClipPlane-Funktion (Gl.h)
description: Die glClipPlane-Funktion gibt eine Ebene an, auf der die gesamte Geometrie abgeschnitten wird.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb55edd88b8c8dcd6b4481e60dfc05a012bb79f4f484fde8987e9ed23239d837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618040"
---
# <a name="glclipplane-function"></a>glClipPlane-Funktion

Die **glClipPlane-Funktion** gibt eine Ebene an, auf der die gesamte Geometrie abgeschnitten wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flugzeug* 
</dt> <dd>

Die Clippingebene, die positioniert wird. Symbolische Namen der Form GL \_ CLIP \_ PLANE *i*, wobei *i* eine ganze Zahl zwischen 0 und GL \_ MAX CLIP \_ \_ PLANES - 1 ist, werden akzeptiert.

</dd> <dt>

*Gleichung* 
</dt> <dd>

Die Adresse eines Arrays mit vier Gleitkommawerten mit doppelter Genauigkeit. Diese Werte werden als Ebenengleichung interpretiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *plane* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die Geometrie wird immer an den Grenzen eines Frustums mit sechs Ebenen in *x*, *y* und *z* abgeschnitten. Die **glClipPlane-Funktion** ermöglicht die Angabe zusätzlicher Ebenen, die nicht notwendigerweise der *x-,* *y-* oder *z-Achse* entsprechen, für die die gesamte Geometrie abgeschnitten wird. Es können bis zu GL \_ MAX \_ CLIP \_ PLANES-Ebenen angegeben werden, wobei GL \_ MAX CLIP \_ \_ PLANES in allen Implementierungen mindestens sechs beträgt. Da der resultierende Clippingbereich die Schnittmenge der definierten Halbräume ist, ist er immer konvex.

Die **glClipPlane-Funktion** gibt einen Halbraum mithilfe einer Gleichung der Vierkomponentenebene an. Wenn Sie **glClipPlane** aufrufen, wird die *Gleichung* durch die Umkehrung der Modellansichtsmatrix transformiert und in den resultierenden Augenkoordinaten gespeichert. Nachfolgende Änderungen an der Modellansichtsmatrix haben keine Auswirkungen auf die gespeicherten Ebenengleichungskomponenten. Wenn das Punktprodukt der Augenkoordinaten eines Scheitelpunkts mit den gespeicherten Ebenengleichungskomponenten positiv oder 0 (null) ist, befindet sich der Scheitelpunkt in Bezug auf diese Clippingebene. Andernfalls ist sie out.

Verwenden Sie die Funktionen [**glEnable**](glenable.md) und [**glDisable,**](gldisable.md) um Clippingebenen zu aktivieren und zu deaktivieren. Rufen Sie Clippingebenen mit dem Argument GL \_ CLIP \_ PLANE *i* auf, wobei *i* die Ebenennummer ist.

Standardmäßig werden alle Clippingebenen als (0,0,0,0) in Augenkoordinaten definiert und deaktiviert.

Es ist immer der Fall, dass GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glClipPlane** ab:

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled**](glisenabled.md) mit argument GL \_ CLIP \_ PLANE *i*

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





