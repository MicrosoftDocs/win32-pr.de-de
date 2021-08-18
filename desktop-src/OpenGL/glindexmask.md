---
title: glIndexMask-Funktion (Gl.h)
description: Die glIndexMask-Funktion steuert das Schreiben einzelner Bits in den Farbindexpuffern.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glIndexMask-Funktion OpenGL
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
ms.openlocfilehash: f8e022bb3cbb5be5ac15049b5e8bc128d2ac7e100d5bcec6a87988dd2d14c5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012198"
---
# <a name="glindexmask-function"></a>glIndexMask-Funktion

Die **glIndexMask-Funktion** steuert das Schreiben einzelner Bits in den Farbindexpuffern.

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

Eine Bitmaske zum Aktivieren und Deaktivieren des Schreibens einzelner Bits in den Farbindexpuffern. Anfänglich ist die Maske alle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glIndexMask-Funktion** steuert das Schreiben einzelner Bits in den Farbindexpuffern. Geben Sie eine *Maske* an, wobei *1* die Anzahl der Bits in einem Farbindexpuffer ist.  Überall dort, wo eine in der Maske angezeigt wird, wird das entsprechende Bit im Farbindexpuffer (oder puffern) schreibbar gemacht. Wenn eine 0 (null) angezeigt wird, ist das Bit schreibgeschützt.

Diese Maske wird nur im Farbindexmodus verwendet und wirkt sich nur auf die Puffer aus, die derzeit zum Schreiben ausgewählt sind (siehe [**glDrawBuffer**](gldrawbuffer.md)). Anfänglich sind alle Bits für das Schreiben aktiviert.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glIndexMask** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ INDEX \_ WRITEMASK

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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





