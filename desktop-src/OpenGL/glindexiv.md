---
title: glIndexiv-Funktion (Gl.h)
description: Die glIndexiv-Funktion legt den aktuellen Farbindex fest.
ms.assetid: 642c243f-046d-474e-8075-ef5692797020
keywords:
- glIndexiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fecb1cad302b4a302c5079f2af3dd72158d4b98ce57794b8f080a8919b9cad5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493440"
---
# <a name="glindexiv-function"></a>glIndexiv-Funktion

Die **glIndexiv-Funktion** legt den aktuellen Farbindex fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexiv(
   const GLint *c
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*c* 
</dt> <dd>

Ein Zeiger auf ein Array mit einem Element, das den neuen Wert für den aktuellen Farbindex enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glIndexiv-Funktion** aktualisiert den aktuellen (einwertigen) Farbindex. Sie benötigt ein Argument: den neuen Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleitkommawert gespeichert. Ganzzahlige Werte werden ohne spezielle Zuordnung direkt in Gleitkommawerte konvertiert.

Indexwerte außerhalb des darstellbaren Bereichs des Farbindexpuffers werden nicht klammern. Bevor ein Index jedoch erweitert (falls aktiviert) und in den Framepuffer geschrieben wird, wird er in das Festkommaformat konvertiert. Alle Bits im ganzzahligen Teil des resultierenden Festkommawerts, die nicht Bits im Framepuffer entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere kann **glIndexiv** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glIndexiv** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ INDEX

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

