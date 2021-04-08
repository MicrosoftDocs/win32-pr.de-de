---
title: glclearcolor-Funktion (GL. h)
description: Die Funktion "glclearcolor" gibt eindeutige Werte für die Farb Puffer an.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glclearcolor-Funktion OpenGL
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
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741937"
---
# <a name="glclearcolor-function"></a>glclearcolor-Funktion

Die Funktion " **glclearcolor** " gibt eindeutige Werte für die Farb Puffer an.

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

*Red* 
</dt> <dd>

Der rote Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen. Der Standardwert ist 0 (null).

</dd> <dt>

*Grünbuchs* 
</dt> <dd>

Der grüne Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen. Der Standardwert ist 0 (null).

</dd> <dt>

*blauen* 
</dt> <dd>

Der blaue Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen. Der Standardwert ist 0 (null).

</dd> <dt>

*alpha* 
</dt> <dd>

Der Alpha-Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glclearcolor** " gibt die Werte für Rot, grün, blau und Alpha an, die von [**glClear**](glclear.md) zum Löschen der Farb Puffer verwendet werden. Die von **glclearcolor** angegebenen Werte werden an den Bereich \[ 0, 1 gebunden \] .

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glclearcolor** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Accum \_ Clear \_ value

**glget** mit dem Argument GL \_ Color \_ Clear \_ value

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





