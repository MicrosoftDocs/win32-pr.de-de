---
title: glclipplane-Funktion (GL. h)
description: Die glclipplane-Funktion gibt eine Ebene an, auf die die gesamte Geometrie zugeschnitten ist.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glclipplane-Funktion OpenGL
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
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337526"
---
# <a name="glclipplane-function"></a>glclipplane-Funktion

Die **glclipplane** -Funktion gibt eine Ebene an, auf die die gesamte Geometrie zugeschnitten ist.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wasser* 
</dt> <dd>

Die Clippingebene, die positioniert wird. Symbolische Namen der Form "GL \_ Clip \_ Plane *i*",  wobei es sich um eine ganze Zahl zwischen 0 und GL \_ Max \_ \_ -Clip-Plane-1 handelt, werden akzeptiert.

</dd> <dt>

*Gleichung* 
</dt> <dd>

Die Adresse eines Arrays von vier Gleit Komma Werten mit doppelter Genauigkeit. Diese Werte werden als Gleichung der Ebene interpretiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | die *Ebene* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Geometry wird immer an die Grenzen einer sechsstufigen Frustration in *x*, *y* und *z* abgeschnitten. Die **glclipplane** -Funktion ermöglicht die Angabe zusätzlicher Ebenen, nicht notwendigerweise senkrecht zur *x-* Achse, *y-* Achse oder *z*-Achse, auf die die gesamte Geometrie zugeschnitten ist. Es können bis zu GL \_ Max \_ cliseplane- \_ Ebenen angegeben werden, wobei \_ Maximale clippinzfelder \_ \_ in allen Implementierungen mindestens sechs ist. Da der sich ergebende Clippingbereich die Schnittmenge der definierten halbräume ist, wird er immer als "konform" bezeichnet.

Die Funktion " **glclipplane** " gibt einen halben Leerraum mithilfe einer Gleichung der Ebene "vier Komponenten" an. Wenn Sie " **glclipplane**" aufrufen, wird die *Gleichung* durch die Umkehrung der Modelview-Matrix transformiert und in den resultierenden Augen Koordinaten gespeichert. Nachfolgende Änderungen an der Modelview-Matrix haben keine Auswirkungen auf die gespeicherten Ebenen-Gleichung-Komponenten. Wenn das Punktprodukt der Augen Koordinaten eines Scheitel Punkts mit den Komponenten der gespeicherten ebenengleichung positiv oder NULL ist, befindet sich der Scheitelpunkt in Bezug auf diese Clippingebene. Andernfalls ist Sie Out.

Verwenden Sie die Funktionen [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) , um Clippingebenen zu aktivieren und zu deaktivieren. Ruft Clippingebenen mit dem Argument GL \_ Clip \_ Plane *i* auf  , wobei die Ebenennummer ist.

Standardmäßig werden alle Clippingebenen als (0, 0, 0, 0) in den Augen Koordinaten definiert und deaktiviert.

Es ist immer der Fall, dass GL \_ Clip \_ Plane *i* = GL \_ Clip \_ PLANE0 + *i*.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glclipplane** abgerufen:

[**glgetclipplane**](glgetclipplane.md)

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Clip \_ Plane *i*

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

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgetclipplane**](glgetclipplane.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> </dl>

 

 





