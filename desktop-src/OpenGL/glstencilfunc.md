---
title: glstencilfunc-Funktion (GL. h)
description: Die Funktion "glstencilfunc" legt die Funktion und den Verweis Wert für Schablonen Tests fest.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glstencilfunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346133"
---
# <a name="glstencilfunc-function"></a>glstencilfunc-Funktion

Die Funktion " **glstencilfunc** " legt die Funktion und den Verweis Wert für Schablonen Tests fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*func* 
</dt> <dd>

Die Testfunktion. Die folgenden acht Token sind gültig.



| Wert                                                                                                                                                   | Bedeutung                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nie**</dt> </dl>          | Schlägt immer fehl.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ weniger**</dt> </dl>             | Übergibt if (*ref*  &  *Mask*) < (*Schablone*  &  *Mask*).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ lequal**</dt> </dl>       | Übergibt if (*ref*  &  *Mask*) = (*Schablone*  &  *Mask*).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ größer**</dt> </dl>    | Übergibt if (*ref*  &  *Mask*) > (*Schablone*  &  *Mask*).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ gequal**</dt> </dl>       | Übergibt if (*ref*  &  *Mask*) = (*Schablone*  &  *Mask*).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ gleich**</dt> </dl>          | Übergibt if (*ref*  &  *Mask*) = (*Schablone*  &  *Mask*).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL- \_ NotEqual**</dt> </dl> | Übergibt if (*ref*  &  *Mask*)? (*Schablone*  &  *Mask*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**immer GL. \_**</dt> </dl>       | Übergibt immer.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

Der Verweis Wert für den Schablonen Test. Der *ref* -Parameter wird an den Bereich \[ von 0, 2 *n* 1 \] , gebunden, wobei *n* die Anzahl der bitebenen im Schablonen Puffer ist.

</dd> <dt>

*mask* 
</dt> <dd>

Eine Maske, die beim Abschluss des Tests sowohl mit dem Verweis Wert als auch mit dem gespeicherten Schablonen Wert **erstellt wird.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Func* war keiner der acht akzeptierten Werte.<br/>                                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Durch die Schablone, z. b. *z*-Pufferung, wird das Zeichnen pro Pixel aktiviert und deaktiviert. Sie zeichnen mithilfe von OpenGL-Zeichen primitiven in die Schablone-Ebenen und erzeugen dann Geometrie und Bilder mithilfe der Schablonen Flächen, um Teile des Bildschirms zu maskieren. Die Schablone wird in der Regel in Multipass-renderingalgorithmen verwendet, um besondere Effekte zu erzielen, wie z. b. Decals, Gliederung und konstruktives solides Geometrie Rendering.

Der Schablone-Test entfernt bedingt ein Pixel basierend auf dem Ergebnis eines Vergleichs zwischen dem Verweis Wert und dem Wert im Schablonen Puffer. Der Test wird durch [**glEnable**](glenable.md) und [**glEnable**](gldisable.md) mit dem Argument GL \_ Stencil \_ Test aktiviert. Auf der Grundlage des Ergebnisses des Schablonen Tests ausgeführte Aktionen werden mit [**glstencilop**](glstencilop.md)angegeben.

Der *Func* -Parameter ist eine symbolische Konstante, die die Schablone-Vergleichsfunktion bestimmt. Er akzeptiert einen der oben gezeigten acht Werte. Der *ref* -Parameter ist ein ganzzahliger Verweis Wert, der im Schablone-Vergleich verwendet wird. Der Wert wird an den Bereich \[ 0, 2 *n* 1 geklammert \] , wobei *n* die Anzahl der bitflächen im Schablonen Puffer ist. Der *Mask* -Parameter ist bitweise **und** wird sowohl mit dem Verweis Wert als auch mit dem gespeicherten Schablonen Wert, wobei die Werte und die ED **-** Werte am Vergleich beteiligt sind.

Wenn *Schablone* den Wert darstellt, der im entsprechenden Schablone-Puffer Speicherort gespeichert ist, zeigt die vorangehende Liste die Auswirkungen jeder Vergleichsfunktion an, die von *Func* angegeben werden kann. Nur, wenn der Vergleich erfolgreich ist, wird das Pixel an die nächste Phase im rasterisierungsprozess übergeben (siehe [**glstencilop**](glstencilop.md)). Alle Tests behandeln *Schablonen* Werte als ganze Zahlen ohne Vorzeichen im Bereich \[ 0, 2 *n* 1 \] , wobei *n* die Anzahl der bitebenen im Schablonen Puffer ist.

Anfänglich ist der Schablone-Test deaktiviert. Wenn kein Schablonen Puffer vorhanden ist, kann keine Schablone geändert werden, und dies ist der Fall, wenn der Schablone-Test immer durchlaufen wird.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glstencilfunc** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ Func

**glget** mit dem Argument GL \_ Stencil \_ Wert \_ Mask

**glget** mit Argument GL \_ Stencil \_ Ref

**glget** mit Argument GL- \_ Schablonen \_ Bits

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Stencil \_ Test

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

[**glalphafunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glblendfunc**](glblendfunc.md)
</dt> <dt>

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**gllogicop**](gllogicop.md)
</dt> <dt>

[**glstencilop**](glstencilop.md)
</dt> </dl>

 

 





