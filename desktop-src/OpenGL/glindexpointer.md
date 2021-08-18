---
title: glIndexPointer-Funktion (Gl.h)
description: Die glIndexPointer-Funktion definiert ein Array von Farbindizes.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27502420121f7373af5425e8aadffe3641ddec539a4521fe6c6bf55e6d807d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012148"
---
# <a name="glindexpointer-function"></a>glIndexPointer-Funktion

Die **glIndexPointer-Funktion** definiert ein Array von Farbindizes.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* 
</dt> <dd>

Der Datentyp jedes Farbindexes im Array mit den folgenden symbolischen Konstanten: GL \_ SHORT, GL \_ INT, GL \_ FLOAT, GL \_ DOUBLE.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byteoffset zwischen aufeinander folgenden Farbindizes. Wenn *stride* 0 (null) ist, werden die Farbindizes eng in das Array gepackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf den ersten Farbindex im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                              | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | *type* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | *stride* oder *count* war negativ.<br/> |



## <a name="remarks"></a>Hinweise

Die **glIndexPointer-Funktion** gibt den Speicherort und die Daten eines Arrays von Farbindizes an, die beim Rendering verwendet werden. Der *Typparameter* gibt den Datentyp jedes Farbindexes an, und *stride* bestimmt den Byteoffset von einem Farbindex zum nächsten, wodurch das Packen von Scheiteltices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays ermöglicht wird. In einigen Implementierungen kann das Speichern der Scheitelungen und Attribute in einem einzelnen Array effizienter sein als die Verwendung separater Arrays. Weitere Informationen finden Sie unter [**glInterleavedArrays**](glinterleavedarrays.md).

Ein Farbindexarray wird aktiviert, wenn Sie die GL \_ INDEX \_ ARRAY-Konstante mit [**glEnableClientState angeben.**](glenableclientstate.md) Wenn diese Option aktiviert ist, verwenden [**glDrawArrays**](gldrawarrays.md) und [**glArrayElement**](glarrayelement.md) das Array color-index. Standardmäßig ist das Farbindexarray deaktiviert.

**GlIndexPointer kann nicht** in Anzeigelisten enthalten sein.

Wenn Sie ein Farbindexarray mit **glIndexPointer** angeben, werden die Werte aller Parameter des Farbindexarrays der Funktion in einem clientseitigen Zustand gespeichert, und statische Arrayelemente können zwischengespeichert werden. Da die Arrayparameter für den Farbindex clientseitig sind, werden ihre Werte nicht durch [**glPushAttrib**](glpushattrib.md) und **glPopAttrib gespeichert oder wiederhergestellt.**

Obwohl beim Aufrufen von **glIndexPointer** in [**glBegin-**](glbegin.md) und **glEnd-Paaren** kein Fehler generiert wird, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glIndexPointer ab:**

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ INDEX \_ ARRAY

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ INDEX \_ ARRAY \_ STRIDE

**glGet** mit Argument GL \_ INDEX \_ ARRAY \_ COUNT

**glGet** mit Argument GL \_ INDEX \_ ARRAY \_ TYPE

**glGet** mit Argument GL \_ INDEX \_ ARRAY \_ SIZE

[**glGetPointerv mit**](glgetpointerv.md) Argument GL \_ INDEX ARRAY \_ \_ POINTER

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





