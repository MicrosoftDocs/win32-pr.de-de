---
title: glindexmask-Funktion (GL. h)
description: Die Funktion "glindexmask" steuert das Schreiben einzelner Bits in den Farb Index Puffern.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glindexmask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340569"
---
# <a name="glindexmask-function"></a>glindexmask-Funktion

Die Funktion " **glindexmask** " steuert das Schreiben einzelner Bits in den Farb Index Puffern.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Eine Bitmaske, um das Schreiben einzelner Bits in den Farb Index Puffern zu aktivieren und zu deaktivieren. Anfänglich ist die Maske alle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glindexmask** " steuert das Schreiben einzelner Bits in den Farb Index Puffern. Die am wenigsten signifikanten *n* Bits der *Maske*, wobei *1* die Anzahl der Bits in einem Farb Index Puffer ist, geben eine Maske an. Wenn ein solches in der Maske angezeigt wird, wird das entsprechende Bit im Farb Index Puffer (oder Puffer) als beschreibbar festgelegt. Wenn ein NULL-Wert angezeigt wird, ist das Bit schreibgeschützt.

Diese Maske wird nur im Farb Index Modus verwendet und wirkt sich nur auf die Puffer aus, die zurzeit zum Schreiben ausgewählt werden (siehe [**gldrawbuffer**](gldrawbuffer.md)). Anfänglich werden alle Bits zum Schreiben aktiviert.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexmask** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Index \_ schreibfrage

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

[**gldepthmask**](gldepthmask.md)
</dt> <dt>

[**gldrawbuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glindex**](glindex-functions.md)
</dt> <dt>

[**glstencilmask**](glstencilmask.md)
</dt> </dl>

 

 





