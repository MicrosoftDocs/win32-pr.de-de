---
title: glEndList-Funktion (Gl.h)
description: Die Funktionen glNewList und glEndList erstellen oder ersetzen eine Anzeigeliste. | glEndList-Funktion (Gl.h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glEndList-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad75f62b3b049f2244b6e701f69654d110c559b337c0d4bb72da75af93f954f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081520"
---
# <a name="glendlist-function"></a>glEndList-Funktion

Die [**Funktionen glNewList**](glnewlist.md) und **glEndList** erstellen oder ersetzen eine Anzeigeliste.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | **glEndList** wurde ohne **vorangehendes glNewList** oder aufgerufen, wenn **glnewlist** aufgerufen wurde, während eine Anzeigeliste definiert wurde.<br/> |



## <a name="remarks"></a>Hinweise

Anzeigelisten sind Gruppen von OpenGL-Befehlen, die für die nachfolgende Ausführung gespeichert wurden. Die Anzeigelisten werden mit [**glNewList erstellt.**](glnewlist.md) Alle nachfolgenden Befehle werden in der Anzeigeliste in der Reihenfolge platziert, in der sie ausgegeben werden, bis **glEndList** aufgerufen wird.

Die [**glNewList-Funktion**](glnewlist.md) verfügt über zwei Parameter. Der erste Parameter, *list,* ist eine positive ganze Zahl, die zum eindeutigen Namen für die Anzeigeliste wird. Namen können mit [**glGenLists**](glgenlists.md) erstellt und reserviert und mit [**glIsList**](glislist.md)auf Eindeutigkeit getestet werden. Der zweite Parameter, *mode,* ist eine symbolische Konstante, die einen der beiden vorangehenden Werte annehmen kann.

Bestimmte Befehle werden nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt, unabhängig vom Anzeigelistenmodus. Diese Befehle sind [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)und alle [**glGet-Routinen.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

Ebenso werden [**glTexImage2D**](glteximage2d.md) und [**glTexImage1D**](glteximage1d.md) sofort ausgeführt und nicht in die Anzeigeliste kompiliert, wenn ihr erstes Argument GL PROXY TEXTURE 2D bzw. \_ GL PROXY TEXTURE \_ \_ \_ \_ \_ 1D ist.

Wenn die **glEndList-Funktion** gefunden wird, wird die Definition der Anzeigeliste abgeschlossen, indem die Liste der Liste mit dem eindeutigen Namen *(angegeben* im [**Befehl glNewList) hinzugefügt**](glnewlist.md) wird. Wenn bereits eine Anzeigeliste mit *einer* Namensliste vorhanden ist, wird sie nur ersetzt, wenn **glEndList** aufgerufen wird.

Die [**Funktionen glCallList**](glcalllist.md) [**und glCallLists**](glcalllists.md) können in Anzeigelisten eingegeben werden. Die Befehle in der Anzeigeliste oder den Listen, die von **glCallList** oder **glCallLists** ausgeführt werden, sind nicht in der zu erstellenden Anzeigeliste enthalten, auch wenn der Listenerstellungsmodus GL \_ COMPILE AND EXECUTE \_ \_ ist.

Die folgende Funktion ruft Informationen im Zusammenhang mit [**glNewList ab:**](glnewlist.md)

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MATRIX \_ MODE

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





