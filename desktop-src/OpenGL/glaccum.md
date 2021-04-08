---
title: glaccum-Funktion (GL. h)
description: Die Funktion "glaccum" wird auf den Akkumulations Puffer angewendet.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glaccum-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741945"
---
# <a name="glaccum-function"></a>glaccum-Funktion

Die Funktion " **glaccum** " wird auf den Akkumulations Puffer angewendet.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*schel* 
</dt> <dd>

Der Akkumulations Puffer Vorgang. Die akzeptierten symbolischen Konstanten lauten wie folgt.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**GL- \_ Accum**</dt> </dl>    | Ruft R, G, B und einen Wert aus dem Puffer ab, der derzeit zum Lesen ausgewählt ist (siehe [**glreadbuffer**](glreadbuffer.md)). Jeder Komponenten Wert wird durch 2 *n*  1 dividiert, wobei *n* die Anzahl der Bits ist, die jeder Farbkomponente im aktuell ausgewählten Puffer zugeordnet ist. Das Ergebnis ist ein Gleit Komma Wert im Bereich \[ von 0, 1 \] , der mit einem *Wert* multipliziert und der entsprechenden Pixel Komponente im Akkumulations Puffer hinzugefügt wird, wodurch der Akkumulations Puffer aktualisiert wird.<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**GL \_ Laden**</dt> </dl>       | Ähnelt dem GL- \_ Accum, mit der Ausnahme, dass der aktuelle Wert im Akkumulations Puffer nicht in der Berechnung des neuen Werts verwendet wird. Das heißt, die R-, G-, B-und A-Werte aus dem aktuell ausgewählten Puffer werden durch 2 *n*  1 dividiert, multipliziert mit *Wert* und werden dann in der entsprechenden Akkumulations Puffer Zelle gespeichert und überschreiben den aktuellen Wert.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**GL \_ Hinzufügen**</dt> </dl>          | Fügt jedem R-, G-, B-und a-Wert im Akkumulations Puffer einen *Wert* hinzu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**GL \_ .**</dt> </dl>       | Multipliziert alle R-, G-, B-und a-Werte im Akkumulations Puffer nach *Wert* und gibt die skalierte Komponente an den entsprechenden akkumulationpufferort zurück.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**GL- \_ Rückgabe**</dt> </dl> | Überträgt akkumulationspufferwerte an den Farb Puffer oder die Puffer, die zurzeit zum Schreiben ausgewählt sind. Jede R-, G-, B-und eine-Komponente wird mit einem *Wert* multipliziert und dann mit 2 *n*  1 multipliziert, an den Bereich \[ 0, 2 *n*  1 gebunden \] und in der entsprechenden Anzeige Puffer Zelle gespeichert. Die einzigen fragmentvorgänge, die auf diese Übertragung angewendet werden, sind Pixel Besitz, Scissor, Dithering und Color Write.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Ein Gleit Komma Wert, der beim Akkumulations Puffer Vorgang verwendet wird. Der *op* -Parameter bestimmt, wie der *Wert* verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | " *op* " war kein akzeptierter Wert.<br/>                                                                                                                                            |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Es war kein Akkumulations Puffer vorhanden, oder die Funktion " **glaccum** " wurde zwischen einem Aufruf von " [**glBegin**](glbegin.md) " und dem entsprechenden Aufruf von " [**glEnd**](glend.md)" aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Der Akkumulations Puffer ist ein Farb Puffer mit erweitertem Bereich. Bilder werden nicht in Sie gerendert. Stattdessen werden dem Inhalt des Akkumulations Puffers nach dem Rendering Bilder hinzugefügt, die in einem der Farb Puffer gerendert werden. Sie können Effekte wie Antialiasing (von Punkten, Linien und Polygone), Bewegungsunschärfe und Tiefe des Felds erstellen, indem Sie mit unterschiedlichen Transformations Matrizen generierte Bilder sammeln.

Jedes Pixel im Akkumulations Puffer besteht aus roten, grünen, blauen und Alpha Werten. Die Anzahl der Bits pro Komponente im Akkumulations Puffer hängt von der Implementierung ab. Sie können diese Zahl überprüfen, indem Sie [**glgetintegerv**](glgetintegerv.md) viermal aufrufen, mit den Argumenten GL \_ Accum \_ Red \_ Bits, GL \_ Accum \_ Green \_ Bits, GL \_ Accum \_ Blue \_ Bits und GL \_ Accum \_ alpha \_ Bits bzw. Unabhängig von der Anzahl der Bits pro Komponente beträgt der von jeder Komponente gespeicherte Wertebereich \[ 1,? 1 \] . Die Akkumulations Puffer Pixel werden mit Frame Puffer Pixel eins-zu-eins zugeordnet.

Die Funktion " **glaccum** " wird auf den Akkumulations Puffer angewendet. Das erste Argument ( *op*) ist eine symbolische Konstante, die einen Akkumulations Puffer Vorgang auswählt. Das zweite Argument, *value*, ist ein Gleit Komma Wert, der in diesem Vorgang verwendet werden soll. Es werden fünf Vorgänge angegeben: GL \_ Accum, GL \_ Load, GL \_ Add, GL \_ mult und GL \_ Return.

Alle Akkumulations Puffer Vorgänge sind auf den Bereich des aktuellen Scheren Felds beschränkt und werden identisch mit den Komponenten rot, grün, blau und Alpha der einzelnen Pixel angewendet. Der Inhalt einer Metadatenkomponente des Akkumulations Puffers ist nicht definiert, wenn der **glaccum** -Vorgang einen Wert außerhalb des Bereichs \[ 1, 1 ergibt \] .

Verwenden Sie zum Löschen des Akkumulations Puffers die Funktion " [**glclearaccum**](glclearaccum.md) ", um die Werte für R, G, B und a festzulegen, und geben Sie eine [**glClear**](glclear.md) -Funktion mit aktiviertem Akkumulations Puffer aus.

Nur die Pixel innerhalb des aktuellen Scheren Felds werden von einem beliebigen **glaccum** -Vorgang aktualisiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glaccum** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Accum- \_ roten \_ Bits

**glget** mit Argument GL- \_ Accum- \_ grünen \_ Bits

**glget** mit dem Argument GL \_ Accum \_ Blue \_ Bits

**glget** mit dem Argument GL \_ Accum \_ alpha \_ Bits

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

[**glblendfunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glclearaccum**](glclearaccum.md)
</dt> <dt>

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gllogicop**](gllogicop.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glread Buffer**](glreadbuffer.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glscissor**](glscissor.md)
</dt> <dt>

[**glstencilop**](glstencilop.md)
</dt> </dl>

 

 





