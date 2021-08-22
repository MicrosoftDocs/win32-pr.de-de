---
title: glIndexs-Funktion (Gl.h)
description: Die glIndexs-Funktion legt den aktuellen Farbindex fest.
ms.assetid: 193304e6-c88a-49a6-935b-29bcf1954564
keywords:
- glIndexs-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexs
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d3e309d8288765e493cac6c586c873d4bb927ca2d0fc89c3b8c621b2e2ed31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493390"
---
# <a name="glindexs-function"></a>glIndexs-Funktion

Die **glIndexs-Funktion** legt den aktuellen Farbindex fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexs(
   GLshort c
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*c* 
</dt> <dd>

Der neue Wert für den aktuellen Farbindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glIndexs-Funktion** aktualisiert den aktuellen (einwertigen) Farbindex. Sie benötigt ein Argument: den neuen Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleitkommawert gespeichert. Ganzzahlige Werte werden ohne spezielle Zuordnung direkt in Gleitkommawerte konvertiert.

Indexwerte außerhalb des darstellbaren Bereichs des Farbindexpuffers werden nicht klammern. Bevor ein Index jedoch erweitert (falls aktiviert) und in den Framepuffer geschrieben wird, wird er in das Festkommaformat konvertiert. Alle Bits im ganzzahligen Teil des resultierenden Festkommawerts, die nicht Bits im Framepuffer entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere können **glIndexs** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glIndexs ab:**

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

 

