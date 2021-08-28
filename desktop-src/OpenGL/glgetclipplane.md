---
title: glGetClipPlane-Funktion (Gl.h)
description: Die glGetClipPlane-Funktion gibt die Koeffizienten der angegebenen Clippingebene zurück.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf551356088db2b99b79a28a396be785ab60f2196cc3e27353cb867d4b151dd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742039"
---
# <a name="glgetclipplane-function"></a>glGetClipPlane-Funktion

Die **glGetClipPlane-Funktion** gibt die Koeffizienten der angegebenen Clippingebene zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flugzeug* 
</dt> <dd>

Eine Clippingebene. Die Anzahl der Clippingebenen hängt von der Implementierung ab, es werden jedoch mindestens sechs Clippingebenen unterstützt. Sie werden durch symbolische Namen der Form GL \_ CLIP \_ PLANE *i* identifiziert, wobei 0 = *i* < GL MAX \_ CLIP \_ \_ PLANES.

</dd> <dt>

*Gleichung* 
</dt> <dd>

Gibt vier Werte mit doppelter Genauigkeit zurück, die die Koeffizienten der Ebenengleichung der *Ebene* in Augenkoordinaten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *plane* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetClipPlane-Funktion** gibt in *Gleichung* die vier Koeffizienten der Ebenengleichung für *ebene* zurück.

Es ist immer der Fall, dass GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

Wenn ein Fehler generiert wird, werden keine Änderungen am Inhalt der *Formel* vorgenommen.

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





