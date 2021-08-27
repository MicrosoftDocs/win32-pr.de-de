---
title: glBindTexture-Funktion (Gl.h)
description: Die glBindTexture-Funktion ermöglicht die Erstellung einer benannten Textur, die an ein Texturziel gebunden ist.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f7f108a0ce4fbc60aba6dc0430227eab15218fe17f80800678fc16b54bbc39f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082220"
---
# <a name="glbindtexture-function"></a>glBindTexture-Funktion

Die **glBindTexture-Funktion** ermöglicht die Erstellung einer benannten Textur, die an ein Texturziel gebunden ist.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Das Ziel, an das die Textur gebunden ist. Muss den Wert GL \_ TEXTURE \_ 1D oder GL \_ TEXTURE \_ 2D aufweisen.

</dd> <dt>

*Textur* 
</dt> <dd>

Der Name einer Textur. Der Texturname kann derzeit nicht verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | Das *Parameterziel* war kein akzeptierter Wert.<br/>                                                                                                                                                       |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die *Parametertextur* hatte nicht die gleiche Dimensionalität wie *das Ziel,* oder die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Mit **der glBindTexture-Funktion** können Sie eine benannte Textur erstellen. Wenn **Sie glBindTexture** aufrufen, wobei *das Ziel* auf GL TEXTURE \_ \_ 1D oder GL TEXTURE \_ \_ 2D festgelegt ist und die *Textur* auf den Namen der neuen Textur festgelegt ist, die Sie erstellt haben, wird der Texturname an das entsprechende Texturziel gebunden. Wenn eine Textur an ein Ziel gebunden ist, ist die vorherige Bindung für dieses Ziel nicht mehr wirksam.

Texturnamen sind ganze Zahlen ohne Vorzeichen, wobei der Wert 0 reserviert ist, um die Standardtextur für jedes Texturziel darzustellen. Texturnamen und die entsprechenden Texturinhalte befinden sich lokal im freigegebenen Anzeigelistenbereich des aktuellen OpenGL-Renderingkontexts. Zwei Renderingkontexte verwenden Texturnamen nur, wenn sie auch Anzeigelisten gemeinsam verwenden. Sie können einen Satz neuer Texturnamen mit [**glGenTextures**](glgentextures.md)generieren.

Wenn eine Textur zum ersten Mal gebunden wird, geht sie von der Dimensionalität ihres Texturziels aus. Eine an GL TEXTURE 1D gebundene Textur \_ \_ wird eindimensional, und eine an GL \_ TEXTURE \_ 2D gebundene Textur wird zweidimensional. Vorgänge, die Sie für ein Texturziel ausführen, wirken sich auch auf eine Textur aus, die an das Ziel gebunden ist. Wenn Sie ein Texturziel abfragen, ist der Rückgabewert der Zustand der texturgebundenen Textur. Texturziele werden zu Aliasen für Texturen, die derzeit an sie gebunden sind.

Wenn Sie eine Textur mit **glBindTexture** binden, bleibt die Bindung aktiv, bis eine andere Textur an dasselbe Ziel gebunden ist oder Sie die gebundene Textur mit der [**glDeleteTextures-Funktion**](gldeletetextures.md) löschen. Nachdem Sie eine benannte Textur erstellt haben, können Sie sie an ein Texturziel binden, das so oft wie nötig die gleiche Dimensionalität hat.

Es ist in der Regel viel schneller, **glBindTexture** zum Binden einer vorhandenen benannten Textur an eines der Texturziele zu verwenden, als das Texturbild mit [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md)neu zu laden. Verwenden Sie [**glPrioritizeTextures, um**](glprioritizetextures.md)die Texturleistung zusätzlich zu steuern.

Sie können Aufrufe von **glBindTexture** in Anzeigelisten einschließen.

> [!Note]  
> Die **glBindTexture-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glBindTexture** ab:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ TEXTURE \_ 1D \_ BINDING

**glGet** mit Argument GL \_ TEXTURE \_ 2D \_ BINDING

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





