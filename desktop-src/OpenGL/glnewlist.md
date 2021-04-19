---
title: glnewlist-Funktion (GL. h)
description: Die Funktionen "glnewlist" und "glendlist" erstellen oder ersetzen eine Anzeigeliste. | glnewlist-Funktion (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glnewlist-Funktion OpenGL
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
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366600"
---
# <a name="glnewlist-function"></a>glnewlist-Funktion

Die Funktionen " **glnewlist** " und " [**glendlist**](glendlist.md) " erstellen oder ersetzen eine Anzeigeliste.

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

Der Name der Anzeigeliste.

</dd> <dt>

*mode* 
</dt> <dd>

Der Kompilierungs Modus. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                      | Bedeutung                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**GL- \_ Kompilierung**</dt> </dl>                                       | Befehle werden lediglich kompiliert.<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**GL \_ -Kompilierung \_ und- \_ Ausführung**</dt> </dl> | Befehle werden ausgeführt, wenn Sie in die Anzeigeliste kompiliert werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Liste* war NULL.<br/>                                                                                                           |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Anzeigelisten sind Gruppen von OpenGL-Befehlen, die für die nachfolgende Ausführung gespeichert wurden. Die Anzeigelisten werden mit " **glnewlist**" erstellt. Alle nachfolgenden Befehle werden in der Anzeigeliste in der ausgestellten Reihenfolge abgelegt, bis **glendlist** aufgerufen wird.

Die **glnewlist** -Funktion verfügt über zwei Parameter. Der erste Parameter *List* ist eine positive ganze Zahl, die zum eindeutigen Namen für die Anzeigeliste wird. Namen können mit " [**glgenlists**](glgenlists.md) " erstellt und reserviert und auf Eindeutigkeit mit " [**glislist**](glislist.md)" getestet werden. Der zweite Parameter, der- *Modus*, ist eine symbolische Konstante, die einen der beiden vorangehenden Werte annehmen kann.

Bestimmte Befehle werden nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt, unabhängig vom Anzeigelisten Modus. Diese Befehle sind " [**glcolorpointer**](glcolorpointer.md)", " [**gldelta etelists**](gldeletelists.md)", " [**gldisableclientstate**](gldisableclientstate.md)", " [**gledgeflagpointer**](gledgeflagpointer.md)", " [**glenableclientstate**](glenableclientstate.md)", " [**glfeedbackbuffer**](glfeedbackbuffer.md) [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", " [**glfinish**](glfinish.md)" [**, "**](glgenlists.md) [**glflush**](glflush.md)" " [**glindexpointer**](glindexpointer.md)", " [**glinterleavedarrays**](glinterleavedarrays.md)", " [**glisenabled**](glisenabled.md)", " [**glislist**](glislist.md)", " [**glnormalpointer**](glnormalpointer.md)", " [**glpopclientatlab**](glpopclientattrib.md)", " [**glpixelstore**](glpixelstore-functions.md)", " [**glpushclientatpub**](glpushclientattrib.md)", " [**gllesepixels**](glreadpixels.md)", " [**glrendermode**](glrendermode.md)", " [**glselectbuffer**](glselectbuffer.md) [**",**](glvertexpointer.md) [**"GL**](gltexcoordpointer.md)

Ebenso werden [**glTexImage2D**](glteximage2d.md) und [**glTexImage1D**](glteximage1d.md) sofort ausgeführt und nicht in die Anzeigeliste kompiliert, wenn Ihr erstes Argument die GL \_ \_ -Proxy Textur \_ 2D bzw. die GL \_ -Proxy \_ Textur \_ 1D ist.

Wenn die Funktion " **glendlist** " gefunden wird, wird die Definition der Anzeigeliste abgeschlossen, indem die Liste mit der eindeutigen namens *Liste* verknüpft wird (angegeben im Befehl " **glnewlist** "). Wenn eine Anzeigeliste mit der namens *Liste* bereits vorhanden ist, wird Sie nur ersetzt, wenn " **glendlist** " aufgerufen wird.

Die Funktionen " [**glCallList**](glcalllist.md) " und " [**glcalllists**](glcalllists.md) " können in Anzeigelisten eingegeben werden. Die Befehle in der Anzeigeliste oder Listen, die von **glCallList** oder **glcalllists** ausgeführt werden, sind nicht in der erstellten Anzeigeliste enthalten, auch wenn der Listen Erstellungs Modus "GL Compile" und "Execute" lautet \_ \_ \_ .

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glnewlist** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glcalllists**](glcalllists.md)
</dt> <dt>

[**gldelta etelists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glendlist**](glendlist.md)
</dt> <dt>

[**glgenlists**](glgenlists.md)
</dt> <dt>

[**glislist**](glislist.md)
</dt> </dl>

 

 





