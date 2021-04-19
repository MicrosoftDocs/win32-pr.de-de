---
title: glarrayelement-Funktion (GL. h)
description: Die Funktion "glarrayelement" gibt die Array Elemente an, die zum Rendering eines Scheitel Punkts verwendet werden.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glarrayelement-Funktion OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346722"
---
# <a name="glarrayelement-function"></a>glarrayelement-Funktion

Die Funktion " **glarrayelement** " gibt die Array Elemente an, die zum Rendering eines Scheitel Punkts verwendet werden.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Ein Index in den aktivierten Arrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktion " **glarrayelement** " innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren, um Vertex-und Attributdaten für Punkt-, Linien-und Polygon primitive anzugeben. Die Funktion " **glarrayelement** " gibt die Daten für einen einzelnen Scheitelpunkt mithilfe von Vertex-und Attributdaten an, die sich am *Index* der aktivierten Scheitelpunkt Arrays befinden.

Sie können " **glarrayelement** " verwenden, um primitive zu erstellen, indem Sie Scheitelpunkt Daten indizieren, anstatt durch das Streamen von Daten Arrays in der Reihenfolge der ersten bis letzten Reihenfolge. Da " **glarrayelement** " nur einen einzelnen Scheitelpunkt angibt, können Sie Attribute für einzelne primitive explizit angeben. Beispielsweise können Sie für jedes einzelne Dreieck einen einzelnen Wert festlegen.

Wenn Sie in Anzeigelisten Aufrufe an " **glarrayelement** " einschließen, werden die erforderlichen Array Daten, die von den Array Zeigern und Aktivier Werten bestimmt werden, auch in der Anzeigeliste eingegeben. Array Zeiger und aktivierte Werte werden bestimmt, wenn Anzeigelisten erstellt werden, nicht, wenn Anzeigelisten ausgeführt werden.

Sie können statische Array Daten jederzeit mit " **glarrayelement**" lesen und Zwischenspeichern. Wenn Sie die Elemente eines statischen Arrays ändern, ohne das Array erneut anzugeben, sind die Ergebnisse aller nachfolgenden Aufrufe von " **glarrayelement** " nicht definiert.

Wenn Sie " **glarrayelement** " aufrufen, ohne zuerst " **glenableclientstate**" aufrufen \_ \_ zu müssen, erfolgt keine Zeichnung, aber die Attribute, die aktivierten Arrays entsprechen, werden geändert. Obwohl kein Fehler generiert wird, wenn Sie ein Array innerhalb der **glBegin** -und **glEnd** -Paare angeben, sind die Ergebnisse nicht definiert.

> [!Note]  
> Die Funktion " **glarrayelement** " ist nur in OpenGL, Version 1,1 oder höher, verfügbar.

 

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

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





