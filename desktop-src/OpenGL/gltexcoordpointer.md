---
title: gltexcoordpointer-Funktion (GL. h)
description: Die gltexcoordpointer-Funktion definiert ein Array von Texturkoordinaten.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- gltexcoordpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345939"
---
# <a name="gltexcoordpointer-function"></a>gltexcoordpointer-Funktion

Die **gltexcoordpointer** -Funktion definiert ein Array von Texturkoordinaten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoordPointer(
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

Die Anzahl der Koordinaten pro Array Element. Der Wert von *size* muss 1, 2, 3 oder 4 sein.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp der einzelnen Texturkoordinaten im Array mit den folgenden symbolischen Konstanten: **GL \_ Short**, **GL \_ int**, **GL \_ float** und **GL \_ Double**.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byte Offset zwischen aufeinander folgenden Array Elementen. Wenn *Stride* 0 (null) ist, werden die Array Elemente im Array eng verpackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf die erste Koordinate des ersten Elements im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                              | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>  | der *Typ* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | die *Größe* lag nicht bei 1, 2, 3 oder 4.<br/>     |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | *Stride* war negativ.<br/>            |



## <a name="remarks"></a>Bemerkungen

Die **gltexcoordpointer** -Funktion gibt den Speicherort und die Daten eines Arrays von Texturkoordinaten an, die beim Rendern verwendet werden sollen. Der *size* -Parameter gibt die Anzahl der Koordinaten an, die für jedes Element des Arrays verwendet werden. Der *Typparameter* gibt den Datentyp der einzelnen Texturkoordinaten an. Der *Stride* -Parameter bestimmt den Byte Offset von einem Array Element zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays. In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter als die Verwendung von separaten Arrays sein. Weitere Informationen finden Sie unter [**glinterleavedarrays**](glinterleavedarrays.md). Wenn ein Texturkoordinaten Array angegeben wird, werden Größe, Typ, Stride und Zeiger als Client seitiger Zustand gespeichert.

Ein Texturkoordinaten Array wird aktiviert, wenn Sie die **GL- \_ Textur \_ Koord- \_ Array** Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwenden [**gldrawarrays**](gldrawarrays.md), [**gldrawelements**](gldrawelements.md)und [**glarrayelement**](glarrayelement.md) das Array der Textur Koordinate. Das Array der Textur Koordinate ist standardmäßig deaktiviert.

Sie können **gltexcoordpointer** nicht in Anzeigelisten einschließen.

Wenn Sie ein Texturkoordinaten Array mithilfe von **gltexcoordpointer** angeben, werden die Werte aller Texturkoordinaten Array-Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden. Da die Texturkoordinaten Array-Parameter den Client seitigen Zustand aufweisen, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md)nicht gespeichert oder wieder hergestellt.

Obwohl beim Aufrufen von **gltexcoordpointer** innerhalb der [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paare kein Fehler generiert wird, sind die Ergebnisse nicht definiert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gltexcoordpointer** abgerufen:

[**glisenabled**](glisenabled.md) mit Argument **GL \_ Textur \_ Koord- \_ Array**

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument **GL \_ Textur \_ Koord- \_ array \_ Größe**

**glget** mit dem Argument **GL \_ Texture \_ Koord \_ array \_ Stride**

**glget** mit Argument **GL \_ Textur \_ Koord- \_ array \_ Anzahl**

**glget** mit dem Argument **GL \_ Texture Koord- \_ Arraytyp \_ \_**

[**glgetpointerv**](glgetpointerv.md) mit Argument **GL \_ Textur \_ Koord- \_ array \_ Zeiger**

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
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

[**glpopclientattrb**](glpopclientattrib.md)
</dt> <dt>

[**glpushclientatpub**](glpushclientattrib.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





