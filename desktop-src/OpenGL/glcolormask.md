---
title: glColorMask-Funktion (Gl.h)
description: Die glColorMask-Funktion aktiviert und deaktiviert das Schreiben von Framepufferfarbkomponenten.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8b3e9e00eaa294f77813f8e994358cbb473fc4e5c02fce8e5115dc517cae20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081720"
---
# <a name="glcolormask-function"></a>glColorMask-Funktion

Die **glColorMask-Funktion** aktiviert und deaktiviert das Schreiben von Framepufferfarbkomponenten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rot* 
</dt> <dd>

Geben Sie an, ob Rot in den Framepuffer geschrieben werden kann oder nicht. Die Standardwerte sind GL \_ TRUE und geben an, dass die Farbkomponente geschrieben werden kann.

</dd> <dt>

*Grün* 
</dt> <dd>

Geben Sie an, ob Grün in den Framepuffer geschrieben werden kann oder nicht. Der Standardwert ist GL \_ TRUE und gibt an, dass die Farbkomponente geschrieben werden kann.

</dd> <dt>

*Blau* 
</dt> <dd>

Geben Sie an, ob Blau in den Framepuffer geschrieben werden kann oder nicht. Der Standardwert ist GL \_ TRUE und gibt an, dass die Farbkomponente geschrieben werden kann.

</dd> <dt>

*alpha* 
</dt> <dd>

Geben Sie an, ob Alpha in den Framepuffer geschrieben werden kann oder nicht. Der Standardwert ist GL \_ TRUE und gibt an, dass die Farbkomponente geschrieben werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glColorMask-Funktion** gibt an, ob die einzelnen Farbkomponenten im Framepuffer geschrieben werden können oder nicht. Wenn *rot* \_ z. B. GL FALSE ist, wird unabhängig vom versuchten Zeichnungsvorgang keine Änderung an der roten Komponente eines Pixels in einem der Farbpuffer vorgenommen.

Änderungen an einzelnen Komponentenbits können nicht gesteuert werden. Stattdessen werden Änderungen entweder für ganze Farbkomponenten aktiviert oder deaktiviert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glColorMask** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ COLOR \_ WRITEMASK

**glGet** mit argument GL \_ RGBA \_ MODE

## <a name="requirements"></a>Requirements (Anforderungen)



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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





