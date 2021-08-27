---
title: glAccum-Funktion (Gl.h)
description: Die glAccum-Funktion arbeitet mit dem Akkumulationspuffer.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum-Funktion OpenGL
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
ms.openlocfilehash: 0820d27bf6aff05916eb179e4dfd0b51a0746e2c6e5a6f4e5f3bdfe8f3e6d91a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082260"
---
# <a name="glaccum-function"></a>glAccum-Funktion

Die **glAccum-Funktion** arbeitet mit dem Akkumulationspuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*op* 
</dt> <dd>

Der Akkumulationspuffervorgang. Die akzeptierten symbolischen Konstanten sind wie folgt.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**GL \_ ACCUM**</dt> </dl>    | Ruft R-, G-, B- und A-Werte aus dem Puffer ab, der derzeit zum Lesen ausgewählt ist (siehe [**glReadBuffer**](glreadbuffer.md)). Jeder Komponentenwert wird durch 2 *n*  1 dividiert, wobei *n* die Anzahl der Bits ist, die jeder Farbkomponente im derzeit ausgewählten Puffer zugeordnet sind. Das Ergebnis ist ein Gleitkommawert im Bereich \[ 0,1, der \] mit dem *Wert* multipliziert und der entsprechenden Pixelkomponente im Akkumulationspuffer hinzugefügt wird, wodurch der Akkumulationspuffer aktualisiert wird.<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**GL \_ LOAD**</dt> </dl>       | Ähnlich wie GL \_ ACCUM, mit der Ausnahme, dass der aktuelle Wert im Akkumulationspuffer nicht bei der Berechnung des neuen Werts verwendet wird. Das heißt, die R-, G-, B- und A-Werte aus dem derzeit ausgewählten Puffer werden durch 2 *n*  1 dividiert, multipliziert mit *dem Wert* und dann in der entsprechenden Akkumulationspufferzelle gespeichert, wobei der aktuelle Wert überschrieben wird.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**GL \_ ADD**</dt> </dl>          | Fügt jedem R, G, B und A im Akkumulationspuffer *einen Wert* hinzu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**GL \_ MULT**</dt> </dl>       | Multipliziert alle R-, G-, B- und A-Werte im Akkumulationspuffer mit dem *Wert* und gibt die skalierte Komponente an die entsprechende Akkumulationspufferposition zurück.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**GL \_ RETURN**</dt> </dl> | Überträgt Akkumulationspufferwerte an den Farbpuffer oder die Puffer, die derzeit zum Schreiben ausgewählt sind. Jede R-, G-, B- und A-Komponente wird mit dem *Wert* multipliziert, dann mit 2 *n*  1 multipliziert, an den Bereich \[ 0, 2 *n*  1 gebunden \] und in der entsprechenden Anzeigepufferzelle gespeichert. Die einzigen Fragmentvorgänge, die auf diese Übertragung angewendet werden, sind Pixelbesitz, Scissor, Dithering und Farbschreibmasken.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Ein Im Akkumulationspuffervorgang verwendeter Gleitkommawert. Der *op-Parameter* bestimmt, wie *value* verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *op* war kein akzeptierter Wert.<br/>                                                                                                                                            |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Es gab keinen Akkumulationspuffer, oder die Funktion **glAccum** wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Der Akkumulationspuffer ist ein Farbpuffer mit erweitertem Bereich. Bilder werden darin nicht gerendert. Stattdessen werden Bilder, die in einen der Farbpuffer gerendert werden, dem Inhalt des Akkumulationspuffers nach dem Rendern hinzugefügt. Sie können Effekte wie Antialiasing (von Punkten, Linien und Polygonen), Bewegungsunschärfe und Feldtiefe erstellen, indem Sie Bilder sammeln, die mit verschiedenen Transformationsmatrizen generiert wurden.

Jedes Pixel im Akkumulationspuffer besteht aus Rot-, Grün-, Blau- und Alphawerten. Die Anzahl der Bits pro Komponente im Akkumulationspuffer hängt von der Implementierung ab. Sie können diese Zahl untersuchen, indem Sie [**glGetIntegerv**](glgetintegerv.md) viermal aufrufen, mit den Argumenten GL \_ ACCUM \_ RED \_ BITS, GL \_ ACCUM \_ GREEN \_ BITS, GL \_ ACCUM BLUE \_ \_ BITS bzw. GL \_ ACCUM ALPHA \_ \_ BITS. Unabhängig von der Anzahl der Bits pro Komponente beträgt der von jeder Komponente gespeicherte Wertebereich jedoch \[ 1,?1 \] . Die Akkumulationspufferpixel werden 1:1 mit Framepufferpixeln zugeordnet.

Die **glAccum-Funktion** arbeitet mit dem Akkumulationspuffer. Das erste Argument *op* ist eine symbolische Konstante, die einen Akkumulationspuffervorgang auswählt. Das zweite Argument, *value,* ist ein Gleitkommawert, der in diesem Vorgang verwendet werden soll. Es werden fünf Vorgänge angegeben: GL \_ ACCUM, GL \_ LOAD, GL \_ ADD, GL \_ MULT und GL \_ RETURN.

Alle Akkumulationspuffervorgänge sind auf den Bereich des aktuellen Scissor-Felds beschränkt und werden identisch auf die Rot-, Grün-, Blau- und Alphakomponenten jedes Pixels angewendet. Der Inhalt einer Akkumulationspufferpixelkomponente ist nicht definiert, wenn der **GlAccum-Vorgang** einen Wert außerhalb des Bereichs \[ von 1,1 \] ergibt.

Verwenden Sie zum Löschen des Akkumulationspuffers die [**glClearAccum-Funktion,**](glclearaccum.md) um R-, G-, B- und A-Werte anzugeben, auf die sie festgelegt werden soll, und geben Sie eine [**glClear-Funktion**](glclear.md) mit aktivierter Akkumulationspuffer aus.

Nur die Pixel innerhalb des aktuellen Scissor-Felds werden durch einen **glAccum-Vorgang** aktualisiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glAccum-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ ACCUM \_ RED \_ BITS

**glGet** mit argument GL \_ ACCUM \_ GREEN \_ BITS

**glGet** mit dem Argument GL \_ ACCUM \_ BLUE \_ BITS

**glGet** mit argument GL \_ ACCUM \_ ALPHA \_ BITS

## <a name="requirements"></a>Requirements (Anforderungen)



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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





