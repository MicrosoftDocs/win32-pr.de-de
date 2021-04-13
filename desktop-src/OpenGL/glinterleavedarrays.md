---
title: glinterleavedarrays-Funktion (GL. h)
description: Die Funktion "glinterleavedarrays" gibt gleichzeitig mehrere verschachtelte Arrays in einem größeren Aggregat Array an und aktiviert Sie.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glinterleavedarrays-Funktion OpenGL
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
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391642"
---
# <a name="glinterleavedarrays-function"></a>glinterleavedarrays-Funktion

Die Funktion " **glinterleavedarrays** " gibt gleichzeitig mehrere verschachtelte Arrays in einem größeren Aggregat Array an und aktiviert Sie.

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

Der Typ des zu aktivierenden Arrays. Der Parameter kann einen der folgenden symbolischen Werte annehmen: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F \_ N3F \_ V3F, GL \_ T2F \_ V3F, GL T4F V4F \_ \_ , GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ C3F \_ V3F, GL \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ N3F \_ V3F oder GL \_ T4F C4F N3F \_ \_ \_ V4F.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Offset in Bytes zwischen jedem Aggregat Array Element.

</dd> <dt>

*Zeiger* 
</dt> <dd>

Ein Zeiger auf das erste Element eines Aggregat Arrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Format* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *Stride* war ein negativer Wert.<br/>                                                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Mit der **glinterleavedarrays** -Funktion können Sie mehrere verschachtelte Farb-, normal-, Textur-und Vertex-Arrays gleichzeitig angeben und aktivieren, deren Elemente Teil eines größeren Aggregat Array Elements sind. Bei einigen Speicher Architekturen ist dies effizienter als das separate angeben der Arrays.

Wenn der *Stride* -Parameter 0 (null) ist, werden die Aggregat Array Elemente nacheinander gespeichert. Andernfalls erfolgt die Anzahl von *Stride* -Bytes zwischen Aggregat Array Elementen.

Der *Format* -Parameter dient als Schlüssel, der beschreibt, wie einzelne Arrays aus dem Aggregat Array extrahiert werden:

-   Wenn das *Format* T enthält, werden Texturkoordinaten aus dem verschachtelten Array extrahiert.
-   Wenn C vorhanden ist, werden Farbwerte extrahiert.
-   Wenn N vorhanden ist, werden normale Koordinaten extrahiert.
-   Scheitelpunkt Koordinaten werden immer extrahiert.
-   Die Ziffern 2, 3 und 4 kennzeichnen, wie viele Werte extrahiert werden.
-   F gibt an, dass Werte als Gleit Komma Werte extrahiert werden.
-   Wenn 4UB auf das C folgt, können Farben auch als 4 nicht signierte Bytes extrahiert werden. Wenn eine Farbe als 4 nicht signierte Bytes extrahiert wird, befindet sich das nachfolgende Vertex-Array Element an der ersten möglichen ausgerichteten Gleit Komma Adresse.

Wenn Sie bei der Kompilierung einer Anzeigeliste " **glinterleavedarrays** " aufrufen, wird diese nicht in die Liste kompiliert, sondern sofort ausgeführt.

Sie können keine Aufrufe von **glinterleavedarrays** in **gldisableclientstate** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von **glEnd** einschließen.

> [!Note]  
> Die Funktion " **glinterleavedarrays** " ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Die Funktion " **glinterleavedarrays** " wird auf Clientseite ohne Protokoll implementiert. Da es sich bei den Scheitelpunkt Array-Parametern um einen Client seitigen Zustand handelt, werden Sie von [**glpushatfferb**](glpushattrib.md) und **glpopatfferb** nicht gespeichert oder wieder hergestellt. Verwenden Sie stattdessen [**glpushclientatpub**](glpushclientattrib.md) und **glpopclientatpub** .

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**glpushclientatpub**](glpushclientattrib.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





