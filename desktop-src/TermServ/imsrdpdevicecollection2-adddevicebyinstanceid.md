---
title: IMsRdpDeviceCollection2 AddDeviceByInstanceId-Methode
description: Fügt der Gerätesammlung ein nicht aufgeführtes Gerät hinzu.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- AddDeviceByInstanceId-Remotedesktopdienste
- AddDeviceByInstanceId-Methode Remotedesktopdienste , IMsRdpDeviceCollection2-Schnittstelle
- IMsRdpDeviceCollection2-Schnittstelle Remotedesktopdienste , AddDeviceByInstanceId-Methode
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df11fa2a58aca505661da1f7643f8d1d6ff2f502e6c10bf835aa67a6e2d0615d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870820"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>IMsRdpDeviceCollection2::AddDeviceByInstanceId-Methode

Fügt der Gerätesammlung ein nicht aufgeführtes Gerät hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ In\]
</dt> <dd>

Typ: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Ein Wert der [**RedirectDeviceType-Enumeration,**](redirectdevicetype.md) der den Typ des hinzugefügten Geräts angibt.

</dd> <dt>

*InstanceId* \[ In\]
</dt> <dd>

Typ: **BSTR**

Der Instanzbezeichner des hinzuzufügenden Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





