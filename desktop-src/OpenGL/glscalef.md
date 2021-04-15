---
title: glScalef-Funktion (GL. h)
description: Die Funktionen "glScalef" und "glScalef" multiplizieren die aktuelle Matrix mit einer allgemeinen Skalierungs Matrix. | glScalef-Funktion (GL. h)
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
keywords:
- glScalef-Funktion OpenGL
topic_type:
- apiref
api_name:
- glScalef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eda183b763f22736370dd5c9ea13ca8793243e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104556052"
---
# <a name="glscalef-function"></a>glScalef-Funktion

Die Funktionen " [**glScalef**](glscaled.md) " und " **glScalef** " multiplizieren die aktuelle Matrix mit einer allgemeinen Skalierungs Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glScalef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Skalierungsfaktoren entlang der *x* -Achse.

</dd> <dt>

*y* 
</dt> <dd>

Skalierungsfaktoren entlang der *y* -Achse.

</dd> <dt>

*z* 
</dt> <dd>

Skalierungsfaktoren entlang der *z* -Achse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glScalef** " erzeugt eine allgemeine Skalierung entlang der *x*-, *y*-und *z* -Achse. Die drei Argumente geben die gewünschten Skalierungsfaktoren entlang der drei Achsen an. Die resultierende Matrix wird in der folgenden Abbildung angezeigt.

![Das Diagramm zeigt die Matrix der Skalierungsfaktoren entlang der x-, y-und z-Achse an.](images/scale01.png)

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Skalierungs Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix. Das heißt, wenn m die aktuelle Matrix und S die Skalierungs Matrix ist, wird m durch m S ersetzt.

Wenn der Matrix Modus "GL \_ Modelview" oder "GL" ist \_ , werden alle Objekte, die nach dem Aufruf von **glScalef** gezeichnet werden, skaliert. Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) , um das nicht skalierte Koordinatensystem zu speichern und wiederherzustellen.

Wenn für die Modelview-Matrix andere Skalierungsfaktoren als 1,0 übernommen werden und Beleuchtung aktiviert ist, sollte die automatische Normalisierung von normalen wahrscheinlich auch aktiviert werden ([**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) mit dem Argument GL \_ normalize).

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glScalef** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Modelview \_ Matrix

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Projektions \_ Matrix

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Textur \_ Matrix

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

[**glEnd**](glend.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glrotiert**](glrotated.md)
</dt> <dt>

[**glrotatef**](glrotatef.md)
</dt> <dt>

[**gltranslate**](gltranslate.md)
</dt> </dl>

 

 





