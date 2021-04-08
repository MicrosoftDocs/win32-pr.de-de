---
title: glindexd-Funktion (GL. h)
description: Die Funktion "glindexd" legt den aktuellen Farbindex fest.
ms.assetid: 4cd72d32-e796-4c94-94cb-591f1ee3b26e
keywords:
- glindexd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d1e7cce6ad2ae39e5ca107ef89b3b86147596e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949581"
---
# <a name="glindexd-function"></a>glindexd-Funktion

Die Funktion " **glindexd** " legt den aktuellen Farbindex fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexd(
   GLdouble c
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

Die Funktion " **glindexd** " aktualisiert den aktuellen Farbindex (mit einem Wert). Es wird ein Argument benötigt: der neue Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleit Komma Wert gespeichert. Ganzzahlige Werte werden ohne besondere Zuordnung direkt in Gleit Komma Werte konvertiert.

Index Werte außerhalb des darstellbaren Bereichs des Farb Index Puffers werden nicht gebunden. Vor der Deaktivierung eines Indexes (sofern aktiviert) und dem Schreiben in den Framebuffer wird der Index jedoch in ein festes Punkt Format konvertiert. Alle Bits im ganzzahligen Teil des resultierenden fest Komma Werts, die nicht Bits im Frame Puffer entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere kann **glindexd** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexd** ab:

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

 

