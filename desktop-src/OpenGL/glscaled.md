---
title: glScaled-Funktion (Gl.h)
description: Die Funktionen glScaled und glScalef multiplizieren die aktuelle Matrix mit einer allgemeinen Skalierungsmatrix. | glScaled-Funktion (Gl.h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- glScaled-Funktion OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46742831eaa0a014de0f6ae50271b28c922893133588758119cbf5bff7ba628b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491790"
---
# <a name="glscaled-function"></a>glScaled-Funktion

Die Funktionen **glScaled** und [**glScalef**](glscalef.md) multiplizieren die aktuelle Matrix mit einer allgemeinen Skalierungsmatrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Skalierungsfaktoren  entlang der x-Achse.

</dd> <dt>

*y* 
</dt> <dd>

Skalierungsfaktoren entlang der *y-Achse.*

</dd> <dt>

*Z* 
</dt> <dd>

Skalierungsfaktoren  entlang der Z-Achse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glScaled-Funktion** erzeugt eine allgemeine Skalierung entlang der *x-,* *y-* und *z-Achse.* Die drei Argumente geben die gewünschten Skalierungsfaktoren entlang jeder der drei Achsen an. Die resultierende Matrix ist

![Diagramm, das die Matrix der Skalierungsfaktoren entlang der x-, y- und z-Achse zeigt.](images/scale01.png)

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Skalierungsmatrix multipliziert, wobei das Produkt die aktuelle Matrix ersetzt. Das heißt, wenn M die aktuelle Matrix und S die Skalierungsmatrix ist, wird M durch M S ersetzt.

Wenn der Matrixmodus entweder GL \_ MODELVIEW oder GL \_ PROJECTION ist, werden alle Objekte skaliert, die nach dem Aufruf von **glScaled** gezeichnet wurden. Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix,**](glpopmatrix.md) um das nicht skalierte Koordinatensystem zu speichern und wiederherzustellen.

Wenn andere Skalierungsfaktoren als 1.0 auf die Modellansichtsmatrix angewendet werden und die Beleuchtung aktiviert ist, sollte wahrscheinlich auch die automatische Normalisierung von Normalwerten aktiviert werden ([**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ NORMALIZE).

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glScaled ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MODELVIEW \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ PROJECTION \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ TEXTURE \_ MATRIX

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
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





