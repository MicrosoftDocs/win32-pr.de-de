---
title: glEnableClientState-Funktion (Gl.h)
description: Die Funktionen glEnableClientState und glDisableClientState aktivieren bzw. deaktivieren Arrays. | glEnableClientState-Funktion (Gl.h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- glEnableClientState-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1ebb9b0278ca6a696183da54c40a6463880a24f6a29a7cca3c2fdd9dd1213a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360417"
---
# <a name="glenableclientstate-function"></a>glEnableClientState-Funktion

Die Funktionen **glEnableClientState** und [**glDisableClientState**](gldisableclientstate.md) aktivieren bzw. deaktivieren Arrays.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*array* 
</dt> <dd>

Eine symbolische Konstante für das Array, das Sie aktivieren oder deaktivieren möchten. Für diesen Parameter kann einer der folgenden Werte angenommen werden.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ COLOR \_ ARRAY**</dt> </dl>                          | Wenn diese Option aktiviert ist, verwenden Sie Farbarrays mit Aufrufen von [**glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays.**](gldrawarrays.md)<br/> Siehe auch [**glColorPointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**GL \_ EDGE \_ FLAG \_ ARRAY**</dt> </dl>             | Wenn aktiviert, verwenden Sie Edgeflagarrays mit Aufrufen von [**glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays**](gldrawarrays.md).<br/> Siehe auch [**glEdgeFlagPointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ INDEX \_ ARRAY**</dt> </dl>                          | Wenn aktiviert, verwenden Sie Indexarrays mit Aufrufen von [**glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays.**](gldrawarrays.md)<br/> Siehe auch [**glIndexPointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL \_ NORMAL \_ ARRAY**</dt> </dl>                       | Wenn diese Option aktiviert ist, verwenden Sie normale Arrays mit Aufrufen von [**glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays.**](gldrawarrays.md)<br/> Siehe auch [**glNormalPointer.**](glnormalpointer.md)<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL \_ TEXTURE \_ COORD \_ ARRAY**</dt> </dl> | Wenn diese Option aktiviert ist, verwenden Sie Texturkoordinatenarrays mit Aufrufen von [**glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays.**](gldrawarrays.md)<br/> Siehe auch [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL \_ VERTEX \_ ARRAY**</dt> </dl>                       | Wenn diese Option aktiviert ist, verwenden Sie Scheitelpunktarrays mit Aufrufen von [**glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays.**](gldrawarrays.md)<br/> Siehe auch [**glVertexPointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                             | Bedeutung                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl> | *Array* war kein akzeptierter Wert.<br/> |



## <a name="remarks"></a>Hinweise

Die Funktionen **glEnableClientState** und **glDisableClientState** aktivieren und deaktivieren verschiedene einzelne Arrays. Verwenden Sie [**glIsEnabled**](glisenabled.md) oder [**glGet,**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) um die aktuelle Einstellung jeder Funktion zu bestimmen.

Das Aufrufen **von glEnableClientState** und **glDisableClientState** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md) kann einen Fehler verursachen. Wenn kein Fehler generiert wird, ist das Verhalten nicht definiert.

> [!Note]  
> Die Funktionen **glEnableClientState** und **glDisableClientState** sind nur in OpenGL Version 1.1 oder höher verfügbar.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





