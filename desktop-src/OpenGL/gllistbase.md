---
title: gllistbase-Funktion (GL. h)
description: Die gllistbase-Funktion legt die Basis für die Anzeigeliste für glcalllists fest.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- gllistbase-Funktion OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46af03477afc1b656df3a321fd8aa652b034b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949527"
---
# <a name="gllistbase-function"></a>gllistbase-Funktion

Die **gllistbase** -Funktion legt die Basis für die Anzeigeliste für **glcalllists** fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*base* 
</dt> <dd>

Ein ganzzahliger Offset, der zu [**glcalllists**](glcalllists.md) -Offsets hinzugefügt wird, um anzeigen Listennamen zu generieren. Der Anfangswert ist NULL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **gllistbase** -Funktion gibt ein Array von Offsets an. Anzeigen von Listennamen werden durch Hinzufügen von *Basis* zu jedem Offset generiert. Namen, die auf gültige Anzeigelisten verweisen, werden ausgeführt. andere werden ignoriert.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **gllistbase** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Listen \_ Basis

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

[**glcalllists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





