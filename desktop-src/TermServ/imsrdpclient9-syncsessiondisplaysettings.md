---
title: IMsRdpClient9 SyncSessionDisplaySettings-Methode
description: Synchronisiert Einstellungen für die Sitzungsanzeige.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- SyncSessionDisplaySettings-Remotedesktopdienste
- SyncSessionDisplaySettings-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , SyncSessionDisplaySettings-Methode
- SyncSessionDisplaySettings-Methode Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , SyncSessionDisplaySettings-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a8021c4e0b7af0de000b96d5b2b094f5894b84746dedf98f699a693a6bddd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990370"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a>IMsRdpClient9::SyncSessionDisplaySettings-Methode

Synchronisiert Einstellungen für die Sitzungsanzeige.

## <a name="syntax"></a>Syntax


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





