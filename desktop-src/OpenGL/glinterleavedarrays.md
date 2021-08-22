---
title: glInterleavedArrays-Funktion (Gl.h)
description: Die glInterleavedArrays-Funktion gibt gleichzeitig mehrere verschachtelte Arrays in einem größeren Aggregatarray an und aktiviert sie.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays-Funktion OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3b37186614fa431585c1e5a932edab946afd6d881ba1cf8eb5c5690220f603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938561"
---
# <a name="glinterleavedarrays-function"></a>glInterleavedArrays-Funktion

Die **glInterleavedArrays-Funktion** gibt gleichzeitig mehrere verschachtelte Arrays in einem größeren Aggregatarray an und aktiviert sie.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*format* 
</dt> <dd>

Der Typ des zu aktivierende Arrays. Der Parameter kann einen der folgenden symbolischen Werte annehmen: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F \_ N3F \_ V3F, GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ C3F \_ V3F, GL \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ N3F \_ V3F oder GL \_ T4F \_ C4F \_ N3F \_ V4F.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Offset in Bytes zwischen jedem Aggregatarrayelement.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf das erste Element eines Aggregatarrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *stride* war ein negativer Wert.<br/>                                                                                             |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Mit der **glInterleavedArrays-Funktion** können Sie gleichzeitig mehrere verschachtelte Farb-, Normal-, Textur- und Scheitelpunktarrays angeben und aktivieren, deren Elemente Teil eines größeren Aggregatarrayelements sind. Bei einigen Speicherarchitekturen ist dies effizienter als die separate Angabe der Arrays.

Wenn der *stride-Parameter* 0 (null) ist, werden die Aggregatarrayelemente nacheinander gespeichert. andernfalls *treten Aggregatarrayelemente* in Bytes auf.

Der *format-Parameter* dient als Schlüssel, der beschreibt, wie einzelne Arrays aus dem Aggregatarray extrahiert werden:

-   Wenn *das Format* ein T enthält, werden Texturkoordinaten aus dem verschachtelten Array extrahiert.
-   Wenn C vorhanden ist, werden Farbwerte extrahiert.
-   Wenn N vorhanden ist, werden normale Koordinaten extrahiert.
-   Scheitelpunktkoordinaten werden immer extrahiert.
-   Die Ziffern 2, 3 und 4 kennzeichnen, wie viele Werte extrahiert werden.
-   F gibt an, dass Werte als Gleitkommawerte extrahiert werden.
-   Wenn 4UB dem C folgt, können Farben auch als 4 Bytes ohne Vorzeichen extrahiert werden. Wenn eine Farbe als 4 Bytes ohne Vorzeichen extrahiert wird, befindet sich das vertex-Arrayelement, das folgt, an der ersten möglichen an Gleitkomma ausgerichteten Adresse.

Wenn Sie beim Kompilieren einer Anzeigeliste **glInterleavedArrays** aufrufen, wird sie nicht in die Liste kompiliert, sondern sofort ausgeführt.

Sie können keine Aufrufe von **glInterleavedArrays** in **glDisableClientState** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von **glEnd** einschließen.

> [!Note]  
> Die **glInterleavedArrays-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die **glInterleavedArrays-Funktion** wird auf clientseitiger Seite ohne Protokoll implementiert. Da die Vertexarrayparameter clientseitig sind, werden sie nicht von [**glPushAttrib**](glpushattrib.md) und **glPopAttrib** gespeichert oder wiederhergestellt. Verwenden Sie stattdessen [**glPushClientAttrib**](glpushclientattrib.md) und **glPopClientAttrib.**

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

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





