---
title: glIndexi-Funktion (Gl.h)
description: Die glIndexi-Funktion legt den aktuellen Farbindex fest.
ms.assetid: c57d2316-4081-40d8-af50-ae0299597803
keywords:
- glIndexi-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d905dba292457654b3f92da132eabbdc58ea316fedf6a11b55c2d1df820bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359336"
---
# <a name="glindexi-function"></a>glIndexi-Funktion

Die **glIndexi-Funktion** legt den aktuellen Farbindex fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexi(
   GLint c
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

Die **glIndexi-Funktion** aktualisiert den aktuellen (einwertigen) Farbindex. Sie benötigt ein Argument: den neuen Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleitkommawert gespeichert. Ganzzahlige Werte werden ohne spezielle Zuordnung direkt in Gleitkommawerte konvertiert.

Indexwerte außerhalb des darstellbaren Bereichs des Farbindexpuffers werden nicht klammern. Bevor ein Index jedoch erweitert (falls aktiviert) und in den Framepuffer geschrieben wird, wird er in das Festkommaformat konvertiert. Alle Bits im ganzzahligen Teil des resultierenden Festkommawerts, die nicht Bits im Framepuffer entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere kann **glIndexi** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glIndexi** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ INDEX

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

