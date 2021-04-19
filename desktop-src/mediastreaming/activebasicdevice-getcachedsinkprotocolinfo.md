---
title: Activebasicdevice getcachedsinkprotocolinfo-Methode (playtodevice. h)
description: Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab. | Activebasicdevice getcachedsinkprotocolinfo-Methode (playtodevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- Getcachedsinkprotocolinfo-Methode Medien Streaming-API
- Getcachedsinkprotocolinfo-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, getcachedsinkprotocolinfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373458"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>Activebasicdevice:: getcachedsink protocolinfo-Methode

Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Die zwischengespeicherten senkenprotokollinformationen für das Gerät.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Playondevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Playto Device. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

