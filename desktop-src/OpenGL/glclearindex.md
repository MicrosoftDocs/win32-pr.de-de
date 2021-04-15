---
title: glclearindex-Funktion (GL. h)
description: Die Funktion "glclearindex" gibt den eindeutigen Wert für die Farb Index Puffer an.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glclearindex-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477241"
---
# <a name="glclearindex-function"></a>glclearindex-Funktion

Die Funktion " **glclearindex** " gibt den eindeutigen Wert für die Farb Index Puffer an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*c* 
</dt> <dd>

Der Index, der verwendet wird, wenn die Farb Index Puffer gelöscht werden. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glclearindex** " gibt den von [**glClear**](glclear.md) verwendeten Index zum Löschen der Farb Index Puffer an. Der *c* -Parameter ist nicht gebunden. Stattdessen wird *c* in einen fest Komma Wert mit nicht spezifizierter Genauigkeit rechts neben dem Binär Punkt konvertiert. Der ganzzahlige Teil dieses Werts wird dann mit 2 <sup>m</sup>  -1 maskiert, wobei *m* die Anzahl der Bits in einem im Framebuffer gespeicherten Farbindex ist.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glclearindex** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Index \_ Clear- \_ Wert

**glget** mit Argument GL- \_ Index \_ Bits

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

 

 





