---
title: glGetTexImage-Funktion (Gl.h)
description: Die glGetTexImage-Funktion gibt ein Texturbild zurück.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage-Funktion OpenGL
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
ms.openlocfilehash: b116bc4ae517d0767d794767ad5232d8537033d62a099a3906f9f2ca96a7166c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493750"
---
# <a name="glgetteximage-function"></a>glGetTexImage-Funktion

Die **glGetTexImage-Funktion** gibt ein Texturbild zurück.

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

Gibt an, welche Textur erhalten werden soll. GL \_ TEXTURE \_ 1D und GL \_ TEXTURE \_ 2D werden akzeptiert.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer des gewünschten Bilds. Ebene 0 ist die Basisimageebene. Ebene *n* ist das *n-te* Mipmap-Reduzierungsbild.

</dd> <dt>

*format* 
</dt> <dd>

Ein Pixelformat für die zurückgegebenen Daten. Die unterstützten Formate sind GL \_ RED, GL \_ \_ GREEN, GL BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ LUMINANCE, GL \_ BGR \_ EXT, GL BGRA EXT und GL \_ \_ \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Ein Pixeltyp für die zurückgegebenen Daten. Die unterstützten Typen sind GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT und GL \_ FLOAT.

</dd> <dt>

*Pixel* 
</dt> <dd>

Gibt das Texturbild zurück. Sollte ein Zeiger auf ein Array des vom Typ angegebenen Typs *sein.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target,* *format* oder *type* war kein akzeptierter Wert.<br/>                                                                    |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* ist kleiner als 0 (null) oder größer als *Protokoll* 2 (*max),* wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ ist.<br/>      |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetTexImage-Funktion** gibt ein Texturbild in Pixel *zurück.* Der *Zielparameter* gibt an, ob das gewünschte Texturbild eins ist, das von [**glTexImage1D**](glteximage1d.md)**(** GL TEXTURE \_ \_ 1D )**oder** von [**glTexImage2D**](glteximage2d.md)**(** GL TEXTURE \_ \_ 2D **)** angegeben wird. Der *level-Parameter* gibt die Detailebenennummer des gewünschten Bilds an. Die *Format-* *und Typparameter* geben das Format und den Typ des gewünschten Bildarrays an. Eine Beschreibung der zulässigen  Werte  für die Format- bzw. Typparameter finden Sie unter **glTexImage1D** und [**glDrawPixels**](gldrawpixels.md).

Der Vorgang **von glGetTexImage** wird am besten verstanden, indem das ausgewählte interne Texturbild mit vier Komponenten als RGBA-Farbpuffer für die Größe des Bilds betrachtet wird. Die Semantik von **glGetTexImage** ist dann mit der von [**glReadPixels**](glreadpixels.md) identisch, die mit dem gleichen Format und Typ aufgerufen werden, bei denen  *x* und *y* auf 0 *festgelegt* sind, die Breite auf die Breite des Texturbilds festgelegt ist (einschließlich rahmen, falls eins angegeben wurde), und die Höhe für 2D-Bilder auf eins oder auf die Höhe des Texturbilds (einschließlich Rahmen, sofern angegeben).  

Da das interne Texturbild ein RGBA-Bild ist, werden die Pixelformate GL \_ COLOR \_ INDEX, GL \_ STENCIL INDEX und GL DEPTH COMPONENT nicht \_ akzeptiert, \_ \_ und \_ der Pixeltyp GL BITMAP wird nicht akzeptiert.

Wenn das ausgewählte Texturbild nicht vier Komponenten enthält, werden die folgenden Zuordnungen angewendet. Einkomponententexturen werden als RGBA-Puffer behandelt, bei dem Rot auf den Einzelkomponentenwert und Grün, Blau und Alpha auf 0 (null) festgelegt sind.

Texturen mit zwei Komponenten werden als RGBA-Puffer behandelt. Rot wird auf den Wert der Komponente 0 festgelegt, Alpha auf den Wert von Komponente 1 und Grün und Blau auf 0 (null). Schließlich werden Texturen mit drei Komponenten als RGBA-Puffer behandelt, bei dem Rot auf Komponente 0 festgelegt ist, Grün auf Komponente 1, Blau auf Komponente 2 und Alpha auf 0 festgelegt ist.

Um die erforderliche Größe von Pixeln zu *bestimmen,* verwenden Sie [**glGetTexLevelParameter,**](glgettexlevelparameter.md) um die Abmessungen des internen Texturbilds  zu ermitteln, und skalieren Sie dann die erforderliche Anzahl von Pixeln anhand des für jedes Pixel erforderlichen Speichers basierend auf Format und *Typ*. Achten Sie darauf, die Pixelspeicherparameter zu berücksichtigen, insbesondere GL \_ PACK \_ ALIGNMENT.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *Pixeln vorgenommen.*

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glGetTexImage ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ PACK ALIGNMENT und \_ anderen

[**glGetTexLevelParameter**](glgettexlevelparameter.md) mit Argument GL \_ TEXTURE \_ WIDTH

**glGetTexLevelParameter** mit Argument GL \_ TEXTURE \_ HEIGHT

**glGetTexLevelParameter** mit Argument GL \_ TEXTURE \_ BORDER

**glGetTexLevelParameter** mit Argument GL \_ TEXTURE \_ COMPONENTS

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





