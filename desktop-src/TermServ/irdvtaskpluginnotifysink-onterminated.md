---
title: Undvtaskpluginnotifysink onbeendete-Methode (sbtsv. h)
description: Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Onbeendete-Methode Remotedesktopdienste
- Onend-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, onend-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518935"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>Undvtaskpluginnotifysink:: onend-Methode

Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Personalabteilung* \[ in\]
</dt> <dd>

Gibt an, ob das Herunterfahren auf ein normales Herunterfahren oder einen Fehler zurückzuführen ist. Wenn das Herunterfahren normal ist, enthält dies **S \_ OK**. Andernfalls enthält Sie einen **HRESULT** -Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                  |
| Header<br/>                   | <dl> <dt>Sbtsv. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Undvtaskpluginnotifysink"**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





