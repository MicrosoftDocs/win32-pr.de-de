---
title: glGetPointerv-Funktion (Gl.h)
description: Die glGetPointerv-Funktion gibt die Adresse eines Scheitelpunktdatenarrays zurück.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv-Funktion OpenGL
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
ms.openlocfilehash: fdbef5cc17a547e82dfa55876d927ef9fed87f106d9e5fa0d5d1c36a5ce269b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493920"
---
# <a name="glgetpointerv-function"></a>glGetPointerv-Funktion

Die **glGetPointerv-Funktion** gibt die Adresse eines Scheitelpunktdatenarrays zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Der Typ des Arrayzeigers, der von den folgenden symbolischen Konstanten zurückgeben werden soll: GL \_ COLOR \_ ARRAY \_ POINTER, GL \_ EDGE FLAG ARRAY \_ \_ \_ POINTER, GL \_ FEEDBACK BUFFER \_ \_ POINTER, GL \_ INDEX ARRAY \_ \_ POINTER, GL \_ NORMAL ARRAY \_ \_ POINTER, GL \_ TEXTURE \_ COORD \_ ARRAY \_ POINTER, GL \_ SELECTION BUFFER \_ \_ POINTER und GL \_ VERTEX ARRAY \_ \_ POINTER.

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert des Arrayzeigers zurück, der durch *pname angegeben wird.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                             | Bedeutung                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl> | *pname* war kein akzeptierter Wert.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetPointerv-Funktion** gibt Arrayzeigerinformationen zurück. Der *pname-Parameter* ist eine symbolische Konstante, die die Art des zurücksenden Arrayzeigers angibt, und *params* ist ein Zeiger auf eine Position, an der die zurückgegebenen Daten gespeichert werden.

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





