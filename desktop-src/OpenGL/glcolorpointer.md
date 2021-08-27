---
title: glColorPointer-Funktion (Gl.h)
description: Die glColorPointer-Funktion definiert ein Array von Farben.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e08f046cc1bd41293a076f36389506320e85025e415b264bed1ed0de14f9a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081710"
---
# <a name="glcolorpointer-function"></a>glColorPointer-Funktion

Die **glColorPointer-Funktion** definiert ein Array von Farben.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorPointer(
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

Die Anzahl der Komponenten pro Farbe. Der Wert muss entweder 3 oder 4 sein.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp jeder Farbkomponente in einem Farbarray. Zulässige Datentypen werden mit den folgenden Konstanten angegeben: GL \_ BYTE, GL \_ UNSIGNED \_ BYTE, GL \_ SHORT, GL \_ UNSIGNED \_ SHORT, GL \_ INT, GL \_ UNSIGNED \_ INT, GL \_ FLOAT oder GL \_ DOUBLE.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byteoffset zwischen aufeinanderfolgenden Farben. Wenn *stride* 0 (null) ist, werden die Farben eng in das Array gepackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf die erste Komponente des ersten Farbelements in einem Farbarray.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                              | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | *size* war nicht 3 oder 4.<br/>            |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | *type* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | *stride* oder *count* war negativ.<br/> |



## <a name="remarks"></a>Hinweise

Die **glColorPointer-Funktion** gibt den Speicherort und das Datenformat eines Arrays von Farbkomponenten an, die beim Rendern verwendet werden. Der *stride-Parameter* bestimmt den Byteoffset von einer Farbe zur nächsten, wodurch das Packen von Vertexattributen in einem einzelnen Array oder Speicher in separaten Arrays ermöglicht wird. In einigen Implementierungen kann das Speichern von Scheitelpunktattributen in einem einzelnen Array effizienter sein als die Verwendung separater Arrays.

Das Farbarray wurde aktiviert, indem die GL \_ COLOR \_ ARRAY-Konstante mit [**glEnableClientState angegeben wird.**](glenableclientstate.md) Beim [**Aufrufen von glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)oder [**glDrawArrays**](gldrawarrays.md) wird das Farbarray verwendet, das aktiviert ist. Standardmäßig ist das Farbarray deaktiviert. Die **glColorPointer-Aufrufe** können nicht durch Eingabe in Anzeigelisten ausgeführt werden.

Wenn Sie ein Farbarray mit **glColorPointer** angeben, werden die Werte aller Farbarrayparameter der Funktion in einem clientseitigen Zustand gespeichert, und Sie können statische Arrayelemente zwischenspeichern. Da sich die Farbarrayparameter in einem clientseitigen Zustand befinden, speichern oder wiederherstellen [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib**](glpopattrib.md) die Werte der Parameter nicht.

Obwohl die Angabe des Farbarrays innerhalb [**von glBegin-Paaren**](glbegin.md) und [**-Paaren**](glend.md) keinen Fehler generiert, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glColorPointer-Funktion** ab:

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ COLOR \_ ARRAY

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ COLOR \_ ARRAY \_ SIZE

**glGet** mit argument GL \_ COLOR \_ ARRAY \_ TYPE

**glGet mit** Argument GL \_ COLOR ARRAY \_ \_ STRIDE

**glGet** mit Argument GL \_ COLOR \_ ARRAY \_ COUNT

[**glGetPointerv mit**](glgetpointerv.md) Argument GL \_ COLOR ARRAY \_ \_ POINTER

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





