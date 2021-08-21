---
title: glDrawElements-Funktion (Gl.h)
description: Die glDrawElements-Funktion rendert Primitive aus Arraydaten.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b260c1112f7ec588b4d83655e5d0aa465b63682164f2ca745b63d3f421e5794c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616572"
---
# <a name="gldrawelements-function"></a>glDrawElements-Funktion

Die **glDrawElements-Funktion** rendert Primitive aus Arraydaten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die Art von primitiven Typen, die gerendert werden sollen. Es kann von einem der folgenden symbolischen Werte ausgegangen werden: GL \_ POINTS, GL \_ LINE \_ STRIP, GL \_ LINE \_ LOOP, GL \_ LINES, GL TRIANGLE \_ \_ STRIP, GL TRIANGLE \_ \_ FAN, GL \_ TRIANGLES, GL \_ QUAD \_ STRIP, GL \_ QUADS und GL \_ POLYGON.

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der elemente, die gerendert werden sollen.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Werte in Indizes. Muss eins von GL \_ UNSIGNED \_ BYTE, GL \_ UNSIGNED \_ SHORT oder GL \_ UNSIGNED \_ INT sein.

</dd> <dt>

*Indizes* 
</dt> <dd>

Ein Zeiger auf die Position, an der die Indizes gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *count* war ein negativer Wert.<br/>                                                                                              |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Mit der **glDrawElements-Funktion** können Sie mehrere geometrische Primitive mit sehr wenigen Funktionsaufrufen angeben. Anstatt eine OpenGL-Funktion aufzurufen, um jeden einzelnen Scheitelpunkt, jede Normale oder Farbe zu übergeben, können Sie im Voraus separate Arrays von Scheitelpunkten, Normalwerten und Farben angeben und diese verwenden, um eine Sequenz von Primitiven (alle vom gleichen Typ) mit einem einzigen Aufruf von **glDrawElements** zu definieren.

Wenn Sie die **glDrawElements-Funktion** aufrufen, verwendet sie count sequential elements from indices *(Sequenzielle* Elemente aus *Indizes* zählen), um eine Sequenz geometrischer Primitive zu erstellen. Der *mode-Parameter* gibt an, welche Art von Primitiven erstellt werden und wie die Arrayelemente zum Erstellen dieser Primitive verwendet werden. Wenn GL \_ VERTEX \_ ARRAY nicht aktiviert ist, werden keine geometrischen Primitive generiert.

Vertexattribute, die von **glDrawElements** geändert werden, haben einen nicht angegebenen Wert, nachdem **glDrawElements** zurückgegeben wurde. Wenn z. B. GL \_ COLOR \_ ARRAY aktiviert ist, ist der Wert der aktuellen Farbe nicht definiert, nachdem **glDrawElements** ausgeführt wurde. Attribute, die nicht geändert werden, bleiben unverändert.

Sie können die **glDrawElements-Funktion** in Anzeigelisten einschließen. Wenn **glDrawElements** in einer Anzeigeliste enthalten ist, werden die erforderlichen Arraydaten (durch die Arrayzeiger bestimmt und aktiviert) ebenfalls in die Anzeigeliste eingegeben. Da die Arrayzeiger und -aktivierten clientseitige Zustandsvariablen sind, wirken sich ihre Werte auf Anzeigelisten aus, wenn die Listen erstellt werden, nicht, wenn die Listen ausgeführt werden.

> [!Note]  
> Die **glDrawElements-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





