---
title: gluTessVertex-Funktion (Glu.h)
description: Die gluTessVertex-Funktion gibt einen Scheitelpunkt auf einem Polygon an.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b3b1dd666fd965e7b6536a20a794481c534ed3e42594017093ee161a067e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488420"
---
# <a name="glutessvertex-function"></a>gluTessVertex-Funktion

Die **gluTessVertex-Funktion** gibt einen Scheitelpunkt auf einem Polygon an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*Coords* 
</dt> <dd>

Die Position des Scheitelpunkts.

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger, der mit dem Scheitelpunktrückruf zurück an das Programm übergeben wird (wie von [*gluTessCallback angegeben).*](glutess.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluTessVertex-Funktion** beschreibt einen Scheitelpunkt auf einem Polygon, das der Benutzer definiert. Aufeinanderfolgende **gluTessVertex-Aufrufe** beschreiben eine geschlossene Kontur. Um z. B. eine quadrierte Liste zu beschreiben, rufen Sie **gluTessVertex viermal** auf. Sie können **gluTessVertex nur zwischen** [**gluTessBeginContour**](glutessbegincontour.md) und [**gluTessEndContour aufrufen.**](glutessendcontour.md)

Der *Datenparameter* verweist normalerweise auf eine Struktur, die die Scheitelpunktposition enthält, sowie auf andere Attribute pro Scheitelpunkt, z. B. Farbe und Normal. Dieser Zeiger wird über den GLU VERTEX-Rückruf nach dem Mosaik an das Programm zurückübertragen \_ (siehe [*gluTessCallback*](glutess.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





