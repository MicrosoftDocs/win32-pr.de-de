---
title: glstencilop-Funktion (GL. h)
description: Die Funktion "glstencilop" legt die Test Aktionen der Schablone fest.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glstencilop-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340355"
---
# <a name="glstencilop-function"></a>glstencilop-Funktion

Die Funktion " **glstencilop** " legt die Test Aktionen der Schablone fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UN* 
</dt> <dd>

Die Aktion, die ausgeführt werden soll, wenn der Schablonen Test fehlschlägt. Die folgenden sechs symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                | Bedeutung                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**GL \_ beibehalten**</dt> </dl>          | Behält den aktuellen Wert bei.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ null**</dt> </dl>          | Legt den Schablonen Puffer Wert auf 0 (null) fest.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**GL \_ ersetzen**</dt> </dl> | Legt den Schablonen Puffer Wert entsprechend der Angabe durch **glstencilfunc** auf *ref* fest.<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**GL- \_ INCR**</dt> </dl>          | Inkremente den aktuellen Schablonen Puffer Wert. Bindet an den maximalen darstellbaren Wert ohne Vorzeichen.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL- \_ decr**</dt> </dl>          | Dekremente den aktuellen Schablonen Puffer Wert. Bindet auf NULL.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ Invert**</dt> </dl>    | Bitweise kehrt den aktuellen Schablonen Puffer Wert um.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Schablone-Aktion, wenn der Schablone-Test erfolgreich verläuft, aber der tiefen Test fehlschlägt. Akzeptiert dieselben symbolischen Konstanten als *fehlgeschlagen.*

</dd> <dt>

*ZPass* 
</dt> <dd>

Schablone-Aktion, wenn der Schablonen Test und der tiefen Test bestanden werden, oder wenn der Schablonen Test erfolgreich verläuft und entweder kein tiefen Puffer vorhanden ist oder keine tiefen Tests aktiviert sind. Akzeptiert dieselben symbolischen Konstanten als *fehl* geschlagen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | " *Fail*", " *zfail*" oder " *ZPass* " war ein anderer Wert als die sechs definierten Konstanten Werte.<br/>                                      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Durch die Schablone, z. b. *z*-Pufferung, wird das Zeichnen pro Pixel aktiviert und deaktiviert. Sie zeichnen mithilfe von OpenGL-Zeichen primitiven in die Schablone-Ebenen und erzeugen dann Geometrie und Bilder mithilfe der Schablonen Flächen, um Teile des Bildschirms zu maskieren. Die Schablone wird in der Regel in Multipass-renderingalgorithmen verwendet, um besondere Effekte zu erzielen, wie z. b. Decals, Gliederung und konstruktives solides Geometrie Rendering.

Der Schablone-Test entfernt bedingt ein Pixel basierend auf dem Ergebnis eines Vergleichs zwischen dem Wert im Schablonen Puffer und einem Verweis Wert. Der Test ist mit " [**glEnable**](glenable.md) "-und " [**gldeaktiviert**](gldisable.md) "-aufrufen mit dem Argument "GL \_ Stencil Test" aktiviert \_ und mit " [**glstencilfunc**](glstencilfunc.md)" gesteuert

Die **glstencilop** -Funktion nimmt drei Argumente an, die angeben, was mit dem gespeicherten Schablonen Wert geschieht, während die Schablone aktiviert ist. Wenn der Schablone-Test fehlschlägt, wird keine Änderung an den Farb-oder tiefen Puffern des Pixels vorgenommen, und der Fehler gibt an, was mit dem Inhalt der *Schablone-Puffer* passiert.

Schablonen Puffer Werte werden als ganze Zahlen ohne Vorzeichen behandelt. Wenn inkrementiert und dekrementiert, werden die Werte an 0 und 2 *n* 1 gebunden, wobei *n* der Wert ist, der durch Abfragen von GL-Schablonen Bits zurückgegeben wird \_ \_ .

Die anderen beiden Argumente für **glstencilop** geben Schablonen Puffer Aktionen an, wenn nachfolgende tiefen Puffer Tests erfolgreich verlaufen (*ZPass*) oder Fail (*zfail*). (Siehe [**gldepthfunc**](gldepthfunc.md).) Sie werden mit denselben sechs symbolischen Konstanten wie " *Fail*" angegeben. Beachten Sie, dass *zfail* ignoriert wird, wenn kein tiefen Puffer vorhanden ist oder wenn der tiefen Puffer nicht aktiviert ist. In diesen Fällen geben *Fail* und *ZPass* eine Schablone-Aktion an, wenn der Schablonen Test fehlschlägt bzw. übergibt.

Anfänglich ist der Schablonen Test deaktiviert. Wenn kein Schablonen Puffer vorhanden ist, kann keine Schablone geändert werden, und es ist so, als ob die Schablonen Tests immer bestanden werden, unabhängig von jedem beliebigen Aufrufe von **glstencilop**.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glstencilop** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ Fail

**glget** mit dem Argument GL \_ Stencil \_ Pass \_ Tiefe \_ Pass

**glget** mit dem Argument GL \_ Stencil \_ Pass \_ Tiefe \_ Fail

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

[**glstencilfunc**](glstencilfunc.md)
</dt> </dl>

 

 





