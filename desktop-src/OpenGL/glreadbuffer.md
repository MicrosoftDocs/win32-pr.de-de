---
title: glread Buffer-Funktion (GL. h)
description: Die glread Buffer-Funktion wählt eine Farb Puffer Quelle für Pixel aus.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glread Buffer-Funktion OpenGL
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
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344697"
---
# <a name="glreadbuffer-function"></a>glread Buffer-Funktion

Die **glread Buffer** -Funktion wählt eine Farb Puffer Quelle für Pixel aus.

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

Ein Farb Puffer. Akzeptierte Werte sind GL \_ Front \_ left, GL \_ Front \_ right, GL \_ Back \_ left, GL \_ Back \_ right, GL \_ Front, GL \_ Back, GL \_ left, GL \_ right und GL \_ aux *i*, wobei ich zwischen 0 und GL  \_ aux \_ buffers 1 bin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war keiner der zwölf (oder mehr) akzeptierten Werte.<br/>                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | der *Modus* hat einen Puffer angegeben, der nicht vorhanden ist.<br/>                                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glread Buffer** -Funktion gibt einen Farb Puffer als Quelle für nachfolgende [**glread Pixels**](glreadpixels.md) -und [**glcopypixels**](glcopypixels.md) -Befehle an. Der *Mode* -Parameter akzeptiert einen von mindestens zwölf vordefinierten Werten. (GL \_ AUX0 bis GL \_ AUX3 sind immer definiert.) In einem vollständig konfigurierten System \_ nennen GL Front, GL \_ left und GL \_ Front \_ left den Front-Left-Puffer, GL \_ Front \_ right und GL \_ right den \_ \_ \_ Namen des Front-Right-Puffers.

Nicht Stereo-doppelt gepufferte Konfigurationen verfügen nur über einen Front-Left-und einen backLeft-Puffer. Einzelpufferte Konfigurationen haben einen Front-Left-Puffer und einen Front-Right-Puffer, wenn Stereo und nur einen Front-Left-Puffer, wenn dies nicht Stereo ist. Es ist ein Fehler, einen nicht vorhandenen Puffer für **glread Buffer** anzugeben.

Standardmäßig ist der *Modus* "GL- \_ Front" in Konfigurationen mit nur einem Puffer und "GL" \_ in Konfigurationen mit doppelter puffert.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glread Buffer** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Lese \_ Puffer

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldrawbuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> </dl>

 

 





