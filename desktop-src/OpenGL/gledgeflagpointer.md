---
title: glEdgeFlagPointer-Funktion (Gl.h)
description: Die glEdgeFlagPointer-Funktion definiert ein Array von Edgeflags.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa648a15542a3f3f2f35f577760991da74bc978c0464c1373c8eddea38941a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061638"
---
# <a name="gledgeflagpointer-function"></a>glEdgeFlagPointer-Funktion

Die **glEdgeFlagPointer-Funktion** definiert ein Array von Edgeflags.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schritt* 
</dt> <dd>

Der Byteoffset zwischen aufeinander folgenden Edgeflags. Wenn *stride* 0 (null) ist, werden die Edgeflags eng in das Array gepackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf das erste Edgeflag im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                             | Bedeutung                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl> | *stride* oder *count* war negativ.<br/> |



## <a name="remarks"></a>Hinweise

Die **glEdgeFlagPointer-Funktion** gibt den Speicherort und die Daten eines Arrays von booleschen Edgeflags an, die beim Rendering verwendet werden. Der *stride-Parameter* bestimmt den Byteoffset von einem Edgeflag zum nächsten, wodurch das Packen von Scheitelzeichen und Attributen in einem einzelnen Array oder Speicher in separaten Arrays ermöglicht wird. In einigen Implementierungen kann das Speichern der Scheitelungen und Attribute in einem einzelnen Array effizienter sein als die Verwendung separater Arrays.

Ein Edgeflagarray wird aktiviert, wenn Sie die GL \_ EDGE FLAG ARRAY-Konstante mit \_ \_ [**glEnableClientState angeben.**](glenableclientstate.md) Bei Aktivierung verwendet [**glDrawArrays**](gldrawarrays.md) oder [**glArrayElement**](glarrayelement.md) das Edgeflagarray. Standardmäßig ist das Edgeflagarray deaktiviert.

Verwenden **Sie glDrawArrays,** um eine Sequenz von Primitiven (alle desselben Typs) aus vorab angegebenen Vertex- und Vertexattributarrays zu erstellen. Verwenden **Sie glArrayElement,** um Primitive anzugeben, indem Sie Scheitelpunkte und Scheitelpunktattribute indizieren, und [**glDrawElements,**](gldrawelements.md) um eine Sequenz von Primitiven zu erstellen, indem Scheitelpunkte und Scheitelpunktattribute indiziert werden.

**GlEdgeFlagPointer kann nicht in Anzeigelisten** enthalten sein.

Wenn Sie ein Edgeflagarray mit **glEdgeFlagPointer** angeben, werden die Werte aller Edgeflag-Arrayparameter der Funktion in einem clientseitigen Zustand gespeichert, und statische Arrayelemente können zwischengespeichert werden. Da sich die Arrayparameter des Edgeflags in einem clientseitigen Zustand befinden, speichern und wiederherstellen [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib**](glpopattrib.md) ihre Werte nicht.

Obwohl der **Aufruf von glEdgeFlagPointer** in einem [**glBegin-gekoppelten**](glbegin.md)Paar keinen Fehler generiert, sind die Ergebnisse / [](glend.md) nicht definiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEdgeFlagPointer-Funktion** ab:

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ EDGE FLAG ARRAY \_ \_ \_ STRIDE

**glGet mit** argument GL \_ EDGE FLAG ARRAY \_ \_ \_ COUNT

[**glGetPointerv mit**](glgetpointerv.md) Argument GL \_ EDGE FLAG ARRAY \_ \_ \_ POINTER

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ EDGE FLAG \_ \_ ARRAY

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





