---
title: gluTessEndContour-Funktion (Glu.h)
description: Die Funktionen gluTessBeginContour und gluTessEndContour begrenzen eine Konturbeschreibung. | gluTessEndContour-Funktion (Glu.h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- gluTessEndContour-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0685a4af264dd2d4093fbb754c09d2124ecb2689063b61280bf55337ebb305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777410"
---
# <a name="glutessendcontour-function"></a>gluTessEndContour-Funktion

Die [**Funktionen gluTessBeginContour**](glutessbegincontour.md) und **gluTessEndContour** begrenzen eine Konturbeschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**Funktionen gluTessBeginContour**](glutessbegincontour.md) und **gluTessEndContour** begrenzen die Definition einer Polygonkontur. Innerhalb jedes gluTessBeginContour-gluTessEndContour-Paars können null oder mehr Aufrufe von  /  [**gluTessVertex verwendet werden.**](glutessvertex.md) Die Scheitelpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit der ersten kontur verknüpft). Sie können **gluTessBeginContour nur zwischen** [**gluTessBeginPolygon**](glutessbeginpolygon.md) und [**gluTessEndPolygon aufrufen.**](glutessendpolygon.md)

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

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





