---
title: glendlist-Funktion (GL. h)
description: Die Funktionen "glnewlist" und "glendlist" erstellen oder ersetzen eine Anzeigeliste. | glendlist-Funktion (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glendlist-Funktion OpenGL
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
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363094"
---
# <a name="glendlist-function"></a>glendlist-Funktion

Die Funktionen " [**glnewlist**](glnewlist.md) " und " **glendlist** " erstellen oder ersetzen eine Anzeigeliste.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | " **glendlist** " wurde ohne vorherige " **glnewlist**" aufgerufen, oder, wenn " **glnewlist** " aufgerufen wurde, während eine Anzeigeliste definiert wurde.<br/> |



## <a name="remarks"></a>Bemerkungen

Anzeigelisten sind Gruppen von OpenGL-Befehlen, die für die nachfolgende Ausführung gespeichert wurden. Die Anzeigelisten werden mit " [**glnewlist**](glnewlist.md)" erstellt. Alle nachfolgenden Befehle werden in der Anzeigeliste in der ausgestellten Reihenfolge abgelegt, bis **glendlist** aufgerufen wird.

Die [**glnewlist**](glnewlist.md) -Funktion verfügt über zwei Parameter. Der erste Parameter *List* ist eine positive ganze Zahl, die zum eindeutigen Namen für die Anzeigeliste wird. Namen können mit " [**glgenlists**](glgenlists.md) " erstellt und reserviert und auf Eindeutigkeit mit " [**glislist**](glislist.md)" getestet werden. Der zweite Parameter, der- *Modus*, ist eine symbolische Konstante, die einen der beiden vorangehenden Werte annehmen kann.

Bestimmte Befehle werden nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt, unabhängig vom Anzeigelisten Modus. Diese Befehle sind " [**glcolorpointer**](glcolorpointer.md)", " [**gldelta etelists**](gldeletelists.md)", " [**gldisableclientstate**](gldisableclientstate.md)", " [**gledgeflagpointer**](gledgeflagpointer.md)", " [**glenableclientstate**](glenableclientstate.md)", " [**glfeedbackbuffer**](glfeedbackbuffer.md) [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", " [**glfinish**](glfinish.md)" [**, "**](glgenlists.md) [**glflush**](glflush.md)" " [**glindexpointer**](glindexpointer.md)", " [**glinterleavedarrays**](glinterleavedarrays.md)", " [**glisenabled**](glisenabled.md)", " [**glislist**](glislist.md)", " [**glnormalpointer**](glnormalpointer.md)", " [**glpopclientatlab**](glpopclientattrib.md)", " [**glpixelstore**](glpixelstore-functions.md)", " [**glpushclientatpub**](glpushclientattrib.md)", " [**gllesepixels**](glreadpixels.md)", " [**glrendermode**](glrendermode.md)", " [**glselectbuffer**](glselectbuffer.md) [**",**](glvertexpointer.md) [**"GL**](gltexcoordpointer.md)

Ebenso werden [**glTexImage2D**](glteximage2d.md) und [**glTexImage1D**](glteximage1d.md) sofort ausgeführt und nicht in die Anzeigeliste kompiliert, wenn Ihr erstes Argument die GL \_ \_ -Proxy Textur \_ 2D bzw. die GL \_ -Proxy \_ Textur \_ 1D ist.

Wenn die Funktion " **glendlist** " gefunden wird, wird die Definition der Anzeigeliste abgeschlossen, indem die Liste mit der eindeutigen namens *Liste* verknüpft wird (angegeben im Befehl " [**glnewlist**](glnewlist.md) "). Wenn eine Anzeigeliste mit der namens *Liste* bereits vorhanden ist, wird Sie nur ersetzt, wenn " **glendlist** " aufgerufen wird.

Die Funktionen " [**glCallList**](glcalllist.md) " und " [**glcalllists**](glcalllists.md) " können in Anzeigelisten eingegeben werden. Die Befehle in der Anzeigeliste oder Listen, die von **glCallList** oder **glcalllists** ausgeführt werden, sind nicht in der erstellten Anzeigeliste enthalten, auch wenn der Listen Erstellungs Modus "GL Compile" und "Execute" lautet \_ \_ \_ .

Die folgende Funktion Ruft Informationen im Zusammenhang mit [**glnewlist**](glnewlist.md)ab:

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

[**glgenlists**](glgenlists.md)
</dt> <dt>

[**glislist**](glislist.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> </dl>

 

 





