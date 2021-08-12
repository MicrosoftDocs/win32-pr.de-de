---
title: glDrawArrays-Funktion (Gl.h)
description: Die glDrawArrays-Funktion gibt mehrere primitive Typen an, die gerendert werden sollen.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349ba3407d84d66afd431d14c3fc97b151661f4f783a05734a55d9ba1dc313ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616992"
---
# <a name="gldrawarrays-function"></a>glDrawArrays-Funktion

Die **glDrawArrays-Funktion** gibt mehrere primitive Typen an, die gerendert werden sollen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die Art von primitiven Typen, die gerendert werden sollen. Die folgenden Konstanten geben zulässige Typen von Primitiven an: GL \_ POINTS, GL \_ LINE \_ STRIP, GL \_ LINE \_ LOOP, GL \_ LINES, GL TRIANGLE \_ \_ STRIP, GL TRIANGLE \_ \_ FAN, GL \_ TRIANGLES, GL \_ QUAD \_ STRIP, GL \_ QUADS und GL \_ POLYGON.

</dd> <dt>

*first* 
</dt> <dd>

Der Startindex in den aktivierten Arrays.

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der zu rendernden Indizes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *count* war negativ.<br/>                                                                                                      |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Mit **glDrawArrays** können Sie mehrere geometrische Primitive angeben, die gerendert werden sollen. Anstatt separate OpenGL-Funktionen aufzurufen, um jeden einzelnen Scheitelpunkt, jede Normale oder Farbe zu übergeben, können Sie separate Arrays von Scheitelpunkten, Normalitäten und Farben angeben, um eine Sequenz von Primitiven (alle gleich) mit einem einzigen Aufruf von **glDrawArrays** zu definieren.

Wenn Sie **glDrawArrays** aufrufen, werden sequenzielle Elemente aus jedem aktivierten Array *gezählt,* um eine Sequenz geometrischer Primitive zu erstellen, beginnend mit dem *ersten* Element. Der *mode-Parameter* gibt an, welche Art von Primitivem erstellt werden soll und wie die Arrayelemente verwendet werden, um die Primitiven zu erstellen.

Nachdem **glDrawArrays** zurückgegeben wurde, sind die Werte von Vertexattributen, die von **glDrawArrays** geändert werden, nicht definiert. Wenn z. B. GL \_ COLOR \_ ARRAY aktiviert ist, ist der Wert der aktuellen Farbe nicht definiert, nachdem **glDrawArrays** zurückgegeben wurde. Attribute, die nicht durch **glDrawArrays** geändert werden, bleiben definiert. Wenn GL \_ VERTEX \_ ARRAY nicht aktiviert ist, werden keine geometrischen Primitive generiert, aber die Attribute, die aktivierten Arrays entsprechen, werden geändert.

Sie können **glDrawArrays** in Anzeigelisten einschließen. Wenn Sie **glDrawArrays** in eine Anzeigeliste einschließen, werden die erforderlichen Arraydaten, die durch die Arrayzeiger und die Aktivierten bestimmt werden, generiert und in die Anzeigeliste eingegeben. Die Werte von Arrayzeigern und -aktivierten werden während der Erstellung von Anzeigelisten bestimmt.

Sie können statische Arraydaten jederzeit lesen. Wenn statische Arrayelemente geändert werden und das Array nicht erneut angegeben wird, sind die Ergebnisse aller nachfolgenden Aufrufe von **glDrawArrays** nicht definiert.

Obwohl kein Fehler generiert wird, wenn Sie ein Array mehr als einmal in [**glBegin-**](glbegin.md) und [**-paaren**](glend.md) angeben, sind die Ergebnisse nicht definiert.

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
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

 

 





