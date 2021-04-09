---
title: gledgeflagpointer-Funktion (GL. h)
description: Die Funktion gledgeflagpointer definiert ein Array von Edge-Flags.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- gledgeflagpointer-Funktion OpenGL
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
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742208"
---
# <a name="gledgeflagpointer-function"></a>gledgeflagpointer-Funktion

Die Funktion **gledgeflagpointer** definiert ein Array von Edge-Flags.

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

Der Byte Offset zwischen aufeinander folgenden Edge-Flags. Wenn *Stride* 0 (null) ist, werden die Edge-Flags im Array eng verpackt.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf das erste Edge-Flag im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                             | Bedeutung                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl> | " *Stride* " oder " *count* " war negativ.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion **gledgeflagpointer** gibt den Speicherort und die Daten eines Arrays von booleschen Edge-Flags an, die beim Rendern verwendet werden sollen. Der *Stride* -Parameter bestimmt den Byte Offset von einem edgeflag zum nächsten, das das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays ermöglicht. In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter als die Verwendung von separaten Arrays sein.

Ein Edge-Flag-Array wird aktiviert, wenn Sie die GL- \_ Edge- \_ Flag- \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben. Wenn diese Option aktiviert ist, verwendet [**gldrawarrays**](gldrawarrays.md) oder [**glarrayelement**](glarrayelement.md) das Edge-Flag-Array. Standardmäßig ist das Edge-Flag-Array deaktiviert.

Verwenden Sie **gldrawarrays** , um eine Sequenz von primitiven (alle desselben Typs) aus den vorspezifizierten Vertex-und Vertex-Attribut Arrays zu erstellen. Verwenden Sie " **glarrayelement** ", um primitive durch Indizierung von Vertices und Scheitelpunkt Attributen anzugeben, und [**gldrawelements**](gldrawelements.md) zum Erstellen einer Sequenz von primitiven durch Indizierung von Vertices und Vertex-Attributen.

Sie können **gledgeflagpointer** nicht in Anzeigelisten einschließen.

Wenn Sie ein Edge-Flag-Array mit **gledgeflagpointer** angeben, werden die Werte aller Edge-Flag-Array Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden. Da sich die Parameter des Edge-Flag-Arrays in einem Client seitigen Zustand [**befinden, speichern**](glpushattrib.md) oder Wiederherstellen [**Sie Ihre Werte nicht.**](glpopattrib.md)

Obwohl das Aufrufen von **gledgeflagpointer** innerhalb eines [**glBegin**](glbegin.md)- / [**glEnd**](glend.md) -Paars keinen Fehler generiert, sind die Ergebnisse nicht definiert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gledgeflagpointer** -Funktion ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Edge- \_ Flag \_ array \_ Stride

**glget** mit dem Argument GL \_ Edge \_ Flag \_ array \_ count

[**glgetpointerv**](glgetpointerv.md) mit Argument GL \_ Edge- \_ Flag \_ array \_ Zeiger

[**glisenabled**](glisenabled.md) mit Argument GL \_ Edge- \_ Flag- \_ Array

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glpopattenb**](glpopattrib.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





