---
title: glclearaccum-Funktion (GL. h)
description: Die Funktion "glclearaccum" gibt die klaren Werte für den Akkumulations Puffer an.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glclearaccum-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104127"
---
# <a name="glclearaccum-function"></a>glclearaccum-Funktion

Die Funktion " **glclearaccum** " gibt die klaren Werte für den Akkumulations Puffer an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Red* 
</dt> <dd>

Der rote Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird. Der Standardwert ist 0 (null).

</dd> <dt>

*Grünbuchs* 
</dt> <dd>

Der grüne Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird. Der Standardwert ist 0 (null).

</dd> <dt>

*blauen* 
</dt> <dd>

Der blaue Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird. Der Standardwert ist 0 (null).

</dd> <dt>

*alpha* 
</dt> <dd>

Der Alpha Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glclearaccum** " gibt die Werte rot, grün, blau und Alpha an, die von [**glClear**](glclear.md) zum Löschen des Akkumulations Puffers verwendet werden.

Die von **glclearaccum** angegebenen Werte werden an den Bereich \[ 1, 1 gebunden \] .

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glclearaccum** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Accum \_ Clear \_ value

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

 

 





