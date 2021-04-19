---
title: gldisableclientstate-Funktion (GL. h)
description: Die Funktionen "glenableclientstate" und "gldisableclientstate" aktivieren bzw. deaktivieren Arrays. | gldisableclientstate-Funktion (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- gldisableclientstate-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350639"
---
# <a name="gldisableclientstate-function"></a>gldisableclientstate-Funktion

Die Funktionen " [**glenableclientstate**](glenableclientstate.md) " und " **gldisableclientstate** " aktivieren bzw. deaktivieren Arrays.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*array* 
</dt> <dd>

Eine symbolische Konstante für das Array, das Sie aktivieren oder deaktivieren möchten. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ - \_ Farbarray**</dt> </dl>                          | Wenn diese Option aktiviert ist, verwenden Sie Farb Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).<br/> Siehe auch [**glcolorpointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**GL \_ - \_ edgeflag- \_ Array**</dt> </dl>             | Wenn diese Option aktiviert ist, verwenden Sie Edge-Flag-Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).<br/> Siehe auch [**gledgeflagpointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL- \_ Index \_ Array**</dt> </dl>                          | Wenn diese Option aktiviert ist, verwenden Sie Index Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".<br/> Siehe auch [**glindexpointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL- \_ normales \_ Array**</dt> </dl>                       | Wenn diese Option aktiviert ist, verwenden Sie normale Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".<br/> Siehe auch [**glnormalpointer**](glnormalpointer.md).<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL- \_ Textur \_ Koord- \_ Array**</dt> </dl> | Wenn diese Option aktiviert ist, verwenden Sie Texturkoordinaten Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".<br/> Siehe auch [**gltexcoordpointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL- \_ Scheitelpunkt \_ Array**</dt> </dl>                       | Wenn diese Option aktiviert ist, verwenden Sie Scheitelpunkt Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).<br/> Siehe auch [**glvertexpointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                             | Bedeutung                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl> | Das *Array* war kein akzeptierter Wert.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktionen " [**glenableclientstate**](glenableclientstate.md) " und " **gldisableclientstate** " aktivieren und deaktivieren verschiedene individuelle Arrays. Verwenden Sie " [**glisenabled**](glisenabled.md) " oder " [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", um die aktuelle Einstellung einer beliebigen Funktion zu bestimmen.

Das Aufrufen von [**glenableclientstate**](glenableclientstate.md) und **gldisableclientstate** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md) kann zu einem Fehler führen. Wenn kein Fehler generiert wird, ist das Verhalten nicht definiert.

> [!Note]  
> Die Funktionen " [**glenableclientstate**](glenableclientstate.md) " und " **gldisableclientstate** " sind nur in der OpenGL-Version 1,1 oder höher verfügbar.

 

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

[**glarrayelement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glinterleavedarrays**](glinterleavedarrays.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





