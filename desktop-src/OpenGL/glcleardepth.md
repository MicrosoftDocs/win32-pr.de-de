---
title: glcleartiefe-Funktion (GL. h)
description: Die glcleartiefe-Funktion gibt den undeutlichen Wert für den tiefen Puffer an.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- glcleartiefe-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340778"
---
# <a name="glcleardepth-function"></a>glcleartiefe-Funktion

Die **glcleartiefe** -Funktion gibt den undeutlichen Wert für den tiefen Puffer an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eingeh* 
</dt> <dd>

Der tiefen Wert, der verwendet wird, wenn der tiefen Puffer gelöscht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glcleartiefe** -Funktion gibt den Tiefen Wert an, der von [**glClear**](glclear.md) verwendet wird, um den tiefen Puffer zu löschen. Die von **glcleartiefe** angegebenen Werte werden an den Bereich \[ 0, 1 gebunden \] .

Die folgende Funktion Ruft Informationen im Zusammenhang mit der Funktion " **glcleartiefe** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Tiefe \_ Clear- \_ Wert

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

 

 





