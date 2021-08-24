---
title: glIndexfv-Funktion (Gl.h)
description: Die funktion glIndexfv legt den aktuellen Farbindex fest.
ms.assetid: 355d1896-ea9d-4a80-9dee-285f3bf638e5
keywords:
- glIndexfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a64c7c51d442d5e0dff14d8377e387b8da183bb3b74e7f2c8a1bceef189cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493480"
---
# <a name="glindexfv-function"></a>glIndexfv-Funktion

Die **funktion glIndexfv** legt den aktuellen Farbindex fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexfv(
   const GLfloat *c
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*c* 
</dt> <dd>

Ein Zeiger auf ein Ein-Element-Array, das den neuen Wert für den aktuellen Farbindex enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glIndexfv-Funktion** aktualisiert den aktuellen (einwertigen) Farbindex. Es wird ein Argument verwendet: der neue Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleitkommawert gespeichert. Ganzzahlige Werte werden ohne spezielle Zuordnung direkt in Gleitkommawerte konvertiert.

Indexwerte außerhalb des darstellbaren Bereichs des Farbindexpuffers werden nicht geklammert. Bevor ein Index jedoch gedithert (sofern aktiviert) und in den Framepuffer geschrieben wird, wird er in das Festpunktformat konvertiert. Alle Bits im ganzzahligen Teil des resultierenden Festpunktwerts, die bits im Framepuffer nicht entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere kann **glIndexfv** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd aufgerufen werden.**](glend.md)

Die folgende Funktion ruft Informationen im Zusammenhang mit **glIndexfv ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ CURRENT \_ INDEX

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

 

