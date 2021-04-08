---
title: glupickmatrix-Funktion (glu. h)
description: Die Funktion "glupickmatrix" definiert einen Auswahlbereich.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- glupickmatrix-Funktion OpenGL
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
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949391"
---
# <a name="glupickmatrix-function"></a>glupickmatrix-Funktion

Die Funktion " **glupickmatrix** " definiert einen Auswahlbereich.

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

Die x-Fenster Koordinate eines Auswahl Bereichs.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Fenster Koordinate eines Auswahl Bereichs.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Auswahl Bereichs in Fenster Koordinaten.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Auswahl Bereichs in Fenster Koordinaten.

</dd> <dt>

*Viewport* 
</dt> <dd>

Der aktuelle Viewport (wie bei einem [**glgetintegerv**](glgetintegerv.md) -Befehl).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glupickmatrix** " erstellt eine Projektions Matrix, die Sie verwenden können, um das Zeichnen auf einen kleinen Bereich des Viewports einzuschränken.

1.  Verwenden Sie " **glupickmatrix** ", um das Zeichnen auf einen kleinen Bereich um den Cursor einzuschränken.
2.  Geben Sie den Auswahlmodus (mit [**glrendermode**](glrendermode.md)) ein, und führen Sie dann die Szene erneut aus.

    Alle primitiven, die in der Nähe des Cursors gezeichnet wurden, werden im Auswahl Puffer identifiziert und gespeichert.

Die von " **glupickmatrix** " erstellte Matrix wird mit der aktuellen Matrix so multipliziert, als wäre " [**glmultmatrix**](glmultmatrix.md) " mit der generierten Matrix aufgerufen worden.

1.  Ruft [**glLoadIdentity**](glloadidentity.md) auf, um eine Identitätsmatrix auf den Perspektiven Matrix Stapel zu laden.
2.  Nennen Sie " **glupickmatrix**".
3.  Ruft eine Funktion (z. b. " [**gluperspective**](gluperspective.md)") auf, um die Perspektiven Matrix anhand der Auswahl Matrix zu multiplizieren.

Wenn Sie " **glupickmatrix** " verwenden, um nicht einheitliche rationelle B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) auszuwählen, achten Sie darauf, die NURBS-Eigenschaft zu deaktivieren \_ \_ \_ . Wenn \_ \_ \_ die Matrix für die automatische Lastenausgleich nicht deaktiviert ist, wird jede gerenderte nursb-Oberfläche anders unterteilt, und die Auswahl Matrix wird ohne die Auswahl Matrix unterteilt.

## <a name="examples"></a>Beispiele

Beim Rendern einer Szene wie folgt:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



mit dem folgenden Code wird ein Teil des Viewports ausgewählt:


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
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glgetintegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glrendermode**](glrendermode.md)
</dt> <dt>

[**gluperspective**](gluperspective.md)
</dt> </dl>

 

 





