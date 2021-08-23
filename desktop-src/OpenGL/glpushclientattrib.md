---
title: glPushClientAttrib-Funktion (Gl.h)
description: Mit den Funktionen glPushClientAttrib und glPopClientAttrib werden Gruppen von Clientzustandsvariablen im Clientattributstapel gespeichert und wiederhergestellt. | glPushClientAttrib-Funktion (Gl.h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glPushClientAttrib-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f378ec3ff735ed916567ea91e211a1d8a1685580b1f1ea80d448b92203b39a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492610"
---
# <a name="glpushclientattrib-function"></a>glPushClientAttrib-Funktion

Mit **den Funktionen glPushClientAttrib** und [**glPopClientAttrib**](glpopclientattrib.md) werden Gruppen von Clientzustandsvariablen im Clientattributstapel gespeichert und wiederhergestellt.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Eine Maske, die angibt, welche Attribute zu speichern sind. Im Folgenden finden Sie die symbolischen Maskenkonstant und die zugehörigen OpenGL-Clientzustände.



| Wert                                                                                                                                                                                                                                            | Bedeutung                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**GL \_ CLIENT \_ PIXEL \_ STORE \_ BIT**</dt> </dl>                                             | Pixelspeichermodusattribute.<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**GL \_ CLIENT \_ VERTEX \_ ARRAY \_ BIT**</dt> </dl>                                          | Vertexarrayattribute.<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**GL \_ CLIENT \_ ALL \_ ATTRIB \_ BITs**</dt> </dl> | alle stapelbaren Clientzustandsattribute.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                               | Bedeutung                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl> | Die Funktion wurde aufgerufen, während der Clientattributstapel voll war.<br/> |



## <a name="remarks"></a>Hinweise

Die **glPushClientAttrib-Funktion** verwendet ihren mask-Parameter, um zu bestimmen, welche Gruppen von Clientzustandsvariablen im Clientattributstapel gespeichert werden. Sie können den bitweise OR-Operator verwenden, um akzeptierte symbolische Konstanten zu verbinden, um Bits zu setzen und eine Maske zu erstellen.

Die [**glPopClientAttrib-Funktion**](glpopclientattrib.md) stellt die Werte der zuletzt mit **glPushclientAttrib** gespeicherten Clientzustandsvariablen wieder auf. Clientzustandsvariablen, die nicht zuvor gespeichert wurden, bleiben unverändert. Durch Das Pushen von Attributen in einen vollständigen Clientattributstapel oder das Ausblenden von Attributen aus einem leeren Stapel wird ein Fehlerflag und keine andere Änderung am OpenGL-Zustand vorgenommen. Standardmäßig ist der Clientattributstapel leer.

Einige OpenGL-Clientzustandswerte können nicht im Clientattributstapel gespeichert werden. Beispielsweise können Sie die Auswahl- oder Feedbackzustände nicht im Clientattributstapel speichern. Die Tiefe des Clientattributstapels beträgt mindestens 16.

Die **Funktionen glPushclientAttrib** und **glPopClientAttrib** werden nicht in Anzeigelisten kompiliert, sondern sofort ausgeführt.

Die **Funktionen glPushClientAttrib** und **glPopClientAttrib** können nur Push- und Poppixelspeichermodi und Scheitelpunktarray-Clientzustände verwenden. Sie müssen [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib**](glpopattrib.md) verwenden, um push- und pop-Zustände zu übertragen, die auf dem Server beibehalten werden.

> [!Note]  
> Die **Funktionen glPushClientAttrib** und **glPopClientAttrib** sind nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die folgenden Funktionen rufen Informationen zu **glPushClientAttrib** und **glPopClientAttrib ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ CLIENT \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MAX \_ CLIENT \_ ATTRIB \_ STACK \_ DEPTH

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





