---
title: glutess begincontour-Funktion (glu. h)
description: Die Funktionen "glutess begincontour" und "gluTessEndContour" begrenzen eine Kontur Beschreibung. | glutess begincontour-Funktion (glu. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- glutess begincontour-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354319"
---
# <a name="glutessbegincontour-function"></a>glutess begincontour-Funktion

Die Funktionen " **glutess begincontour** " und " [**gluTessEndContour**](glutessendcontour.md) " begrenzen eine Kontur Beschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessBeginContour(
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

Die Funktionen " **glutess begincontour** " und " [**glutessendpolygon**](glutessendpolygon.md) " trennen die Definition einer Polygon Kontur. Innerhalb jedes **glutessenbegincontour**-Paars " / **glutessendpolygon** " können NULL oder mehr Aufrufe an " [**glutess Vertex**](glutessvertex.md)" vorhanden sein. Die Eckpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit dem ersten-Element verknüpft). Sie können " **glutess begincontour** " nur zwischen " [**glutess beginpolygon**](glutessbeginpolygon.md) " und " **glutessendpolygon**" aufrufen.

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

 

 





