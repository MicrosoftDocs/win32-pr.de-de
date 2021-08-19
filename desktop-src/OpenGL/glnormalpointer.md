---
title: glNormalPointer-Funktion (Gl.h)
description: Die glNormalPointer-Funktion definiert ein Array von Normalitäten.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f188a65a0a2bff0438188ae7521615de45341147b138a849d2fd375ed8a959b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938409"
---
# <a name="glnormalpointer-function"></a>glNormalPointer-Funktion

Die **glNormalPointer-Funktion** definiert ein Array von Normalitäten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* 
</dt> <dd>

Der Datentyp jeder Koordinate im Array unter Verwendung der folgenden symbolischen Konstanten: GL \_ BYTE, GL \_ SHORT, GL \_ INT, GL \_ FLOAT und GL \_ DOUBLE.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byteoffset zwischen aufeinander folgenden Normalitäten. Wenn *stride* 0 (null) ist, sind die Normalitäten eng im Array gepackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf die erste Normale im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *stride* oder *count* war negativ.<br/> |



## <a name="remarks"></a>Hinweise

Die **glNormalPointer-Funktion** gibt die Position und die Daten eines Arrays von Normalwerten an, die beim Rendern verwendet werden sollen. Der *Typparameter* gibt den Datentyp jeder normalen Koordinate an. Der *stride-Parameter* bestimmt den Byteoffset von einem normalen zum nächsten, wodurch das Packen von Scheitelpunkten und Attributen in einem einzelnen Array oder Speicher in separaten Arrays ermöglicht wird. In einigen Implementierungen kann das Speichern der Scheitelpunkte und Attribute in einem einzelnen Array effizienter sein als die Verwendung separater Arrays. Weitere Informationen finden Sie unter [**glInterleavedArrays.**](glinterleavedarrays.md)

Ein normales Array wird aktiviert, wenn Sie die GL \_ NORMAL \_ ARRAY-Konstante mit [**glEnableClientState**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwenden [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md) und [**glArrayElement**](glarrayelement.md) das normale Array. Standardmäßig ist das normale Array deaktiviert.

Sie können **glNormalPointer** nicht in Anzeigelisten einschließen.

Wenn Sie mit **glNormalPointer** ein normales Array angeben, werden die Werte aller normalen Arrayparameter der Funktion in einem clientseitigen Zustand gespeichert. Da die normalen Arrayparameter in einem clientseitigen Zustand gespeichert werden, werden ihre Werte nicht von [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib**](glpopattrib.md)gespeichert oder wiederhergestellt.

Obwohl beim Aufrufen von **glNormalPointer** innerhalb der Paare [**glBegin**](glbegin.md) und [**glEnd**](glend.md) kein Fehler generiert wird, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen sind **glNormalPointer** zugeordnet:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ NORMAL \_ ARRAY \_ STRIDE

**glGet** mit dem Argument GL \_ NORMAL \_ ARRAY \_ COUNT

**glGet** mit dem Argument GL \_ NORMAL \_ ARRAY \_ TYPE

**glGetPointerv** mit argument GL \_ NORMAL \_ ARRAY \_ POINTER

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ NORMAL \_ ARRAY

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> </dl>

 

 





