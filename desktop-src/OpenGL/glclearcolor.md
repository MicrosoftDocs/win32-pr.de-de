---
title: glClearColor-Funktion (Gl.h)
description: Die glClearColor-Funktion gibt klare Werte für die Farbpuffer an.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd68590ab9221dd094265a54f3c69ca396f810fb1f716c194b627a675196edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061918"
---
# <a name="glclearcolor-function"></a>glClearColor-Funktion

Die **glClearColor-Funktion** gibt klare Werte für die Farbpuffer an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rot* 
</dt> <dd>

Der rote Wert, den [**glClear**](glclear.md) verwendet, um die Farbpuffer zu löschen. Der Standardwert ist 0 (null).

</dd> <dt>

*Grün* 
</dt> <dd>

Der grüne Wert, den [**glClear**](glclear.md) verwendet, um die Farbpuffer zu löschen. Der Standardwert ist 0 (null).

</dd> <dt>

*Blau* 
</dt> <dd>

Der blaue Wert, den [**glClear**](glclear.md) verwendet, um die Farbpuffer zu löschen. Der Standardwert ist 0 (null).

</dd> <dt>

*alpha* 
</dt> <dd>

Der Alphawert, den [**glClear**](glclear.md) verwendet, um die Farbpuffer zu löschen. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glClearColor-Funktion** gibt die von [**glClear**](glclear.md) verwendeten Werte für Rot, Grün, Blau und Alpha an, um die Farbpuffer zu löschen. Die von **glClearColor** angegebenen Werte werden an den Bereich \[ 0,1 \] gebunden.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glClearColor-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ ACCUM \_ CLEAR \_ VALUE

**glGet** mit argument GL \_ COLOR \_ CLEAR \_ VALUE

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





