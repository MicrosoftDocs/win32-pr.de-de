---
title: glTexCoordPointer-Funktion (Gl.h)
description: Die glTexCoordPointer-Funktion definiert ein Array von Texturkoordinaten.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0892f06b3fd5027939710be9ac74a2ae18c0dc0d712572d094b9a54fd6bb5b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888250"
---
# <a name="gltexcoordpointer-function"></a>glTexCoordPointer-Funktion

Die **glTexCoordPointer-Funktion** definiert ein Array von Texturkoordinaten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*size* 
</dt> <dd>

Die Anzahl der Koordinaten pro Arrayelement. Der Wert der *Größe* muss 1, 2, 3 oder 4 sein.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp jeder Texturkoordinate im Array unter Verwendung der folgenden symbolischen Konstanten: **GL \_ SHORT,** **GL \_ INT,** **GL \_ FLOAT** und **GL \_ DOUBLE**.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byteoffset zwischen aufeinander folgenden Arrayelementen. Wenn *stride* 0 (null) ist, sind die Arrayelemente eng im Array gepackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf die erste Koordinate des ersten Elements im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                              | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | *type* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | *Die Größe* war nicht 1, 2, 3 oder 4.<br/>     |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | *stride* war negativ.<br/>            |



## <a name="remarks"></a>Hinweise

Die **glTexCoordPointer-Funktion** gibt die Position und die Daten eines Arrays von Texturkoordinaten an, die beim Rendern verwendet werden sollen. Der *size-Parameter* gibt die Anzahl der Koordinaten an, die für jedes Element des Arrays verwendet werden. Der *Typparameter* gibt den Datentyp jeder Texturkoordinate an. Der *stride-Parameter* bestimmt den Byteoffset von einem Arrayelement zum nächsten und ermöglicht das Packen von Scheitelpunkten und Attributen in einem einzelnen Array oder Speicher in separaten Arrays. In einigen Implementierungen kann das Speichern der Scheitelpunkte und Attribute in einem einzelnen Array effizienter sein als die Verwendung separater Arrays. Weitere Informationen finden Sie unter [**glInterleavedArrays.**](glinterleavedarrays.md) Wenn ein Texturkoordinatenarray angegeben wird, werden Größe, Typ, Schritt und Zeiger clientseitig gespeichert.

Ein Texturkoordinatenarray wird aktiviert, wenn Sie die **GL \_ TEXTURE \_ COORD \_ ARRAY-Konstante** mit [**glEnableClientState**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwenden [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md)und [**glArrayElement**](glarrayelement.md) das Texturkoordinatenarray. Standardmäßig ist das Texturkoordinatenarray deaktiviert.

Sie können **glTexCoordPointer** nicht in Anzeigelisten einschließen.

Wenn Sie mit **glTexCoordPointer** ein Texturkoordinatenarray angeben, werden die Werte aller Texturkoordinatenarrayparameter der Funktion in einem clientseitigen Zustand gespeichert, und statische Arrayelemente können zwischengespeichert werden. Da die Parameter des Texturkoordinatenarrays clientseitig sind, werden ihre Werte nicht von [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib**](glpopattrib.md)gespeichert oder wiederhergestellt.

Obwohl beim Aufrufen von **glTexCoordPointer** in [**glBegin-**](glbegin.md) und [**glEnd-Paaren**](glend.md) kein Fehler generiert wird, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glTexCoordPointer** ab:

[**glIsEnabled**](glisenabled.md) mit argument **GL \_ TEXTURE \_ COORD \_ ARRAY**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument **GL \_ TEXTURE \_ COORD ARRAY \_ \_ SIZE**

**glGet** mit argument **GL \_ TEXTURE \_ COORD ARRAY \_ \_ STRIDE**

**glGet** mit argument **GL \_ TEXTURE \_ COORD ARRAY \_ \_ COUNT**

**glGet** mit argument **GL \_ TEXTURE \_ COORD ARRAY \_ \_ TYPE**

[**glGetPointerv**](glgetpointerv.md) mit argument **GL \_ TEXTURE \_ COORD ARRAY \_ \_ POINTER**

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopClientAttrib**](glpopclientattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





