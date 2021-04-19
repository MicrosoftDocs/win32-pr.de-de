---
title: glgetteximage-Funktion (GL. h)
description: Die Funktion "glgetteximage" gibt ein Textur Bild zurück.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glgetteximage-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342660"
---
# <a name="glgetteximage-function"></a>glgetteximage-Funktion

Die Funktion " **glgetteximage** " gibt ein Textur Bild zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Gibt an, welche Textur abgerufen werden soll. GL \_ Texture \_ 1D und GL \_ Texture \_ 2D werden akzeptiert.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailstufe des gewünschten Bilds. Ebene 0 ist die Basis Image Ebene. Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.

</dd> <dt>

*format* 
</dt> <dd>

Ein Pixel Format für die zurückgegebenen Daten. Die unterstützten Formate sind GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ Luminance, GL \_ BGR \_ ext, GL \_ BGRA \_ ext und GL \_ Luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Ein Pixeltyp für die zurückgegebenen Daten. Die unterstützten Typen sind GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.

</dd> <dt>

*Pixel* 
</dt> <dd>

Gibt das Textur Bild zurück. Muss ein Zeiger auf ein Array des Typs sein, der durch den- *Typ* angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Ziel*, *Format* oder *Typ* war kein akzeptierter Wert.<br/>                                                                    |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Ebene* ist kleiner als 0 (null) oder größer als *Log* 2 (*Max*), wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.<br/>      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md) aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetteximage** " gibt ein Textur Bild in *Pixel* zurück. Der *target* -Parameter gibt an, ob das gewünschte Textur Bild durch [**glTexImage1D**](glteximage1d.md)**(** GL \_ Texture \_ 1D **)** oder durch [**glTexImage2D**](glteximage2d.md)**(** GL \_ Texture \_ 2D **)** angegeben wird. Der *Level* -Parameter gibt die Detailstufe des gewünschten Bilds an. Die *Format* -und *Typparameter* geben das Format und den Typ des gewünschten Bilds an. Eine Beschreibung der zulässigen Werte für die *Format* -und *Typparameter* finden Sie unter **glTexImage1D** und [**gldrawpixels**](gldrawpixels.md).

Der Vorgang von **glgetteximage** ist am besten zu verstehen, indem das ausgewählte, interne Textur Bild mit vier Komponenten als RGBA-Farb Puffer für die Größe des Bilds betrachtet wird. Die Semantik von **glgetteximage** ist dann identisch mit denen von [**glread Pixel**](glreadpixels.md) , die mit dem gleichen *Format* und *Typ* aufgerufen werden. Wenn *x* und *y* auf 0 (null) festgelegt sind, wird die *Breite* auf die Breite des Textur Bilds (einschließlich des Rahmens, falls angegeben) und die *Höhe* auf 1 für 1-d-Bilder festgelegt, oder auf die Höhe des Textur Bilds (einschließlich des Rahmens, sofern angegeben) für 2D-Bilder.

Da es sich bei dem internen Textur Bild um ein RGBA-Bild handelt, werden die Pixel Formate "GL \_ Color \_ Index", "GL \_ Stencil \_ Index" und "GL- \_ tiefen Komponente" \_ nicht akzeptiert, und die Bitmap "Pixel Type GL" \_ wird

Wenn das ausgewählte Textur Bild keine vier Komponenten enthält, werden die folgenden Zuordnungen angewendet. Texturen mit einer einzelnen Komponente werden als RGBA-Puffer behandelt, wobei rot auf den Einzelkomponenten Wert festgelegt ist und grün, blau und Alpha auf 0 (null) festgelegt ist.

Texturen mit zwei Komponenten werden als RGBA-Puffer behandelt, wobei rot auf den Wert von Komponente NULL, Alpha auf den Wert von Komponente 1 und grün und blau auf NULL festgelegt ist. Schließlich werden drei komponententexturen als RGBA-Puffer behandelt, wobei rot auf Komponente 0 (null), grün auf Komponente 1, blau auf Komponente 2 und Alpha auf NULL festgelegt ist.

Um die erforderliche Größe von *Pixeln* zu ermitteln, verwenden Sie [**glgettexlevelparameter**](glgettexlevelparameter.md) , um die Dimensionen des internen Textur Bilds zu ermitteln, und Skalieren Sie dann die erforderliche Anzahl von Pixeln nach dem für die einzelnen Pixel erforderlichen Speicher, basierend auf *Format* und *Typ*. Stellen Sie sicher, dass die Parameter für die Pixel Speicherung berücksichtigt werden, insbesondere die Ausrichtung von GL \_ Pack \_ .

Wenn ein Fehler generiert wird, wird keine Änderung an dem Inhalt der *Pixel* vorgenommen.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit " **glgetteximage**" abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pack \_ -Ausrichtung und anderen

[**glgettexlevelparameter**](glgettexlevelparameter.md) mit Argument GL \_ Textur \_ Width

**glgettexlevelparameter** mit Argument GL \_ Textur \_ Height

**glgettexlevelparameter** mit dem Argument "GL \_ Texture \_ Border"

**glgettexlevelparameter** mit Argument GL- \_ Textur \_ Komponenten

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

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgettexlevelparameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





