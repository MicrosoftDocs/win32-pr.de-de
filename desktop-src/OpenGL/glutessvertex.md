---
title: glutess Vertex-Funktion (glu. h)
description: Die Funktion "glutess Vertex" gibt einen Scheitelpunkt auf einem Polygon an.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- glutess Vertex-Funktion OpenGL
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
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518857"
---
# <a name="glutessvertex-function"></a>glutess Vertex-Funktion

Die Funktion " **glutess Vertex** " gibt einen Scheitelpunkt auf einem Polygon an.

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

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*CoOrds* 
</dt> <dd>

Der Speicherort des Scheitel Punkts.

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger, der mit dem Vertex-Rückruf an das Programm zurückgegeben wurde (wie von " [*glutesscallback*](glutess.md)" angegeben).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glutess Vertex** " beschreibt einen Scheitelpunkt auf einem Polygon, den der Benutzer definiert. Aufeinander folgende " **glutess Vertex** "-Aufrufe beschreiben eine geschlossene Kontur. Um z. b. einen vierfachen zu beschreiben, nennen Sie " **glutess Vertex** " viermal. Sie können " **glutess Vertex** " nur zwischen " [**glutess begincontour**](glutessbegincontour.md) " und " [**gluTessEndContour**](glutessendcontour.md)" aufrufen.

Der *Data* -Parameter zeigt normalerweise auf eine-Struktur, die den Scheitelpunkt Speicherort enthält, sowie auf andere pro-Vertex-Attribute wie Farbe und normal. Dieser Zeiger wird nach dem Mosaik Prozess über den glu-Vertex-Rückruf an das Programm zurückgegeben \_ (siehe [*glutesscallback*](glutess.md)).

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

[**glutess begincontour**](glutessbegincontour.md)
</dt> <dt>

[**glutess beginpolygon**](glubeginpolygon.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**glutess normal**](glutessnormal.md)
</dt> <dt>

[**glutessproperty**](glutessproperty.md)
</dt> </dl>

 

 





