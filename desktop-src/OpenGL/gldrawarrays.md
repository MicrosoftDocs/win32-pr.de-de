---
title: gldrawarrays-Funktion (GL. h)
description: Die Funktion "gldrawarrays" gibt mehrere primitive zum Rendering an.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- gldrawarrays-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956600"
---
# <a name="gldrawarrays-function"></a>gldrawarrays-Funktion

Die Funktion " **gldrawarrays** " gibt mehrere primitive zum Rendering an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die Art der zu Rendering enden primitiver. Die folgenden Konstanten geben akzeptable Typen von primitiven an: GL- \_ Punkte, GL-Zeilen \_ \_ Streifen, GL- \_ Zeilen \_ Schleife, GL \_ -Linien, GL \_ \_ -Dreiecks Streifen, GL \_ \_ -Dreiecks Lüfter, GL \_ -Dreiecke, GL \_ Quad \_ Strip, GL \_ QUADS und GL- \_ Polygon.

</dd> <dt>

*first* 
</dt> <dd>

Der Start Index in den aktivierten Arrays.

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der zu Rendering enden Indizes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Anzahl* war negativ.<br/>                                                                                                      |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Mit **gldrawarrays** können Sie mehrere geometrische Primitive zum Rendering angeben. Anstatt separate OpenGL-Funktionen zum übergeben einzelner Scheitel Punkte, normaler Werte oder Farben aufzurufen, können Sie separate Arrays von Scheitel Punkten, normalen und Farben angeben, um eine Sequenz von primitiven (alle Arten) mit einem einzigen Aufruf von **gldrawarrays** zu definieren.

Wenn Sie **gldrawarrays** aufzurufen, werden sequenzielle Elemente aus den einzelnen aktivierten Arrays *verwendet, um* eine Sequenz geometrischer primitiver Elemente zu erstellen, beginnend mit dem *ersten* Element. Der *Mode* -Parameter gibt an, welche Art von primitiver konstruiert werden soll und wie die Array Elemente zum Erstellen der primitiven verwendet werden.

Nachdem **gldrawarrays** zurückgegeben wurde, sind die Werte von Vertex-Attributen, die von **gldrawarrays** geändert werden, nicht definiert. Wenn z. b. \_ das GL- \_ Farbarray aktiviert ist, ist der Wert der aktuellen Farbe nach dem Zurückgeben von **gldrawarrays** nicht definiert. Von **gldrawarrays** nicht geänderte Attribute bleiben definiert. Wenn das GL- \_ Scheitelpunkt \_ Array nicht aktiviert ist, werden keine geometrischen primitiven generiert, aber die Attribute, die aktivierten Arrays entsprechen, werden geändert.

Sie können **gldrawarrays** in Anzeigelisten einschließen. Wenn Sie **gldrawarrays** in eine Anzeigeliste einschließen, werden die erforderlichen Array Daten, die durch die Array Zeiger und die aktiviert werden, in der Anzeigeliste generiert und eingegeben. Die Werte der Array Zeiger und-Aktivierung werden während der Erstellung von Anzeigelisten bestimmt.

Sie können statische Array Daten jederzeit lesen. Wenn statische Array Elemente geändert und das Array nicht erneut angegeben wird, sind die Ergebnisse aller nachfolgenden Aufrufe von **gldrawarrays** nicht definiert.

Obwohl kein Fehler generiert wird, wenn Sie ein Array mehr als einmal innerhalb der [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paare angeben, sind die Ergebnisse nicht definiert.

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

[**glarrayelement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
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

 

 





