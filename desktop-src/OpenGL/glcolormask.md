---
title: glcolormask-Funktion (GL. h)
description: Die glcolormask-Funktion aktiviert und deaktiviert das Schreiben von Frame-Puffer Farbkomponenten.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glcolormask-Funktion OpenGL
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
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858746"
---
# <a name="glcolormask-function"></a>glcolormask-Funktion

Die **glcolormask** -Funktion aktiviert und deaktiviert das Schreiben von Frame-Puffer Farbkomponenten.

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

*Red* 
</dt> <dd>

Geben Sie an, ob rot in den Framebuffer geschrieben werden kann oder nicht. Die Standardwerte lauten "GL \_ true", was darauf hinweist, dass die Farbkomponente geschrieben werden kann.

</dd> <dt>

*Grünbuchs* 
</dt> <dd>

Geben Sie an, ob grün in den Framebuffer geschrieben werden kann oder nicht. Der Standardwert ist "GL \_ true", der angibt, dass die Farbkomponente geschrieben werden kann.

</dd> <dt>

*blauen* 
</dt> <dd>

Geben Sie an, ob blau in den Framebuffer geschrieben werden kann oder nicht. Der Standardwert ist "GL \_ true", der angibt, dass die Farbkomponente geschrieben werden kann.

</dd> <dt>

*alpha* 
</dt> <dd>

Geben Sie an, ob Alpha in den Framebuffer geschrieben werden kann oder nicht. Der Standardwert ist "GL \_ true", der angibt, dass die Farbkomponente geschrieben werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glcolormask** -Funktion gibt an, ob die einzelnen Farbkomponenten im Frame Puffer geschrieben werden können oder nicht. Wenn *rot* den Wert "GL \_ false" hat, wird z. b. unabhängig vom versuchten Zeichnungs Vorgang keine Änderung an der roten Komponente eines Pixels in einem der Farb Puffer vorgenommen.

Änderungen an einzelnen Komponenten Komponenten können nicht gesteuert werden. Stattdessen werden die Änderungen für ganze Farbkomponenten aktiviert oder deaktiviert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glcolormask** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Color \_ Write-Frage

**glget** mit dem Argument GL \_ RGBA- \_ Modus

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

[**gldepthmask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glindex**](glindex-functions.md)
</dt> <dt>

[**glindexmask**](glindexmask.md)
</dt> <dt>

[**glstencilmask**](glstencilmask.md)
</dt> </dl>

 

 





