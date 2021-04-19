---
title: glgetpointerv-Funktion (GL. h)
description: Die Funktion "glgetpointerv" gibt die Adresse eines Vertex-Daten Arrays zurück.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glgetpointerv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338757"
---
# <a name="glgetpointerv-function"></a>glgetpointerv-Funktion

Die Funktion " **glgetpointerv** " gibt die Adresse eines Vertex-Daten Arrays zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Der Typ des Array Zeigers, der von den folgenden symbolischen Konstanten zurückgegeben werden soll: GL- \_ Farb \_ array \_ Zeiger, GL- \_ \_ \_ \_ \_ \_ edgeflag-Array Zeiger, GL-Feedback \_ -Puffer Zeiger, GL \_ \_ -Index Array \_ Zeiger, GL- \_ normaler \_ array \_ Zeiger, GL \_ -Textur- \_ \_ array \_ Zeiger, GL \_ \_ -Auswahl Puffer \_ Zeiger und GL/ \_ tex- \_ array \_ Zeiger

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert des durch " *PName*" angegebenen Array Zeigers zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                             | Bedeutung                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl> | *PName* war kein akzeptierter Wert.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetpointerv** " gibt Array Zeiger Informationen zurück. Der *PName* -Parameter ist eine symbolische Konstante, die die Art des zurück zugebende Array Zeigers angibt, und *params* ist ein Zeiger auf einen Speicherort, um die zurückgegebenen Daten zu platzieren.

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

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





