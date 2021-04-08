---
title: gluquadricdrawstyle-Funktion (glu. h)
description: Die Funktion "gluquadricdrawstyle" gibt die gewünschte Zeichnungs Art für viercs an.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluquadricdrawstyle-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956849"
---
# <a name="gluquadricdrawstyle-function"></a>gluquadricdrawstyle-Funktion

Die Funktion " **gluquadricdrawstyle** " gibt die gewünschte Zeichnungs Art für viercs an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadobject* 
</dt> <dd>

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*DrawStyle* 
</dt> <dd>

Der gewünschte Zeichnungs Stil. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**Glu \_ ausfüllen**</dt> </dl>                   | Viercs werden mit Polygon primitiven gerendert. Die Polygone werden gegen den Uhrzeigersinn in Bezug auf ihre normale (wie mit " [**gluquadricorientation**](gluquadricorientation.md)" definiert) gezeichnet.<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**Glu- \_ Linie**</dt> </dl>                   | Viercs werden als Zeilen Satz gerendert.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**Glu- \_ Silhouette**</dt> </dl> | Viercs werden als Zeilen Satz gerendert, mit dem Unterschied, dass Kanten, die Coplanar trennen, nicht gezeichnet werden.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**Glu- \_ Punkt**</dt> </dl>                | Viercs werden als eine Gruppe von Punkten gerendert.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluquadricdrawstyle** " gibt den Zeichnungs Stil für viercs an, die mit **quadobject** gerendert werden.

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

[**glunewquadric**](glunewquadric.md)
</dt> <dt>

[**gluquadricnormals**](gluquadricnormals.md)
</dt> <dt>

[**gluquadricorientation**](gluquadricorientation.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> </dl>

 

 





