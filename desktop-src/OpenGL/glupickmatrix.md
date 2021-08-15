---
title: gluPickMatrix-Funktion (Glu.h)
description: Die gluPickMatrix-Funktion definiert einen Auswahlbereich.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- OpenGL-Funktion "gluPickMatrix"
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 394e10c460b406e510b1423f299b4a8724492f5a5b180212ff121f4ad593041e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061578"
---
# <a name="glupickmatrix-function"></a>gluPickMatrix-Funktion

Die **gluPickMatrix-Funktion** definiert einen Auswahlbereich.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die x-Fensterkoordinate eines Auswahlbereichs.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Fensterkoordinate eines Auswahlbereichs.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Auswahlbereichs in Fensterkoordinaten.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Auswahlbereichs in Fensterkoordinaten.

</dd> <dt>

*Ansichtsfenster* 
</dt> <dd>

Der aktuelle Viewport (wie bei einem [**glGetIntegerv-Aufruf).**](glgetintegerv.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluPickMatrix-Funktion** erstellt eine Projektionsmatrix, mit der Sie das Zeichnen auf einen kleinen Bereich des Viewports beschränken können.

1.  Verwenden **Sie gluPickMatrix,** um das Zeichnen auf einen kleinen Bereich um den Cursor zu beschränken.
2.  Wechseln Sie in den Auswahlmodus [**(mit glRenderMode),**](glrendermode.md)und rerendern Sie die Szene erneut.

    Alle Primitive, die in der Nähe des Cursors gezeichnet worden wären, werden identifiziert und im Auswahlpuffer gespeichert.

Die von **gluPickMatrix** erstellte Matrix wird mit der aktuellen Matrix multipliziert, als ob [**glMultMatrix**](glmultmatrix.md) mit der generierten Matrix aufgerufen würde.

1.  Rufen [**Sie glLoadIdentity auf,**](glloadidentity.md) um eine Identitätsmatrix in den Perspektivenmatrixstapel zu laden.
2.  Rufen Sie **gluPickMatrix auf.**
3.  Rufen Sie eine Funktion (z. B. [**gluPerspective**](gluperspective.md)) auf, um die Perspektivmatrix mit der Auswahlmatrix zu multiplizieren.

Wenn Sie **gluPickMatrix** zum Auswählen einer nicht einheitlichen rationalen B-Spline [(NURBS)](using-nurbs-curves-and-surfaces.md)verwenden, deaktivieren Sie die NURBS-Eigenschaft GLU \_ AUTO LOAD \_ \_ MATRIX. Wenn GLU AUTO LOAD MATRIX nicht deaktiviert ist, wird jede \_ \_ gerenderte NURBS-Oberfläche anders mit der Auswahlmatrix von der Unterteilung ohne die Auswahlmatrix \_ unterteilt.

## <a name="examples"></a>Beispiele

Beim Rendern einer Szene wie folgt:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



Der folgende Code wählt einen Teil des Viewports aus:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glGetIntegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





