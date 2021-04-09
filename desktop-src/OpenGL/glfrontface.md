---
title: glfrontface-Funktion (GL. h)
description: Die Funktion "glfrontface" definiert Front-und rückwärts gerichtete Polygone.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glfrontface-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957159"
---
# <a name="glfrontface-function"></a>glfrontface-Funktion

Die Funktion " **glfrontface** " definiert Front-und rückwärts gerichtete Polygone.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die Ausrichtung von nach vorne gerichteten Polygonen. GL \_ CW und GL \_ CCW werden akzeptiert. Der Standardwert ist GL \_ CCW.

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

In einer Szene, die vollständig aus nicht transparenten geschlossenen Oberflächen besteht, werden die rückwärts gerichteten Polygone nie sichtbar. Die Beseitigung dieser unsichtbaren Polygone hat den offensichtlichen Vorteil, dass das Rendering des Bilds beschleunigt wird. Sie aktivieren und deaktivieren die Beseitigung von mit der Rückseite verknüpfte Polygone mit [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) mithilfe des "Argument GL \_ cull \_ Face".

Die Projektion einer Polygon-zu-Fenster-Koordinate wird als "im Uhrzeigersinn" bezeichnet, wenn ein imaginäres Objekt, das auf den Pfad vom ersten Scheitelpunkt, seinen zweiten Scheitelpunkt usw., bis zum letzten Scheitelpunkt folgt, und schließlich zurück zum ersten Scheitelpunkt in einer Richtung im Uhrzeigersinn zum Inneren des Polygons bewegt wird. Das Vieleck des Polygons wird gegen den Uhrzeigersinn gesetzt, wenn das imaginäre Objekt, das denselben Pfad folgt, gegen den Uhrzeigersinn zum Inneren des Polygons bewegt wird. Die **glfrontface** -Funktion gibt an, ob Polygone mit dem Uhrzeigersinn im Uhrzeigersinn in Fenster Koordinaten oder gegen den Uhrzeigersinn im Uhrzeigersinn in Fenster Koordinaten übernommen werden. Durch \_ die Übergabe von GL CCW an *Mode* werden Polygone gegen den Uhrzeigersinn als Front-on ausgewählt; GL \_ CW wählt Polygone im Uhrzeigersinn als Front-on aus. Standardmäßig werden Polygone gegen den Uhrzeigersinn als Front-on verwendet.

Mit der folgenden Funktion werden Informationen zu **glfrontface** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Front- \_ Face

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

[**glcullface**](glcullface.md)
</dt> <dt>

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gllightmodel**](gllightmodel-functions.md)
</dt> </dl>

 

 





