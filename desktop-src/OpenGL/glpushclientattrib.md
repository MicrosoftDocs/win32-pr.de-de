---
title: glpushclientatpub-Funktion (GL. h)
description: Die Funktionen glpushclientattab und glpopclientatpub speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her. | glpushclientatpub-Funktion (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glpushclientatpub-Funktion OpenGL
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
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353779"
---
# <a name="glpushclientattrib-function"></a>glpushclientatpub-Funktion

Die Funktionen **glpushclientattab** und [**glpopclientatpub**](glpopclientattrib.md) speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her.

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

Eine Maske, die angibt, welche Attribute gespeichert werden sollen. Im folgenden finden Sie die symbolischen Masken Konstanten und ihre zugeordneten OpenGL-Client Zustände.



| Wert                                                                                                                                                                                                                                            | Bedeutung                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**GL- \_ Client \_ Pixel \_ Speicher \_ Bit**</dt> </dl>                                             | Pixel Speicher Modus-Attribute.<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**GL- \_ Client- \_ Vertex- \_ array \_ Bit**</dt> </dl>                                          | Vertex-Array Attribute.<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**GL- \_ Client \_ alle \_ attrb- \_ Bits**</dt> </dl> | Alle Stackable Client-State-Attribute.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                               | Bedeutung                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL- \_ Stapel \_ Überlauf**</dt> </dl> | Die Funktion wurde aufgerufen, während der Client Attribut Stapel voll war.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glpushclientatpub** -Funktion verwendet den mask-Parameter, um zu bestimmen, welche Gruppen von Client Zustandsvariablen im Client Attribut Stapel gespeichert werden. Sie können den bitweisen OR-Operator verwenden, um akzeptierte symbolische Konstanten zum Festlegen von Bits und zum Erstellen einer Maske zusammenzufassen.

Die Funktion " [**glpopclientatpub**](glpopclientattrib.md) " stellt die Werte der Client Zustandsvariablen wieder her, die zuletzt mit " **glpushclientatpub**" gespeichert wurden. Nicht zuvor gespeicherte Client Zustandsvariablen bleiben unverändert. Durch das Übertragen von Attributen auf einen vollständigen Client Attribut Stapel oder das Pop von Attributen aus einem leeren Stapel wird ein Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen. Der Client Attribut Stapel ist standardmäßig leer.

Einige OpenGL-Client Zustands Werte können nicht auf dem Client Attribut Stapel gespeichert werden. Beispielsweise können Sie die SELECT-oder Feedback Zustände nicht im Client Attribut Stapel speichern. Die Tiefe des Client Attribut Stapels beträgt mindestens 16.

Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " werden nicht in Anzeigelisten kompiliert, sondern sofort ausgeführt.

Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " können nur die Pixel Speicher Modi per Push und Pop und den Scheitelpunkt Array-Client Status per Push Sie müssen zum überführen von Push-und Pop-Zuständen, die auf dem Server aufbewahrt werden, [**glpushattab**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) verwenden.

> [!Note]  
> Die Funktionen **glpushclientatpub** und **glpopclientatpub** sind nur in OpenGL, Version 1,1 oder höher, verfügbar.

 

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpushclientatpub** und **glpopclientatpub** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Client- \_ attrb- \_ Stapel \_ Tiefe

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max. Client Nachweis \_ \_ \_ \_ Tiefe für Client Nachweis

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

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldisableclientstate**](gldisableclientstate.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgeterror**](glgeterror.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





