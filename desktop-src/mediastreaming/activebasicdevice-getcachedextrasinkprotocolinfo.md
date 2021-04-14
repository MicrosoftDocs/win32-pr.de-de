---
title: Activebasicdevice getcachedextrasink protocolinfo-Methode (playtodevice. h)
description: Ruft zusätzliche Informationen zum zwischengespeicherten senkenprotokoll für das Gerät ab.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- Getcachedextrasink protocolinfo-Methode Medien Streaming-API
- Getcachedextrasink protocolinfo-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, getcachedextrasink protocolinfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392008"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a>Activebasicdevice:: getcachedextrasink protocolinfo-Methode

Ruft zusätzliche Informationen zum zwischengespeicherten senkenprotokoll für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Die zusätzlichen zwischengespeicherten senkenprotokollinformationen für das Gerät.

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

 

