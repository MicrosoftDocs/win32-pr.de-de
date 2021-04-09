---
title: glindexs-Funktion (GL. h)
description: Die Funktion "glindexs" legt den aktuellen Farbindex fest.
ms.assetid: 193304e6-c88a-49a6-935b-29bcf1954564
keywords:
- glindexs-Funktion OpenGL
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
ms.openlocfilehash: 0cdc2036b3aec37c8f727dc38a5186998a5bc80c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102946"
---
# <a name="glindexs-function"></a>glindexs-Funktion

Die Funktion " **glindexs** " legt den aktuellen Farbindex fest.

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

Der neue Wert für den aktuellen Farb Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glindexs** " aktualisiert den aktuellen Farbindex (mit einem Wert). Es wird ein Argument benötigt: der neue Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleit Komma Wert gespeichert. Ganzzahlige Werte werden ohne besondere Zuordnung direkt in Gleit Komma Werte konvertiert.

Index Werte außerhalb des darstellbaren Bereichs des Farb Index Puffers werden nicht gebunden. Vor der Deaktivierung eines Indexes (sofern aktiviert) und dem Schreiben in den Framebuffer wird der Index jedoch in ein festes Punkt Format konvertiert. Alle Bits im ganzzahligen Teil des resultierenden fest Komma Werts, die nicht Bits im Frame Puffer entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere kann **glindexs** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexs** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Current \_ Index"

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

