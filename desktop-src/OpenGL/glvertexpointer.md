---
title: glvertexpointer-Funktion (GL. h)
description: Die glvertexpointer-Funktion definiert ein Array von Vertex-Daten.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glvertexpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478228"
---
# <a name="glvertexpointer-function"></a>glvertexpointer-Funktion

Die **glvertexpointer** -Funktion definiert ein Array von Vertex-Daten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glVertexPointer(
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

Die Anzahl der Koordinaten pro Scheitelpunkt. Der Wert von *size* muss 2, 3 oder 4 sein.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp der einzelnen Koordinaten im Array mit den folgenden symbolischen Konstanten: GL \_ Short, GL \_ int, GL \_ float und GL \_ Double.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byte Offset zwischen aufeinander folgenden Vertices. Wenn *Stride* gleich 0 ist, werden die Scheitel Punkte im Array eng verpackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf die erste Koordinate des ersten Vertex im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                              | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | die *Größe* lag nicht bei 2, 3 oder 4. <br/>        |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>  | der *Typ* war kein akzeptierter Wert.<br/>  |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | " *Stride* " oder " *count* " war negativ. <br/> |



## <a name="remarks"></a>Bemerkungen

Die **glvertexpointer** -Funktion gibt den Speicherort und die Daten eines Arrays von Vertex-Koordinaten an, die beim Rendern verwendet werden sollen. Der *size* -Parameter gibt die Anzahl der Koordinaten pro Scheitelpunkt an. Der *Typparameter* gibt den Datentyp der einzelnen Scheitelpunkt Koordinaten an. Der *Stride* -Parameter bestimmt den Byte Offset von einem Scheitelpunkt zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays. In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter sein als die Verwendung separater Arrays (siehe [**glinterleavedarrays**](glinterleavedarrays.md)).

Ein Scheitelpunkt Array wird aktiviert, wenn Sie die GL- \_ Vertex- \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwenden [**gldrawarrays**](gldrawarrays.md), [**gldrawelements**](gldrawelements.md)und [**glarrayelement**](glarrayelement.md) das Vertex-Array. Standardmäßig ist das Scheitelpunkt Array deaktiviert.

Sie können " **glvertexpointer** " nicht in Anzeigelisten einschließen.

Wenn Sie ein Scheitelpunkt Array mithilfe von **glvertexpointer** angeben, werden die Werte aller Scheitelpunkt Array-Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden. Da es sich bei den Scheitelpunkt Array-Parametern um einen Client seitigen Zustand handelt, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und **glpopatfferb** nicht gespeichert oder wieder hergestellt.

Obwohl kein Fehler generiert wird, wenn Sie **glvertexpointer** innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren aufrufen, sind die Ergebnisse nicht definiert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glvertexpointer** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der Größe des Argument-GL- \_ Vertex- \_ Arrays \_

**glget** mit Argument GL \_ Vertex \_ array \_ Stride

**glget** mit Argument-GL-Anzahl der \_ Vertex- \_ Arrays \_

**glget** mit dem Argument "GL \_ Vertex- \_ \_ Arraytyp"

[**glgetpointerv**](glgetpointerv.md) mit Argument, GL \_ Vertex- \_ array \_ Zeiger

[**glisenabled**](glisenabled.md) mit Argument "GL \_ Vertex \_ Array"

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

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> </dl>

 

 





