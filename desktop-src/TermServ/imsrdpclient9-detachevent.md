---
title: IMsRdpClient9 detachEvent-Methode
description: Trennt ein Ereignis.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- detachEvent-Remotedesktopdienste
- detachEvent-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , detachEvent-Methode
- detachEvent-Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , detachEvent-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc60a3a7e1499632ac721192ce324fcf786e179604c11e2a70c4450b6171b779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099460"
---
# <a name="imsrdpclient9detachevent-method"></a>IMsRdpClient9::d etachEvent-Methode

Trennt ein Ereignis.

## <a name="syntax"></a>Syntax


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*eventName* \[ In\]
</dt> <dd>

Name der Veranstaltung.

</dd> <dt>

*Rückruf* \[ In\]
</dt> <dd>

Der dem Ereignis zugeordnete Rückruf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> IID \_ IMsRdpClient9 ist als 28904001-04B6-436C-A55B-0AF1A0883DC9 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> </dl>

 

 





