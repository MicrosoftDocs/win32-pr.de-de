---
title: glcullface-Funktion (GL. h)
description: Mit der Funktion "glcullface" wird angegeben, ob Front-of-und Back-of-factorins gefiltert werden können.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glcullface-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949529"
---
# <a name="glcullface-function"></a>glcullface-Funktion

Mit der Funktion " **glcullface** " wird angegeben, ob Front-of-und Back-of-factorins gefiltert werden können.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Gibt an, ob Vordergrund-oder Hintergrund Facetten als Kandidaten für die Berechnung dienen. Die symbolischen Konstanten GL \_ Front, GL \_ Back und GL \_ Front \_ und \_ Back werden akzeptiert. Der Standardwert ist "GL \_ Back".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glcullface** " gibt an, ob Front-und Hintergrund Facetten (wie im Modus festgelegt) durch ein-und facetentergebnissen (im *Modus* festgelegt) gefiltert werden. Sie aktivieren und deaktivieren die faceterelung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ cull \_ Face. Facetten sind Dreiecke, Vierecke, Polygone und Rechtecke.

Die [**glfrontface**](glfrontface.md) -Funktion gibt an, welcher der Uhrzeigersinn-und gegen Uhrzeigersinn-Facetten Front-und rückwärts-ausgerichtet ist.

Wenn der *Modus* "GL" \_ vor \_ und hinten ist \_ , werden keine Facetten gezeichnet, aber andere primitive, z. b. Punkte und Linien, werden gezeichnet.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glcullface** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ cull \_ Face \_ Mode"

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ cull \_ Face

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

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glfrontface**](glfrontface.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> </dl>

 

 





