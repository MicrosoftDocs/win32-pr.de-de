---
title: glnormalpointer-Funktion (GL. h)
description: Die glnormalpointer-Funktion definiert ein Array von normalen.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glnormalpointer-Funktion OpenGL
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
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957207"
---
# <a name="glnormalpointer-function"></a>glnormalpointer-Funktion

Die **glnormalpointer** -Funktion definiert ein Array von normalen.

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

Der Datentyp der einzelnen Koordinaten im Array mit den folgenden symbolischen Konstanten: GL \_ Byte, GL \_ Short, GL \_ int, GL \_ float und GL \_ Double.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byte Offset zwischen aufeinander folgenden normalen. Wenn *Stride* 0 (null) ist, werden die normale eng im Array verpackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf den ersten normal im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Typ* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | " *Stride* " oder " *count* " war negativ.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glnormalpointer** -Funktion gibt den Speicherort und die Daten eines Arrays von normalen an, die beim Rendern verwendet werden sollen. Der *Typparameter* gibt den Datentyp der einzelnen normalen Koordinaten an. Der *Stride* -Parameter bestimmt den Byte Offset von einem normalen zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays. In einigen Implementierungen, die die Scheitel Punkte und Attribute in einem einzelnen Array speichern, kann es effizienter sein, als separate Arrays zu verwenden. Weitere Informationen finden Sie unter [**glinterleavedarrays**](glinterleavedarrays.md) .

Ein normales Array wird aktiviert, wenn Sie die reguläre GL- \_ \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwenden [**gldrawarrays**](gldrawarrays.md), [**gldrawelements**](gldrawelements.md) und [**glarrayelement**](glarrayelement.md) das normale Array. Standardmäßig ist das normale Array deaktiviert.

Sie können **glnormalpointer** nicht in Anzeigelisten einschließen.

Wenn Sie ein normales Array mit **glnormalpointer** angeben, werden die Werte aller normalen Array Parameter der Funktion in einem Client seitigen Zustand gespeichert. Da die normalen Array Parameter in einem Client seitigen Zustand gespeichert werden, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md)nicht gespeichert oder wieder hergestellt.

Obwohl beim Abrufen von **glnormalpointer** innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren kein Fehler generiert wird, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen sind mit **glnormalpointer** verknüpft:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ normales \_ array \_ Stride

**glget** mit Argument GL \_ normale \_ array \_ Anzahl

**glget** mit Argument GL \_ normaler \_ \_ Arraytyp

**glgetpointerv** mit Argument GL \_ normaler \_ array \_ Zeiger

[**glisenabled**](glisenabled.md) mit Argument GL \_ Normal \_ Array

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

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glinterleavedarrays**](glinterleavedarrays.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> </dl>

 

 





