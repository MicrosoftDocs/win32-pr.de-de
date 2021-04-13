---
title: glindexpointer-Funktion (GL. h)
description: Die Funktion "glindexpointer" definiert ein Array von Farbindizes.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glindexpointer-Funktion OpenGL
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
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475261"
---
# <a name="glindexpointer-function"></a>glindexpointer-Funktion

Die Funktion " **glindexpointer** " definiert ein Array von Farbindizes.

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

Der Datentyp der einzelnen Farbindizes im Array mit den folgenden symbolischen Konstanten: GL \_ Short, GL \_ int, GL \_ float, GL \_ Double.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Byte Offset zwischen aufeinander folgenden Farbindizes. Wenn *Stride* gleich NULL ist, werden die Farbindizes im Array eng verpackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf den ersten Farb Index im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                              | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>  | der *Typ* war kein akzeptierter Wert.<br/> |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | " *Stride* " oder " *count* " war negativ.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glindexpointer** " gibt den Speicherort und die Daten eines Arrays von Farbindizes an, die beim Rendern verwendet werden sollen. Der *Typparameter* gibt den Datentyp jedes Farbindexes an, und *Stride* bestimmt den Byte Offset von einem Farb Index zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays. In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter als die Verwendung von separaten Arrays sein. Weitere Informationen finden Sie unter [**glinterleavedarrays**](glinterleavedarrays.md).

Ein Farb Index Array wird aktiviert, wenn Sie die GL- \_ Index \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwenden " [**gldrawarrays**](gldrawarrays.md) " und " [**glarrayelement**](glarrayelement.md) " das Farb Index Array. Standardmäßig ist das Farb Index Array deaktiviert.

Sie können " **glindexpointer** " nicht in Anzeigelisten einschließen.

Wenn Sie ein Farb Index Array mithilfe von **glindexpointer** angeben, werden die Werte aller Farb Index Array-Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden. Da es sich bei den Farb Index Array-Parametern um einen Client seitigen Zustand handelt, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und **glpopatpub** nicht gespeichert oder wieder hergestellt.

Obwohl kein Fehler generiert wird, wenn Sie **glindexpointer** innerhalb von [**glBegin**](glbegin.md) -und **glEnd** -Paaren aufzurufen, sind die Ergebnisse nicht definiert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glindexpointer** abgerufen:

[**glisenabled**](glisenabled.md) mit Argument-GL- \_ Index \_ Array

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Index \_ array \_ Stride

**glget** mit Argument GL \_ Index \_ array \_ count

**glget** mit Argument-Typ für GL- \_ Index \_ array \_

**glget** mit Argument-GL- \_ Index \_ array \_ Größe

[**glgetpointerv**](glgetpointerv.md) mit Argument GL \_ Index \_ array- \_ Zeiger

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

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





