---
title: glgetclipplane-Funktion (GL. h)
description: Die Funktion "glgetclipplane" gibt die Koeffizienten der angegebenen Clippingebene zurück.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glgetclipplane-Funktion OpenGL
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
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345530"
---
# <a name="glgetclipplane-function"></a>glgetclipplane-Funktion

Die Funktion " **glgetclipplane** " gibt die Koeffizienten der angegebenen Clippingebene zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wasser* 
</dt> <dd>

Eine Clippingebene. Die Anzahl der Clippingebenen hängt von der Implementierung ab, es werden jedoch mindestens sechs Clippingebenen unterstützt. Sie werden durch symbolische Namen der Form "GL \_ Clip Plane i" identifiziert, \_ wobei 0 = *i* < GL  \_ Max \_ \_ .

</dd> <dt>

*Gleichung* 
</dt> <dd>

Gibt vier Werte mit doppelter Genauigkeit zurück, bei denen es sich um die Koeffizienten der ebenengleichung *der Ebenen in* Eye-Koordinaten handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | die *Ebene* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetclipplane** " gibt die vier Koeffizienten der ebenengleichung für die *Ebene* in *Gleichung* zurück.

Es ist immer der Fall, dass GL \_ Clip \_ Plane *i* = GL \_ Clip \_ PLANE0 + *i*.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Gleichung* vorgenommen.

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

[**glclipplane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





