---
title: glGetTexGenfv-Funktion (Gl.h)
description: Die Funktionen glGetTexGendv, glGetTexGenfv und glGetTexGeniv geben Texturkoordinatengenerierungsparameter zurück. | glGetTexGenfv-Funktion (Gl.h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- glGetTexGenfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40e916f98270c163ed8f299a8466ae66fc2775e466efaeb76a36b0953056eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493790"
---
# <a name="glgettexgenfv-function"></a>glGetTexGenfv-Funktion

Die [**Funktionen glGetTexGendv,**](glgettexgendv.md) **glGetTexGenfv** und [**glGetTexGeniv**](glgettexgeniv.md) geben Parameter für die Texturkoordinatengenerierung zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Coord* 
</dt> <dd>

Eine Texturkoordinate. Muss GL \_ S, GL \_ T, GL \_ R oder GL \_ Q sein.

</dd> <dt>

*pname* 
</dt> <dd>

Der symbolische Name der werte, die zurückgegeben werden sollen. Muss entweder GL TEXTURE GEN MODE oder der Name einer der Gleichungen der Texturgenerierungsebene \_ \_ \_ sein: GL \_ OBJECT PLANE oder GL EYE \_ \_ \_ PLANE. Diese Werte lauten wie folgt.



| Wert                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ MODE**</dt> </dl> | Der *Parameter params* gibt die einwertige Texturgenerierungsfunktion zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**\_ \_ GL-OBJEKTEBENE**</dt> </dl>              | Der *Parameter params* gibt die vier Ebenengleichungskoeffizienten zurück, die die Linearkoordinatengenerierung des Objekts angeben. Ganzzahlige Werte werden, wenn sie angefordert werden, direkt aus der internen Gleitkommadarstellung zugeordnet.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**GL \_ EYE \_ PLANE**</dt> </dl>                       | Der *Parameter params* gibt die vier Ebenengleichungskoeffizienten zurück, die die Generierung der linearen Augenkoordinate angeben. Ganzzahlige Werte werden, wenn sie angefordert werden, direkt aus der internen Gleitkommadarstellung zugeordnet. Die zurückgegebenen Werte werden in Augenkoordinaten beibehalten. Sie sind nicht gleich den Werten, die mit [**glTexGen**](gltexgen-functions.md)angegeben wurden, es sei denn, die Modellansichtsmatrix wurde zum Zeitpunkt des **GlTexGen-Namens** identifiziert.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *coord* oder *pname* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetTexGen-Funktion** gibt in *Parametern* ausgewählte Parameter einer Texturkoordinatengenerierungsfunktion zurück, die Sie mit **glTexGen angegeben haben.** Der *koord-Parameter* benennt eine der Texturkoordinaten (*s*, *t*, *r*, *q*) unter Verwendung der symbolischen Konstante GL \_ S, GL T, GL R oder GL \_ \_ \_ Q.

Wenn ein Fehler generiert wird, werden keine Änderungen am Inhalt der *Parameter vorgenommen.*

## <a name="requirements"></a>Anforderungen



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

[**glEnd**](glend.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





