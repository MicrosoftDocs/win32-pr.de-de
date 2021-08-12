---
title: glArrayElement-Funktion (Gl.h)
description: Die glArrayElement-Funktion gibt die Arrayelemente an, die zum Rendern eines Scheitelpunkts verwendet werden.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement-Funktion OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb6fdf3b90c5145c46730e530f26ba7d4f7f3875e51cc4d510e9763d03e27207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618059"
---
# <a name="glarrayelement-function"></a>glArrayElement-Funktion

Die **glArrayElement-Funktion** gibt die Arrayelemente an, die zum Rendern eines Scheitelpunkts verwendet werden.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Ein Index in den aktivierten Arrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **glArrayElement-Funktion** in [**glBegin-**](glbegin.md) und [**glEnd-Paaren,**](glend.md) um Scheitelpunkt- und Attributdaten für Punkt-, Linien- und Polygonprimitive anzugeben. Die **glArrayElement-Funktion** gibt die Daten für einen einzelnen Scheitelpunkt mithilfe von Scheitelpunkt- und Attributdaten an, die sich am *Index* der aktivierten Scheitelpunktarrays befinden.

Sie können **glArrayElement** verwenden, um Primitive zu erstellen, indem Sie Scheitelpunktdaten indizieren, anstatt Arrays von Daten in der Reihenfolge von vorn nach der letzten zu streamen. Da **glArrayElement** nur einen einzelnen Scheitelpunkt angibt, können Sie explizit Attribute für einzelne Primitive angeben. Sie können z. B. eine einzelne Normalität für jedes einzelne Dreieck festlegen.

Wenn Sie Aufrufe von **glArrayElement** in Anzeigelisten einschließen, werden die erforderlichen Arraydaten, die durch die Arrayzeiger und Aktivierungswerte bestimmt werden, ebenfalls in die Anzeigeliste eingegeben. Arrayzeiger und Aktivierungswerte werden bestimmt, wenn Anzeigelisten erstellt werden, nicht wenn Anzeigelisten ausgeführt werden.

Sie können statische Arraydaten jederzeit mit **glArrayElement** lesen und zwischenspeichern. Wenn Sie die Elemente eines statischen Arrays ändern, ohne das Array erneut anzugeben, sind die Ergebnisse aller nachfolgenden Aufrufe von **glArrayElement** nicht definiert.

Wenn Sie **glArrayElement** aufrufen, ohne zuerst **glEnableClientState**(GL \_ VERTEX \_ ARRAY) aufzurufen, erfolgt keine Zeichnung, aber die Attribute, die aktivierten Arrays entsprechen, werden geändert. Obwohl beim Angeben eines Arrays innerhalb der Paare **glBegin** und **glEnd** kein Fehler generiert wird, sind die Ergebnisse nicht definiert.

> [!Note]  
> Die **glArrayElement-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
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

 

 





