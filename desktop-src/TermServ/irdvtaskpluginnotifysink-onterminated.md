---
title: IRDVTaskPluginNotifySink OnTerminated-Methode (Sbtsv.h)
description: Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- OnTerminated-Methode Remotedesktopdienste
- OnTerminated-Methode Remotedesktopdienste , IRDVTaskPluginNotifySink-Schnittstelle
- IRDVTaskPluginNotifySink-Schnittstelle Remotedesktopdienste , OnTerminated-Methode
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
ms.openlocfilehash: 29ab2a3e8ddea5999b6d63322dbeb9fca07983e591e849f22a3e98e27c67609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129132"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>IRDVTaskPluginNotifySink::OnTerminated-Methode

Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hr* \[ In\]
</dt> <dd>

Gibt an, ob das Herunterfahren auf ein normales Herunterfahren oder einen Fehler zurückzuführen ist. Wenn das Herunterfahren normal ist, enthält **dies S \_ OK**. Andernfalls enthält  sie einen HRESULT-Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                  |
| Header<br/>                   | <dl> <dt>Sbtsv.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





