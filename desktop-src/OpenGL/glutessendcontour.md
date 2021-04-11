---
title: gluTessEndContour-Funktion (glu. h)
description: Die Funktionen "glutess begincontour" und "gluTessEndContour" begrenzen eine Kontur Beschreibung. | gluTessEndContour-Funktion (glu. h)
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
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352539"
---
# <a name="glutessendcontour-function"></a>gluTessEndContour-Funktion

Die Funktionen " [**glutess begincontour**](glutessbegincontour.md) " und " **gluTessEndContour** " begrenzen eine Kontur Beschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktionen " [**glutess begincontour**](glutessbegincontour.md) " und " **gluTessEndContour** " begrenzen die Definition einer Polygon-Kontur. Innerhalb jedes **glutessenbegincontour**-Paars " / **gluTessEndContour** " können NULL oder mehr Aufrufe an " [**glutess Vertex**](glutessvertex.md)" vorhanden sein. Die Eckpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit dem ersten-Element verknüpft). Sie können " **glutess begincontour** " nur zwischen " [**glutess beginpolygon**](glutessbeginpolygon.md) " und " [**glutessendpolygon**](glutessendpolygon.md)" aufrufen.

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

[**glunewtess**](glunewtess.md)
</dt> <dt>

[**glutess beginpolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> <dt>

[**glutessendpolygon**](glutessendpolygon.md)
</dt> <dt>

[**glutess normal**](glutessnormal.md)
</dt> <dt>

[**glutessproperty**](glutessproperty.md)
</dt> <dt>

[**glutess Vertex**](glutessvertex.md)
</dt> </dl>

 

 





