---
title: glcolorpointer-Funktion (GL. h)
description: Die glcolorpointer-Funktion definiert ein Array von Farben.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glcolorpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475846"
---
# <a name="glcolorpointer-function"></a>glcolorpointer-Funktion

Die **glcolorpointer** -Funktion definiert ein Array von Farben.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*size* 
</dt> <dd>

Die Anzahl der Komponenten pro Farbe. Der Wert muss 3 oder 4 sein.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp jeder Farbkomponente in einem Farbarray. Zulässige Datentypen werden mit den folgenden Konstanten angegeben: GL \_ Byte, GL \_ unsigned \_ Byte, GL \_ Short, GL \_ unsigned \_ Short, GL \_ int, GL \_ unsigned \_ int, GL \_ float oder GL \_ Double.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byte Offset zwischen aufeinander folgenden Farben. Wenn *Stride* 0 (null) ist, werden die Farben im Array eng verpackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf die erste Komponente des ersten Farb Elements in einem Farbarray.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                              | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | *Größe* war nicht 3 oder 4.<br/>            |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>  | der *Typ* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | " *Stride* " oder " *count* " war negativ.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glcolorpointer** -Funktion gibt den Speicherort und das Datenformat eines Arrays von Farbkomponenten an, die beim Rendern verwendet werden sollen. Der *Stride* -Parameter bestimmt den Byte Offset von einer Farbe zum nächsten und ermöglicht das Packen von Scheitelpunkt Attributen in einem einzelnen Array oder Speicher in separaten Arrays. In einigen Implementierungen kann das Speichern von Vertex-Attributen in einem einzelnen Array effizienter als die Verwendung separater Arrays sein.

Aktivieren Sie das Farbarray, indem Sie die GL- \_ Farb \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben. Beim Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md) " wird das Farb Array verwendet, das daher aktiviert ist. Standardmäßig ist das Farbarray deaktiviert. Die **glcolorpointer** -Aufrufe können nicht in Anzeigelisten eingegeben werden.

Wenn Sie ein Farb Array mithilfe von **glcolorpointer** angeben, werden die Werte aller Farb Array Parameter der Funktion in einem Client seitigen Zustand gespeichert, und Sie können statische Array Elemente Zwischenspeichern. Da sich die Farb Array Parameter in einem Client seitigen Zustand befinden, speichern oder wiederherstellen die Werte der Parameter von [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) nicht.

Obwohl die Angabe des farbarrays innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren keinen Fehler generiert, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glcolorpointer** " ab:

[**glisenabled**](glisenabled.md) mit Argument GL \_ - \_ Farbarray

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ \_ array \_ Größe des Argument GL

**glget** mit Argument GL \_ Color \_ array \_ Type

**glget** mit Argument GL \_ Color \_ array \_ Stride

**glget** mit Argument GL \_ Color \_ array \_ count

[**glgetpointerv**](glgetpointerv.md) mit Argument GL \_ Color \_ array- \_ Zeiger

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

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glpopattenb**](glpopattrib.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





