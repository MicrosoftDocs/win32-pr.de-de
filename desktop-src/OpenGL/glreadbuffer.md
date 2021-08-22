---
title: glReadBuffer-Funktion (Gl.h)
description: Die glReadBuffer-Funktion wählt eine Farbpufferquelle für Pixel aus.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a25e9a799185b1a509510abb81617895fbbd0624d8816110e4c2ba8e4a7c1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937950"
---
# <a name="glreadbuffer-function"></a>glReadBuffer-Funktion

Die **glReadBuffer-Funktion** wählt eine Farbpufferquelle für Pixel aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Ein Farbpuffer. Akzeptierte Werte sind GL \_ FRONT \_ LEFT, GL \_ FRONT \_ RIGHT, GL BACK \_ \_ \_ LEFT, GL BACK \_ \_ RIGHT, GL FRONT, GL \_ BACK, GL \_ LEFT, GL RIGHT und GL AUX i , wobei i zwischen 0 und GL \_ \_   \_ AUX \_ BUFFERS 1 liegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein der zwölf (oder mehr) akzeptierten Werte.<br/>                                                             |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | *-Modus* hat einen Puffer angegeben, der nicht vorhanden ist.<br/>                                                                             |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glReadBuffer-Funktion** gibt einen Farbpuffer als Quelle für nachfolgende [**glReadPixels-**](glreadpixels.md) und [**glCopyPixels-Befehle**](glcopypixels.md) an. Der *mode-Parameter* akzeptiert einen von zwölf oder mehr vordefinierten Werten. (GL) \_ AUX0 bis GL \_ AUX3 sind immer definiert.) In einem vollständig konfigurierten System nennen GL FRONT, GL LEFT und GL FRONT LEFT den Puffer ganz links vorne, GL FRONT RIGHT und GL RIGHT den Puffer rechts vorn und GL BACK LEFT und GL BACK den \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Back-Left-Puffer.

Nichtstereo-Konfigurationen mit doppelter Pufferung verfügen nur über einen Linken-Front-End- und einen back-left-Puffer. Einzelpufferkonfigurationen verfügen über einen Front-Left-Puffer und einen Front-Right-Puffer bei Stereo und nur über einen puffer von links nach vorn, wenn nonstereo. Es ist ein Fehler, einen nicht vorhandenen Puffer für **glReadBuffer anzugeben.**

Standardmäßig ist *der Modus GL* FRONT in Einzelpufferkonfigurationen und GL BACK in doppelt \_ \_ gepufferten Konfigurationen.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glReadBuffer ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ READ \_ BUFFER

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





