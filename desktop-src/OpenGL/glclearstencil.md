---
title: glclearstencil-Funktion (GL. h)
description: Die glclearstencil-Funktion gibt den eindeutigen Wert für den Schablonen Puffer an.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glclearstencil-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956604"
---
# <a name="glclearstencil-function"></a>glclearstencil-Funktion

Die **glclearstencil** -Funktion gibt den eindeutigen Wert für den Schablonen Puffer an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* 
</dt> <dd>

Der Index, der verwendet wird, wenn der Schablonen Puffer gelöscht wird. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glclearstencil** -Funktion gibt den von [**glClear**](glclear.md) verwendeten Index zum Löschen des Schablonen Puffers an. Der *s* -Parameter wird mit 2 <sup>m</sup>  -1 maskiert, wobei *m* die Anzahl der Bits im Schablonen Puffer ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glclearstencil** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ Clear \_ value

**glget** mit Argument GL- \_ Schablonen \_ Bits

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

 

 





