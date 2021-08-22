---
title: glNewList-Funktion (Gl.h)
description: Die Funktionen glNewList und glEndList erstellen oder ersetzen eine Anzeigeliste. | glNewList-Funktion (Gl.h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glNewList-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0103baa9786cdfed0d6e999021453e30da5083571c9a2c9054da701977a9493f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741340"
---
# <a name="glnewlist-function"></a>glNewList-Funktion

Die **Funktionen glNewList** und [**glEndList**](glendlist.md) erstellen oder ersetzen eine Anzeigeliste.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*list* 
</dt> <dd>

Der Anzeigelistenname.

</dd> <dt>

*mode* 
</dt> <dd>

Der Kompilierungsmodus. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                      | Bedeutung                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**GL \_ COMPILE**</dt> </dl>                                       | Befehle werden lediglich kompiliert.<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**GL \_ COMPILE \_ AND \_ EXECUTE**</dt> </dl> | Befehle werden ausgeführt, wenn sie in die Anzeigeliste kompiliert werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *list* war 0 (null).<br/>                                                                                                           |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Anzeigelisten sind Gruppen von OpenGL-Befehlen, die für die nachfolgende Ausführung gespeichert wurden. Die Anzeigelisten werden mit **glNewList erstellt.** Alle nachfolgenden Befehle werden in der Anzeigeliste in der ausgegebenen Reihenfolge platziert, bis **glEndList** aufgerufen wird.

Die **glNewList-Funktion** verfügt über zwei Parameter. Der erste Parameter, *list,* ist eine positive ganze Zahl, die zum eindeutigen Namen für die Anzeigeliste wird. Namen können mit [**glGenLists**](glgenlists.md) erstellt und reserviert und mit [**glIsList**](glislist.md)auf Eindeutigkeit getestet werden. Der zweite Parameter, *mode,* ist eine symbolische Konstante, die einen der beiden vorangehenden Werte annehmen kann.

Bestimmte Befehle werden nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt, unabhängig vom Anzeigelistenmodus. Diese Befehle sind [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)und alle [**glGet-Routinen.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

Ebenso werden [**glTexImage2D**](glteximage2d.md) und [**glTexImage1D**](glteximage1d.md) sofort ausgeführt und nicht in die Anzeigeliste kompiliert, wenn ihr erstes Argument GL PROXY TEXTURE 2D bzw. \_ GL PROXY TEXTURE \_ \_ \_ \_ \_ 1D ist.

Wenn die **glEndList-Funktion** gefunden wird, wird die Definition der Anzeigeliste abgeschlossen, indem die Liste der Liste mit dem eindeutigen Namen *(angegeben* im **Befehl glNewList) hinzugefügt** wird. Wenn bereits eine Anzeigeliste mit *einer* Namensliste vorhanden ist, wird sie nur ersetzt, wenn **glEndList** aufgerufen wird.

Die [**Funktionen glCallList**](glcalllist.md) [**und glCallLists**](glcalllists.md) können in Anzeigelisten eingegeben werden. Die Befehle in der Anzeigeliste oder den Listen, die von **glCallList** oder **glCallLists** ausgeführt werden, sind nicht in der zu erstellenden Anzeigeliste enthalten, auch wenn der Listenerstellungsmodus GL \_ COMPILE AND EXECUTE \_ \_ ist.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glNewList ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MATRIX \_ MODE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEndList**](glendlist.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> </dl>

 

 





